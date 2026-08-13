---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-08-12 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)


**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Nathan, Sam Morley, Joren, Pratham, Chuck, Iason, Tyler, Maanas, Shoumik


## Follow-up from previous meetings / discussions

* discussion about changing templates and considering auto closing, etc.
    * Pratham: maybe increase to 2?
    * Nathan now has admin access to the NumPy repo

* Sebastian: Should we consider using https://ilayn.github.io/semicolon-lapack/
  * Agent generated (rather than f2c)... Both may be not perfect, but one is at least maintainable (I don't think our f2c stuff even still works from what I remember).
  * Everyone seems to think this is probably better than the f2c version but it will need testing and validation

* Any takes on fixing `np.linalg.norm` overflow for representable results https://github.com/numpy/numpy/pull/31927?

## New topics

* Shoumik: https://github.com/numpy/numpy/pull/32126
    * not a lot of appetite for masked array changes
    * Maybe we should look at officially deprecating and pointing people at https://github.com/mdhaber/marray

* Iason: `np.minmax` PR up: https://github.com/numpy/numpy/pull/32231. Decision needed on where we want the ufunc `minimummaxium` to live. It currently is inside `np._core.umath` but perhaps there are use-cases out there? (Marten found one already). For `np.minmax` I have about 20 use-cases only in numpy so it deserves a top-level API imo. Review needed on SIMD as well.
    * What about nanminmax?
    * Iason will start a mailing list post about the new API surface

* Iason: PRs for generalizing reduction loops to `ufunc.reduceat` and `ufunc.accumulate` are open:  https://github.com/numpy/numpy/pull/32212 and https://github.com/numpy/numpy/pull/32213. Segfault found on the reduction loops by Nathan while reviewing: https://github.com/numpy/numpy/pull/32264

* Iason: experimented on draft of `ufunc.segmented_reduce` over the weekend with AI. Opened it as draft mainly for broad thoughts on the design: https://github.com/numpy/numpy/pull/32243

* Iason: I think I can safely backport https://github.com/numpy/numpy/pull/32156 as I'm responsible for the conflicts in `PyUFunc_ReduceWrapper` if you want to for the next 2.5.x patch release.

* https://github.com/numpy/numpy/pull/32231#discussion_r3753376764

### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
