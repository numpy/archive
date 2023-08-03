# 2023-08-02 NumPy community meeting

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


**Present:** Matti, Jan, Chuck, Sayed, Ralf, Mars, Ganesh, Tyler, Nathan, Chris, Alex Szatmary, Raghuveer, Brigitta, Sebastian, Ross


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-07-19.md_

-  Update on **Writing Script, Thumbnailing stage** for GSOD-NumPy 2023
    -  [Link to script draft](https://docs.google.com/document/d/1AzK9Q1vCPjcK6j9pMQTOm6K-zMiZf5FU/edit?usp=sharing&ouid=110556856523158639329&rtpof=true&sd=true)
    - **Next steps**
        - Match script to drawings. Start thumbnailing, paneling and pacing
        - Learn Krita (open souce graphics software) 
        - Writing blog post on first 2 months
        -  At this stage, will work closely with project mentors Mukulika and Ross
        -  Once script is cleaned up (pages, dialogue), will open for Review #2 with wider community
    -  **Recent changes**
        -  Rewrite bullet-points into full script format
        - Focus on grad students and Open Science
        -  Shift scope from 'big picture contribution pathways' to 'characters entering open source'

- Meson module and NumPy work is in the final stages.
  - We are going to ship a NumPy version of meson that does the SIMD discovery. Hopefully, it will be merged soon for 1.26.
  
- Highway NEP is in the works. Google Highway is about to dual license as MIT:  https://github.com/numpy/numpy/pull/24138
  - A number of concerns: dispatch/discovery, c/c++ transition, actual kernels.
  - We should resolve the discussions and additionally ask Jan and Sayed to add their opinions, and merge the NEP soon.

- Create Optimization Team (SIMD)
  - With its own focused meetings.
  - Start with using the #simd Slack channel.
  - Set up meetings schedule on the NumPy community calendars (Google and Scientific Python).

- [name=Melissa] Update on numpy.org translations
  They are live!

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



## New Topics

- Preparing for the first 1.26.0 beta or RC: next steps (logistics of preparing the branch, do we backport new deprecations in preparation for 2.0, any other changes on the radar?) 


- The Python Steering Council provistionally accepted the no-GIL PEP. What will NumPy need to do to eventually release (or not) no-GIL wheels and how should we handle messaging around this?

   * For now, wait-and-see.
   * Hopefully, people will show up to help with the necessary work.
   * The dual wheel issue is not as big of a problem as it might seem, no need to ship on all platforms and will only need to do it for a few Python versions.


- Cirrus CI changes: starting to pay for some compute credits? (see https://cirrus-ci.org/blog/2023/07/17/limiting-free-usage-of-cirrus-ci/ and https://github.com/numpy/numpy/issues/24280)
  - The approach is in general to pay $100-$200 for their service.

- Slimming down the CI infrastructure:
  - remove/rework Azure jobs into GHA
  - have DOC PRs run doc builds/doc related CI, not the full
  - have some labels that trigger extra CI



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
