# 2023-10-25 NumPy community meeting

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

**Present:** Ralf Gommers, Inessa Pawson, Tyler Reddy, Mateusz Sokol, Raghuveer, Stefan va der Walt, Nathan Goldbaum, Sebastian Berg, Chuck Harris, Ross Barnowski

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-10-11.md_
- Starting to make ABI breaks
  - there is some header cleanup we could do to move us closer to the limited API. There are some non-limited API uses in the public headers, and these should be hidden so that cython users can do `cimport numpy` with the limited API.


## New topics

- Cancel the next Optimization Team meeting, because at least Sayed, Matt, and Jan are not available. Inessa will do this, and also start sending invites to the mailing list.

- BLAS support in 1.26.1 had one bug (split libblas/libcblas related), will require a 1.26.2

- Setting a new target date for 2.0.0 branching/rc1.
   - Need new tracking issues on API changes for Numba and array API support
   - Reduced availability from quite a few folks for various reasons, both personal and because they're still busy with the Python 3.12 fallout
   - Updating [the 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)
   - The deadline for completing the tasks that remain in scope: Jan 1st, 2024 (there is some flexibility)



## Action items



---

### Let's connect and keep the conversation going!
Please enquire in a meeting or by mail how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
