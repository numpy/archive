# 2021-07-21 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Bas, Ryan, Charles, Melissa, Matti, Mars, Sebastian, Ralf, Tony, Ross


## Follow-up from last meeting / discussions

* 2021 user survey will launch on July 12th.
 Stephanie Mendoza is coordinating the project.
 The questionnaire draft: https://docs.google.com/document/d/1wCyuxll55ZjTR8RLbuGCB1VJkk5yjMMBdaP7glLitQ8/edit?usp=sharing
 * Dario Taraborelli, from CZI, reached out to congratulate the team for the great work on the survey



## Topics

* Next survey online :tada: https://berkeley.qualtrics.com/jfe/form/SV_aaOONjgcBXDSl4q
  * Add it to the newsbar on numpy.org

* Add the release announcement to 1.21.1 to numpy.org.

* Should we discuss the `copy=never` thing?

* SVML addition - it's very large, how to review & deal with it?
  * Raghuveer made a PR to vendor SVML from intel (100+k lines of code) and almost 1MB in binary (12MiB currently, but before 30MiB).
  * Within NumPy or separate?
  * Intel specific (it will not give any advantage e.g. on AMD)
  * The function advertise 4 ULP error:
    * How much worse is the high precision (1 ULP)  (Chuck: comment on it)
    * Run this by the mailing list  (Sebastian)
  * Verification data is now a separate PR which is great
  * Vendor vs. submodule vs. something else?  (Ralf)

* Accessibilty work for website/docs
  * github.com/isabela-pf/jupyterlab/pull/1
  * We should add alt texts
  * Melissa: Host a "sprint" with the newcomers to fix up alt-texts.
  * Also plots could use alt-texts

* Translations:
  * Coming along well
  * Preview available on the PRs(?)





---

Please remember to archive this file and commit it to github.com/numpy/archive



