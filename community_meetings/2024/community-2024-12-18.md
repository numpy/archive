---
title: NumPy community meeting
tags: [NumPy]

---

# 2024-12-18 NumPy community meeting

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

**Present:** Charles, Tyler, Mateusz, Matti, Melissa, Matt Haberland

## Follow-up from the last meeting / discussions


- The breathe (https://github.com/breathe-doc/breathe) team has been struggling to maintain the project. Refer to the comment:  https://github.com/breathe-doc/breathe/issues/990
 Can we help? Should we consider another dependency?
 Conclusion: we should hide the page that claims we support doxygen -> breathe-> sphinx and see if we can find a different c -> html system. Maybe mkdocs + [mkdocstrings](https://mkdocstrings.github.io/). Sayed suggests using direct doxygen -> HTML via https://github.com/jothepro/doxygen-awesome-css

- Sebastian: Do we still need the config flag on nditer?
  - was temporarily removed in https://github.com/numpy/numpy/pull/27883
  - It seems somewhat useful.
  - Just re-add it, if removal, we should deprecate probably.


## New topics

- NumPy 2.2.1: bugfix. What do we do with the typing? Maybe we should add a note recommending pyright over pypy.
- We are now using ruff instead of pycodestyle
- Melissa: PDF docs https://github.com/numpy/numpy/issues/27573. Melissa is happy to build the PDF docs and we are happy to accept them. She will create a PR with some number of PDF docs back not too far.
- OK for [`marray` logo](https://github.com/mdhaber/marray/blob/main/docs/logo.svg) to be derivative of NumPy logo? We have no real objections, as long as there is clarification in the documentation that we are not responsible for it.

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
