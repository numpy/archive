# 2022-11-23 NumPy community meeting


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


**Present** *(add your name and GitHub handle)*: Ross Barnowski, Ralf Gommers, Brigitta Sipőcz, Charles Harris, Sheng Pei Wang, Matti Picus, Melissa Mendonca, Inessa Pawson, Grace

**Notes taken by:** Sebastian Berg, Inessa Pawson


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-11-09.md_


- Documentation artifact link broke due to the permission changes for the OSSF security card.
  - Still broken, Ross was trying to find the right thing, but the permissions are still broken and debugging is a bit unclear.
  - Lets open it up again (i.e. no limits on permission) and tighten it up later.
   

## New Topics

- Should we just make the call have no waiting room
  - Seems like we can just do that.

- 1.24.x branched :tada: :cake: :champagne:

- Inessa: A video recording of Ross Barnowski’s presentation “Maintaining /numpy-tutorials” has been posted on the NumPy YouTube channel: https://youtu.be/A-UCO1F09M4

- [name=seberg] (if stakeholders are around) `longdouble` change, likely road forward
  - was mailing list discussion
  - How feasible do starts on alternatives seem?
    1. Creation of new DType (seems feasible to Sebastian, maybe we can even say its OK if it is finished _after_ the NumPy release)
    2. Limiting use to sane platforms.
  - How would the implementation of removing it look like as a C-API break.  This probably requires NumPy 2.0?
  - The interesting long doubles are really only, Intel extended precision (80bits), IBM double-double, and true quad precision (which nowadays is starting to exist in arm64).
  - Right now the issue seems not a big issue, so long certain fallback paths get removed.

- [name=rgommers] Update on Meson build & merging it into `main`
  - It is getting there, plan: Add one CI job, to make sure meson keeps working.  Doing a single clean PR.
  - Current remaining work is full SIMD support and improving blas/lapack detection.
  - Add CI for other jobs, but only run it manually?
  - PyPy working? :)


- [name=seberg] Creation of a new unit DType repo (partially just for organizational reasons)
  - This has to do with NASA grant which goes via 3 years, and has many things in pandas, numpy, etc....  One of these is working on a string DType for NumPy which also works on pandas.
  - Lets do that.


- [name=rossbar] Announcement: Brigitta and Mukulika have been added as maintainers to numpy-tutorials :confetti_ball: 



- [name=seberg] "Road to NumPy 2.0" 
  - *When should we do it?* 
  Jan 2024 seems reasonable.
  We should start planning in June 2023.
  - *What should go into 2.0?*
Clean up Python API, e.g., namespaces, libraries that are historical artifacts, functions with underscores
Remove C API.
  - *What should go into 1.25?*
Deprecation warnings in Python API.
Introduce Meson build.
This should be a deprecation release.

  - *To do:* 
[] Sebastian to propose a plan for NumPy 2.0


## Standing topics

- Inessa: Presentation topics for NumPy Newcomers’ Hour 
To suggest a topic for future presentations, leave a comment in this tracking issue: https://github.com/numpy/archive/issues/58.

- Inessa & Melissa: Documentation user stories (https://github.com/numpy/numpy/issues/22089)
*Feel free to add yours!*

---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
