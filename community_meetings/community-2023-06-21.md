
- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Charles, Sayed, Tyler, Raghuveer, Mars, Sebastian, Ross, Brigitta, Inessa



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-06-07.md_




## New Topics

- Inessa: YouTube videos update: Jules Kouatchou (@JulesKouatchou) has provided timestamps for 4 videos.:tada:

- First big removals in the C-API, two new tags `python_removal`, `c_api_removals`

- A huge amount of work on https://github.com/numpy/numpy/pull/21057
  - doxygen used for documentation (should land in the build artifacts)
  - Will be split up into multiple PRs (e.g. split out testing)
  - Supports sizeless SIMD
  - [before](https://github.com/numpy/numpy/blob/main/numpy/core/src/umath/loops_comparison.dispatch.c.src) and [after](https://github.com/numpy/numpy/blob/1bd85d3bdc62141aaa98d338beda01f7f6602ff3/numpy/core/src/umath/loops_comparison.dispatch.cpp)

- Meson work

- **Review #1 stage** for GSOD-NumPy 2023
    - Will share on this community call and make Github issue to open to wider community who may not be in call
    - Also shared in NumPy Docs meeting earlier this wek
    - Drew some Concept Art
        - 1. How do you use NumPy? 
![](https://hackmd.io/_uploads/BJ2_l2xuh.png)
        - 2. How did you start using NumPy? ![](https://hackmd.io/_uploads/ByOca3TDh.jpg)
        - 3. How do we start a sprint? ![](https://hackmd.io/_uploads/ByHip36Dh.jpg)
        - [Link to full Concept Art prompts](https://github.com/MarsBarLee/gsod-numpy-2023/blob/main/outlining/concept-art.md)
    - Discussion points
        - Writing out specific parts I would like feedback on 
            - **Is there an issue that was actually completed during a sprint, that can be used in the comics?**
                - Currently taken from random issue tagged as 'sprintable' https://github.com/numpy/numpy/issues/22435
            - **Metaphor**: Making digital pages into physical media (Github issues as paper scrolls)
            - **Characters**: over-confident, under-confident and just right
                - Over-confident: "I bet I already know how to do this!"
                - Under-confident: "Can I start working on this issue?""
                - Just right: "Let's review the documentation if this already exists and if I'm still not sure, I'll ask someone."
    - Next steps
        - Putting together review: Github issue
            - 3 main drawings, as shown above
            - [Chapters](https://github.com/MarsBarLee/gsod-numpy-2023/blob/main/outlining/chapters.md)
                - Introduction
                    - To characters and how in-person sprints work
                - The sprint itself
                    - Collaboration and the importance of different approaches
                - After the sprint
                    - Meeting remotely, connecting to mailing  list and Slack
                - Goals and future
                    - Contributor's goals, how open source processes are open to change too
        - Annoucing that open for review: mailing list and Slack channel
            - 2 weeks period for getting reviews?
            - But I think most comments will come from community meetings
            - For Review stage #2, want to coordinate so people know they can join community calls to give reviews
    - Comments from this call:
        - Different levels of problem, of 'sprintable'
        - Emphasize following-up after the sprint
        - It's normal it won't be done in one sprint
        - De-emphasize the onramp of sprinting becasue fly-bys
        - Focus on user-contributor, most likely to follow through, sustainable commmunity growth
        - There's a specific example Ross has about loading data, NPZ archive, why won't it work like a dictionary?
        - Ross opened issue
        - Ganesh wrote implementation, Sebastian and Ross review
        - NumPy is driven by people who use it
        - Maybe start with a character in classroom (meteorology thesis character)
        - NPZ as 20 year old, not brought up until by users
        - Instead of sprint leader, maybe Professor character guiding students
        - Maybe interview, get links to PRs and issues, get narrative flow
        - Sprints as not primary onboarding mechanism, people who make larger contributions come through other channels, driven by scientific research
        - Mars will follow-up with Ross
        - Similar examples: AstroPy
        - We serve everybody who lives on top of NumPy
        - Can check against user surveys how people use NumPy
        - Maybe add sprint to end, not be center of conversation
        - Can talk to a new contributor to NumPy, a maintainer of SciPy but newcomer to NumPy (talk to Melissa)
    - Previous steps in GSOD-NumPy 2023:
        - Completed Outlining stage for GSOD-NumPy 2023 (May 15-26)
        - Completed Gathering community input stage and 3 brainstorming sesions
            - At Newcomer(May 4) NumPy Docs (May 8), Commmunity (May 10)
            - [Link to Google Jamboard](https://jamboard.google.com/d/1j_rEIslOh59N9cLGU1VGc7rTc88SuLTi7l4YqTqAULc/edit?usp=sharing)
            - [Summary from Brainstorming Sessions](https://github.com/MarsBarLee/gsod-numpy-2023/blob/main/outlining/summary-from-brainstorming-sessions.md)



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
