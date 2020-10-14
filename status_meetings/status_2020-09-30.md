---
tags: NumPy
---

# 2020-09-30 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Bas van Beek, Sebastian, Ross, Ben, Ralf, Inessa, Maia Kaplan, Matti, Chuck


## Follow-up from last meeting / discussions

## Topics

 - **Community Survey**
   * Rough draft of data analysis is complete:
     - repo: https://github.com/rossbar/numpy-survey-results
     - rendered: https://rossbar.github.io/numpy-survey-results/
   * Please take a look and share feedback (issues/PRs welcome!)
   * Next steps:
     - Narrative text
     - Data modification for public distribution
   * Narritive: Inessa working on it (done in the next week)
   * Ralf will look into summarizing/analyzing the freeform text fields (roadmap related)

* Typing import cycle bug
  - An issue recently surfaced wherein mypy would crash when running the typing tests ([numpy/numpy#17316](https://github.com/numpy/numpy/issues/17316)). 
    - Reproducing the issue has been problematic, suggesting there are platform-specific factors.
  - The issues' origin was eventually tracked down to a mypy bug related to import cycles ([python/mypy#8481](https://github.com/python/mypy/issues/8481)).
    - More specifically one between `numpy` and `numpy.core`.
  - What next? Wait for mypy to fix the bug? Move the stubs in `numpy.core` back to `numpy`?
  
  Action items
   - Consider marking mypy tests as slow
   - band-aid fix for `mypy` test failures

- Unsolicited PRs - update the template

  - Create (or flesh out) the PR template
  - We currently mention that a PR may need a while to be reviewed, and especially some PRs unfortunately can get forgotten.  We should make these things very clear in the PR template?
  - We can invite PR creators to join the triage meeting, since it is a good time to discuss with higher bandwidth.
  - Ralf is looking into adding an expected time of reply --> done in https://github.com/numpy/numpy/pull/17407

- Update on paper feedback, DEI controversy on Twitter, and next step(s)
  - There will be a townhall meeting, and a discourse is in the process of setting up (within the next week hopefully)

* Test improvements would be nice, hypothesis could be part of this.

- (Sebastian) If time: I would like to propose NEP 42 for accepting, that will go to the mailing list, but if anyone wants to discuss/comment now.  (Also NEP 40, but that is only informational.)


## Additional Details

- Warren

  - Work on a faster text reader is on github at [npreadtext](https://github.com/WarrenWeckesser/npreadtext).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

