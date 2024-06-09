# 2022-05-11 NumPy community meeting


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

**Present** *(please add your name and GitHub handle, it's completely optional)*: Inessa Pawson (@inessapawson), Charles Harris (@charris), Ross Barnowski (@rossbar), Sebastian Berg (@seberg), Mars Lee(@marsbarlee), Stéfan (@stefanv), Matti , Rohit Goswami (@haozeke)


## Follow-up from last meeting / discussions

* Discussion about NEP 50 work.
  * (Sebastian) Will work on updating NEP this week probably with Ross and Stéfan


- NumPy 2.0 NEP?
  - We have the wiki page: https://github.com/numpy/numpy/wiki/Backwards-incompatible-ideas-for-a-major-release


## Topics

- [name=rossbar] Small development grant for the doctest work.  ([Melissa's draft](https://hackmd.io/@melissawm/HJHOL08Ic)) 
    - Still a proposal, let us know your thoughts (discussed at previous docs team meeting)
    - Sure ☺
    - The grant should try to include SciPy (since that is very similar anyway).
    - Who would take up the grant?  Maybe ask someone from astropy! We need a candidate for the grant application.

- [name=seberg] After the discussion on the mailing list, should we adopt `black`? (And clang-tidy for C probably).
  - If yes, should we aim to do a "full" restyling of the code base soonish?
    - I assume we would "backport" a big style fix to make normal backports easier.
    - It should also create merge conflicts for open PRs probably?  But running the code formatter on the PRs itself should fix that?
    - numpydoc is now black!
    - Seems we are pretyt much agreed on going ahead with black.

- NumPy 1.23 branching should happen end of next week.

    
 - [name=inessa pawson] Call for contributions
Monitor and review submitted examples: https://github.com/numpy/numpy/issues/21351
https://github.com/numpy/numpy/issues/21461
    - People other than maintainers to write docstring examples
    - Lowering Barriers in contributions
        - Having general users instead of power users contribute
        - Moving from interested in contributing to actually contributing
        - Learning workflow
            - Not just Git, but where tutorial would exist in folder structure
            - Example: Does this go into 'module', 'class' or 'method'?
        - Assumption 'Everyone is on Github' or 'Everyone interested in contributing'
            - Lots of data experts don't use Github like this
            - Counterargument: Anyone with knowledge and interest in contributing should learn Git workflow anyway
        - [name=Inessa] Learning from PyCon 2022 sprint: 5 hours with 8 people. Even if there's people willing to learn and teach, will take time
        - [name=Ross] Learning from Outreachy: there's a lot of 'gotchas' of learning doctests and workflow.
            - Having a pair programming made it much easier to learn
            - BUT difficult to reach everyone as Outreachy session had 20-25 people
    - Possible Solutions
        - [name=Inessa] Via GitHub Suggestion on existing PR
            - Similar setup to [Alt-Text Workshops](https://github.com/isabela-pf/jupyter/pull/1#discussion_r790167180)
            - Contributor only need to write text, not learn Git or NumPy documentation structure
        - Pair programming, 20 minute meeting with potential contributor
            - [name=Rohit] We do that on LFortran, where we pair with new contributors the first time (but we're a smaller community and mostly only get a bunch of people before GSo(C,D))
            - We have maintainers willing to do this. Easiest to set up meeting with people who come to Newcomers, community calls, already interested
        - Linking to tutorials instead of having people make a Github PR
            - For people with domain expertise, familiar with notebooks more than Git
            - BUT for changes on NumPy docs, need to run the CI on changes, need to come back to Git anyway
        - [name=Rohit] Maybe something like https://web.hypothes.is/ for annotations on the existing online docs? 
            - (would at-least let us know where the proposal is meant to go)



https://github.com/numpy/numpy/issues/21351#issuecomment-1118685435

 - [name=inessa pawson] [Scarf Gateway](https://about.scarf.sh) is an open-source service that provides a central access point to the containers and packages, no matter where they are hosted. It sits in front of the current registry.
Should we try out?
Benefits: gaining better observability into how NumPy is used (which companies are downloading NumPy, where in the world downloads are coming from (probably not very accurate due to VPN usage), whether or not they come from a CI pipeline, etc.)
Cons: ?

For more info, watch this presentation by Avi Press, the founder of Scarf, from the Maintainers Summit at PyCon US'22 organized by Inessa and Alex: https://www.youtube.com/watch?v=aKUJ0_n0KZ0


- [name=rossbar] Update to docs main page (and general layout) to better match scipy/pandas:
  * Current numpy docs: https://numpy.org/devdocs/
  * Proposed numpy docs: https://output.circle-artifacts.com/output/job/506fce9d-df71-4616-942c-85974d9a7466/artifacts/0/doc/build/html/index.html
  * [Scipy](https://scipy.github.io/devdocs/index.html) and [pandas](https://pandas.pydata.org/pandas-docs/stable/) docs for reference

- [name=seberg] In case it is not [resolved](https://github.com/numpy/numpy/pull/19226).  For structured arrays to compare, the both dtypes must be promotable, which means the following "fails":
  ```python
  arr1 = np.array([1, 2, 3], dtype="i,i")
  arr2 = np.array([1, 2, 2], dtype="i,i,i")
  arr1 == arr2
  ```
  Currently returns `False` (not quite "fail") and gives a `FutureWarning` that it may error, or return `[False, False, False]` in the future.
  This is _also_ the current behaviour for:
  ```python
  arr1 = np.array([1, 2, 3], dtype="i,i")
  arr2 = np.array([1, 2, 2], dtype="d,d")
  arr1 == arr2
  ```
  But in this case, `"i,i"` and `"d,d"` can be promoted to `"d,d"`.  So arguably, we can define the result as `[True, True, False]`!
  I am changing the second one in the above PR, but am not quite sure what to do with the first one.  Make it an error (for now at least), keep returing `False`+`FutureWarning`?



---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A
Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion
Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)
Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file and commit it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


