---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-08-26 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)


**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian, Iason, Nathan, Chuck, Sam, Aniket, Maanas, Tyler, Shoumik, Joren, Inessa


## Follow-up from previous meetings / discussions

* Increased number of open PRs allowed to 2.

* Sebastian: Should we consider using https://ilayn.github.io/semicolon-lapack/
  * Agent generated (rather than f2c)... Both may be not perfect, but one is at least maintainable (I don't think our f2c stuff even still works from what I remember).
  * Everyone seems to think this is probably better than the f2c version but it will need testing and validation
  * Our current vendored LAPACK (lapack_lite) is a very old translation of the fortran LAPACK.
  * Gets us updates, maybe?
  * It's probably possible to regenerate at this point

## New topics

* Discuss `np.minmax` name and location and potential namespace for fused functions as Sebastian mentioned in the mailing list thread. 
    * what about a nan-version? (see https://github.com/numpy/numpy/issues/32439)
        * nan_policy kwarg needs a big discussion
        * it's possible to do with with a `where`

* Blog post about Iason's NumPy work this summer: https://github.com/Quansight/Quansight-website/pull/995
    * https://labs-git-fork-ikrommyd-ikrommyd-post-quansight.vercel.app/blog/teaching-numpys-ufuncs-new-tricks

* Maanas: Iason's np.searchsorted PR: https://github.com/numpy/numpy/pull/32346. Wanted to discuss the gufunc architecture briefly. It would be nice to move this!

* Inessa: prep for the NumFOCUS Contributor Series in partnership with Bloomberg, NVIDIA, G-Research, AWS
  - timeline: starts Sept 16, 10 weeks long
  - mentors: Sebastian, Ganesh, Inessa,...
  - issues labeled as `sustain-2026`
  - update the guide: https://hackmd.io/vkacBJioTp2O22NaIBnx2w

* ByteStringDType
    * https://github.com/numpy/numpy/pull/32433
    * https://github.com/numpy/numpy/compare/main...ngoldbaum:numpy:bytestringdtype

* [numpy-financial](https://github.com/numpy/numpy-financial)
    * https://github.com/numpy/numpy-financial/issues/137
    * Inessa will invite the person who volunteered to a meeting
    * Also will talk to Ralf/Travis to find resources to cut a release



### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
