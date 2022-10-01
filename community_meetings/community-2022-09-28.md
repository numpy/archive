# 2022-09-28 NumPy community meeting


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


**Present** *(add your name and GitHub handle)*: Michael Siebert, Ross Barnowski, Sebastian Berg, Matti Picus, Inessa Pawson, Brigitta Sipocz, Mars Lee, Tyler Reddy, Chuck Harris, Melissa Mendonca, Stefan van der Walt, Meekail Zain

**Notes taken by:** Inessa Pawson, Sebastian Berg, Mars Lee


## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-09-14.md_

- NumPy hosted a sprint for newcomers at [Grace Hopper Celebration Open Source Day 2022](
https://ghc.anitab.org/programs-and-awards/open-source-day/) on Friday, September 16th. 
~80 joined for the opening presentation
~70 stayed for the first 5 hours
30+ PRs submitted on the day
Special thanks to Rohit, Brigitta, and Ross for mentoring the newcomers.


- [name=inessa] Presentation topics for NumPy Newcomers’ Hour 
To suggest a topic for future presentations, leave a comment in this tracking issue: https://github.com/numpy/archive/issues/58.

- [name=Inessa & Melissa] [Documentation user stories](https://github.com/numpy/numpy/issues/22089)
    - Feel free to add yours
    - [name=Mars] Can add some based on Newcomers Design Jam, will anonymize names

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
  - Going towards `is_dtype(arr.dtype, dtype)`.


- September 22nd NumPy Newcomers Hour 
Hosted by Mars Lee 
Topic: Design Jam Session
    - Prompt #1: What does the NumPy Newcomer’s Journey look like to you?
    - Prompt #2: What do you need/want to further your NumPy Newcomer’s Journey?
    - ![Higlighted slide showing the results of the design jams](https://i.imgur.com/3duZWbY.png)
    - Link to [Slides](https://docs.google.com/presentation/d/1zQ9mGzs4360IXuUQBVs5kk80xJfrK8QD4VWBos1xXIA/edit#slide=id.g15534e57164_0_3)
    - Link to [Jamboard](https://jamboard.google.com/d/10dIw7ptXrFwPpHin1DgMQsi5i-KCVn10BpCshtOgUq8/edit?usp=sharing)
    - [name=Mars] Currently cannot upload to NumPy Youtube channel. Cannot convert video, stuck as 'double_click_to_convert' Zoom file.
    - Compiled [responses back into Github WIP: NumPy Contributor Journey](https://github.com/numpy/numpy.org/pull/600#issuecomment-1258157615), as a comment
        - Higlights
           - "I feel that there is more space to make mistakes in newer projects"
           - If we acknowledge these fixed properties of NumPy (mature project): Would it be better for a newcomer to open source to start with a downstream project?
       - Synergy with other efforts
           - Meekail's [“Zones” of contribution](https://hackmd.io/zm65_TjfSpi9DSSkE2o7Iw) ([Github project board](https://github.com/orgs/numpy/projects/4/views/1)). Newcomers benefit from achievable goals, structured starting points
           - Inessa & Melissa: [Documentation user stories](https://github.com/numpy/numpy/issues/22089)
    - Introduce design process
        - User research: embolden partcipants by saying their responses do matter
        - ![Slide showing problem: fuzzy pathway for newcomers](https://i.imgur.com/eTKiRlG.png)
        - ![Slide showing bigger problem: maintainers](https://i.imgur.com/g9QEVeA.png)
        - Inspired by Belen Barros Pena: "[No design without research – Why and how to incorporate design research practices into our free software projects](https://speakerinnen.org/en/profiles/belen-barros-pena)"
        - Balance between encouraging honest responses and protecting anonymity
            - Check all mediums: jamboard, video, written summary, etc
            - As we bring in design methods, need to keep in mind proper technique, ethics
        - [name=Mars] Eventually, would like to make resource/template for other Scientific Python projects to host own Design jam
            - Design Jam resources already exist in other spaces (hardware, UX/UI)
            - Need to account for differences: Often CLI, different definitions of "newcomer"
            - ![Slide showing different levels of newcomer](https://i.imgur.com/A7roDND.png)
 - Purpose of Newcomers Hour
     - More casual space than other community calls
     - Useful for onboarding
     - Alternate between open hang out and speaker series (videos on youtube.com/numpy_team)
     - 2 years going 


## New Topics

- [Official NumPy Youtube channel](http://youtube.com/numpy_team) is hard to find (impossible to search for)
  -  maybe it should be also in the github repo readme?
  -  A repeated name might help (always include NumPy Team) in the title.
  -  Suggestion: Tell people to search by keyword > search by channel
  -  Catching up with SEO optmization, outlisted by other NumPy videos
  -  It's best to subscribe to the channel

- "Zones of contribution" project (Meekail, Inessa, Melissa):
    - Next steps: Continue sorting the broad catagories
    - Hardest part is distingishing and dividing Python and C code
        - [name=Chuck] NumPy in maintainance mode, hard to split up, need to read in full regardless
        - Example: Person X took 2 months to familiarize with the codebase
        - [name=Matti] Possible task: Moving masked array to array function?
        - Popularity of masked array: According to the [2020 NumPy user survey](https://numpy.org/user-survey-2020-details/content/2021/features_and_deprecations.html#numpy-components
), masked array is used by ~15% of respondents
        - [name=Stéfan] We've been wondering if we should add any of the array interfaces to SciPy sparse (does that even make sense?)
        - [name=Michael] Adding new data types?
        - High level task: fixing headers


- [name=rossbar] Setup github sponsorship page?
  * See e.g. matplotlib's setup: https://github.com/sponsors/matplotlib
  * Setup requires someone with org ownership privileges
      * Who? Stéfan, Ralf, Matti
      * Owner > Admin privileges
  * Point at both NumFOCUS and OpenCollective
  * Easy to set-up. Github shows set-up process, copy matplotlib
  * Need to set up.github/FUNDING.yml, copy matplotlib's yml file
      * Point to Tidelift
  * [ ] [name=Matti] Set up Github sponsorship page


- [name=seberg] NEP 50 wants to change the following:
  - `uint8_arr + (-1)`  should Error!
  
  Should we also change these to error as well?
  - `uint8_arr[0] = -1`
  - `np.array([-1], dtype=np.uint8)`
  
  And maybe:
  - `np.uint8(-1)`  (this one _could_ be special!)
  - Continue discussion on mailing list


---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
