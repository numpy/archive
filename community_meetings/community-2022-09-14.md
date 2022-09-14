# 2022-09-14 NumPy community meeting


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


**Present** *(add your name and GitHub handle)*: Inessa Pawson, Tyler Reddy, Mars Lee, Ross Barnovski, Stéfan van der Walt, Sebastian Berg, Brigitta Sipőcz, Charles Harris

**Notes taken by:** Mars Lee


## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-08-31.md_

- NumPy is hosting a sprint for newcomers at [Grace Hopper Celebration Open Source Day 2022](
https://ghc.anitab.org/programs-and-awards/open-source-day/) on Friday, September 16th. If you signed up as a mentor, make sure it's on your calendar.

- A video recording of Sebastian Berg’s presentation “Ufuncs and dtypes: new possibilities in NumPy” has been posted on the NumPy YouTube channel: https://youtu.be/u9qU6cy5JkE.
For the slide deck, visit: https://github.com/numpy/archive/blob/main/content/UFunc%2BDType_SciPy2022_presentation.pdf

- [name=inessa] Presentation topics for NumPy Newcomers’ Hour 
To suggest a topic for future presentations, leave a comment in this tracking issue: https://github.com/numpy/archive/issues/58.

- [name=Inessa & Melissa] [Documentation user stories](https://github.com/numpy/numpy/issues/22089)
Feel free to add yours!


## New Topics


- [name=seberg] Changing NumPy scalar repr's?
  - For booleans, `np.True_` and `np.False_` seems right, the PR used `numpy.False_` and `numpy.True_`.  Which seems preferable?
    - types print as `numpy.bool_`, but maybe `repr` can be pragmatic and `np.` is actually _more_ copy/pasteable.
  - For numbers we should include e.g. `float32(3.0)`, but also include the module?
    - `np.float32(3.0)` or `numpy.float32(3.0)`?
  - Integer types sometimes print as `numpy.longlong` to distinguish their C equivalent.  I would say they should still print as `int64(3)`?
  - Sebastian will make the PR and feedback can be posted there.

- [name=seberg] The Data-API's is discussing [dtype inspection functionanlity](https://github.com/data-apis/array-api).  This is not strictly related to NumPy, but our `issubdtype` is awkward, so maybe someone here has a thought on what a better API would be.  Some ideas there were:
  - `has_dtype(arr, dtype)`  where dtype could be a tuple and also a special string (e.g. for ``"floating"`).
  - Use an API of `arr.dtype in floating_dtypes`, and allow things like `floating_dtypes | int_dtypes`.


- [name=melissa & inessa] Recognizing and crediting the invisible work in the project.
E.g., taking notes during meetings. Mars has been doing it for quite some time. 
    - Possible solution: add a line “Notes taken by…” in community meeting notes to credit the work of notetakers –> add “co-authored by” in PRs to numpy/archive.
    - It’s clear in hack.md, but can't be automatically transferred to GitHub.
Discussion: Good idea, let's do it.


- [WIP: Contributor Journey Comics](https://github.com/numpy/numpy.org/pull/600)
    - ![](https://i.imgur.com/OzbEsS7.png)
    - ![](https://i.imgur.com/BfHJTE0.png)
    - Invite NumPy Community Call attendees and beyond to this collaborative design prrocess, all in Github
    - Can comment now in call or another time.
    - Comic based on discussion of contributor → maintainer, from the NumPy community call on August 31, 2022. ([meeting notes with details](https://github.com/numpy/archive/blob/main/community_meetings/community-2022-08-31.md#new-topics))
    - Follow-up action from NumPy Docs Call on 09/12/2022 and [Open Source Design discussion](https://discourse.opensourcedesign.net/t/open-source-comics-resources-collaboration-and-funding-for-making-comics-for-open-source-projects/3130/4)
    - Story: Equal standing, different roles, zoom out
    - Seniority not tied to maintainence code, you won't become automatically leader
        - Feels too Hierachal, soften the hierarchy
        - Instead of going up like mountain, a flat plane like a forest? With different paths
            - eg pandas maintainer could become numpy maintainer, still need to familize self with codebase and community but could 'skip ahead'? 
            - visual image of parachuting in?
        - Discussion on blog post: [Imposter Syndrome in Data Science](https://www.caitlinhudon.com/posts/2018/01/19/imposter-syndrome-in-data-science)
            - Expaning sphere, until spheres intesect
            - Continue fire metaphor, rather than put torch to central fire, 
            - Horizontal collaboration
            - What pushes projects is not unilateral decision, get enough consensus or passion to convince others
    - What if people have different mental models and want to be represented differently?
        - One maintainer feels that when offer merge rights, nobody took it. Visual image of alone at top of mountain.
        - The model we have in reality vs the model we want to move to 
        - Maybe show both models? To compare
    - There's so few people in this space, it's a matter of putting in the time
    - Format
        - Using alt text, annotating
    - Making invisible process visible
        - Struggles are universal: What is this, Should we do this, How do we do this
    - Get more feedback across projects
        - SPEC post
    - Discussion: [Why your PhD advisor can solve your problem so "easily"](https://twitter.com/vicgrinberg/status/1560625847223996417)
        - Call member: I also like this cartoon
        - e.g. we know a how to solve a lot of cryptic looking cases as we all run into those already, and for newcomers it may look like wizardry

    - Next actions
        - Ross to comment on PR, say it's good step
        - Mars to show sketches, to structures and fires

- Shoutout to NumPy Community + interest in NumPy Newcomers Hour from RSE Unconference
    - Mars gave a Early Career Keynote for the RSE Asia Australia Unconference, highlighting intersection between open source, open science and research software engineers (RSEs) on Sept 13 2022
    - Other RSEs interested in hosting their own Newcomers Hours
        - make their own videos showing the codebase
        - get to know the developers
        - show applications such as Open Curriculum
    - From Twitter "[now I want to watch all of the @numpy_team Newcomers Hour talks](https://twitter.com/rob_models/status/1569895926701117440)"
    - Is there documentation we can share of how projects can host their own Newcomers Hour?
        - Inessa: the Contributor Experience Handbook is in the works. Melissa, Noa, and Inessa will present about it at CZI Summit, a link to the repo is coming.
        - There are some resources, specific to NumPy, are already in the achive:
            - [Meeting Template](https://github.com/numpy/archive/blob/main/newcomers_meetings/NumPyNewcomersHour_meeting_template.md)
        - Make the invisible visible
        - Highlight non-code contributions such as community growth and hosting
    - [Highlights and links to slides](https://github.com/MarsBarLee/2022-RSE-Asia-Australia-Unconference)
    - ![](https://i.imgur.com/flmlqsm.png)
    - ![](https://i.imgur.com/VQNAOMd.png)
    - ![](https://i.imgur.com/uiGqVUL.png)

- Hosting NumPy Newcomers' Hour
    - Inessa, the usual host, will be out, currently there are two people interested in hosting for next Thursday, Sept 22 - Sebastian and Mars.
    - Pop-up exit survey, would be helpful to people new to the project, how it went and how it could be done better
[x] Inessa - to move Zoom link from the BIDS to NumFOCUS license.




---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
