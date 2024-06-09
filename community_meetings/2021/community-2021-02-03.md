---
tags: NumPy
---


# 2021-02-03 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Bas, Matti, Ross, Inessa, Ralf, Melissa, Sebastian, Danuta, Mars



## Follow-up from last meeting / discussions




## Topics

- GSoC'21: 175 hrs (half the lenght of before), deadline 19 Feb. Do we want to participate?
  - Maybe we could mentor SciPy projects?
  - Over at NetworkX they have a section of the dev docs that are for projects. They should be ~175 hours and have the name of a mentor.
    * https://networkx.org/documentation/latest/developer/projects.html


- NumPy 1.20 questions:
    * The distutils issue (Fortran libs) regression caused issues in scipy (can't compile on windows) https://github.com/numpy/numpy/pull/18295
    * `np.isclose` on `timedelta64` fails, because `np.result_type(np.dtype("m8[ns]"), 1.)` now symmetrically fails just as `np.result_type(1., np.dtype("m8[ns]"))`.  My plan would be to try and work around this in `np.isclose` specifically?
    * `signed_integer_arr[...] = np.float64(np.nan)` now fails, this was not intentional when undoing behaviour changes `np.array(np.float64(np.nan))`. Note that `signed_integer_arr[...] = np.nan` always errored.
      Failing seems right, and it is a rare thing. So I think we should just keep the error until a time where `np.array(np.nan).astype(int)` might at least give a warning? (https://github.com/numpy/numpy/issues/18316)
    * Aim for 1.12.1 a release next weekend.


- Community Survey 2020 
The reports (website + pdf) are at final stages.
An infographic about the demographics of the survey participants is in the works as well.



- Fundraising
    - https://opencollective.com/numpy
    - An example of what is possible: https://opencollective.com/webpack + [Webpack lead community developer interview](https://www.youtube.com/watch?v=AEtg5KYO22c)


- Release note review: Lets review the release note in the "triage" meetings before the release.


---

Please remember to archive this file and commit it to github.com/numpy/archive

