---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-06-17 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sam, Joren, Iason, Nathan, tgamblin, Charles, Manaas, Kumar, Sebastian, Inessa, Josh

## Follow-up from previous meetings / discussions

* For 2.6 add a `top_k` implementation is on the horizon (via parition for now probably).
    * PR up (https://github.com/numpy/numpy/pull/31659), may be good to check once for API, and also compare beloe array API issues:
    * https://github.com/data-apis/array-api/issues/629
    * and PR: https://github.com/data-apis/array-api/pull/722
 
* 2.5 rc is out, but we can still backport things (especially bug fixes).

* Iason starting an internship on making things gufuncs and possibly `segmented_reduce`.

* 2.6 will drop 32bit wheel builds.

* Add highway for partitioning https://github.com/numpy/numpy/pull/31506
  * highway had a problem with sorting for everything: Enabling it for all dtypes (complex/float16).


## New topics

* Enabling support for reductions of ufuncs that return more than one outputs by registering reduction loops. First draft implementation: https://github.com/numpy/numpy/compare/main...ikrommyd:numpy:minmax and https://gist.github.com/ikrommyd/6d485183e19af69bc7ad6eb01327060c

* Has anyone ever thought of windows "arm64ec" builds (just curious at this point)?  (That is windows x86 ABI on arm)

* Speculative discussion about better functionality for calculating collections of reductions a well loop fusion.
  * Adding stdmean along with minmax maybe? 

* Nathan: Planning to work on a ByteStringDType and maybe also latin1, ascii encodings for STringDtype.


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
