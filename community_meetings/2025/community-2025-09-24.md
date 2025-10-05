---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-09-24 NumPy community meeting

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

**Present:** Sam Morley, MattiP, Chuck, Manaas, Nathan, Nick Byrne, Sayed, Tyler

## Follow-up from the last meeting / discussions

- Sebastian: Discussion about [sort PR](https://github.com/numpy/numpy/pull/28516)
  - Discussion about python API, C-API and lower level struct of the context. Chuck suggests we start with the C-API, get it called from python, and then modify the other parts to support the new parameters. Maanas suggests shrinking the PR to special-case string dtype. It seems in the end Chuck will try to submit a PR to do the high-level things.
  - 9 Sep discussion: Chuck's PR got merged, Maanas will make a new PR with some of the basic infrastructure, and then get input from Sebastian. 

  
- Inessa: make the numpy.org Plausible dashboard public
  - Update: we can collect stats about the traffic to NumPy docs via Plausible. Inessa will submit a PR.


- numpy-simd-routines: Dynamic/Precise SIMD Control, and testing unit based on buffer protocol.
  * Currently static, 1~ulp(F64), 4~ulp(F32), https://github.com/numpy/numpy/pull/29699
  * To enable independent testing, npsr intrinsics are mapped to support the buffer protocol, allowing Python projects to reuse them without low-level access. Could NumPy be one of the potential users?

## New topics

- Nick Byrne (OpenTeams) - Placeholder for discussion on internal numpy serialization format and potential link to zarr file format
- Nick Byrne (OpenTeams) - Placeholder for discussion on community interest (e.g. zarr-python) in extension of Buffer Protocol, and how this links to numpy
- Can we rust? https://hackmd.io/SBZ5vrLQRrOOlUog2tZ_9Q

### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
