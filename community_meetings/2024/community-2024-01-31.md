# 2024-01-31 NumPy community meeting

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

**Present:** Stefan, Chuck, Tyler, Sebastian, Ralf, Sayed, Ross, Mateusz, Matti, Brigitta, Nathan


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2024-01-17.md_

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

- [String DType PR](https://github.com/numpy/numpy/pull/25347) is under review by Martin


## New topics

- Run towncrier to update release notes?
  - Ralf is planning to update the release note to start editing it.

- Issue to not remove the `trapz` functionality, but keep it under a name like `trapezoid`: https://github.com/numpy/numpy/issues/25586

- The project roadmap is a few years out of date. We should make an effort to update it. More broadly, we should think about scheduling time to think about long-term goals for the project -- what would we like to see in a NumPy 3.0?
  - Maybe as part of SciPy 2024 in July with a remote component?
  - Nathan will go through and update the things that are clearly out-of-date

- copy kwarg:
  - Add the string values as well?

- [NEP 56](https://github.com/numpy/numpy/pull/25542) about moving the array API into the main namespace

- [2.0 milestones](https://github.com/numpy/numpy/issues?q=is%3Aopen+is%3Aissue+milestone%3A%222.0.0+release%22) review

- Note new [GitHub mac 14 / M1 runners](https://github.blog/changelog/2024-01-30-github-actions-introducing-the-new-m1-macos-runner-available-to-open-source/)

  > Today, GitHub is excited to announce the launch of a new M1 macOS runner! This runner is available for all plans, free in public repositories, and eligible to consume included free plan minutes in private repositories. The new runner executes Actions workflows with a 3 vCPU, 7 GB RAM, and 14 GB of storage VM, which provides the latest Mac hardware Actions has to offer. The new runner operates exclusively on macOS 14 and to use it, simply update the runs-on key in your YAML workflow file to `macos-14`.

- [1.26.4 milestones] review(https://github.com/numpy/numpy/milestone/125)
  - Serious issue from Debian; [timestamp on package](https://github.com/numpy/numpy/issues/25681)

- GH issue to track ways to reduce binary wheel size: [ENH: Reduce size of distributed wheels #25737]((https://github.com/numpy/numpy/issues/25737))


## Action items


---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
