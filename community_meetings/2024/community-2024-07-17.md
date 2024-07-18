---
title: NumPy community meeting
tags: [NumPy]

---

# 2024-07-17 NumPy community meeting

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

**Present:** Matti Picus, Chuck Harris, Nathan Goldbaum, Brigitta Sipocz, Ralf Gommers, Inessa Pawson, Ben Woodruff, Paul Otieno, Astha Puri, Tyler Reddy

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings

- Release 2.1.0 with Python 3.13?
  - Python RC is coming in July, we should try to have a release around that time/soon after.
  - Branching 2.1 would have to be very soon: probably mid-next week (before July 26).
  - That may also be fine: align us to the old release version.
  - It usually takes about 2 weeks to receive feedback on a new release. Let's hold of decisions for the next release until the next community call.
  - Nathan is already testing against Python 3.13 on main.
  - Dropping distutils: wait until the support for 3.11 ends.
  - Branching 2.1.x around July 24-28 is the plan. The one identified critical item is `numpy.f2py` support for free-threading. 

- Discussion that we have to use Python 3.11 for docs build because otherwise distutils docs doesn't work. Could we make a static copy of the documents built with an older python and add them as legacy? Probably too difficult, maybe just link to the old documentation and drop the autosummary.


## New topics

* NumPy 2.0 community feedback BoF
    * https://hackmd.io/y4DHXX8SSvKVG2bCBsgK2w
    * Overall relatively quiet, all things considered.
    * We were complimented on the communication around the breaking changes, Ralf's name came up a few times positively.

- POSSEE NumPy GenAI project updates: 
  - Project repo: https://github.com/possee-org/genai-numpy
  - Moving ahead with a regular code review of the AI-generated PRs. Paul and Ben pointed out that the code was generated from the NumPy code base (other examples and code), which addresses the copyright question, since one of the sources for the learning is the code base itself.


- NumPy optimization team meeting schedule: should we change the cadence? 
Conclusion: no, seems to be working well for the team. 
It's a small team, but they are making progress on their objectives.

- Newcomers meetings: 3-4 newcomers on average at each meeting. This works well for onboarding. 


## Action items

- 2.0.1 release:
  Chuck plans a release this weekend. All looks ready.

---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
