---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-11-04 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)


**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Nathan, Sidharth, Inessa, Sam, Tyler, Abhinay, Iason, Maanas, Joren, Pratham, Francesca, Matti

## Follow-up from previous meetings / discussions
 
- (mattip) Any thoughts about adding PyPy 3.12 wheels for the release? CI is passing and it is not too slow https://github.com/numpy/numpy/pull/32332 ?

- Branchinig 2.6 probably some time mid november.



## New topics

- merge maxlag PR? https://github.com/numpy/numpy/pull/31261
  We decided to close it, leaving the option open to implement the feature in a new, clean PR
- https://github.com/numpy/numpy/issues/21916 
  - Inessa will work on adding the section about `block`, maybe create a flow chart/infographic about usage of each of the functions. 
  - Sid will record a tutorial for the "how-to".
- Bytes coercion deprecation? https://github.com/numpy/numpy/pull/32757
    - Nathan will ping Sebastian and Marten, Matti will try to take a look.
- Plan to merge ByteStringDType.
    - Dealing with to-be-implemented casts and ufuncs?
    - Delay to 2.7? Or merge now and leave some things not implemented to fill in on `main`.
    - Consensus is that this is a good plan. We should explicitly document that ByteStringDType has some missing functionality that will be filled in, along with a followup summary issue for contributors.
- Iason: incosistent NaT handling in nan* functions (https://github.com/numpy/numpy/issues/33207 and https://github.com/numpy/numpy/pull/33212)

- Pratham https://github.com/numpy/numpy/pull/32552#issuecomment-6637073473 decision 

- Maanas: https://github.com/numpy/numpy/pull/33110 should probably get this in before 2.6

### Let's connect and keep the conversation going!


Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
