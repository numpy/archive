---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-01-29 NumPy community meeting

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

**Present:** Sebastian Berg, Tyler Reddy, Joren Hammudoglu, Charles Harris, Maanas Arora, Stéfan van der Walt


## Follow-up from the last meeting / discussions

- Petr asked if we want to write a PEP about allowing custom DType definitions in the buffer protocol format (by abusing/etending format):
  - Yes, Sebastian and Nathan would want to but have to see when time comes around.

- Setting up CI for windows arm may be possible now.
  - flang is available for openblas and f2py tests


## New topics

- A few new mypy only issues: redirected to MyPy.

- Shape type meeting summary (there are PEP drafts around that, but it is still in an early phase, with two approaches and neither were convincing to Eric Traut).

- New repo to develop typing stubs outside of NumPy: https://github.com/jorenham/numtype
  - move to `numpy` GitHub org at some point
  - We should look into names e.g. `numpy-stubs` and liberate the project on PyPI (since it seems reserved, potentially by us).





## Action items



---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
