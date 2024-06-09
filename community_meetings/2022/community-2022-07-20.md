# 2022-07-20 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present** *(please add your name and GitHub handle, it’s completely optional)*: Matteo Santamaria, Matti Picus, Meekail Zain (@micky774), Mars Lee (@marsbarlee), Sebastian Berg, Charles Harris, Melissa, Brigitta Sipocz, Ross Barnowski, Inessa Pawson (@inessapawson), Tyler Reddy


## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-07-06.md_

- LinkedIn account for NumPy: 
https://www.linkedin.com/company/numpy

- NumPy 1.23.1 happened soon (may happen this weekend)
  - Generally not too many problems with the release.

- NumFOCUS Summit
    - Sept 21-23, Santa Rosa, CA
    - 2 people per project will be funded by NumFOCUS.
    Who is representing NumPy?
    - Inessa will be there for the CZI EOSS Annual Meeting and NumFOCUS.
    - Melissa will be there for the both events as well. 
    - Others going: Stefan (board member), Brigitta (Scientific Python Project).
    - We can acoommodate more community members. Please send a request TODAY to Melissa or the NumFOCUS Slack.


## New Topics

- [SciPy 2022 Conference](https://www.scipy2022.scipy.org/)
    - Sebastian presented at the Maintainer's Track (recording may be partial/low quality).
Let's do another recording for the NumPy Newcomers Hour.

- [name=Meekail] Semantics of copy keyword for array methods (see [this PR](https://github.com/numpy/numpy/pull/21913)).
    - Goal: bring the ndarray API close to the Array API spec. Unfortunately the copy kwarg in reshape and maybe elsewhere has slightly different semantics. What would be a path to moving the two kwarg versions into compliance?
    - We rejected using T/F/None and chose enums very concientiously.
    - We don't have a copy=never, ours is more copy=only-if-necessary
    - Array API [repository](https://github.com/data-apis/array-api)
    - Sebastian will bring this up at their meeting, as well as open an issue.

- [name=Meekail/Inessa] Recorded documentation writing to fill out and discuss developer [zones of contributions](https://hackmd.io/zm65_TjfSpi9DSSkE2o7Iw)
    - [name=Meekail ]Help people build experience in one 'zone' so they can develop mastery without needing to learn the entire library.
    - **How to implement this idea?**
    - **How do you define a zone?**
    - Start large areas. If beneficial and good feedback, then zoom ito specifics.
    - For example, start with the pure Python machinery, internal testing and utilitity functions
    - For example, capture discussion on video, show the interation discussion
        - Meekail and Matti discussion
    - **What would things look like in the end?**
        - Melissa, Mars could make diagram of conceptual pieces of NumPy
        - Like a tour guide- link to annotated PRs, or workthrough examples or videos of discussion
    - [name=Charles] Need a list of what these exact pieces are
        - [name=Meekail] Need some help in identifying 
    - This is a big piece of work needing someone to be doing sustained work on it
    - [name=Brigitta] Like the idea. Compared to astropy, NumPy is much bigger and could benefit from division
        - [AstroPy has a annotated example of contributing a bugfix to AstroPy](https://docs.astropy.org/en/latest/development/workflow/git_edit_workflow_examples.html#astropy-fix-example), similar to what Meekail suggested
    - [name=Meekail] Sebastian's deprecation example at NumPy Newcomer's was super helpful. Having someone asking the 'newcomers questions'
    - [name=Ross] Idea has come up before ('How to find yourself in the NumPy codebase'), a good idea
        - Hesitance to frame as contributions, can be overwhelming
    - [name=Charles] Need to have a problem to solve to keep people interested, contributor angle
        - "I want to learn NumPy" vs "I want to fix X"
        - Could look at data, last 100 PRs, how they started, issue based, someone playing around, a student, to see who the zones is for
    - [name=Melissa] Let's zoom out our discussion a bit, not just contributor focus. 
        - **Contributor -> Maintainer conversion**, a topic brought up in the NumPy Docs meeting
        - Information is all there but direction is not clear
    - [name=Charles] This is indicative of a deeper maintainability problem
        - C-code is undocumented and somewhat opaque
        - Code is scattered
        - Tests aren't systemic and could be improved
    - [name=Melissa] Mentorship for Contributor -> Maintainer
        - For next grant we write, add time for shadowing and mentoring
        - **Chicken and egg problem- not enough maintainers to make more maintainers**
    - [name=Inessa] We need to create a pathway to becoming a maintainer.
    - [name=Ross] Comparison to NetworkX, easy to contribute to, smaller, not have stability worries like NumPy
        - Similar distibution to NumPy's, heavily weighted towards 1st timers, so this is a problem for all projects
    - [name=Charles] **We're in a transition, from volunteers to paid work, which are different environments**
        - Paid looks like the long term
    - [name=Inessa] Even experienced engineers struggle due to the lack of documentation about some parts of the NumPy codebase (e.g., C, C-API)
        - Inessa's direction: Have current maintainers share their current knowledge so we can make the documentation, onboarding material
    - [name=Matti] **Are we going to get a 'return on investment'?**
        - Alterating between wanting to do these 'zones' video with Meekail and not doing it
        - Most popular videos have around only 100 views, most people don't know the NumPy channel
    - **Is there value in structuring the documentation when people generally search for what they want?**
        - Information is all there but direction is not clear
    - [name=Meekail] Throughly documented code with sturcutre would achieve the 'zone' idea
    - [name=Sebastian] Would it be better to just organzie the code (higher priority) than explain how we're organzing it?
    - [name=Melissa] **"If all of us disappeared tomorrow, could someone pick up and learn what's happening in NumPy?"**
    - Sebastian: "Matti and I had to start from nothing. This is doable."
    - **Are there plans to hire developers long-term?**
        - Possible organizations: Berkley, grants (but not long term funding)
        - [name=Charles] Grant limitations: 6 months to just come up to speed, not good use for grant money.
        - [name=Inessa] Let’s use our funding more efficiently and shorten the onboarding time of new NumPy maintainers by having better documentation for them.
    - [name=Brigitta] Absence of this documentation is a technical debt.
    - Hire scientists to be engineers (current model, more difficult) vs Hire engineers to make software for scientists 
    - [name=Inessa] **To Sebastian, Charles (long time maintainers with the most knowledge) Let us know the best way to document your knowledge.**
      
    - Possibility of using [Doxygen](https://doxygen.nl/) to standardize how documentation is made
        - Melissa could tap Rohit (who is with f2py) to help with Doxygen since current NumPy folks are not experienced with it.
    - [name=Melissa] Have 2 levels in mind: High level and reorganize C code
    - [name=Inessa] **Meekail, it would be best to document this in a tracking issue,** to expand the discussion beyond this community call.


- [name=Inessa] Slack is making some big changes to its free plan: https://slack.com/intl/en-gb/blog/news/pricing-and-plan-updates. Currently, free Slack servers show the last 10,000 messages and up to 5GB of uploaded content. From September 1st, Slack is changing this to show the last 90 days of messages and uploads, with no limit on how many messages have been sent or the amount of uploaded content.
  -  Astropy/NumFOCUS may have a specific plan we could potentially get.


---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
