---
tags: NumPy
---


# 2021-05-26 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Bas, Sebastian, Mars, Ross, Matti, Chuck, Ryan


## Follow-up from last meeting / discussions



## Topics

- Announcement: *next* meeting we will have a presentation/guests about tensor typing. (Bas, is in two weeks good for you?)
    - Bas: Yup, works for me


- String futurewarning/promotion [problem 1 – No way to get "future" behaviour for `np.array([1, "string"])`](https://github.com/numpy/numpy/issues/19078):
    - I could add a new flag to allow object (could be encoded with some special `dtype="object_fallback"` or `dtype="any"`).  [draft PR](https://github.com/numpy/numpy/pull/19101)
    - Or: Can we try to get pandas to actually just go with the warning themselves?
    - Or…
    - (Sebastian) will try to talk to Joris, to see how painful this is for pandas.

- String [problem 2 – `obj_arr.astype("U")`](https://github.com/numpy/numpy/issues/19085)
    - `np.can_cast("O", "U", casting="unsafe")` is the crux:  It tries to figure out the correct string length (but can't, unless I hardcode a "default" for object, which is bad).  Whether or not this can be an error, changes where I have to attempt to fix it. (`U` and `U0`)
    - (Sebastian) I will assume that it is OK to break the `can_cast`.

- AMMI OSS Python Workshop: https://bids-numpy.github.io/workshop_site_AIMS_2021/
  * **What:** A workshop to teach/encourage masters students in AI/ML to participate in OSS scientific Python development
  * **When:** June 3rd & 4th
  * **What I'm looking for**
    - Volunteers to introduce the projects that they work on:
      * Project intro: 10 min - Thursday June 3rd [4PM GMT (click for your timezone)](https://www.timeanddate.com/worldclock/fixedtime.html?msg=Project+Introductions&iso=20210603T16&p1=%3A&ah=1)
      * Mentored "sprint": 2 hours - Friday June 4th [3-5PM GMT (click for your timezone)](https://www.timeanddate.com/worldclock/fixedtime.html?msg=Mentored+sprint&iso=20210604T15&p1=%3A&ah=2)
    - Would be great to have mentors from projects like numpy, scipy, matplotlib, scikit-image, scikit-learn.
      * If you're interested, or know someone who you think might be, please let me (Ross) know!
  * I expect somewhere in the ballpark of 25-30 students
  
- Survey report :tada:
  * Feedback please!

- WiMLDS Summary/feedback


- CZI DEI grant proposal was submitted (with pandas, matplotlib, scipy)


- Contributor retention is the big problem with sprints/contributors in general.

- Ross has problems on GCC 11, the tests are hanging, e.g. on `repr(arr)`.




---

Please remember to archive this file and commit it to github.com/numpy/archive

