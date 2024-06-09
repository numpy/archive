# 2022-10-26 NumPy community meeting


- Time: 6:00 pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present** *(add your name and GitHub handle)*: Inessa Pawson, Tyler Reddy, Micheal Siebert, Ross Barnowski, Sebastian Berg, Mars Lee, Charles Harris, Melissa Mendonca

**Notes taken by:** Mars Lee, Sebastian Berg


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-10-12.md_

- [name=inessa] Presentation topics for NumPy Newcomers’ Hour 
To suggest a topic for future presentations, leave a comment in this tracking issue: https://github.com/numpy/archive/issues/58.
    - Nov 17th, 8pm UTC - Ross presenting on maintainig the NumPy Tutorials repo

- [name=Inessa & Melissa] [Documentation user stories](https://github.com/numpy/numpy/issues/22089)
*(Feel free to add yours!)*

- Updates from the NumFOCUS Project Summit
  - [x] Inessa has shared her notes via email 
  - Different groups exploring refguide check vs pytest-based approach
      - built-in tools, different speeds

- Ralf: plan to implement some [OSSF security scorecard](https://github.com/ossf/scorecard) improvements that are relevant for NumPy
  - PR 22367 added permissions to the github actions, but broke the circleCI artifact link and the labelbot, so permissions were reverted for the labelling job in PR 22371. I opened issues on the upstream action providers.
  - Examples: branch protections, dependencies check
  - Some are already implemented, irrelevant or chosen to implement differently from OSSF
  - Do we have an official security policy?
      - NumPy's README.md links to [Tidelift](https://tidelift.com/docs/security), make report on Tidelift
      - OSSF recommends standalone SECURITY.md file
      - [x] Add SECURITY.md to NumPy with same instructions as READ.md: "Report a security vulnerability: https://tidelift.com/docs/security"
      - numpy.org has a [security page](https://numpy.org/devdocs/reference/security.html)

  - *Update*
      - PR opened
      - NumPy has pilot project for OSSF: what does that entail?


- Setting up OpenCollective 
  - Finance team has to look into this.

- Craig Peters (GitHub): demo of Codespaces
  - *Follow-up*
Early access is granted to the following users:
bsipocz
charris
inessapawson
mattip
marsbarlee
melissawm
rossbar
rgommers
seberg
tylerjereddy

Share feedback, including feature requests, with Craig via NumPy Slack
      
- Discussion of Github Copilot (AI pair programmer) and open source licenses
  - Uncertainty of given code's source and license

  - NumPy.org website to mention that it is trademarked?
      - In Fair Use NEP? 
      - In README? The landing page for most people
      - In [terms of use page](https://numpy.org/terms/)?
      - [ ] [name=Sebastian] Ask NumFOCUS where to put it


## New Topics

- Melissa: New schedule for NumPy documentation team meetings
  - Move it to two hours later
  - To address this comment (https://mail.python.org/archives/list/numpy-discussion@python.org/message/DMLHUAS7P32CHE3DDVRFZWYYES6ZPQYH/), move to an alternating schedule. 
  - Initial proposal: 4PM UTC and 12PM UTC

- [name=seberg] Changing NumPy scalar repr's?
  - [NEP](https://github.com/numpy/numpy/pull/22261) and [implementation](https://github.com/numpy/numpy/pull/22449) are largely updated (hopefully settled besides doc followup and new tests)
    - Questions:
      - How to print NaN's, currently: `np.float64(nan)`, could use `np.float64(np.nan)` or `np.float64('nan')` to make it copy-pastable.  But, even Python just prints 'nan' and 'inf'!
      - Any other wishes/concerns, or should we merge the NEP and officially propose it?
          - complex numbers
      - How should implementation move forward?  Can we try for NumPy 1.24?  Aim for just after that?  Look into making it optional in 1.24?
        - Doing it after gives people time to fixup things and test
        - From a NEP 50 adoption perspective it probably doesn't matter, since there won't be a deprecation period, so next release is just as well.  (And NEP 50 switch would be earliest that release)
        - Seems like: Get it accepted soon, put it in right after release.
     - `np.void((1, 2, 3), dtype=...)`




---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
