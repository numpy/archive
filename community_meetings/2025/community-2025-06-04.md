---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-06-04 NumPy community meeting

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

**Present:** Joren, Chuck, Sebastian, Nathan, Maanas, Sayed, Tyler


## Follow-up from the last meeting / discussions

- Performance monitoring: https://github.com/numpy/numpy/issues/28801 Can we make this step a part of release process? 
    - List of regressions: https://r-devulap.github.io/numpy/#regressions?sort=3&dir=desc

- 2.3 branching should happen in 3 weeks or so.
  - Now in ~1.5 weeks or so.
  - Get the churn in.
  - Sorting PR with OpenMP (optional support) would be nice (Raghuveer).
  - update vendored meson

- Moving forward with Highway wrapper
  - https://github.com/numpy/numpy/pull/28622

* https://github.com/numpy/numpy/issues/28687
    * Apple seems to think there is no good way to fix it on their end, because this is due to new use of vector extensions on ARM chicps.  (This should not be limited to M4, but rather the new OS).
    * They saying that with new extensions and using them, FPEs are just not going to work, so not sure what to do about that.
        * Just disable FPE checking?  But on which systems?
        * Any ideas what to ask more?
    * They are willing to look into a solution, but not sure what.

- Is windows_arm64 github action running? Should it be?


## New topics

- Sayed made great progress on https://github.com/numpy/numpy-simd-routines/pull/1

- 2.3 release RC our for 1-2 weeks now, no reports yet (which makes us nervous ;)).
  - The gcc 15.1 related PR to not do alignment trickery is the main outstanding PR.

- Discussion about strict aliasing (because it was part of the alignment PR discussion).



### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
