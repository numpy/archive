# 2022–03-02 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 6:00 pm UTC
- [Numpy community events calendar](https://calendar.google.com/calendar/r?cid=YmVya2VsZXkuZWR1X2lla2dwaWdtMjMyamJobGRzZmIyYzJqODFjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Tyler, Sebastian, Ross, Rohit, Inessa, Stéfan, Matti


## Follow-up from last meeting / discussions

* **2021 Survey**
  - Need to change URL: currently `user-survey-2020-details`, want to drop the "2020". Is a repo name change sufficient or does there need to additional changes to e.g. CNAME?
  - (Renaming should just be renaming the repo when we are ready)
  - [name=Rohit] I would have thought we need to update the CNAME
  - 2021 results are (mostly) ready to go live: https://rossbar.github.io/user-survey-2020-details/index.html
    * List of outstanding issues: https://github.com/numpy/user-survey-2020-details/issues
    * Please add to the list if you happen to have a chance to review and notice anything that can be improved!
      - Milestoning blockers
  - Data in CI: include encrypted data and de-encrypt during workflow with secrets - any thoughts?

* **GSoC 2022** discussion (cross-discussed at the [SciPy Meeting](https://hackmd.io/pyhudrC5TgSwdJtpPldHgQ))
    * Mentoring organization application deadline – Feb 21st, 2022 18:00 UTC (https://developers.google.com/open-source/gsoc/timeline)
    * Joint proposal? [Ralf]
    * If anyone is interested in checking NumFOCUS org vs. PSF, ping Mridul from Networkx

* **GSoD 2022**
    * Updating https://scipy-lectures.org/, https://scipy-cookbook.readthedocs.io/?
    * https://developers.google.com/season-of-docs/docs/timeline
    * (Is being continued in the docs meeting)

* **doctests** seem to be broken (and the documentation about it as well)
  - refguide check runs on the `.rst` files, but not the function (etc.) docstrings, maybe non-ufunc ones?
  - There is also a large skiplist


## Topics
    
* Apparently the fix for one of the CVEs got missed for 1.22.2? https://github.com/numpy/numpy/issues/19038#issuecomment-1048886879
  * Sebastian will send an update request.

* **NumPy Newcomers' Hour** – March 10th, 2022 at 4 pm UTC 
*Speaker:* Mukulika Pahari
*Topic:*  Presentation of the tutorial <i>Analyzing the impact of the lockdown on air quality in Delhi, India</i> (https://numpy.org/numpy-tutorials/content/tutorial-air-quality-analysis.html)

* **PyCon US 2022 – Maintainers Summit**
Call for proposals is open: https://forms.gle/oWbzY6B4MJwhUjTQ7
*Event schedule:*
Sunday, April 24th, 2022 – pre-recorded talks are released
Friday, April 29th, 2022 – live Q&A with the presenters of talks
Time: TBD
Location: in person and via Zoom

* Nvidia is hiring a NumPy maintainer: https://mail.python.org/archives/list/numpy-discussion@python.org/message/G3C46ECE5SA6AXJZVVA7JKANSRYPJRNQ/

* Address #10363 where numpy.vectorized functions return array unconditionally: https://github.com/numpy/numpy/pull/10378
It looks like the behaviour described in the linked issue is specific to SymPy. A broader discussion is needed, perhaps even a NEP.



---

Please remember to archive this file and commit it to github.com/numpy/archive


