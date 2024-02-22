# 2024-02-14 NumPy community meeting

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

**Present:** Chuck Harris, Ralf Gommers, Lysandros Nikolaou, Sebastian Berg, Inessa Pawson, Tyler Reddy, Ross Barnowski, Sayed Adel, Matti Picus, Nathan Goldbaum, Stefan van der Walt


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2024-01-31.md_

- Review of [the NumPy 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)
  - Improve NumPy-Numba compatibility - nice to have, but not a blocker
  - https://github.com/numpy/numpy/issues/23999 - documentation is pending

- NumPy 2.0:
  - Chuck would like to prepare for branching
  - A few things are still open. The biggest points are:
    - Array API NEP 56 (and maybe implementation)
    - Breaking dtype struct
    - Exposing new dtype API
    - Hiding descriptors

- How to announce 2.0?
  - Put a link into the release notes
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is a while away.
  - We should try to add more links out from the release notes to docs.
  - Can also add a short snippet into the project readme "on github".

- [2.0 milestones](https://github.com/numpy/numpy/issues?q=is%3Aopen+is%3Aissue+milestone%3A%222.0.0+release%22) review

  - numpy.array_api was moved to a separate package for NumPy 2.0: https://pypi.org/project/array-api-strict/


## New topics
- Any discussion need for descriptor changes?

- UMATH C++ interface a kiss of life from Marten, https://github.com/numpy/numpy/pull/19753.
  - Do we still need a NEP for the transition?
     - Sayed: we should move fast with merging the PR, without the NEP. 
     -  Mattip: since we already have solved many of the compiler availability and warning problems, I think there is not much of the change that is user-facing. So I don't think we need a NEP.
  -  When to merge? After the branching of NumPy 2.0
  -  Changing the signature of the inner loop is problematic, especially around dispatching. But Sayed suggests making the wrapper around the changed signature into be meta-objects that will mitigate much of the problem.

- Proposal to adopt an extended JSON format: expect a proposal via the mailing list

---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
