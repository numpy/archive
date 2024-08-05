---
title: NumPy community meeting
tags: [NumPy]

---

# 2024-07-31 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Inessa, Matti, Sebastian, Chuck, Tyler, Tammy, Nathan

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings 

- Addressing distutils issues:
We have to use Python 3.11 for docs build, otherwise distutils docs doesn't work. We could link to the old documentation and drop the autosummary/internal links.


## New topics

- NumPy 2.1 release:
Chuck is waiting on response from OpenBLAS [issue 27036](https://github.com/numpy/numpy/issues/27036). 
The choices are:
  - patch OpenBLAS to revert to older threading code on Windows
  - use an older OpenBLAS version
  - find the problem


- Project's social media presence.
Discussion: Currently, we have accounts on X and LinkedIn for announcements only. There was some discussion on [a numpy.org issue](https://github.com/numpy/numpy.org/issues/765) to update the Twitter icon to X or to remove the X link altogether. There is some feeling X has become a controversial platform. Should we maintain our presence there?
  - Both "yes" and "no" were heard in the meeting.
  - Follower stats:
    - LinkedIn - 3.2k
    - X - 38.9k
  - Despite the increasing level of user engagement on LinkedIn, X continues to serve as a primary channel for communication with the broader NumPy community.
  - Conclusion: we should keep our presence on various social media platforms, but we do not need to invite users and contributors to connect with the project on social media. This decision is motivated by the fact that the primary goal of the NumPy social media accounts is to direct traffic to the website, rather than to expand our social media audience.

- What to do about `#include <complex.h>` defining `I`? It is breaking SymPy, but undefining `I` breaks other users. [issue](https://github.com/numpy/numpy/issues/27083)
  - We would prefer to stay with the current solution (`#undef I`) and document it better, since boost uses `I` in its public headers.

- NumPy 2.0 AMA
When: Tuesday, August 6th at 12 pm ET / 4 pm UTC
Where: via Zoom https://numfocus-org.zoom.us/webinar/register/WN_HRKnCdfhStW31Hc-LEnwfQ (Registration is required.)
Ask Me Anything (AMA) session with Nathan Goldbaum to dive deep into the new features of NumPy 2.0 and discuss future direction of the project.

## Action items

---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
