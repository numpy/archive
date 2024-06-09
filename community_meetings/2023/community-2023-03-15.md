# 2023-03-15 NumPy community meeting


- Time: 7:00 pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Inessa, Ralf, Charles, Brigitta, Sayed, Sebastian, Ross



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-03-01.md_


- Google Season of Docs 2023
    - Mukulika and Ross are available for mentoring.
    - Important dates: 
March 24th at 18:00 UTC - deadline for organization applications
For the full GSOD timeline, visit https://developers.google.com/season-of-docs/docs/timeline
  - Ideas for the projects:
    - Tutorials or how-to-guides on best practices for using numpy functions or performing certain tasks.
    - See some ideas in this doc: https://hackmd.io/8KTav_wLRY6hc6h-T8_1dA
    - NumPy Comics: https://github.com/numpy/numpy.org/pull/600


- Policy for not including copyright notices in the code base: https://github.com/numpy/numpy/issues/23315


- adding `types` to `np` or `np.lib`
  - Mainly used for DType classes, but available to other internal classes that would not end up in the main namespace (except exceptions).
  - `np.dtype[np.int64]`
  - Sebastian will make a poll (and then potentially abide by the result).


- Meson schedule/work discussion
  - SciPy on conda-forge is smoking out some issues (mainly related to cross compiling).

- `np.types`: Seems we can go ahead and add it.

- Inessa: NumPy 2.0 meeting - Monday, April 3rd, 3 - 7pm UTC
Meeting format: 4 hours in total, 30-45 minutes per main topic for the release. Everyone is welcome to listen in.


## New Topics

- Inessa: Newcomers sprints 2022 retrospective
If you mentored or reviewed PRs submitted as part of the sprints, share your thoughts here: https://docs.google.com/document/d/18Y5JBmA-_eSOcdfjaoDDU_ISu7HUPjxYzLgAu59ie8s/edit?usp=sharing
Questions:
What went well?
What didn’t work?
What could be improved?

- Inessa: Newcomers sprints schedule for 2023
  - **Confirmed** NumPy mentored sprint at PyCon US’23 (in person). 
For details about the event, visit: https://us.pycon.org/2023/events/mentored-sprints/.
Sign up as a mentor here: https://docs.google.com/spreadsheets/d/1IZKuxwbBWf-KDT29dcW2yrrdzXbKrwY12LzvvFf9cpo/edit?usp=sharing
  - **Invited:** https://ghc.anitab.org/programs-and-awards/open-source-day/
  - **Proposed**: SciPy'23, one newcomers sprint in LatAm or Africa
  - Discussion on sprints: there's a problem with CI that gets backed up. We can ask GitHub whether we can temporarily get a higher allocation of CI runners during sprints; Inessa will follow up on this.

- [name=rgommers] Accelerate is back :rocket:
    - Updated to LAPACK 3.9.1 & ILP64 support: https://developer.apple.com/documentation/macos-release-notes/macos-13_3-release-notes#New-Features. Performance improvements as well.

- [name=rossbar] Is dependabot back?
Discussion: Yes, Chuck activated it on Monday, March 13th. If it continues being noisy, he will switch to the manual mode.





## Action Items

- [ ] Melissa to check with Mars for interest and availability in developing NumPy comics as part of GSoD


---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
