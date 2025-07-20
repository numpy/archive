---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-07-16 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Chuck, Joren, Sebastian, Ben, Ketan Prajapati


## Follow-up from the last meeting / discussions

- Doxygen follow up from [here](https://github.com/numpy/archive/blob/main/docs_team_meetings/2025/docs-2025-02-10.md#follow-up-from-last-meeting--discussions)
  - breathe (used in the conversion of doxygen output to RST) is being maintained, and the latest version has cleaned up problems with later versions of sphinx.
  - Is it a priority to move documentation into the code? Not clear. We could ask for a small development grant from NumFOCUS to help fund someone to do it, but we would need a core developer to help mentor the project.

- Short discussion about the [sort PR](https://github.com/numpy/numpy/pull/28516)


## New topics

- Discussion about the possible doxygen project:
  - Create a slack chat for now with those who may mentor or would be interested in.


- Serialization discussion:
  - Manaas was thinking about how to store more complex dtypes (just as StringDType)
  - Would be good to have Nathan around who had some thoughts on this.

- Discussion about ufunc loop fusion (mainly out of curiosity).

- Awkward array has a use-case that seems to match our `reduceat`

- Discussion about critical section adoption:
  - Nathan is working on fixing the PySequence_FAST issues and will add some helper for it to avoid the fact that the critical section includes `{}` (to make this hard, but also... we kinda want to do this here)




### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
