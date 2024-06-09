# 2023-11-08 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian, Stefan van der Walt, Nathan, Ralf, Mars, Meteusz, Sayed, Tyler, stevenkell, Matti

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-10-25.md_
- Starting to make ABI breaks
  - there is some header cleanup we could do to move us closer to the limited API. There are some non-limited API uses in the public headers, and these should be hidden so that cython users can do `cimport numpy` with the limited API.

- Reviewing 2.0 board (as a recurring thing)
   - Updating [the 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)


## New topics

- Completed giving talk about NumPy at PyData NYC conference
    - Talk title: Comics in NumPy? More Likely Than you Think!
    - Digital comic: https://heyzine.com/flip-book/3e66a13901.html
    - Recording will be uploaded in a few weeks at PyData's Youtube channel, will share when ready
    - Krita source files, printable PDF and talk slides in the [repository](https://github.com/MarsBarLee/gsod-numpy-2023/tree/main/source-files)
    - Next steps
        - Review with Mukulika, one of the project mentors
        - Community Review #3 of 10/16 pages so far
        - Uploading comic to NumPy website, currently on heyzine
        - Completion of last 6 pages
    - <img src="https://hackmd.io/_uploads/ryIHONKmp.png" width="400">


- Change time?
  - Probably change "back" (move by one hour w.r.t. to UTC).
  - Ping mailing list.


- Array API changes PRs open


- Locking for string dtype
  - Not hard to attach mutex to dtype, might help fixing certain mutexes
  - GIL removal may need this in any case.
  - New Mutex is merged in CPython (as part of the nogil work)
  - This should be necessary for object dtypes.
  - `stdatomic.h` is available in C11 (maybe useful)?

- Cyclic garbage collection?
  - The hook used for it, would also be useful for string allocation management.

- Dropping Python 3.10:
  - Not yet, there is probably little gain anyway.


- Thoughts on new array conversion API (guessing internal for now):
  ```python
  conv = _array_converter(*arrays)
  dt = conv.common_dtype()  # always applicable, may do initial conversion to arrays
  conv.was_pyscalar  # maybe.  Or an enum with `0-D, scalar, python scalar`.
  arrays = conv.arrays(subok=True, pyscalars="convert_if_no_array")

  return conv.wrap(result)
  ```
  or maybe:
  ```python
  conv = _array_converter()
  conv.add(arr1, copy=True, ...)
  conv.add(arr2, ...)
  ```
  to avoid code like `np.asarray(obj) if not isinstance(obj, (int, float, complex)) else obj`.




## Action items



---

### Let's connect and keep the conversation going!
Please enquire in a meeting or by mail how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
