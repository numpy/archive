---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-02-26 NumPy community meeting

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

**Present:** Matti, Joren, Tyler, Chuck, Sebastian, Lysandros Nikolaou, Michael Siebert, Nathan


## Follow-up from the last meeting / discussions


## New topics

- (Sebastian) Merge hash based unique: https://github.com/numpy/numpy/pull/26018 or does anyone have concerns?
  - adds `sorted=True` kwarg
  - changes `unique_values` to return non-sorted.
  - Squash merge it soon is good.

- PyPy wheels for NumPy?
  - Matti runs weekly tests of NumPy on PyPy (some small issues on windows).
  - No priority to create wheels.

- Allow 0 results for norms of empty matrices?!
  - https://github.com/numpy/numpy/pull/28343
  - Now that `inf` results are removed, this seems probably OK to me (sebastian).  (`max(abs(...))` isn't actually a consistent norm, but it doesn't use `min` at least.  TBH, I can see just everything returning 0, but dunno)
  - Lapack always returns 0, it implements these (plus `max(abs(...)`) except `ord='nuc'`.
  - Ask for a release note, then should be fine.  I.e. this seems like the typical convention at least.

- (Lysandros) Use BLAS with `einsum` when `optimize=False` but no contractions needed?

- Sequence coercion of array.


---


### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
