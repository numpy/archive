# 2023-03-01 NumPy community meeting


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


**Present:** Matti Picus, Sebastian Berg, Ralf Gommers, Inessa Pawson, Brigitta Sipőcz, Tyler Reddy, Charles Harris, Melissa Mendonça



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-02-15.md_


- inessapawson/rossbar: Google Season of Docs 2023
    - Mukulika and Ross are available for mentoring.
    - Important dates: 
March 24th at 18:00 UTC - deadline for organization applications
For the full GSOD timeline, visit https://developers.google.com/season-of-docs/docs/timeline
  

- Topics for a GSoD:
  - Tutorials or how-to-guides on best practices for using numpy functions or performing certain tasks?
  - Google Season of Docs 2023 ideas by Mukulika: https://hackmd.io/8KTav_wLRY6hc6h-T8_1dA
  - Possibility: NumPy Comics
    - https://github.com/numpy/numpy.org/pull/600


- Adding copyright to code like in [PR 23171](https://github.com/numpy/numpy/pull/23171): do we have a policy? Is there one we can adopt?
*Discussion:* Introduce a policy for not including copyright notices in the code base. Possible exception: for complete files that can be used stand-alone in a different code base. 
*Update: See in New Topics*

- adding `types` to `np` or `np.lib`
  - Mainly used for DType classes, but available to other internal classes that would not end up in the main namespace (except exceptions).
  - `np.dtype[np.int64]`
  - Sebastian will make a poll (and then potentially abide by the result).


## New Topics

- Meson schedule/work discussion
  - SciPy on conda-forge is smoking out some issues (mainly related to cross compiling).

- `np.types`: Seems we can go ahead and add it.

- Copyright discussion followup:
  - A general consensus is to document that we do not add copyrights any more to this page: https://numpy.org/devdocs/dev/index.html
  - Possible next step: SPDX identifier per file.
  https://reuse.software/spec/ - this specification defines a standardized method for declaring copyright and licensing for software projects.
No priority at this point, it would be great to add it though.

- rossbar: How best to handle data for `numpy-tutorials`. Add a repo to the numpy organization?
Discussion: a general consensus is to go ahead. 
Question for Ross: Are there any pitfalls to watch out for?


- Pandas asked for a way to call a pure NumPy version in their `__array_function__` implementation: https://github.com/pandas-dev/pandas/pull/51653
  - Should we think about something like this `_implementation` exists, but they probably need `np.asarray()` called.
  - Not generally trivial (not all args are dispatched, concatenate/block take lists/nested lists, ...)
  - Should ask about using `_implementation`, doesn't solve the issue, but might be good enough here?

- Inessa: indicate your availability for the NumPy 2.0 meeting here: http://whenisgood.net/numpy2-meeting. 
Meeting format: 4 hours in total, 30-45 minutes per main topic for the release. Everyone is welcome to listen in.
So far, Monday, April 3rd looks best for everyone.


## Action Items

- [ ] Melissa to check with Mars for availability and interest in developing NumPy comics as part of GSoD


---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
