---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-12-03 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sayed, Sam, Amelia, Tyler, Kader, Maanas, Sebastian, Chuck


## Follow-up from previous meetings / discussions


## New topics

- Qemu update to Python 3.12 ppc64le (and one other) are failing in weird ways:
  - ppc64le segfaults, probably when looking at the C-stack/backtrace for temporary elision.
  - Another fails during setup.
  - Sayed: Should drop the ppc64le qemu build, could be a bug in qemu and we have a job on native hardware.

- Scientific-python-nightly wheels contain rather old ones (because they retain 5 releases and that goes back to May as we re-upload under the same name).
  - Might ping someone to clean it up. Ralf, Stefan or Brigitta or so can probably do.




### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
