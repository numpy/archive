# NumPy Team Summit 

(Mildly reformatted version of google docs used during the meeting.)

**Date: 2022-07-12**

**Location for in-person attendance: AT&T Convention Center, 1900 University Ave, Austin, TX 78705
Room: 214**

Join via Zoom: https://us02web.zoom.us/j/82177549896?pwd=amFPV0VsWVhsVGUzU0NJd0lmTWhxdz09
Meeting ID: 821 7754 9896
Passcode: 001068

## Summit agenda


| Time | Topic | Attendees |
|------|-------|-----------|
| 10am CDT/3pm UTC | SIMD working session | Ralf, Sayed, Ganesh, Raghuveer, Matti, Sebastian, Brigitta, Melissa, Inessa |
| 11 am CDT/4 pm UTC | State of NumPy: review of the roadmap, [reflection on sustainability](https://docs.google.com/spreadsheets/d/1L56Pb4rz4mfxYaCCCg7nE4WX0AYAd_wNK0idDa2rKGY) | Inessa, Sebastian, Ralf, Chuck, Sayed, Ganesh, Raghuveer, Matti, Brigitta, Melissa, Simon Cross |


### Notes on SIMD session

Sayed: second IBM bounty arrived! $16k(-10% Bountysource fees) for s390x support (VSX one was 6,400)
Issues Sayed brings up as potential issues going forward:


1. C++ support: there are problems with the test harness for SIMD support and replacing the macro-based universal SIMD system with templated code. Sayed is working on some PRs to implement this. There is more work to use DoxyGen. https://github.com/numpy/numpy/pull/21057
2. Sizeless data types (e.g. SVE for ARM), is going to cause issues when combined with C++
   1. Sayed is working on initial testing for this. Involves Google Highway (?)
3. 13rd gen Intel architectures without AVX512, just AVX2 with many cores. They claim it will be supported in the future again in Xeon. SVML works only on AVX512, so that won’t do anything anymore. We miss AVX2 support in NumPy!
   1. Sayed opened one PR to convert SVML to SIMD universal intrinsics


Ganesh: always willing to help with adding support, happy to be tagged.


Matti: trying to write a blog post for a high-level story of how our SIMD support makes a difference, looking for a good benchmark.
* Ganesh: can we have benchmarks in CI? → There used to be some job, but it fluctuates a lot.


Parallelism: also very important and we need to work on it. Separate from SIMD, but in many use cases more important even (it depends, actually). 


Sayed: it’d be great to have an internal dispatcher as a new layer within NumPy. 
Sebastian: NumPy does have a lot of machinery to go to multi-threading (this is what pnumpy already tried to do, on the inner-loop level). Could also do it on the outer loop level; half of the things we need is there probably.
Issues though: dealing with cache, reduction operations, also composition between different packages & oversubscription.


Fusing operations is also important. Needs a JIT like Numba, or something like Numexpr. 


We have over 150 PRs dealing with SIMD so we have made nice progress.
Task: summarize which ufuncs and operations support universal intrinsics.


C++ for universal intrinsics implementation: PR is mostly ready (Sayed), the remaining issue is the sizeless data types.


GCC versions: we need to test with a wider range of compilers, and drop older compilers. Sayed would like GCC 9, that’s stable for AVX512/SkylakeX features. Also influenced by C++ code. We need C99 and C++11. Proposal: minimum version gcc 6.3 and error out if the compiler is older.


We have some support via the NASA-Rose project for performance enhancements. There are restrictions about doing research-looking work outside of the US, but there are less restrictions for more mundane “support” work. Are there SIMD topics we can push forward?


AVX512 / ARM(SVE2) / macOS arm64 / Windows on ARM → traditionally we haven’t wanted to do this, but now maybe we should, at scale together with other projects? One proposal: allocate funds and management from the projects, outsource the IT/devops work to something like Quansight on a contract.


Note: NEON currently not enabled on Windows. 


Replacement for TravisCI is a big deal, but only in custom cloud solutions, not CI vendors. Currently it’s kinda best effort on TravisCI. 


AWS custom runners (SVE2) + macOS M1 are the highest prios. Also, we’re rethinking the offer from Niyas on Windows on ARM integration in our CI. Ralf takes an action to see what this would cost to get running and maintain over time. Ganesh offers to help with AWS to open a ticket if needed.


### Roadmap review/update

Maybe add a bit of context on what is in this roadmap (e.g., why no timelines, last update date).

**Interoperability:**
1. What is there is outdated
2. Array API support: Sebastian: can put this on, how fast we want to move it forward is still TBD. Do the low-impact breakages and compatible stuff first.
3. Value-based casting removal 
4. Hooks for internals, ufunc hooks, configurable memory allocator
5. HPy support (exploring it at least?): will need a NEP
6. Other interop needs?


**Performance:**
1. Can we replace SVML codewith universal intrinsics? Tricky bit is that there’s no description at all of what it does. Raghuveer is working on this! Also working on better readable code. Sayed willing to help, Raghuveer is moving it forward.


**Extensibility:**
1. currently the only point is dtypes improvements.
2. Chuck: what about dtypes we need? → answer is to start them outside of NumPy (e.g. quad-precision, bfloat16)
   1. Remove `long double`, what do we need for this process-wise? Proposal: NEP first, then doc-deprecate and remove from downstream projects, then deprecate in numpy, then remove. Timeframe TBD.
   2. Sayed: should we get rid of C types, and just use fixed-precision types? We can save a lot of binary size (maybe 10%), use internally fixed-width types.
      1. We can do this for ufunc loops, and create aliases for C names (there was a PR actually).
      2. This will help with C++, if we don’t do this the size will increase.
      3. Agreement, just needs to be done comprehensively.
      4. C++14 would be helpful -> yes, we can do this.
      5. Ralf: other binary size reduction: remove vendored libs! (openblas in particular)
3. Variable-length strings; experiment with this outside of NumPy itself, this is possible now. Kind of a toss-up whether this should be on the roadmap. 


**Docs & website:**
1. Docs restructuring is done, remove
2. Translations: we have several >95% complete translations (Japanese, Portuguese, Chinese), just needs to be launched.
3. Docs: most parts are in good shape, the user guide needs an overhaul (NumPy Fundamentals, Miscellaneous should go). Under-the-hood docs would be great to extend as well.
4. Need to come up with and outline for the main user guide 


**User Experience:**
1. Typing: small update, but in great shape
2. Platform support: we need to formalize this into tiers like PEP 11 and declare what architectures are in which tier, and establish a process for changing support.
3. Clean up NumPy namespaces! `numpy`, fft/random/linalg/ma/array_api + lib.<module-name>. (e.g., `np.lib.bitwise`). New submodules should be complete / developed outside of NumPy. 


**Maintenance section:**
1. We still need a replacement for masked arrays.
2. F2py topic needs to stay, but the text and link to issue needs an update (could link to https://github.com/numpy/numpy/projects?type=classic&query=is%3Aopen+f2py+)
3. Replace the point about fft-mkl, change numpy’s c fft version to c++?
4. Mention adopting more c++ code to replace our templating. Can we simplify the templating macros to make it easier to read?
5. Linalg: “make APIs match” still needs doing
6. Np.matrix: extend topic, vendor np.matrix into scipy *and* make sparse arrays more complete.
7. Indexing; this is a new feature, not maintenance
8. Polynomial API: can be removed (there’s just some docs updates to do)
9. Improved text file loader: done, remove this
10. ufuncs/gufunc: let’s remove this point, mostly done




**Missing topics?**
1. C++ as a separate topic
2. How can we improve ufuncs?
3. SIMD: move it to C++, supporting SVE2 & other sizeless dtypes, map universal intrinsics to WASM (which uses SSE for SIMD - https://emscripten.org/docs/porting/simd.html)
4. Support Pyodide/WASM! (PR for CI is up)
5. Moving to Meson & proper cross-compiling support 
6. Making numpy.org & docs more accessible

 
**Benchmarking:** we have it in the roadmap, we should move this forward. Why don’t we rely on profiling code. We may use this on overheads.
  
### Other Discussion
  
Intel’s new processors have native support for float16, Raghuveer has a PR up already. Now we convert to float32, compute, convert back. Supported from GCC 12 onwards. float16 matmul is builtin, not dispatched to openblas.
