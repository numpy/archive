# 2026-02-11 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Matti, Sam, Iason, Inessa, Tyler, Sebastian, Chuck, Maanas 


## Follow-up from previous meetings / discussions

- Deprecations review: https://github.com/numpy/numpy/issues/30440
  - Would be nice to get these done some time soonish (but not urgent)

* Issue https://github.com/numpy/numpy/issues/28378. For the polynomial fitting in `numpy.polynomial` there is a parameter`deg` to fit a polynomial with only the specified degrees. This option does not play well with the `domain` and `window` arguments (and in particular the automatic selection of the `domain`/`window`) since whether a term of a specific degree is present or not depends on the choice of `domain`/`window`. Chuck will try to take a look.

* Thoughts on new `reduceat` with better meaning for the start/stop points.
  * (Sebastian):
      * I like "segmented"
      * Happy to just add `start=, stop=` kwargs now
  * New name makes for a bit less API hassle.
  * Slight preference for a new name.
  * JAX and awkward have similar functionality. It is not clear if the Array-API working group would have an opinion.


## New topics

- (mattip) Are there any actionable take-aways from the AI discussion on the mailing list that we should discuss here?
  - We did discuss it and basically reached some kind of concensus around a very short (4 line) policy statement, maybe based off the RedHat one, to guide contributors.

- NEP 57 tiered platform support was merged :tada:

- Does [deprecating `np.typename`](https://github.com/numpy/numpy/pull/30774#issuecomment-3885495766) need to hit the mailing list?

- Is it OK to stop honoring holes in structured dtypes?
  - We should add the flag now, and in a year bump the pickle format to handle it.

- User dtypes and formatting: we should finish the PRs.

- [PR 30806](https://github.com/numpy/numpy/pull/30806) (C99 Annex G recoveries for complex multiplication and division following CPython) - opinions?
 
### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
