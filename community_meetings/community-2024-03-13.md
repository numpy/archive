# 2024-03-13 NumPy community meeting

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

**Present:** Sebastian Berg, Chuck Harris, Inessa Pawson, Tyler Reddy, Nathan Goldbaum, Ralf Gommers, Matti Picus, Brigitta Sipocz, Raghuveer Devulapalli, Michael Haas, Sayed Adel


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2024-02-28.md_

- Review of [the NumPy 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)
    - All done!
 

- How to announce 2.0?
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is a while away.
  - Can also add a short snippet into the project readme "on github".

- UMATH C++ interface a kiss of life from Marten, https://github.com/numpy/numpy/pull/19753.
  -  When to merge? After the branching of NumPy 2.0
  -  Changing the signature of the inner loop is problematic, especially around dispatching. But Sayed suggests making the wrapper around the changed signature into be meta-objects that will mitigate much of the problem.


## New topics

- NumPy 2.1 might need to be pushed back. Following the regular schedule it would be released in July. Coordinating with the CPython release could help.
   

- (idea) Targeting the NumPy C API with a header-only install.
    - We're down to only this for platform/build-dependent code: [numpy/_core/include/numpy/_numpyconfig.h.in](https://github.com/numpy/numpy/blob/main/numpy/_core/include/numpy/_numpyconfig.h.in)
    - Seems feasible indeed, no one sees a real blocker right now at least

- Can we clean up integer types?
    - Internally we can clean up a lot
    - External API is a large change and would need deprecating

---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
