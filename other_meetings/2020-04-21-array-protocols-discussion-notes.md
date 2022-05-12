# NumPy Protocol discussions (NEP 37, etc.)

This is an attempt to rekindle discussions around improving array-protocols and array-like dispatching. Since the tensor summit which could have been a venue to move this forward was canceled, lets try a video conference.


### Organizational

**When:** Tuesday, April 21st, 11am PDT (18:00 UTC)

**Where:** https://berkeley.zoom.us/j/762261535

**Attending:** John Kirkham, Peter Entschev, Ralf Gommers, Sebastian Berg, Warren Wackesser, Thomas Fan, Stéfan van der Walt, Hameer Abbasi, Stephan Hoyer, Ross Barnowski



## Agenda


* Libraries will want to do implicit dispatching.

* We need assurance that `__array_module__` is implemented (but not `__array_function__`)

    - shoyer: can we provide an example implementation of `__array_module__` that defers to `__array_function__`?

* Array module does answer a bunch of questions:

  - e.g. array creation, random number generation.

* Many libraries use Cython, etc. so it doesn't help them.

* Use case scikit-learn estimators, qml(?), with cupy arrays, 

- An approach: provide NumPy with both (seperately possibly) for experimentation
  - We need experience as to what is possible
  - shoyer: can we clarify exactly which the alternatives are?
      - NEP 37: `get_array_module`
      - Expanding `__array_function__` with NEP 30, NEP 35, maybe more?
          - For example: how do we spell coerce all of these arrays into a like duck type? `np.duckarray` may not be quite enough (but `get_array_module` can do this)
          - How do we handle classes like `np.vectorize`? (This is actually one of the most interesting parts of NumPy to override on JAX arrays.)
              - Could we make it an actual ufunc? (Needs dtype inference)
              - Just use `__array_ufunc__` anyways?
              - Uarray/unumpy uses dispatching on other argument types
          - Access to the "original" function?
      - NEP 31 uarray/unumpy

* Dask (users) seemed to have few transition issues when `__array_function__` was added.
  * More issues about incomplete support rather than rough transition

* xarray (users) had a rougher transition apparently
  * Note: likely more inexperienced users than dask

- `vectorize`, `Generator` etc. still are an issue for `__array_function__`

- Action: try doing both NEP 30/35 (`like=`) and NEP 37 (`__array_module__`) at once?
        - do we need `like` on random functions? maybe not?
        - `__array_module__` is most useful for filling in gaps of `__array_function__` support
        - two new functions (`np.duckarray` and `np.get_array_module`)

- Libraries to target for experimentation:
  - Email to the mailing list!


## Topics


* Library needs (Sebastian: Adding this, since I would love to discuss this first, or best try to make a rough list even before the actual meeting)
  - Are libraries willing to adopt a purely experimental implementation outside of NumPy?

* Array-provider/NumPy wishes:
  * `__array_function__` is implicit on the full API and Opt-Out. This has backward compatibility
    concerns for functions in the NumPy namespace in conjunction with generic array-objects.

* Can we decide on a preferred "next" approach, expand `__array_function__` vs. new explicit and Opt-In:
  - [NEP 30](https://numpy.org/neps/nep-0030-duck-array-protocol.html) – Add `np.duckarray()`
  - [NEP 35](https://numpy.org/neps/nep-0035-array-creation-dispatch-with-array-function.html) – `like=` argument for creation functions
  - [NEP 31](https://numpy.org/neps/nep-0031-uarray.html) – uarray/unumpy
  - [NEP 37](https://numpy.org/neps/nep-0037-array-module.html) – `get_array_module()`
  - **Discuss:** Is there an approach that is definitely preferable from a _library_ perspective?

* **Generalizing ``__array_function__``**
  * What is the transition story for array-providers?
    * If array providers cannot or will not transition, this is not a solution.
    * Even if they wish to transition, is a smooth transition possible?
  * **[NEP 30](https://numpy.org/neps/nep-0030-duck-array-protocol.html) – Add `np.duckarray()`**:
    - Provides a way to migrate away from `np.asarray`
    - Does not provide a way to coerce other arrays to same type.

  * **[NEP 35](https://numpy.org/neps/nep-0035-array-creation-dispatch-with-array-function.html) – `like=` argument for creation functions:**
    - `__array_function__` is not explicit, but sometimes we need it.

* **[NEP 31](https://numpy.org/neps/nep-0031-uarray.html) – uarray/unumpy**:
  - Designed around a fixed context-local (with statements) state (but could "discover backends") 
  - `unumpy` provides a "dispatching" namespace

* **[NEP 37](https://numpy.org/neps/nep-0037-array-module.html) – `get_array_module()`:**
  - Add global opt-in, opt-in context managers?
  - Provide "transitioning" help?
  - Is context manager scoping problematic?
  - Allow libraries to limit which array-types they accept?
    - To be clear: Maybe everyone but me (Sebastian) thinks this is *definitely* a terrible idea, but I would like to hear it :)

* ...

* **Backburner: What about libraries such as SciPy?**
  * E.g. even a library using implicit dispatching could allow overriding in theory.

* **Backburner: Reduced NumPy API?**


---

## Further Notes

*Thought not everything is an agenda item, so room for general notes ☺*

### Comparisons Table (initially Hameer's)

|Problem|`__array_module__`|`__array_function__` + NEP 30/35|`uarray`/`unumpy`|Class Hierarchy|
|-|-|-|-|-|
|Basic Dispatch with Array Arguments|Implement `func`, possibly by `__name__`/`__module__` or dictionary based dispatch|Return a module/object that has the correct attributes|Can register backend and then use same rules as `__array_function__`|No dispatch --- Need to know the backend module ahead of time.|
|Dispatch without array arguments|May need to pass around an array module (`np=`) to work|Defaults to NumPy/`like=` needed|Can use `with` statements to choose what gets selected|Everything is a method|
|Dispatch for a sequence of calls containing array creation|May need to pass around an array module (`np=`) to work|Not possible/May need to pass around an array for `like=` to work|No problems --- state persisted down the stack|Just call methods on your class|
|Multithreading issues|None|None|Need to get the state in a closure and set it. [Dask example](https://github.com/Quansight-Labs/unumpy/blob/master/unumpy/dask_backend.py#L39)|None|
|Composition/Meta arrays|Meta arrays may need to store inner array module|Need to unwrap inner array before calling NumPy function|Meta-backend needs to store inner backend|Need to store the "inner" class instance.|
|Implementation overriding/replacing for submodules that take in `np.ndarray` e.g. `np.linalg`, `np.random`, or `np.fft`|Not possible (separate issue)|Not possible (separate issue)|As usual|Store "inner" submodule options?|
|Coercion/conversion|Using `module.asarray()`|Using `np.asarray(module, like=ArrayType)`|`__ua_convert__` protocol|Manual
|Default implementations, ties into reduced API | MixIn? | MixIn? | `default=` when creating multimethod | On base class/MixIn |
|Separation of array-type and backend | Not possible | Not possible | Separate | Separate |
| Warnings for library functions | Manual | Manual | Manual | Manual |
| Wrapping other arrays | Manual | Manual | `__ua_convert__` helps here | Manual |




## Sebastian's Notes (but feel free to delete/change)

*Note: I use "libraries" here, of course an end-user writing a helper function that supports multiple array-likes effectively writes a library in this regard.*

### General

In General, it seems to me that implicit control (best without Opt-In), such as we are doing with `__array_function__` seems nice for end-users. But may or may not be problematic from a library perspective?

With `get_array_module` we were going for a dual model:
  * End-users can use implicit dispatch *for array-likes which opt-in to it*
  * Libraries can use explicit dispatching (sometimes clearer)

`uarray` supports both interchangeably. Meaning that end-users can (potentially) decide whether they want implicit or explicit behaviour.

Libraries on the other have to decide whether they want an implicit or explicit API. *I assume that all libraries will want to expose (mainly) an implicit API!*


### User Stories

I would like to develop the user story, or possible user stories?
> I have split this (and other things) into library and end-users. Ideally, those differences are probably blurry to non-existent, but I think it may help to converge. [name=seberg]


* **Overcome backward incompatible changes to how *NumPy* functions work when adding support to an array-like?**
  * `__array_function__`: *Missing*
    * Transitioning would require a lot of warnings? And an array-object related context manager.
    * ***If array-providers are not happy with transitioning how the main NumPy namespace interacts with their array-objects expanding `__array_function__` is useless for library support and thus IMO secondary at this time!***
      * The only way to rescue it would be moving to an (undesired) separate name-space
      * This questions a bit whether implicit dispatching is all that helpful within the NumPy namespace?! 
  * `get_array_module()`: effectively new (local/bound) namespace
  * `uarray`: New namespace
  * **So:** New namespace allows to decide _not_ to support implicit dispatching within NumPy.

* **Overcome backward incompatible changes to how *library* functions work when adding support to an array-like?**
  * `__array_function__`: Controlled by `__duckarray__`
  * `get_array_module()`: Controlled by `__array_module__`
  * `uarray`: *Two stories:*
    1. Explicitly set by user, so no "transition"
    2. Library function is implicit based on inputs, so during implicit dispatching in `unp.function()` calls or future `uarray.discover_backend()`.
      * Not sure, in principle backend can control but it may need a story to distinguish the explicit usage.
  * **All:**
    * array-object/backend will probably have to issue a transition warning and provide an Opt-In context manager?
    * Or: Some way to type-strictly (requires an Opt-In solution?)

* **Library *transitioning* to supporting array-likes:**
  * (This is independent of the Opt-In vs. Opt-Out decision)
  * Implement new behaviour (but disable it by default)
  * Issue FutureWarning if new behaviour is (or may be) used.
  * Add context manager to disable warning (old behaviour must be achieved using `np.asarray()` by the user)

* **Library function supporting all array-likes is Opt-In vs. Opt-Out:**
  * Guidelines may be good, but it seems irrelevant if we have a transition story? Since NumPy is often opt-out with `__array_function__` currently, that may be the best default?

* **End-User usage story**:
  * `__array_function__` and `get_array_module()` assume end-users use/want/need (almost) only implicit dispatching.
  * `uarray`: *Two stories*
    * End-user uses implicit with `__array_function__`, libraries provide implicit behaviour to the user using `uarray`.
    * End-user uses `unumpy` themselves and can "pick" which array-like globally/locally thus *disabling* implicit behaviour *globally*. (This affects all `unumpy` users)


* **Libraries need some assurance their functions will not misbehave for some array-likes?**
  * Only current story: We need a reduced namespace-API (including array methods?)
    * `uarray` or `get_array_module` have a namespace so no problem
    * Such a namespace is easy to create for `__array_function__`
  * Possible (but likely not wanted) thought by Sebastian:
    * Library may white-list array-likes it tests with. All others would be rejected unless the user opts-in. This is a bit inconvenient, and of course not a very safe safety net.


* **We may need a solution for a "common" type or module:**
  ```python
  def function(*arrays):
      # A new or internal array, should use the best/common array-like
      out_array = np.empty_like(...)
      # or:
      arrays = [best_type.asarray(arr) for arr in arrays]
  ```
  * `__array_function__`: No solution yet.
    * Would require an additional `np.common_array_type()` function (or similar)?
  * Others: namespace is/can be (context-local) "bound" to the best/common array-like to achieve this.

* **User wishes to "transition" a full program**
  * *Is this an important or desirable use-case?*
    * If all dispatching is implicit, only a few functions should need changing?
    * If you transition a whole program, maybe it should be a function :)
  * Currently: Some may use `import cupy as np` which may be bad.
  * `unumpy`: Has explicit backend setting story, this can also affect e.g. functions
    in the same file/project directly.
  * `get_array_module()`: possible but less powerful/convenient.

* **Partial support of NumPy API (`__array_function__`, etc.):**
  * Raising an error is always possible.
  * `__array_function__`: Currently no fallback mechanism.
    * But: This seems like a solvable issue, just needs a small API decision?
  * `get_array_module`: Fallback possible (assuming `__array_function__` does not make problems)
  * `uarray`: Fallback to different other explicit backend possible.
  * Defaults/MixIns, etc. are plausible in most solution but differ in technique (see Hameer's table)


* **Beautiful API concerns:**
  * Do you consider an additional argument for creation functions ugly?
  * Is providing a full namespace ugly/inconvenient (e.g. including `np.random.default_gen()`?)

    Consider some library-specific array creation function:

    ```python=
    def some_other_function_in_user_or_lib_code(array_likes):
        ...
        library_arr_creation_func(no_array_args) # Will not dispatch
        ...

    def library_arr_creation_func(no_array_args):
        # Do some stuff with np
        return array
    ```

    This will need to be changed to (`npx` used here for any compatible library)

    ```python=
    def some_other_function_in_user_or_lib_code(array_likes):
        npx = np.get_array_module(*array_likes)
        ...
        library_arr_creation_func(no_array_args, np=npx) # Will now dispatch
        ...

    def library_arr_creation_func(no_array_args, np=numpy):
        # Do some stuff with np
        return array
    ```

    Which is equivalent to the use of the `like=` argument used when expanding
    `__array_function__` (except for skipping the `np.get_array_module()` call).
    
    With a context-local approach (`uarray`), the solution would be:
    ```python=
    def some_other_function_in_user_or_lib_code(*array_likes):
        # Or possibly a decorator extracting (and preparing)
        # the array_likes.
        with discover_backend(*array_likes):
            ...
            library_arr_creation_func(no_array_args)
            ...
    ```


* **The global Opt-In thought (See also transitioning below)**
  * This is an option we could provide for libraries if they wish to not change their API default.
  * May make some transitions a bit easier (not as such easier, but easier to swallow)?
    I.e. only those get transition warnings who want the new behaviour.
    Those who do not, can "disable" everything. (but does add complexity by context!)
  * Could be useful for transitioning if we make the Opt-In stricter typed.
    That allows (context local) "strict typing" which resolves some transition issues
    since objects of "unknown" type could be rejected, since they may transition
    to implementing `__array_function__` in the future. This hinges also a bit
    on finding a good definition for "unknown"? Maybe even by allowing the array-object
    to signal this.


* **Dangers of Scoping**
  * Any context-local explicit has _some_ scoping issues to be aware of.
    I am unsure how bad this is for an explicit after-implicit discovery
    (e.g. `discover_backend()`) approach.
    ```python
    def library_arr_creation_func(shape):  # no array
        # `dispatched_np` is set context-local to a backend
        return dispatched_np.random_array()
        
    def library_B_func(shape):
        """Still uses NumPy only"""
        arr = library_arr_creation_func(shape)
        # do things with arr
    ```
    If the user explicitly sets a backend `library_B_func()` may break unexpectedly.
    If the backend is set context-local by `discover_backend()` this is less likely.
  * Similar dangerous exist (less bad) with transitioning context-managers.
 

### Additional/other things:

* **Transitioning:**
  * **Libraries:** In all designs, transition requires **non-local** control with context managers?
    ```python
    def library_function_transitioning(arr):
        # was: arr = np.asarray(arr)
        arr = np.duckarray(arr)
        # Or: uarray.current_backend is not numpy
        # Or: np.get_array_module(arr) is not numpy
        if type(arr) is not np.ndarray and not future_dispatch_behaviour_enabled():
          warnings.warn(FutureWarning)
          arr = np.asarray(arr)

    library_function_transitioning(dask_array)  # FutureWarning
    with future_dispatch_behavior():
        library_function_transitioning(dask_array)  # no warning
    ```

  * **Array-providers:** An array-object adding support for the new protocols?
    * This was one reason for NEP 37. Transitioning to providing `__array_function__`
      seems tricky. Transitioning to an explicit `np.get_array_module()` seems not as
      problematic. Especially if that is Opt-In.
    * Two main Solutions?
      1. Strict Typing: Reject any unknown type this would be similar for all solutions:
         * `np.duckarray()`
         * `np.get_array_module()` is strictly typed. An "unknown type" will always
         * `uarray.discover_backend()`
         
         If the given solution is *not* end-user opt-in, this will also limit the
         NumPy-only signature of library functions `func(obj): np.asarray(obj)`.
         For example `__array_function__` cannot simply do this, since we would
         stop supporting everything that `np.asarray(...)` supports in most functions.

      2. The array object has to give a FutureWarning and provide an opt-in context
         as in the library-transition case:
         * `__array_function__`: To spammy?
         * `get_array_module()`: Noisy, but less bad?
         * `uarray`/`unumpy` (Sebastian: not sure what story could be, probably same
           as `get_array_module` if dispatching is implicit.)


* **Extensibility:**
  * `__array_ufunc__`: works also for non-NumPy ufuncs
  * `uarray`, the `discovered_backend()` for implicit dispatching may work for others libraries also using `uarray` for allowing dispatching?
  * `get_array_module()` has no clear story for adding other modules. But seems plausible?
  * `__array_function__` has no story currently, since it is tied directly to the type (unless the type is extended by importing additional libraries). In theory libraries could wrap their functions with `__array_function__`, or something similar.

* **Interaction?**
  * With `uarray` or `get_array_module`, the module can be `numpy`, which also still
    dispatches using `__array_function__`, this may create some (rare) inconsistencies?


### What are the actual downsides to just expanding `__array_function__`?

The given downside: Using NumPy's function as functions which coerce to ndarray
always, is not possible. There is no explicit NumPy namespace anymore.

If `__duckarray__` + `like=` arguments are a solution, they have to overcome certain
shortcomings that NEP 37 notes to overcomes (or at least improve the story around
overcoming them). See the [NEP 37 section](https://numpy.org/neps/nep-0037-array-module.html#why-array-function-hasn-t-been-enough)

  0. Backward compatibility during introduction of `__array_function__` on an object.
     * This has to be solved before we can try and think about the others?
  2. `__array_function__` is all or nothing and fallback to NumPy's implementation is hard to impossible.
    * This seems like it could be overcome?
  3. It is not possible to alias functions (again fallback is difficult)
  4. We have to accept expanding `like=` to e.g. random functions/methods
    * These also would require dispatching and maybe add internal logic to handle
      some array-likes. (e.g. NumPy *can* handle those exposing `__array_interface__`)
    * For random functions, this has both the advantage and disadvantage that
      the `Generator` object is NumPy's (tricky for CuPy).
  4. We may need a way to spell `np.asarray(..., like=other_type)`



### Random thoughts

* Probably thought and thrown away before: What if we use/create a bound `__array_function__` namespace? Maybe there is no actual difference there. But, we may have an issue that the returned `np` namespace or uarray "implementer" is still dispatched.


* The current APIs are use methods, but work with types. Should they be classmethods to avoid passing around a (potentially large) instance?
