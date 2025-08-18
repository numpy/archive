---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-08-13 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sam, Chuck, Joren, Sebastian, Tyler, Britney Whittington, Maanas, Inessa, MattiP


## Follow-up from the last meeting / discussions

- Sebastian: Discussion about [sort PR](https://github.com/numpy/numpy/pull/28516)



## New topics

- Inessa: Take the poll to help us find a new time slot for weekly community meetings: https://crab.fit/numpy-community-calls-582036

- [Same-value casting](https://github.com/numpy/numpy/pull/29129) in asarray
  We will currently only allow numpy numerical types, and Matti will open an issue to detail what would be needed to support same_value casting in user-defined dtypes:
  - we need a way to ask the user-defined dtype if they can do same_value casting in general (`can_cast()`)
  - we need a way to actually get the correct inner loop with a same_value cast <- Correction, we have this already. We just need a way for `resolve_descriptors(...)` which returns `NPY_CASTING` to return "same_value works". Because same-value seems orthogonal to all other cast levels, it needs to be a flag though!

- Inessa: https://github.com/orgs/numpy/projects/9 - can we archive/close it? 
  - The project board has been closed.

- Inessa: https://github.com/numpy/doc/pull/20 - more feedback is welcome
  - No further feedback from the meeting participants, merging as it is.

### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
