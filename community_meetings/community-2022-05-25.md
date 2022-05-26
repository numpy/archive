# 2022-05-25 NumPy community meeting


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


**Present** Charles Harris, Melissa, Stéfan, Ralf, Inessa, Ross, Brigitta, Rohit, Mars Lee, Meekail Zain, Ricardo Prins, Craig Bosco, Matti Picus, Maureen Ononiwu, Sebastian Berg


## Follow-up from last meeting / discussions

* Discussion about NEP 50 work.
  * Merging now (05-25), will announce later today or in the coming days.


- [name=rossbar] Small development grant for the doctest work.  ([Melissa's draft](https://hackmd.io/@melissawm/HJHOL08Ic)) 
    - [name=Melissa] Follow-up today at [SciPy community meeting](https://hackmd.io/@tupui/scipy-meetup/edit)
        - separate to a package (a first pass at https://github.com/ev-br/scpdt)
        - Initial work: https://github.com/ev-br/scipydoctest
        - What is the maintenance cost of keeping this separate plugin? (pytest releases may break plugins)
        - What about https://github.com/astropy/pytest-doctestplus?
        - Context: https://github.com/numpy/numpy/issues/21070



## Topics

* **NumPy 1.23 is branched**:
  - Travis build wheels, but did not upload [issue](https://github.com/numpy/numpy/issues/21599)
  - "highlights" may still be mutable, so please suggest additions
  - This means now/soon is a good time to push larger changes! 

* **next NumPy Newcomers’ Hour** – June 2nd, 2022 at 4 pm UTC
  **Speaker:** Sebastian Berg
  **Topic:** Maintaining NumPy: Deprecations

* **The policy about inactive PRs:** https://github.com/numpy/numpy/pull/21537

*History of the policy:*
– 2018-10-31 - the first mention of the need for a documented process for closing inactive/abandoned PRs: https://github.com/numpy/archive/blob/main/triage_meetings/triage-2018-10-31.md

 – 2021-12-15 -  the first draft is introduced at the NumPy triage meeting: https://github.com/numpy/archive/blob/663fd30feb6ec553929e9970129906968a9d7fb1/triage_meetings/triage-2021-12-15.md

– 2021-12-22 - the first draft is introduced at the NumPy community meeting: https://github.com/numpy/archive/blob/bf7ac87d0eb143ecc7f0882e8f8159683c4bc5af/community_meetings/community-2021-12-08.md

– 2022-03-30 - approval of the latest version at the NumPy community meeting:
https://github.com/numpy/archive/blob/3cd5b6ce3af12b649c3b053265e060393a25c26f/community_meetings/community-2022-03-30.md

*Discussion:*
Implementation via a bot - a case study from astropy 
Links to the bot that astropy uses:
https://github.com/astropy/astropy/blob/main/.github/workflows/stalebot.yml
https://github.com/pllim/action-astropy-stalebot
also tried https://github.com/actions/stale, but it coundn't be configured to fit the policies of the project.

* Bot automatically closes inactive PRs older than 6 months.
* Bot sets the binary: active and inactive.
* Complexities in between, such as wanting to finish someone's PR, could be managed by an interested maintainer.
Parties involved:
        - bot
        - reviewers
        - contributors
Advantages of using the bot:
        - more sustainable: currently astropy has only 64 PRs open as opposed to 260+ in the NumPy main repo.
        - it sends a clear message: this rule applies to everyone, both a maintainer and newcomer.
Cons:
     - it can seem cold to some people,
     - could discourage newcomers, especially if the closing occurs due to the delay in review.
     
Rohit: Manual might be better for `numpy` where some portions just review slower (e.g. `f2py`). Practically this would just mean we'd reopen PRs more often, not a problem just kinda weird.

Rohit: What's the relation to `triage-review`? What about our `close?` label?
        - What if I want to finish someone else PR? (e.g. PR is inactive but only needs a little finishing.)
        - Perhaps an inbetween status? Active, Open to Community, Inactive

Ross: Maintainers know that finalizing is fairly common / but contributors should also be told that it is generally OK to finalize before 6 months is over.

If we have both bot and this cultural expectation, maybe humans and robots can live in harmony?
    
Charles: We all want to be nice, all want to finish things, but we don't reach ideal. So how do we handle the reality? 
As a reviwer, introducing a bot maybe worthwhile in long term. 
Implementation is a process, it's always messy at first.

Brigitta: What counts as active / responding?
        - Maybe a commit
        - Maybe a comment
        - Maybe a rebase 
        
Sebastian: Bot forces you to make PR active, every 6 months
        - Not so bad, makes you jump into action

Ralf: For new contributors, if you're waiting for the maintainers / reviewers and the bot closes it, then that is a great way to ruin the contributor experience (e.g. stalebot). The issue is that the warning / other issues might not be under control of the contributor.

 - No bot vs with bot:
        - Reviewer needs to take time to read through an 2 old year PR, needs to evaulate without a contributor here to explain.
        - vs Maintainer forced to evaluate in 6 months. 

Melissa: We can segregate the implementation and the policy discussions. Timeline first, then automation.

- People have good and bad experiences about bots in other projects. If we do have a bot in NumPy, how can we do better?

Brigitta: from the maintainer side, what I see in astropy that a few maintainers are get guilted into review a PR if they get the nudge from the bot. They more likely ignored the direct ping by users. But this is not real stats but anecdotes based on the behaviour of a very small number of maintainers.

Rohit: Guilting people into review in the first place might not be good. A bot saying (the project) thinks this has sat around long enough and it was your (the maintainers) responsibility isn't being very kind to volunteers. Bots needs to be suited for each project and community resources.

Brigitta: yes, I suppose astropy has a very different setup, as we hardly ever waited on reviews from the very few who had astropy explicitely as their job. The rest were volunteer in the sense that they are working on it as part of the “flexible 30%” of research time, but there is hardly any volunteers in the project who has nothing to do with astronomy on their day job. It helps with slow maintainers. Guilt may not work on NumPy since NumPy has different commmunity than astropy.

- Bot cost vs Reviewer cost:
        - Bot makes a decision
        - Maintainers are forced to 'take on their own burden'
        - VS Triage team takes burden
        - (Ralf did one triage session for issues and went through 1000+, closed 70 or so in one night).

*Action items:*
1. Inessa will submit stats on inactive PRs at the next community meeting.
2. Inessa and Sebastian will review the pending PR to incorporate the changes that were approved at the meeting: 
       - a PR can be closed after a review by one maintainer,
       - expand on what "finalazing a PR" includes.

* **Should f2py be moved out of NumPy eventually?**

---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A
Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion
Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)
Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


