# 2021-10-13 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 16:30 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Tyler, Bas, Stephanie, Mars, Chuck, Mukulika, Ross, Melissa, Matti, Rohit, Ralf

## Follow-up from last meeting / discussions

* [Experimental DType/UFunc API exposure](https://github.com/numpy/numpy/pull/19919)

* PyPy 3.8 testing is back :tada:

* Replace LGTM with github security scan?

* 2021 Community Survey
  * 522 Responses (not all complete; ~60% complete, which is good)
  * Got responses in each of the provided languages, which means all of the translations were utilized
  * Next steps:
    - Detailed report (Ross + Stephanie will set up a meeting for this)
    - Sentiment gathering from write-in responses - need volunteers (Melissa and Inessa can help)
    - Public data: personal disclosure is the concern - ideas?
    - Timeline proposal
      * It'd be good to release the executive summary + the detailed summary at the same time
      * Best to work synchronously on the development of the high-level report 
      * Not concrete "deadline" - it'd be good to have results in place before the next round of survey though
  * We now also have data from multiple years! Could add some additional "time-series" analysis of the data as well
  * Suggestion for numpy.org: to improve the navigation to /user-survey-2020 and future reports.




## Topics

* Move triage meeting move to this (the same) time.

* Use [discourse](https://discuss.scientific-python.org/) additionally/move?  (and spam)
  - Ping python people about the spam (We did this, but no response yet)
  - It sounds like a gentle consensus to move forward with discourse
  - Possible categories to start: Developers, Users, Announcements

* Moving to cibuildwheel. And to not having a separate `numpy-wheels` repo (?).
  * related to https://github.com/numpy/numpy/pull/20102
  * We should migrate

* Annotating the main numpy namespace is, more or less, complete :tada:

* [Factoring out the numpy.org hugo theme](https://github.com/numpy/numpy.org/issues/475): related [SciPy.org PR](https://github.com/scipy/scipy.org/pull/413), [repo for scientific-python-hugo-theme](https://github.com/scientific-python/scientific-python-hugo-theme) -> posted on the #numpy-dot-org channel on slack for those interested in discussing
– the theme used for numpy.org (https://github.com/scientific-python/scientific-python-hugo-theme/) is being adopted by other projects in the SciPy ecosystem;
– it will be maintained and enhanced by Stéfan van der Walt and Jarrod Millman as part of the Scientific Python Ecosystem Coordination project (https://scientific-python.org).


* Side discussion: SciPy seems to be drowning in PRs
  * There is a problem with "general purpose" maintainers
  * There are some grants (mainly Nasa) which should be helpful at least in a while.

* Should we consider https://meeseeksbox.github.io/ for backporting? (ipython and matplotlib use it, I believe)
  - Probably not much gain at this time


---

Please remember to archive this file and commit it to github.com/numpy/archive



