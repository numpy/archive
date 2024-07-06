---
title: NumPy community meeting
tags: [NumPy]

---

# 2024-07-03 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian, Chuck, Nathan, Tyler, Mateusz

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings

- Release 2.0.1 with Python 3.13?
  - Python RC is coming in July, we should try to have a release around that time/soon after.
  - Branching 2.1 would have to be very soon.
  - That may also be fine: align us to the old release version.
  - It usually takes about 2 weeks to receive feedback on a new release. Let's hold of decisions for the next release until the next community call.
  - Nathan is already testing against Python 3.13 on main.
  - Dropping distutils: wait until the support for 3.11 ends.

- Discussion that we have to use Python 3.11 for docs build because otherwise distutils docs doesn't work.

- User annoyance reported:
  ```
  In [4]: np.clip(np.array([0, 255], dtype=np.uint8), 0, 455)
  ```
  Fails due to no promotion (Python integer) of the uint8 but 455 doesn't fit uint8.
  - Clip is implemented in Python, so if the input is a Python integer and the dtype is integral, we could check and just ignore the bound!


## New topics

* Single-initialization cache PR?
    * https://github.com/numpy/numpy/pull/26780
    * Sebastian will take a look, with an eye toward merging before 2.1.

* revert unique inverse indices? https://github.com/numpy/numpy/issues/26738
  * Probably, revert.

* NaN sort order in top k with lowest/highest.
  * Pushing to the end seems to be the most logical.
  * torch includes them in the largest, but not smallest.  Except when it doesn't (it breaks at least sometimes with signed nans or so)
  * https://github.com/numpy/numpy/issues/15128

* "import numpy as np" in docs
    * Just wanted to make people aware this change is coming.

* pylance wants us to take their type stubs https://github.com/numpy/numpy/issues/26845

* Integer `dtype` support for rounding functions: https://github.com/numpy/numpy/pull/26766 can we merge it?


## Action items




---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
