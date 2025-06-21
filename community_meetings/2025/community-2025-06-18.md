---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-06-18 NumPy community meeting

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

**Present:** Chuck, Joren, Michael, Sebastian


## Follow-up from the last meeting / discussions

- Performance monitoring: https://github.com/numpy/numpy/issues/28801 Can we make this step a part of release process? 
    - List of regressions: https://r-devulap.github.io/numpy/#regressions?sort=3&dir=desc

- Is windows_arm64 github action running? Should it be?


## New topics

- Apple fix for the matmul issue is there.
  - The PR looks good, can probably put it in as is.

- NumPy 2.3 is out, 2.3.1 will be released this weekend for a few more improtant fixes (e.g., the two matmul ones).

- PyPy in CI is broken again.

- Some discussion about `casting="same_value"`.
  - Maybe can-cast really doesn't matter, since in the end you never know that the cast will succeed.
  - Erroring on unsupported ones would be nicer though (but I guess no strong opinions).





### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
