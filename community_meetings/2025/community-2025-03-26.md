---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-03-26 NumPy community meeting

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

**Present:** Tyler, Chuck, Maanas, Sebastian, Michael S., Chris S., Sayed


## Follow-up from the last meeting / discussions

- We may want to shift the time slot again (at least when Europe shifts time zones, which is in April).
  - Send a mail to the mailing list and ask.

- Sayed work plan for NumPy.
  - Idea for getting more math kernels/moving svml:
    - subrepository for working on these
    - Use highway (mostly?)
    - Do not work within highwigh (churn, python tests, FPE needs that might not quite match.)


## New topics

- Subrepository naming discussion, using "svml" in the name is maybe not great.  `numpy-simd-routines` could be one name.
  - We should create this repository.
  - Sebastian: Will create a repo with Sayed, Chris and Raghuveer to be admin.

- Use `out=...` to ensure no scalar return.
  - Useful internally in a few places (more than in PR), mostly to deal with `object` and maybe for better speed.
  - `_methods.py` usage is tricky (unless I don't drag along subclasses, which may well be the right thing)
  - Does not preclude returning fewer scalars in general.  (Sebastian: My opinion as usual is 0-D array result for 0-D array input rather than aiming for no scalars at all.  We can do this now pretty easily -- I have a branch -- the main issue is actually downstream because for them aligning to return return scalars where NumPy would isn't easy.  If downstream was OK to just consider much of their things "array only", things would be easy, but someone has to test things or write a NEP...)

- Sorting DType slot came up, curious if we should remember something:
  - Should provision for ascending/descending flag, I think (Sebastian).  (This would be public C-API, it can be changed but it's not that nice.)
  - I think we could probably do only contiguous+aligned (because copying is probably usually worthwhile), but could also pass strides (even if always contiguous)
  - Considering if we need am "unsupported sort kind" return indicator (i.e. so if we add one, we can also add logic to fall back to another)
  - (NA placement is usually a parameter in dataframes. I lean towards always sorting to the end, no matter which ascending/descending.  But we could provision for an option here as well.)
  - Should we allow non-contiguous sort functions?

- Discussion that string sort should be an indirect sort (which should be possible without the above refactor as well).

- Discussion about matmul and copies.



---


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
