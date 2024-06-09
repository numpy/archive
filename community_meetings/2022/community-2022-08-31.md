# 2022-08-31 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present** *(please add your name and GitHub handle)*: 
Mars Lee (@marsbarlee), Melissa Mendonca, Inessa Pawson, Charles Harris, Sebastian Berg, Brigitta Sipőcz

## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-08-17.md_

- [name=Meekail/Melissa/Inessa] Zones of Contribution project board to start forming cohesive groups of issues/tasks (also see the notes above).

- [name=Inessa] numpy.org has fully transitioned from Google Analytics to Plausible.

- [name=Mars] Grant idea: 'NumPy Comics' 
    -  May not move foward with a grant proposal to [NumFOCUS Small Development Grant](https://numfocus.org/programs/small-development-grants) due to a conflict of interest
    - Proposal artist (Mars) already has hours for NumPy through employer (Quansight)
    - Work to move foward
        -  Mars will follow up with her manager about the proposal details.
     - Discussion continued during the NumPy Docs Team meeting earlier this week. See [the meeting notes.](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)
     - Working with NumPy community members to connect with educators, students, other groups (Albus Code, Open Source Design, etc)
     - Adapatation:  NumPy fundamentals perfectly integrate with Algebra 2/Precalc and AP CS Principles curricular -> comics, 1 hour lesson plan in classroom
     - Other possible stages: GSOD intern with instructional desgin
     - Fililng gaps and interest: educators, younger and potential NumPy users.
         - Different groups from usual user flow to NumPy. Not university students, researchers, professionals from other software
     - Moving date forward, no longer following deadline of Sept 2 2022, more time to refine details
     - How to make this global, beyond US? 
         - Already plenty of US-focused material
         - Adapting to different curriclums and languages
         - Pilot program: Following up SciPy US connnections and current connections are connected to US high school district
         - In developing plan, making plan for non-US educators
             - Open call to educators? Melissa in Brazil, etc
             - In some countries, might be better as after-school than in main curriculum
     - Ensure digital version works on mobile
         - [SciPy comics](https://github.com/alt-text-task-force/.github/blob/main/profile/scipy-2022-comic.md): Scanning QR code on front page of comics leads to landing page to various digital versions: Alt Text version, flippable version and PNG version.
         - Landing page provide options instead of defaulting to flippable version (more load)
         - Different devices, internet access, preferences, across world

## New Topics

- NumPy was selected as a featured project for [Grace Hopper Celebration Open Source Day 2022](
https://ghc.anitab.org/programs-and-awards/open-source-day/) held on Friday, September 16th, 8:00 am - 3:00 pm Pacific Time. 
We are currentlylooking for mentors who would be helping NumPy newcomers during this event. If you are available, please sign up here:
https://docs.google.com/spreadsheets/d/1Y1t7-Yu2INR-Unl277TCJmlKOSNWok8fX2NbES5jcgk/edit?usp=sharing.
You may choose to help for 2 hours only or stay longer.
  ***Who can be a NumPy mentor at a mentored/newcomers sprint?***
If you are comfortable providing guidance on git, NumPy development workflow, building NumPy documentation, setting up and using development environment, and using Gitpod, you are a great candidate for being a NumPy mentor to newcomers.
    - In-person event but sprint is virtual only. Will have dedicated Slack channel
    - Example guiding document for mentors and mentees: [PyCon US’22 Mentored Sprints - NumPy & SciPy](https://hackmd.io/@melissawm/H14qfHRZY)
    - Overview: Begin with 10-15 minutes to introduce projects, overview of how to contribute with Git depending on set-up (Windows, Mac, Gitpod), have sprint-issues ready
    - Adjusting expectations: Newcomers to introduce themselves and each other, learn about project and team, may not finish issue but more of introduction
    - Outreach rather than complete PR necessarily

- [name=inessa] Presentation topics for NumPy Newcomers’ Hour 
To suggest a topic for future presentations, please leave a comment in this tracking issue: https://github.com/numpy/archive/issues/58.

- [name=Inessa, Melissa] How to celebrate first-time *reviewers*?
Will Tirone as a first-time reviewer: https://github.com/numpy/numpy/pull/22179 
    - Send message in the mailing list, similar to announcements about gaining commit rights.
    - Pamphile's request for recognition of the work done by reviewers: https://github.com/orgs/community/discussions/4525
    - Problem: How to identify first time reviewers. Github doesn't identify it. Would have to track manually.
    - Possible Approaches:
        - Ask reviewers to self-report of their first review in NumPy Slack or mailing list
            - But who would do that publicly? Self-selecting?
        - Put first-time reviewer's name in commit message? 
        - Put on list of contributors?
    - What's stoppping people to start reviewing? 
        - People don't know how to start reviewing?
        - Want to get involved but need encouragement?
        - Misunderstanding, think that only maintainers can review?
    - Make explicit an implicit practice
        - "Don't be scared to do a review"
        - Have a more seasoned reviewer with the first-time reviewer? Mentoring
    - One thing not enough to get reviewers, would need multiple approaches together
    - In some ways, reviewing is harder than a code contribution
        - Smaller pool than contribution. Everyone can start a contribution but only seasoned contribution with understanding of NumPy codebase can review
        - 'Sell' review as a exciting challenge, to shake things up, apply old skills in a new way?
            - e.g if you're good and bored with horse racing, try horse jumping
            - e.g if you're good and bored with coding, try management
    - Docs currently do not promote reviewing as much as we'd like
    - Multi-step review process: first time reviewer is helping the front of the review pipeline, will be passed down to seasonsed reviewer for corner cases
    - Tension between want more reviewers vs want substative first time-reviewers
        - but if not have merge rights, no major problems if pass through seasonsed reviewer (the only risk is to derail a PR/mislead the PR contributor that all is fine while the corner cases are not taken into account)
    - Related to bigger issue of sustainability: from first time contributor -> experienced contributor -> first time reviewer -> experienced reviewer -> maintainer
        - NumPy needs more paid maintainers to review PRs.

- [name=Inessa, Melissa] [Documentation user stories](https://github.com/numpy/numpy/issues/22089)
    - Feel free to add yours!



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
