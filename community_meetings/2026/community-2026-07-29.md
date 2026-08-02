---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-07-29 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)


**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Nathan, Iason, Tyler, Chuck, Joren, Pratham, Melissa


## Follow-up from previous meetings / discussions


## New topics

* Chuck is doing a release this weekend

* Sphinx is updated to v8.x

* PR label bot is not working anymore.
    * Melissa can take a look (maybe already fixed?)

* discussion about changing templates and considering auto closing, etc.
    * https://github.com/matplotlib/matplotlib/pull/32075
    * auto-close label too
    * Move AI disclosure to the top?

* Sebastian: Should we consider using https://ilayn.github.io/semicolon-lapack/
  * Agent generated (rather than f2c)... Both may be not perfect, but one is at least maintainable (I don't think our f2c stuff even still works from what I remember).
  * Everyone seems to think this is probably better than the f2c version but it will need testing and validation

* Iason: `np.unwrap` implemented as a gufunc has been merged https://github.com/numpy/numpy/pull/31848. The masked version `np.ma.unwrap` is almost finished too https://github.com/numpy/numpy/pull/32091

* Iason: axis/axes argument on `np.searchsorted` https://github.com/numpy/numpy/issues/4224. Needs API design decision.

* Iason: taking over https://github.com/numpy/numpy/pull/25476 and my take would be to add a `segmented_reduce` method on the ufunc. Different APIs below. Personally heavily leaning on the cuda one + axis support
    * https://docs.pytorch.org/docs/2.12/generated/torch.segment_reduce.html
    * https://docs.jax.dev/en/latest/_autosummary/jax.ops.segment_sum.html
    * https://www.tensorflow.org/api_docs/python/tf/math/segment_sum
    * https://nvidia.github.io/cccl/unstable/python/compute_api.html#cuda.compute.algorithms.segmented_reduce

* Iason: `np.unique` performance https://github.com/numpy/numpy/issues/31969. The plan with Nathan was to add a HyperLogLog implementation + a hardware-specific heuristic to choose the algorithm.

* Iason: sent out an email on the mailing list regarding the C99 Annex G recoveries for complex multiplication and division. Mine and Nathan's take are that we should probably not do this.

* Any takes on fixing `np.linalg.norm` overflow for representable results https://github.com/numpy/numpy/pull/31927?

Pratham: (prathamhole14) To be reviewed/merged 
- https://github.com/numpy/numpy/pull/31765
- https://github.com/numpy/numpy/pull/31992
- https://github.com/numpy/numpy/pull/31069
- https://github.com/numpy/numpy/pull/32130

Melissa: https://github.com/numpy/numpy/issues/28734
 * should we close this?

### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
