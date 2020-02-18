---
tags: NumPy
---

# 2020-02-05 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 11am Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)


**Present:** Stéfan, Ross, Warren, Matti, Sebastian, Inessa, Hameer, Chuck, ZJ Poh


## Follow-up from last meeting / discussions

- SIMD progress
  - Draft [NEP 38](https://numpy.org/neps/nep-0038-SIMD-optimizations.html),
    "Using SIMD optimization instructions for performance", was merged and a
    [mail sent to the mailing
    list](https://mail.python.org/pipermail/numpy-discussion/2020-February/080372.html).

    The [PR for cpu feature detection](https://github.com/numpy/numpy/pull/13421)
    has been merged. Now the real work to implement useful ufuncs in terms of
    universal intrinsics can be proposed.
  - In the mean time we have merged a number of AVX512-specific PRs that will provide a baseline for comparison.

- UMich visit summary
  * Summarized survey-related discussion from last week's triage meeting and
    sent along to the SURVMETH student team
    - Preliminary feedback from students suggests that releasing the survey
      before April is doable.
    - Meeting minutes/related documentation in 
      [github repo](https://github.com/numpy/numpy-surveys)
    - Next meeting Thursday 2/6 @ 1PM PST
  * EECS/MiDAS talks went well - lots of interesting convo with students
    and faculty


## Topics


- Scipy [preprint available](https://www.nature.com/articles/s41592-019-0686-2) - congratulations!!

- Update on NumPy paper
  - [first draft](https://github.com/bids-numpy/numpy-paper) is up and moving forward

- [Tensor Developer Summit website](https://xd-con.org/tensor-2020/) is up
  - Program is still in flux; likely will include more discussion / collaborative time
  - Now is the time to register
  - Will there be some coordination for housing?

- Other events: 
  - [SciPy Registrations](https://www.scipy2020.scipy.org/register) opened
  - Maintainer summit PyCon 2020 (Pittsburgh, April 15-23), call for proposal
    coming soon; Actual summit on the 17th (first day of conference proper).

- NEP 41: https://github.com/numpy/numpy/pull/15506
  - Can we move NEP 41 forward fairly quickly
  - Agree (as proposed) that the first step
    [PR-15508](https://github.com/numpy/numpy/pull/15508) can and *should* be
    added without a finalized full API proposal. Even if the direct use and usage
    is very limited.

- Documentation for v1.18 still is not on numpy.org, [issue
  15155](https://github.com/numpy/numpy/issues/15155). Should we produce the
  documentation as we did for previous versions (mattip did it) and try to fix
  the process documentation before 1.19?
  * **Ross B** - Have successfully built v1.18.1 docs manually - will PR/push today

- IEEE quad precision support? What should we change the name of float128 to?
  Proposals: floatdouble, then floatquad for true 128?
  - We should aim for a very small NEP proposing new names/warnings, etc.

- Storing unicode strings as UTF-8: can the new dtype system support it? What
  do you do about unicode points vs byte points? Do we need a latin-1 encoded
  dtype?


## Additional Details

- Matti
  - working on wheels for aarch65, ppc64le, s390x. Multibuild PR waiting for merge
  - Example of using cython with the new random API exposed some cruft
  - Some movement with cython 

- Warren
      
  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * NEPs, see above.

- Ross
  * "New" feature discoverability
    - Think about adding discoverability-related questions to survey
    - Rework user-facing docs (quickstart, tutorials) to use new `random`?
  * [Advertise `random` module](https://trello.com/c/PkP9KzeU/173-advertise-usage-of-new-random-api)


---

Please remember to archive this file and commit it to github.com/numpy/archive

