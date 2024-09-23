---
title: NumPy community meeting
tags: [NumPy]

---

# 2024-09-11 NumPy community meeting

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

**Present:** Inessa Pawson, Tyler Reddy, Nathan Goldbaum, Mars Lee, Chuck Harris

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings 


## New topics

- Uploads to anaconda.org
  - Tokens expired and wheels were not uploaded. Why do we have a 1 year expiration date on the tokens? Do we want to change that? Do we need more maintainers with privileges?
  - This got fixed by Sebastian
  - We need better visibility about when this starts failing more than adding more maintainers with access.
  - Possible solutions: a calendar event reminder or a hook in the script to send an email if the upload fails.

- Should we stop using the staging file repo and only upload to the scientific-python one?
  Advantages:
  - single point for uploading/downloading
  - the scientific-python area is managed, older wheels are removed
  - anyway a download script picks the wheels to download and later upload via twine, so the multiplicity of files should not be too confusing
  - single source for early adopters to get the wheels

  Disadvantages
    - the wheels will disappear after a month

  Chuck: the staging is only used for releases and isn't related to nightlies.

- 2024 NumFOCUS Project Summit
  - Mars, Mukulika, and Inessa were in attendance
  - Inessa was a co-Chair
  - Mars gave a lightning talk about her work on the NumPy comics
  - Mars and Ross [sprinted on the continuation of the NumPy comics for the GSOD 2025 proposal](https://github.com/numfocus/project-summit-2024-sprints/issues/5#issuecomment-2336768626). This will cover how to work with the NumPy codebase and making a first code contribution.
  - Highlights: 
    - Elections to the Board and Technical Committee
    - OpenCollective will be sunset
        - too much manual data entry work
    - Infrastructure Committee is asking for feedback on the statement wrt to the recent changes in the Anaconda licensing policy: https://github.com/orgs/numfocus/discussions/8 
    - new support system - HappyFox
    - new NumFOCUS Code of Conduct policy. If you are interested to serve on the Working Group, please reach out to Inessa via Slack DM.

- Community Review for GSoD-NumPy comics
    - Can leave review in [GitHub issue](https://github.com/numpy/numpy/issues/27375) or this meeting
    - Next steps: upload full PDF, announce on the mailing list and Slack


---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
