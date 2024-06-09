# 2022-08-03 NumPy community meeting


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


**Present** *(please add your name and GitHub handle, it’s completely optional)*: Melissa, Inessa (@inessapawson), Matti (@mattip), Chuck, Ross, Eric Roberts, Mars Lee(@marsbarlee)


## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-07-20.md_

- [SciPy 2022 Conference](https://www.scipy2022.scipy.org/)
    - Sebastian presented at the Maintainer's Track (recording may be partial/low quality).
Let's do another recording for the NumPy Newcomers Hour: tentatively scheduled for September 8, 2022.

- [name=Meekail] Semantics of copy keyword for array methods (see [this PR](https://github.com/numpy/numpy/pull/21913)).
    - Goal: bring the ndarray API close to the Array API spec. Unfortunately the copy kwarg in reshape and maybe elsewhere has slightly different semantics. What would be a path to moving the two kwarg versions into compliance?
    - We rejected using T/F/None and chose enums very concientiously.
    - We don't have a copy=never, ours is more copy=only-if-necessary
    - Array API [repository](https://github.com/data-apis/array-api)
    - Sebastian will bring this up at their meeting, as well as open an issue.

- [name=Meekail/Inessa] Recorded documentation writing to fill out and discuss developer [zones of contributions](https://hackmd.io/zm65_TjfSpi9DSSkE2o7Iw)
*Action item:* to document the proposed as a tracking issue to expand the discussion beyond the community call.
    - Update: Will begin with project tracker to help figure out what *useful* categories/zones there may be. (Mentioned in **New Topics**).
    - How many issues do we have for each category: ufuncs, dtypes, multi-array module, array methods, SIMD
    - Evaluate what categories should be merged or expanded
    - So far, this project doesn't move anything else. So if we decide to not move forward with this Zones project, nothing is lost
    - [ ] [name=Melissa, Inessa] Set up the [Github project](https://github.com/orgs/numpy/projects/4/views/1)
        - [ ] Give Meekail admin rights


- [name=Inessa] Slack is making some big changes to its free plan: https://slack.com/intl/en-gb/blog/news/pricing-and-plan-updates. 
    - Inessa reached out to NumFOCUS. They will help us to switch to the Pro plan. 
    - Caveat: under the Slack's nonprofit program, the Pro plan is free for up to 250 members. Anything above that is billed at an 85% discount. NumFOCUS wouldn’t be paying for it.
        - Around $1/member per month
    - Currently, we have 217 members registered in the Slack workspace.
    - We should plan for the time when we hit 250 members.
    - Not the best use of money... Possible next actions
        - Negotiate with Slack for non-profit, up to 500 people, safe for a few more years
        - Move to an open source platform (Discourse)
        - [name=Ross] Maybe continue to negotiate with NUMFocus instead of each project deciding for themselves
        - [ ] [name=Melissa] To list possible platforms are solution or complement and send to mailing list
    - Factors in deciding next action
        - Be on same platform to other projects
        - Not too much busywork if we switch
        - Self-hosting and cost, such as Discord Nitro
            - OpenCollective for NumPy to open soon, so we could have another source of funds besides NumFOCUS
            - Ralf, Arliss finalizing NumPy's OpenCollective
        - Let's consider moving to an OSS product.
It's not a requirement though. E.g., Zoom is our platform of choice for meetings, it is commerical.
        - Archival and Search
            - Discord's indexable chats
            - How often do people search the NumPy Slack? 2 people in the call said 'no', 1 person said 'yes'
    - Why NumPy chose Slack in the first place
        - Familarity with Slack in job
    - **Options**
        - [Discord](https://discord.com/) (more IRC chat like Slack)
        - [Zulip](https://zulip.com/) (open source Discord competitor)
            - Used by Napari
            - [name=Melissa] Likes the UI
            - Most people don't have Zulip accounts, slightly higher barrier to entry
        - [Discourse](https://www.discourse.org/) (forum)
    - **A possible SPEC topic or to NUMFocus: what tools do open source projects use and why?**
        - [name=Ross] Let's have a centralized place where tools are tracked and collective advocacacy
        - [ ] [name=Ross] Bring up with SPEC
        - [ ] [name=Melissa] Bring up in NumFocus summit
        - For example, Project X uses Platform A, Project Y uses Platform B
        - Advantages, Drawbacks, checklist to help projects decide
        - Similar re-occuring problem with chat platforms, CI, video conference options

## New Topics
* [name=Meekail/Melissa] Zones of Contribution project board to start forming cohesive groups of issues/tasks (also see the notes above).
* [name=Inessa] Suggestion from Serge Guelton to use xsimd (https://github.com/xtensor-stack/xsimd)
https://mail.python.org/archives/list/numpy-discussion@python.org/message/CZUXQU7BJVXJP5OFXEWBREOCW7MVQ4TA/
Not a good solution for NumPy.
* [name=Inessa] New Zoom links for NumPy community events
All NumPy community events have been moved to the NumFOCUS Zoom license.
    * Inessa, Melissa, Matti, and Sebastian have host rights to all of them. More hosts will/can be added.
    * Historically, relied on Berkeley Institute for Data Science (BIDS) license, but all the comunity meeting facilitators are not working at BIDS any longer.
    * Watch out for outdated BIDS links.

* [name=Inessa] Define one place for NumPy community discussions.
    * Previously brought up in Aug 1 2022 NumPy Docs Meeting
    * Decisions usually made in the NumPy Community Meeting
    * Sometimes discussions don't show up in the mailing list- want to open and more transparently show decision-making process
    * [name=Chuck] Mailing list is not to make a decision. It's to get comments, and maintainers to make decision in an GitHub issue/PR.
    * [name=Matti] Implicit hierarchy of discussion and decisions
        * NEP
        * Issues, PRs
        * Community and Doc Calls
        * Mailing List
    * [ ] [name=Matti] Adapt an existing document
        * [scikit-learn has an example: Decision Making Process](https://scikit-learn.org/stable/governance.html#decision-making-process). 
    * Where is the final decision made?
        * Not formalized due to small group in calls, about 6 people consistently
        * Most formal, consistent place where feedback is received is PRs, such as [Matti for a contributor's PR](https://github.com/numpy/numpy/pull/22075#issuecomment-1203129506)
            * But a PR requires a relatively finished contribution, not good for early idea discussion
    * General trends in NumPy community
        * Mailing list: people rarely openly disagree
        * Send people to the mailing list ([formally listed in documentation](https://numpy.org/doc/stable/dev/development_workflow.html#get-the-mailing-list-s-opinion))
            *  if they get positive signal: right path
            *  silence: your idea could be improved
    *  **Let's make explicit these cultural expectations in NumPy?**
        *  [name=Meekail] Comparion to another project: scikit-learn has 'lazy consensus', therefore silence is positive signal
        *  Could be confusing for newcomers
        *  Depends on the discussion
            *  such as for API discussion, higher standards, want feedback
        *  [name=Ross] Hesitant to write this expectation in documentation
    * **How do we decide to make these implicit practices more explicit?**
        * Should people figure out on their own?
        * The implicit can change... maybe not worth documenting/setting in stone
    * [name=Inessa] Let's make explicit "If you don't get response on the mailing list, attend a community call."
        * Maybe a newcomer's first idea isn't great, but can be improved by meeting us in a call or they could contribute to another part of the NumPy project.

---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
