---
tags: NumPy
---


# 2020-12-09 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Bas, Andy Terrel, Matti, Danuta, Al-Baraa, Inessa, Ryan



## Follow-up from last meeting / discussions


- Community Survey
Final report in the text format (WIP): https://docs.google.com/document/d/1kUqxIMLIczfKLXYUiwnqE1SqH1N4EKLCUqDX20FHquA/edit?usp=sharing.
 - static site (rough draft): https://rossbar.github.io/numpy-survey-results/index.html


- Data umbrella talk 12/2/2020 went well, youtube link:
  - https://youtu.be/lHJqOE5j6xE
  



## Topics


- Delay 1.20 release (probably mid-end January) for PyArrow? See [numpy issue](https://github.com/numpy/numpy/issues/17913) and [PyArrow fix](https://github.com/apache/arrow/pull/8834) summary of the issue: 
  - PyArrow is broken with 1.20 due to a necessary macro change in NumPy. (This is a problem if compiled with NumPy <1.16.6, which their wheels are)
  - (The fix/workaround itself is trivial)
  - if we release before PyArrow, `pip install pyarrow` may end up installing NumPy 1.20 (at least if NumPy is not installed already), meaning pyarrow will not work.
  - Arrow's release process is apparently very clunky, so they are not planning on a bugfix release. Their next release will probably start early January (with an rc) so the final release would likely be a few weeks later.
  - To be clear: No, we can't work around it in NumPy, there is a reason this was the *first* dtype related change that went in.

  After disucssion we decided to release a rc2 now and delay the 1.20 release to after the release of PyArrow.

- A current typing-related challenge is that of platform-specific `np.number`s. For example, `np.int_` can map to either `np.int32` or `np.int64`. 
  Unfortunately the concept of "platform-specific" is a too dynamic for static type checking, so we have to get a bit creative. Thus far there are two potential resolutions:
  - Dynamically generate a stub file (containing all relevant annotations) when building numpy. See [numpy/numpy#17514](https://github.com/numpy/numpy/pull/17514).
  - Let a mypy plugin deal with the (platform-specific) precisions. Usage of such a plugin would be opt-in; without it the precision of the affected `np.numbers` will be left at ambiguous (_i.e._ set to `Any`). See [numpy/numpy#17843](https://github.com/numpy/numpy/pull/17843).

  After discussion the concensus seemed to lean to using the mypy plugin

- DevOps for numpy.org

- NumFOCUS Academy is expanding to courses on project contributing. (Melissa was in contact with that) academy.numfocus.org
    - Looking for folks who would want to write / organize a course on contributing to numpy
    - Is the first of it's kind but hope to be adding courses for all our courses in the near future
    - questions: ping andy@numfocus.org


## Additional Details

- Warren

  - Work on a faster text reader is on github at [npreadtext](https://github.com/WarrenWeckesser/npreadtext).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

