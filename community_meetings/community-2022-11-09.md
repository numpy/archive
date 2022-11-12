# 2022-11-09 NumPy community meeting


- Time: 6:00 pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present** *(add your name and GitHub handle)*: Rohit Goswami (@HaoZeke), Cliff Hansen (@cwhanse), Micheal Siebert, Sebastian Berg, Evgeni Burovski, Matti Picus, Tyler Reddy

**Notes taken by:** Sebastian Berg

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-10-26.md_


## New Topics

- Documentation artifact link broke due to the permission changes for the OSSF security card.
   

- Sebastian: Should we move this meeting time? 
  - Let's create a http://whenisgood.net poll to see if one time slot is clearly better.

- Sebastian: Remove the Google community calendar.  (If no complains, will remove all events, and add a single full day event that the calendar is not being used anymore.)
  - Inessa will take charge of this (Sebastian had talked to her before.)

- Does "casting safety" make sense to you for values, lets say `np.array([1.0, 100], dtype=int, casting="safe")` existed, what should happen? `np.can_cast(int, "int8", casting="same_kind")`.
  - If you would allow "safe" for floats, that seems weird.



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
