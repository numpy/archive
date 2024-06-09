# 2023-07-19 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Matti, Sayed, Chuck, Raghuveer, Melissa, Mars, Tyler, Sebastian


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-07-05.md_

-  Update on **Writing Script, Thumbnailing stage** for GSOD-NumPy 2023
    -  [Link to script draft](https://docs.google.com/document/d/1AzK9Q1vCPjcK6j9pMQTOm6K-zMiZf5FU/edit?usp=sharing&ouid=110556856523158639329&rtpof=true&sd=true)
    - **Next steps**
        -  At this stage, will work closely with project mentors Mukulika and Ross
        -  Once script is cleaned up (pages, dialogue), will open for Review #2 with wider community
    -  **Major changes to script:**
        - Focus on grad students and Open Science
        -  Removal of Professor character
            -  provide distance from purely academic setting
            -  remove clear authority figure that provides solution and approval
            -  shift to students to muck around and find out themselves what to do next
        -  Add different POVs, from the PR Maker and Maintainer Characters
            -  show different people do different things
            -  show different priorities eg maintainer thinks about release cycle, students in story don't know anything about release cycles
        -  Shift scope from 'big picture contribution pathways' to 'characters entering open source'
            -  Started project with keen interest in mapping culture of open source, questions that community members engage in such as ‘How do we turn first time contributors to second time contributors?’ and ‘How do we encourage tagging issues or documentation as equal ways to contribute?’
            -  However, these questions may not be engaging to people not already in the community
            -  Expands potential audience, everyone can relate to a human struggle vs debates on niche topic


## New Topics

- Meson module and NumPy work is in the final stages.

- Highway NEP is in the works. Google Highway is about to dual license as MIT:  https://github.com/numpy/numpy/pull/24138

- Create Optimization Team
  - With its own focused meetings.
  - Start with using the #simd Slack channel.
  - Set up meetings schedule on the NumPy community calendars (Google and Scientific Python).

- [name=Melissa] Update on numpy.org translations

- Update documentation to mention how to use meson for developers:
  ```
  pip install -e .
  ```
  or, if running on python3.11+
  ```
  pip install -r build_requirements.txt
  spin build --clean
  spin python   # or spin ipython
  ```
  just testing:
  ```
  spin test
  ```
  
- For building the release version of the docs, currrently we use `cd doc; make merge-doc`. What replaces that?



## Action Items



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
