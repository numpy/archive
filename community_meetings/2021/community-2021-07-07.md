# 2021-07-07 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Chuck, Stephanie, Inessa, Melissa, Ryan, Ross, Matti, Mars, Sebastian


## Follow-up from last meeting / discussions

* 2021 user survey will launch on July 12th.
 Stephanie Mendoza is coordinating the project.
 The questionnaire draft: https://docs.google.com/document/d/1wCyuxll55ZjTR8RLbuGCB1VJkk5yjMMBdaP7glLitQ8/edit?usp=sharing
 * Dario Taraborelli, from CZI, reached out to congratulate the team for the great work on the survey



## Topics

* New survey status:
    * Currently with the translators (should be done by friday, or maybe already done)
    * Left: Put into qualtrics
    * live on Monday
    * Advertising the survey:
      * Numpy.org, mailing list, NumFocus newsletter, our twitter (and numfocus), SciPy "tools plenary" and organizer slack
      * Email the numpy tutorial people?
    * Very similar to last years survey (intentional), we added "did you participate last year"

* Can we converge on the `copy=never` discussion?

* Floating point warnings flags (if time/interest it is a bit technical)
  1. ``NaN > 0`` should warn or not? IEEE warns, we currently do not. ``NaN != 0`` is True.
     * Maybe keep the current behaviour.
  3. We do not care about signalling NaN do we?
  4. Do we "fix" compiler/glibc shortcomings?

* Adding yet another CI service: aarch64 and https://github.com/WorksOnArm/cluster 
  * The Travis CI now works for now so no need to change anything further


* Ready to open discussion on [SPEC forum](https://discuss.scientific-python.org/c/development/12)
  - New SPEC about accessibility in OS projects
  - SPECs are going to go live at SciPy
  - Good people on the SPEC's team, so this is a great fit.

* Add accessibility label?
  - Can do, but not sure that there will be many.



---

Please remember to archive this file and commit it to github.com/numpy/archive
