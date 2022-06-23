# 2022-06-22 NumPy community meeting


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


**Present** *(please add your name and GitHub handle, it’s completely optional)*: Angélica Cardozo, Alex de Siqueira, Rohit Goswami, Inessa Pawson (@inessapawson), @dwesl, Brigitta Sipőcz, Ricardo Prins, Mars Lee (@marsbarlee)


## Follow-up from last meeting / discussions

* seberg: Ralf brought up "NumPy-Numba interaction" on the mailing list, discuss?

* seberg: Pushing forward the [NEP 50 "prototype"](https://github.com/numpy/numpy/pull/21626)
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


* inessa: stats on inactive PRs: https://docs.google.com/document/d/13D4rex8gkani7PkGdAFqOK497zLHK7ne8XmS8Wob0Fw/edit?usp=sharing.

Action item for Inessa: Move this from Google Docs to Github

Consider adding a bot notifying about PRs that's been inactive for 6+ months (following the policy about inactive PRs: https://numpy.org/devdocs/dev/reviewer_guidelines.html).</br>
This is a low priority.
 
        
## New Topics

* Getting better notifications about discussions on GitHub. (GitHub will hopefully implement that.)

* rgommers: Windows on ARM request (https://mail.python.org/archives/list/numpy-discussion@python.org/message/QVVY24CHAQFLREKO26LUX4LN6J4AJ7BQ/) & supported platforms
  - Deferred

* rohit: f2py `int` return? 
seberg: May depend on the platform calling convention? Does that always return an int?


* next NumPy Newcomers’ Hour – Thursday, June 30th, 2022 at 4 pm UTC
Speaker: Ryan C. Cooper
Topic: NumPy in the classroom


- NumPy sprint at SciPy'22. 
Sebastian will sign up.



---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


