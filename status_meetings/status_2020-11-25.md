---
tags: NumPy
---





# 2020-11-25 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (19:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Ralf, Chuck, Matti, Bas, Sebastian, Al-Baraa, Inessa, Ryan, Maximiliano Rios



## Follow-up from last meeting / discussions


- Community Survey
  * Dec 6, 2020 - final survey report to be released.
  * The analysis start is here: https://rossbar.github.io/numpy-survey-results/, still lacking narrative and certain fields (free-form)



- Data umbrella: 12/2/2020
  - Finding "sample issues" is difficult but would be good, we have to sit down find issues.
  - Test related improvements could be good projects, e.g. using parametrize, moving things around to gather like tests together
  - preview of the talk is on the `data_umbrella` branch of [mattip/archives](https://github.com/mattip/archive/blob/data_umbrella/content/data_umbrella_dec_2_2020/data_umbrella.ipynb)
    - don't forget to show the basic layout of the repos, how they work together, and scan some issues




## Topics

- Plan a translations sprint for Jan'21? See [tracking issue](https://github.com/numpy/numpy.org/issues/55)
    - A sprint would be useful; aim for second half of January. 
    - Would be good to find a coordinator per language, and let them help pick a date.
    - Ralf will plan this.

- 1.20 release?
  - There is one more PR
  - Take a bit more time with RCs and ask to test specifically on certain hardware

- PyData Cambridge meeting Zoom bombing?

-  naming/link title for the NumPy tutorials repo domain name numpy-tutorials (numpy.org <-> github-pages). Since the repo is called numpy-tutorials, the canonical link will be numpy.org/numpy-tutorials. Is that what we want?
   - we should add a redirect from numpy.org/tutorials to that URL

- https://github.com/scipy/oldest-supported-numpy
  - Tries to solve the issue of installing the oldest numpy a certain python version supports


* TravisCI did gives us credits now, lets see if it is any useful

- Conda forge has some system to unify CI:
  - https://conda-forge.org/docs/user/ci-skeleton.html



## Additional Details

- Warren

  - Work on a faster text reader is on github at [npreadtext](https://github.com/WarrenWeckesser/npreadtext).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

