---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-04-08 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:**  Sebastian, Nathan, Chuck, Tyler, Joren, Kumar Aditya, Maanas


## Follow-up from previous meetings / discussions

- Deprecations review: https://github.com/numpy/numpy/issues/30440
  - Would be nice to get these done some time soonish (but not urgent)

- [PR 30806](https://github.com/numpy/numpy/pull/30806) (C99 Annex G recoveries for complex multiplication and division following CPython) - opinions?

- Float32/float16 precision, any other thoughts?
  - Default should be comparable to glibc, etc.
  - Huge speed benefits might move this trade-off a bit.
  - Can be very application specific unfortunately


## New topics

- Stable C-API for free-threading in NumPy headers.
  - https://github.com/numpy/numpy/pull/31091 

- Discussion around caching: We should try mimalloc to see if it is fast enough to just disable small allocation caches.
  (For now relevant for free-threading, but mimalloc might hit normal
  Python in the not so far future as well.)


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
