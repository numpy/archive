---
tags: NumPy
---

# 2020-05-27 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Themistoklis, Anirudh, Ben Nathanson, Matti, Warren, Chuck, Hameer, Ross, Melissa, Inessa, Rakesh, Ralf,


## Follow-up from last meeting / discussions


- Google Season of Docs application next deadline: June 8


- What to do about shipping a `__init__.pxd` without tests?
  - We have some tests, maybe need more
  - Test may need to be marked slow
  - Backport the changes the the `__init__.pxd`? not critical.
  - Refactored changes from Pandas into NumPy.


- NumPy logo redesign
  Isabela submitted some ideas, feedback is needed. https://github.com/numpy/numpy.org/issues/37#issuecomment-624348230
  - timeline: hopefully weeks


## Topics

- Website launch! :tada:

- Website next steps: [tracking issue](https://github.com/numpy/numpy.org/issues/266)
  - Tracking issue for small incremental improvements
  - Sphinx theme for documentation still needs to be updated
    - Tutorials will integrate with that.

- CodeCov re-activation: https://github.com/numpy/numpy/issues/16405
  - Code coverage does not work for reused C-code?

- Call for help to SIMD specialist reviewers to help push the SIMD changes over the finish line?!
  - seiko2plus PRs are a big chunk being finished. This week he split them into 3 PRs:one to handle the compile-time build pieces, one to use the new intrinsics in ufuncs (and a few other places), and one to expose the features to python-level. They are supposed to be sequential. 
  - Raghuveer has some PRs open to use more intrinsics
  - Talk to experts for ARM, Intel/AMD (for x86), and IBM to review the performance and code generation.

- Inessa, Ben and Ralf will work on the newsletter. There's a subscribe form in the footer of the mailing list, who signs up there will get the newsletter.


- NumPy Community Survey - at the back translation stage. The survey team will hold a meeting in early June.


- NumPy 2.0?
  - What should go into a 1.x last release (e.g. SIMD)
  - How long do we need to keep supporting a 1.x series?
  - Here is the list of ideas: https://github.com/numpy/numpy/wiki/Backwards-incompatible-ideas-for-a-major-release
    - Similiar changes to implementing `__round__` correctly for Python 3. There may be remaining Py3 backcompat things.


- Complex numbers, Rakesh is looking into deprecating complex comparisons.




## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  - Finish leak check (pytest-leaks, pytest-valgrind runs) and fixes
  - Scalar speed/buffers
  - some NEP 42 revising

- Ross

  * Thoughts on switching the default latex engine for the latex/pdf version of the docs to `xelatex`? Please share opinions in [#16394](https://github.com/numpy/numpy/issues/16394)

---

Please remember to archive this file and commit it to github.com/numpy/archive

