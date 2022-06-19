# 2022-06-08 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present** *(please add your name and GitHub handle, it’s completely optional)*: Lev Maximov, Meekail Zain, Inessa Pawson (@inessapawson), Rohit Goswami, Ross Barnowski, Ralf Gommers, Brigitta Sipőcz, Sebastian Berg, Mars Lee (@marsbarlee), Sanya Sinha, Matti Picus, Chuck Harris


## Follow-up from last meeting / discussions


* **NumPy Newcomers’ Hour** – June 2nd, 2022 at 4 pm UTC<br>
  Speaker: Sebastian Berg<br>
  Topic: Maintaining NumPy: Deprecations<br>
  Video recording is now available on the NumPy YouTube channel: https://youtu.be/DjiC4-8c5f0
  (Remember to subscribe!)


## New Topics

* [name=seberg] Ralf brought up "NumPy-Numba interaction" on the mailing list, discuss?
  - This [tracking issue on Numba](https://github.com/numba/numba/issues/8008)
  - Compatibility: something in NumPy not working in Numba
  - if a very important downstream project like Numba says there's a problem, it should be a higher priority than a random bug
  - historical: dubious decisions that a random person made in NumPy 15 years ago affecting Numba now, e.g. lists are mutable, D-types
  - read the list Numba gave and get a big picture
      - labeling
      - identify small fixes, what can be clarified in documentation, what needs long term work
      - Ralf gave initial feedback and would like others too as well
  - Whose responsible: downstream vs upstream?
      - downstream projects to report upstream
      - Numba could avoid big breaks if ...?
      - ask downstream projects to check CI? Testing against main?
  - Sebasitan: Mark big issues, such as API changes. Need someone to champion changes before gets lost to other issues, time passing
      - "This is important for X, Y, Z project, here's the PR, discuss at one triange meeting, done"

* [name=seberg] Pushing forward the [NEP 50 "prototype"](https://github.com/numpy/numpy/pull/21626)
    * Can we push this forward without being final, what would still be needed?
    * Make the new API functionality underscored?
    * Add to "global state" help page (and maybe NEP 50 itself)
    * Other things...?
    - Charles: maybe not best way. A seperate branch as whole new release
    - Matti: turn default on, if breaking to closer to release, turn off
    - Ralf: in principle, merge into main early so people can test non-default behavior (eg Windows)
    - Charles: Why seperate branch? If you want people to run it, make it absolutely simple, may not even know it's there until it breaks
        - Simple to run = widely tested
    - Ross: Maybe put in main with default behavior, put pinned issue "if you got problem, post, we'll fix at 1.24" before next release
        - Matti: If break a lot of things, need to decide to commit to behavior or revert. Would need to stop nightly, don't want to stop nightlys
    - Sebastian: Are we OK with development branch as main branch? Or environmental release?
    - Ralf: leaning towards environmental. bunch of issues, harder to install if seperate branch
    - Reach out to people we want to test it

* [name=axil] Two minor enhancements to np.polynomial: [ENH: Make Polynomial adhere to set_printoptions #21653](https://github.com/numpy/numpy/issues/21653) and [ENH: Replace x**1 with x in polynomials str representation #21695](https://github.com/numpy/numpy/issues/21695)
    * Reduce digits displayed
    * Currently overly long, over 16 digits...
    * Different contexts, different needs
        * teaching class, less digits, cleaner presentation
        * doing work like interpolation
    * Modes
        * Fixed float mode, keeps trailing 0s intact
        * Default float mode, drops 0s
    * Only changes display, not change results, so shouldn't break anything
    * Ross: Yes, why shouldn't polynomials follow set_printoptions as well? Will look at it
    * General consensus: makes sense

* [name=inessa] stats on inactive PRs (>75% complete): https://docs.google.com/document/d/13D4rex8gkani7PkGdAFqOK497zLHK7ne8XmS8Wob0Fw/edit?usp=sharing.
The list gives an idea of *truly* inactive PRs. 
    * Reasons for the lack of progress:
        * Inactivity of the author
        * Waiting for a review (about 1/3 in the presented list)
    * Action item for Inessa: Move this from Google Docs to Github
    * What is the best way to identify and label inactive PRs automatically?
            * Charles: could easily change a changelog script, Python interface for Github
        * Default Github filter, last comment date
        * Built queries in triage meeting notes
    * Fundamental problem is not discoverability but what to do with inactive PRs
    * How to close these PRs
        * Charles: If we close 3-4 at each triage meeting, we'll make a noticeable progress in a year.
        * Inessa: A sprint where core developers review inactive PRs.
        * Sustained or sprint, need to do something
    * Suggested workflow: ping author of inactive PR, if no response in 6 months, bring up in Triage Meetings, then close? (As per the newly adopted policy.)
    * Issues older than a year will need a rebase
        * Brigitta: old PR broke main because didn't break on old tests
        * Ross: You mean the colors are lying to me??
---
### Let's connect and keep the conversation going!

Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


