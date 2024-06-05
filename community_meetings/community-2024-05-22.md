# 2024-05-22 NumPy community meeting

- Time: 7:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Ben Woodruff, Tyler, Sebastian, Matti, Anne Gunn, Nathan, Charles, Ralf

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/tree/main/community_meetings

- (after rc1 and maybe rc2) How to announce 2.0?
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is in a few weeks.
  - Can also add a short snippet into the project readme "on github".

- Release date: we are mainly waiting for other packages to release for compatibility. 
    - We are trying to set a date. There are no real blockers, but some downstream packages are not ready (tensorflow is a bit slow. netcdf4, sympy, xarray are slowly moving forward). CuPy is also not ready.
    - https://github.com/numpy/numpy/issues/26191
    - Let's arbitrarily pick June 16 - this gives downstream packages 3.5 more weeks to do their releases. Ralf will announce on the tracking issue and mailing list. (mattip) Maybe we can get some traction on Hacker News or Python Bytes?
    - What about 2.1? Let's try and target September, which would before the 3.13 release. By then we should have much of the no-gil support in place.


## New topics

- Release schedule (discussed, see higher up)

- [name=seberg] https://github.com/numpy/numpy/pull/26497/files
      - We have a lot of such delayed inits, any chance we can have local pattern instead!? We discussed a global static struct with a lock to hold all the globals

- [name=rgommers] Roadmap update: https://github.com/numpy/numpy/pull/26505
      - The PR updates the roadmap and adds a few new topics. As the Roadmap states, this is the framework for searching for new funding and developers, so it should reflect the desires of the NumPy community. We should publish this on the mailing list and maybe have a "summit" around the Roadmap.

- NEP 50 and NumPy API 2.0 changes: we should apply the  label to be able to keep track.



## Action items



---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
