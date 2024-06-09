# 2023-08-30 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Ralf, Matti, Tyler, Inessa, Sayed, Brigitta, Mateusz, Nathan, Mars


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-08-16.md_

- The Optimization Team (SIMD) had its second meeting this week, and it's on the NumPy community calendar now.

- Short update on GSOD-NumPy 2023
    - Timeline may shift a bit

- CI restructure and moving all jobs over to Meson (https://github.com/numpy/numpy/issues/24410)
  - There are a few jobs left to move, it is progressing well. We will use QEMU on github actions instead of travis.
  - Giving up on Intel SDE for now.
  - Add oldest/newest version of clang/gcc (but only after we finish the migration)

- Follow up on leftover items for `bitwise_count` UFunc (added by Ganesh): https://github.com/numpy/numpy/pull/21429#
  * Sayed: SIMD optimization can be seamlessly applied by relocating the implementation of bitwise_count to [loops_autovec.dispatch.c.src](https://github.com/numpy/numpy/blob/main/numpy/core/src/umath/loops_autovec.dispatch.c.src)
  * Sayed has an update working that uses autovectorization, he'll push it to the PR.


## New Topics
- Inessa's CZI grant supporting her role as NumPy Contributor Experience Lead is ending on September 1st.
    - Australasia newcomers events could be good to keep going.
    - Video from presentation at SciPy US'23: https://youtu.be/uytmM0ulG6E?si=zoR2vXG0QiTpDujz
    - A report covering grant activities and outcomes will be ready in October.
    - We'd like to figure out later what activities that were grant-supported for the past two years to keep going and support as a team on a volunteer basis (or look for new funding for).

- NEP 55 (new string dtype)
  - merged a draft of the PR 
  - need a `numpy.strings` namespace, there's some steps to take 
  - Comments are very welcome, Nathan is happy to help with questions on the mailing list or privately

- Accelerate PR ([gh-24053](https://github.com/numpy/numpy/pull/24053)
  - will merge soon, targetting NumPy2.0
  - since it targets macos13.3+ arm64 we will need a new wheel for each python version


- NumPy 1.26
  - We should release an rc soon:
    - revert the cython bind Pr
    - fix the f2py issues
    - documentation for development with meson/spin

- Standalone benchmark script (https://github.com/numpy/numpy/pull/15987): it's useful for work on SIMD, but hard to integrate with `asv`. So we can merge it in its current form under `tools/`.

## Action Items



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: Please enquire in a meeting or by mail.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
