# 2023-02-01 NumPy community meeting


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


**Present:** Ralf Gommers, Charles Harris, Nathan Goldbaum, Craig Peters, Sayed, Matti Picus, Dennis Chukwunta, Sergio Rojas, Ross, Brigitta



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-01-18.md_



## New Topics

- Mukulika Pahari is a new NumPy maintainer! :tada: 

- Discussion about array clearing.

- Status of "exotic" CI jobs & their maintenance burden
    - Some issues with Cygwin recently, Emscripten has been stable, musllinux so far so good.
    - We're still happy with the current status on average.
    - Some discussion about CI platforms: Azure is the most problematic platform - can we get rid of it? Ralf volunteers to deduplicate some jobs, and Brigitta volunteers to work on moving jobs to GitHub Actions.

- Cleaning up CI jobs

- Speaking of the GIL: https://peps.python.org/pep-0703/

- 1.24.2 release not very pressing and a few things that should happen, but should probably happen soon.

- SSE3 vs. AVX2 as baseline (triggered by issue [gh-23074](https://github.com/numpy/numpy/issues/23074)):
    - https://github.com/scipy/scipy/issues/16984#issuecomment-1241698174





## Action Items


- [] Add Mukulika to the Maintainers Team on numpy.org (https://numpy.org/teams/)




---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
