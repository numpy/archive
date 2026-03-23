---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-03-11 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Joren, Sebastian, Tyler 


## Follow-up from previous meetings / discussions

- Deprecations review: https://github.com/numpy/numpy/issues/30440
  - Would be nice to get these done some time soonish (but not urgent)

- [PR 30806](https://github.com/numpy/numpy/pull/30806) (C99 Annex G recoveries for complex multiplication and division following CPython) - opinions?

- Discussion on AI-generated contirbutions
  - Long continued discussion on AI tooling and it's use/adoption and policies in the ecosystem.
  - Using the SciPy one looks pretty good, possibly make a PR and try to start another round of discussion?
  - The steering council is currently discussing how to address concerns raised in the discussion on the mailing list: https://mail.python.org/archives/list/numpy-discussion@python.org/thread/LAR7P3KQWHWAIKYSHTS2MY7X4HUBVA3L/


## New topics

- AI PR: dependabot exception, let's not spell it out (even if it might technically use some AI stuff in the background).

- PR for changing `.imag` and `.real` has `object` loop, which does:
  `getattr(element, "real", element)` and `getattr(element, "imag", 0)`.

- Float32/float16 precision, any other thoughts?
  - Default should be comparable to glibc, etc.
  - Huge speed benefits might move this trade-off a bit.
  - Can be very application specific unfortunately

- Discussion about how to create fast path
  - Sebastian: State on errstate -> stored in context -> get_loop can get a flag passed in.  *But* of course the current loops go through `get_loop` very indirectly, so you'll have quite some code churn to actually override `get_loop()` nicely.

- `npz` file loading speed.
  - nibabel probably doesn't even load the whole file?


- pixi builds, add pixi CI jobs for thread sanitizer builds for NumPy which take ~35 minuts.
  - Discussion around CI jobs, rather ambivalent about this new jobs
  - Cron-jobs seem fine, so long we get a clear issue and notice and that doesn't get too often/annoying.
  - It would be good to make it easy to trigger the full jobs on some PRs (e.g. SIMD related, run all SIMD tests).
  - It would definitely be good to run less tests/subsets most of the time!


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
