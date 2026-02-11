# 2026-01-28 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Chuck, Tyler, Sebastian, Maanas


## Follow-up from previous meetings / discussions

- Deprecations review: https://github.com/numpy/numpy/issues/30440
  - Would be nice to get these done some time soonish (but not urgent)


## New topics

* Issue https://github.com/numpy/numpy/issues/28378. For the polynomial fitting in `numpy.polynomial` there is a parameter`deg` to fit a polynomial with only the specified degrees. This option does not play well with the `domain` and `window` arguments (and in particular the automatic selection of the `domain`/`window`) since whether a term of a specific degree is present or not depends on the choice of `domain`/`window`.

* Thoughts on new `reduceat` with better meaning for the start/stop points.
  * (Sebastian):
      * I like "segmented"
      * Happy to just add `start=, stop=` kwargs now
  * New name makes for a bit less API hassle.


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)

