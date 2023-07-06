# 2023-07-05 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Tyler, Sayed, Matti, Raghuveer, Chris Sidebottom, Nathan, Jan Wassenberg, Charles, Ralf, Stéfan, Brigitta, Inessa 

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-06-21.md_

- Inessa: YouTube videos update: Jules Kouatchou (@JulesKouatchou) has provided timestamps for 4 videos.:tada:

- First big removals in the C-API, two new tags `python_removal`, `c_api_removals`

- A huge amount of work on https://github.com/numpy/numpy/pull/21057
  - doxygen used for documentation (should land in the build artifacts)
  - Will be split up into multiple PRs (e.g. split out testing)
  - Supports sizeless SIMD
  - [before](https://github.com/numpy/numpy/blob/main/numpy/core/src/umath/loops_comparison.dispatch.c.src) and [after](https://github.com/numpy/numpy/blob/1bd85d3bdc62141aaa98d338beda01f7f6602ff3/numpy/core/src/umath/loops_comparison.dispatch.cpp)

-  Mars: I'm not in this call, so here's written update: At **Writing Script, Thumbnailing stage** for GSOD-NumPy 2023
 

## New Topics

- Introductions from Chris (ARM) and Jan (Google)
  -  SIMD / [Google Highway](https://github.com/google/highway)
  - Adopting Google Highway would require a NEP. 
  - If we decide not to adopt it, we'll write a summary about this decision and devise an alternative plan.


## Action Items

- Matti P. will write the first draft of the summary of today's discussion.



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
