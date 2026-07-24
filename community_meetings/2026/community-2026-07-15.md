---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-07-15 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/).
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sam, Joren, Matti, Sebastian, Ryan Vaughn, Hafiz Azhari, Chuck, Maanas, Pratham


## Follow-up from previous meetings / discussions

* Iason: Draft PR for registering reduction loops on the array method for multi-output reductions is open for comments on the design: https://github.com/numpy/numpy/pull/31816. Happy to make it a short NEP once the design is consolidated.
  * Not draft anymore


## New topics

* mattip: Pratham (welcome!) has started working. He chose to start with global state. Does anyone mind if I merge the
  * Going to test going towards support of subinterpreters.
  * Goal is that things work without slowing down normal usage.

* Hafiz is a new contributor, welcome!

* Adding the `ty` type-checker (Astral / OpenAI): https://github.com/numpy/numpy/pull/31956


* Bunch of deployment errors for the docs a while ago: but seems to be OK now/again.

* PR label bot is not working anymore.

* discussion about changing templates and considering auto closing, etc.


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
