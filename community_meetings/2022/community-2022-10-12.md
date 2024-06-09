# 2022-10-12 NumPy community meeting


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


**Present** *(add your name and GitHub handle)*: Matti Picus (mattip), Charles Harris, Brigitta Sipöcz, Sebastain Berg, Inessa Pawson, Ralf Gommers, Mars Le (@marsbarlee), Ross Barnowski, Tyler Reddy, Craig Peters (guest presenter from GitHub)

**Notes taken by:** Mars Lee, Inessa Pawson


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-09-28.md_

- [name=inessa] Presentation topics for NumPy Newcomers’ Hour 
To suggest a topic for future presentations, leave a comment in this tracking issue: https://github.com/numpy/archive/issues/58.

- [name=Inessa & Melissa] [Documentation user stories](https://github.com/numpy/numpy/issues/22089)
*(Feel free to add yours!)*

- [name=seberg] Changing NumPy scalar repr's?
  - WIP (put it on hold for a bit).  Need to distinguish printing a scalar (e.g. `"1.234"` for longdouble), the scalar instance `np.longdouble("1.234")`, and the "normal"  array repr/printing with limited precision.  (the first doesn't exist as a concept right now since we can effectively use the second for it.)


- September 22nd NumPy Newcomers Hour 
Hosted by Mars Lee 
Topic: Design jam session on the NumPy contributor journey map
https://youtu.be/QhrqPr0TNrs


- [name=seberg] NEP 50 (e.g. `np.uint8(-1)` deprecation):
  - *[PR Merged](https://github.com/numpy/numpy/pull/22385) (no followup for now, have to see how downstream feels, though)*


## New Topics

- NumPy newsletter - ideas for content: https://github.com/numpy/numpy-newsletter/issues/23
*(Feel free to add yours!)*
  
- Updates from the NumFOCUS Project Summit
  - [ ] Inessa will share in the coming days


- NumPy 1.23.4 release :tada:

- Inessa: NumPy has been accepted to the Slack for Nonprofits program.
Under the current Pro Plan, we can accommodate 250 members for free,  and above that, a 85% discount will be applied.
For more info about the program, visit: https://slack.com/help/articles/204368833-Apply-for-the-Slack-for-Nonprofits-discount.
  - The situation is slightly better than it seems, but it is still easy to run out of the quota (it is "active" members, not all members)
  - Setting purpose and culture of NumPy Slack, e.g., different from user forums such as StackOverflow.

- Inessa: DOC: Remove info specific to Python 2 from the latest docs version: https://github.com/numpy/numpy/issues/22400
Would in any of the instances above we prefer to keep references to Python 2? What are your thoughts on editing references to Python 2 in the NumPy documentation and code base in general?
  - Yes, we can remove everything related to Python 2.


- Ralf: plan to implement some [OSSF security scorecard](https://github.com/ossf/scorecard) improvements that are relevant for NumPy
  - PR 22367 added permissions to the github actions, but broke the circleCI artifact link and the labelbot, so permissions were reverted for the labelling job in PR 22371. I opened issues on the upstream action providers.
  - Examples: branch protections, dependencies check
  - Some are already implemented, irrelevant or chosen to implement differently from OSSF
  - Do we have an official security policy?
      - NumPy's README.md links to [Tidelift](https://tidelift.com/docs/security), make report on Tidelift
      - OSSF recommends standalone SECURITY.md file
      - [ ] Add SECURITY.md to NumPy with same instructions as READ.md: "Report a security vulnerability: https://tidelift.com/docs/security"
      - numpy.org has a [security page](https://numpy.org/devdocs/reference/security.html)
  - Can try OSSF if not add too much to maintainer workload


- Setting up OpenCollective 
  - "Finance team" has to look into this.


- Craig Peters (GitHub): demo of Codespaces
    - Context with NumPy: part of onboarding is building a dev environment. However, can be difficult (especially on Windows).
    - Gitpod has helped and GitHub is making a similarly helpful tool that NumPy could benefit from
    - Codespaces to be tightly integrated with Github, included in Free user tier
    - Use cases
        - Maintainers: Maintain multiple different environments, review, depencies
        - New contributor: see why tests don't run, reproduce
        - Build test locally, make Actions run locally on Windows or Mac
    - Demo
        - Start Codespace from Github browser inferface
        - Select cores
        - devcontainer.json and Docker file
        - Choose complier and Python version
        - default IDE: VSCode. Working to include others such as PyCharm, VIM in future beta
        - On Github-flavored Markdown, README.md could include a button with setup Codespaces to specific devcontainer
    - Discussion
        - Would be nice to know what processor cores are being used: i7, i5...?
        - NumPy would have a large Docker image (over 1 GB), what sort of start-up time is expected?
            - 15-20 seconds since baked-in
            - would be upgrade from current 2 minute start-up time
        - What if multiple devcontainers?
            - If repository has devcontainers folder with different user profiles, in Codespaces set-up there is a drop down menu to select the devcontainer
        - Can you make PRs from Codespaces?
        - Feature request: If have permission on own fork and upstream, be forbidden to push upstream repo?
            - Maybe define in json
        - Feature request: Windows!
            - Currently Codespaces is only Linux
            - We need to test on many different hardware
            - Possiblity for now: Microsfot DevBoxes
        - Can you rebase inside this environment? Such as on someone else PR?
            - Yes
        - Open for feedback on Codespaces documentation: https://docs.github.com/en/codespaces
    - Follow-up
        - [x] For early access, Inessa will send to Craig a list of GitHub handles of everyone present at today's meeting.

---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
