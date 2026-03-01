---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-02-25 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Chuck, Sam Morley, Joren, Tyler, Sebastian, Maanas, Inessa, Stefan van der Walt


## Follow-up from previous meetings / discussions

- Deprecations review: https://github.com/numpy/numpy/issues/30440
  - Would be nice to get these done some time soonish (but not urgent)

* Thoughts on new `reduceat` with better meaning for the start/stop points.
  * (Sebastian):
      * I like "segmented"
      * Happy to just add `start=, stop=` kwargs now
  * New name makes for a bit less API hassle.
  * Slight preference for a new name.
  * JAX and awkward have similar functionality. It is not clear if the Array-API working group would have an opinion.

- NEP 57 tiered platform support was merged :tada:

- [PR 30806](https://github.com/numpy/numpy/pull/30806) (C99 Annex G recoveries for complex multiplication and division following CPython) - opinions?


## New topics

- Discussion on AI-generated contirbutions
  - Long continued discussion on AI tooling and it's use/adoption and policies in the ecosystem.
  - Using the SciPy one looks pretty good, possibly make a PR and try to start another round of discussion?
  - The steering council is currently discussing how to address concerns raised in the discussion on the mailing list: https://mail.python.org/archives/list/numpy-discussion@python.org/thread/LAR7P3KQWHWAIKYSHTS2MY7X4HUBVA3L/


- datetime unitless deprecation. Did we have an opinion about preserving `timedelta_ns + 1`?
  - https://github.com/numpy/numpy/pull/29619
  - (Sebastian) I'll ping the mailing list, but in case we have a thought here.
  - Sebastian: I'll try to push this along then.


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
