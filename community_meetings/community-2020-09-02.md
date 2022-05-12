---
tags: NumPy
---

# 2020-09-02 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (18:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa Pawson, Charles Harris, Melissa Mendonca Weber, Matti Picus, Sebastian Berg, Warren Weckesser, Ben Nathanson, Ryan Cooper



## Follow-up from last meeting / discussions

**Community Survey**
The survey is closed.
*Responses:*
- completed: 925
- in progress: 326 

27 volunteers helped with the initiative.

The minutes from the latest Survey Team meeting: https://hackmd.io/4sAhygrmS8mr7_BZmqXuKA?view


## Topics

- New Sphinx theme: merged. Cleanup is needed [issue 17211](https://github.com/numpy/numpy/issues/17211), [issue 17207](https://github.com/numpy/numpy/issues/17207), [issue 17200](https://github.com/numpy/numpy/issues/17200), [PR 17220](https://github.com/numpy/numpy/pull/17220) reverting another PR. Version selector may be on the horizon from the theme itself: [here](https://github.com/pandas-dev/pydata-sphinx-theme/issues/23) and [here](https://github.com/pandas-dev/pydata-sphinx-theme/issues/234)


- [Policy on tools that share information with commercial firms](https://github.com/numpy/numpy/issues/17066)
  - The actual proposal: https://github.com/numpy/numpy/issues/17066#issuecomment-672180898
  - Google Analytics: is present on numpy.org. --> seems fine; Matti is more worried about matching expectations (a user can set their browser to block this stuff, so not much of a worry).
  - For now we're good; if someone wants to put in the work to have a more privacy-sensitive option, they're welcome to do so.



- NEP process
  - Mailing list discussion [link](https://mail.python.org/pipermail/numpy-discussion/2020-August/080942.html)
  - Matti suggests a two-stage process, where phase 1 is just the user-facing part of the NEP, get that right first, merge as draft. Then add the implementation related sections in a second PR.
  - User story / user-centered design / etc. the essential bit is: how does the user interact with the feature being proposed.
  - The examples that would go in a docstring should be in the first part.

  - Do we need to update [the template](https://numpy.org/neps/nep-template.html) with an extra section on API usage examples? --> Usage and Impact section is present in the template.


- API standardization initiative
  - [Announcement blog post](https://data-apis.org/blog/announcing_the_consortium/)
  -  People involved: https://github.com/data-apis/governance/blob/master/members_and_sponsors.mdy7




## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

