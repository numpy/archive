# 2022-08-17 NumPy community meeting


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


**Present** *(please add your name and GitHub handle, it’s completely optional)*: Inessa (@inessapawson), Chuck, Matti (@mattip), Brigitta, Ross, Mars, Rohit (@HaoZeke)


## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-08-03.md_

* [name=Meekail/Melissa/Inessa] Zones of Contribution project board to start forming cohesive groups of issues/tasks (also see the notes above).




## New Topics

- [name=Inessa] numpy.org has fully transitioned from Google Analytics to Plausible.
- [name=Inessa] NumPy is now on LinkedIn: https://www.linkedin.com/company/numpy/. Please follow us!
The communications policy: announcements only.
- [name=Chuck] NumPy 1.23.2 is released

- [name=Mars] Grant idea: NumPy Documentation Comics for Fun, Visual Learners and Newcomers
    - [Document of discussion of idea with Rohit](https://thin-feverfew-bfe.notion.site/Grant-idea-NumPy-Documentation-Comics-for-Fun-Visual-NewComers-e60d6dc7ae2f41d4819fb8ad8dd6cb23)
        - In this case, inspired by Ryan Cooper’s talk at [NumPy Newcomer’s Hour: NumPy in the classroom](https://cooperrc.github.io/), specifically at University of Connecticut, Mechanical Engineering Department
    - Source
        - NumPy Docs?
        - [Professor Cooper's course: Applied Mechanics II with NumPy](https://cooperrc.github.io/engineering-dynamics/intro.html)?
    - Target Audience: People who have not used NumPy before, who wouldn't look up 'NumPy Documentation' on a search engine
    - Publication, Reach
        - Digital, Print
    - Previous Work as Samples
        - [How to Write Alt Text for Scientific Diagrams and Documentation](https://heyzine.com/flip-book/f3c7f85cdc.html)
            - Debuted at SciPy 2022
            - Tabled for Quansight, gave out 200 print copies
            - Gave Lightning Talk 
            - Led a sprint: 4 people, 3 in-person and 1 remote contributor
             - Interactive, not just read
             - Slides showing this [multi-media experience](https://docs.google.com/presentation/d/1pYU-vvT5HG5x4Zmy5HWZHUdPtiEyPumUSB9lZszraH8/edit?usp=sharing)
![](https://i.imgur.com/S28qWmK.png)
        - CodeSprite Explains
            - Debuted at PyData NYC 2019
            - Digital, has [Twitter](https://twitter.com/codespritee) and Medium precense
    - ![](https://i.imgur.com/XIj4Laj.png)
    - Possible grants
        - [NUMFocus: Small Development Grants](https://numfocus.org/programs/small-development-grants)
            - Round 3 (maybe too soon, due on Sept 2) or next year 
        - CZI
            - Interest from [Dario's tweet, CZI](https://twitter.com/ReaderMeter/status/1547250705521643522?s=20&t=BRltiD0m-KCHvRBXMzUbSw)
        - GSoD as well
            - It is more technical than our last proposal, so it should have more of leg to stand on
    - Interested parties
        -  Educators
            -  Met at SciPy 2022 conference, US high school teachers, college professors, who want to photocopy their SciPy comic and give to their students
        -  Open Source Design
            -  Talked about in August's OSD Call. [Link to my OSD agenda for the call](https://discourse.opensourcedesign.net/t/monthly-open-source-design-call/253/148)
            -  OSD community interested in how Mars knowledge in comic making can be open source as well
        -  Rohit
    -  Questions and Concerns
        -  Clarifying the design process
            - [Script and early sketch process](https://docs.google.com/document/d/15tv6rHUG7z_kM68rwl2m-Gkce8cP_AEt1aJhzdi7Vnw/edit#bookmark=id.s77y5mc5h2hj), shows people the process, comment with feedback
        - Level of detail
            - Images take more time than plain text
    - Moving forward with Small Development Grant
        - Grants proposal need to be specific: which part of the documentation?
        - For example, [strides](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.strides.html)?
        - Absolute Beginners?
        - 700 words of details, 400 words of impact, 1000 words overall
        - Decide target audience
            - People who already know Python and exploring data?
                - Know lists, array, attribute
                - Don't know how to make things fast
            - ML, what are these matrices people are talking about? Have math background but no programming background
        - Educators: High school? if college, get Python somewhere else
            - Take advantage of print comics, educators who want to photocopy their SciPy comic and give to their students
            - Teachers are a connection to a group who may not have reached
            - If US highschoolers (14-18), may not know matrixes
            - If it's a sophmore taking pre-calc, perfect time for NumPy to be introduced
            - Inessa, AlbusCode, high schoolers, can have focus group
            - Concern: are comics relevant in younger generation? Yes
        - Maybe similar focus to [James Munroe on SciPy Lectures discussion](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg?view):  After newcomers complete the first tutorial,they think ‘why continue with this tool?’. How does this replace my current tool?
        - [name=Mars] Working adults have SciPy Lectures, college students have Ryan Cooper, high schoolers have these comics. Introduce NumPy to younger group
        - Grant intent: not just a comic, but comic to be used by specific people, why useful for this specific group. 
        - 700 words on the overview and 400 words on impact, and budget, timeline, contributor in mind, and a catchy title
        - Specific group: a specific high school district, make focus groups, attach to high school curriculum and semester schedule
        - Present output at exhibit? Multiple possible tie-ins
        - [ ] Mars to follow-up with Inessa

            
- [name=Inessa] Updating [SciPy Lectures](https://github.com/scipy-lectures/scipy-lecture-notes)          
    - Follow-up with discussion with James Munroe and Jan 2022 discussion of updating SciPy Lectures
    - Stages of SciPy Lectures updates
        - 1. Infastructure
        - 2. Content
    - Checking in with reviewer's bandwidth
        - James, Ross, 
        - Brigatta offers help with the infrasturcture
    - Adding sphinx-gallery? Or switching to the executable books/MyST-nb tool stack.
        - Ross and Brigitta has experience in implementing

---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
