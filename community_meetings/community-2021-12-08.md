# 2021-12-08 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 7:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Michael Siebert, Sayed, Matti, Ralf, Stephanie, Mars, Inessa, Melissa, Chuck


## Follow-up from last meeting / discussions

* Moving to cibuildwheel (anything left to discuss here?)

* 2021 NumPy survey results
  * There are volunteers for each section to perform an analysis (and review it), first iteration should be done soon (~1 week).
  * After that, analysis needs to be put together into a report.
  * "Detailed report" (the website) is updated but not available online yet (Ross should look into that)
  * "public use" data; clean data enough so there is no disclosure risk:
    - classify data based on sensitivity, threshold. 

* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  - tagged for 1.22.1, is this good enough?
      - [RG] yes should be fine. ship has sailed for 1.22.0 I think.

* Docs front landing page with sphinx-panels almost ready
    * [CircleCI preview](https://23834-908607-gh.circle-artifacts.com/0/doc/build/html/index.html) (recommended to view in Firefox to see all images, will not show in Chrome)
    * Trying to land before next release (late December) and backport candidate label
    * Need to change link to current Getting Started page
    * We have a least a few days (backport label should be used)



## Topics

* How do you announce on numpy.org?
  * A yaml file is added using a PR

* 1.22.0 and reduction dispatching: https://github.com/numpy/numpy/pull/20484
  - This is complicated, I (sebastian) will try to sort the behaviour a bit to explain, but not sure it is easy to discuss without getting up to date first.
  - (merged now, but I have to rip out the converters again, happy to discuss but overall I am not sure there is much point)

* Thoughts on `numpy.distutils` [change of plans](https://github.com/numpy/numpy/issues/18588#issuecomment-988110634)?
  - This means we will never try to make fortran, etc. work on setuptools, but go directly to meson or similar.
  - Basically, `numpy.distutils` is pretty limited when it comes to compiler support, but numpy uses its SIMD, BLAS and would have to move by Python 3.12.
  - matploltlib's C++ should be fine with this.
  - tl;dr some questions, but overall 

* Workflow policy about “abandoned” pull requests
  * General agreement on adding a policy for closing (but not auto-closing/messages by a bot)


* Apple NEON PR - merge strategy

* We have generally a bit of a SIMD backlog, also for Sayed PRs

* Appending to NPY: There is a new idea to leave one dimension at an undefined length (inferred from size)
  * Is multiple threads/fileIOs accessing a problem?

---

Please remember to archive this file and commit it to github.com/numpy/archive


