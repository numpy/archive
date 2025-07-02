---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-07-02 NumPy community meeting

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

**Present:** Joren, Sebastian, Matti, Charles, Maanas, Mahfuza, Sayed, Riley, Nathan

## Follow-up from the last meeting / discussions


## New topics

- Is windows_arm64 github action running? Should it be?
  - We need to delete the yaml file and delete the [workflows](https://github.com/numpy/numpy/actions/workflows/windows_arm64.yml)

- floating point problems in OpenBLAS builds on mac:
  - Trying with `/clang:-ftrapping-math` may be an option, since either can definitely cause this type of issues.

- Doxygen follow up from [here](https://github.com/numpy/archive/blob/main/docs_team_meetings/2025/docs-2025-02-10.md#follow-up-from-last-meeting--discussions)
  - breathe (used in the conversion of doxygen output to RST) is being maintained, and the latest version has cleaned up problems with later versions of sphinx.
  - Is it a priority to move documentation into the code? Not clear. We could ask for a small development grant from NumFOCUS to help fund someone to do it, but we would need a core developer to help mentor the project.

- Documentation Team meeting: is it still happening? If not, we can fold documentation discussion topics into this meeting.
*Update from Mukulika via Slack:* The attendance numbers have been very low. Folding Docs Team meetings into Wed meetings makes sense.

- Next Wednesday’s triage meeting is canceled due to most regular attendees being out of office. Inessa will make the announcement.

- Short discussion about the [sort PR](https://github.com/numpy/numpy/pull/28516)


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
