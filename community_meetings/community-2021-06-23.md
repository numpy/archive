# 2021-06-23 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** 


## Follow-up from last meeting / discussions


## Topics

* Remove non-public objects from `__all__`?
    * Potential canidates: [numpy/tests/test_public_api.py](https://github.com/numpy/numpy/blob/001c1ca1c507ca18aa22742a5ca0b426a3b877e2/numpy/tests/test_public_api.py#L34-L56)
    * We can modify the `__all__` _except_ in the main namespace(s) `np.__all__`, `np.fft.__all__`, etc.
    * We can probably deprecate a lot of them, or deprecate the exposure in the main namespace.

* Accepting NEP 36 (fair play)

* 1.21.0 release announcements?
  * Not yet, but there were issues with the docs build.

* 2020 user survey results are released
 pdf report: https://numpy.org/surveys/NumPy_usersurvey_2020_report.pdf
 Detailed analysis: https://numpy.org/user-survey-2020-details/
 Infographic: https://github.com/numpy/numpy-surveys/blob/master/images/2020NumPysurveyresults_community_infographic.pdf
 
 * 2021 user survey will launch on July 12th.
 Stephanie Mendoza is coordinating the project.
 The questionnaire draft: https://docs.google.com/document/d/1wCyuxll55ZjTR8RLbuGCB1VJkk5yjMMBdaP7glLitQ8/edit?usp=sharing
 * Dario Taraborelli, from CZI, reached out to congratulate the team for the great work on the survey


* What to do about https://devdocs.io/numpy?
    * This is a [freeCodeCamp project](https://github.com/freeCodeCamp/devdocs)
    * In the docs team meeting, we decided we should add a link to the "canonical" docs at the Welcome message in our devdocs. 
    * Another idea is to add a top banner in our theme that only renders when not in the numpy.org site. <- probably not necessary.




---

Please remember to archive this file and commit it to github.com/numpy/archive



