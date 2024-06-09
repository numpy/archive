# 2023-12-20 NumPy community meeting

- Time: 6:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian Berg, Ralf Gommers, Inessa Pawson, Chuck Harris, Tyler Reddy, Nathan Goldbaum, Mateusz Sokol, Sayed Adel, Matti Picus, Brigitta Sipocz

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-12-06.md_

- Review of [the NumPy 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)
  - Improve NumPy-Numba compatibility - nice to have, but not a blocker
  - https://github.com/numpy/numpy/issues/23999 - documentation is pending

## New topics

- Separating out `libnpymath`; also undoing the C++ addition there.
    - Update 20 Dec '23: https://github.com/numpy/numpy/issues/20880#issuecomment-1863558462
    - Deprecate now (emit a warning when relevant header is used), don't remove for 2.0 yet
    - Lysandros' plan can move ahead roughly as posted

- Sebastian: Opinions about adding `return_scalar=True` to `array_wrap`:
    - Downside: forces everyone to change their `__array_wrap__` quickly (deprecation but effectively forces you to update)
    - Upside: NumPy sometimes returns 0-D arrays, and sometimes scalars.  Without something new (and the only idea I have is this).  E.g. `memmap` can never _quite_ get this right (yes it might only really affect reductions, but...)
    - Doesn't seem like a huge problem as it only affects `__array_wrap__`.


- Inessa: NumFOCUS EOY fundraiser in partnership with PyCharm
  - Please review and merge https://github.com/numpy/numpy.org/pull/713 -> merged now


- Inessa: Moving forward on [ENH: add cov parameter to numpy.polynomial.polynomial.polyfit](https://github.com/numpy/numpy/pull/20889)
  - advanced users, especially from academia keep asking about it
  - Related issue: https://github.com/numpy/numpy/issues/20871
  - Chuck will review the related PRs and issues

---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
