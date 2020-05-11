---
tags: NumPy
---

# 2020-04-29 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Guilherme, Melissa, Warren, Anirudh, Ross, Matti, Chuck, Sebastian, Ralf, Inessa



## Follow-up from last meeting / discussions

- [NEP 41 (dtype redesign)](https://numpy.org/neps/nep-0041-improved-dtype-support.html)

- Call about array protocols/`like=` argument (next tuesday) NEP 30, 31, 35, 37
  - Put minutes into the archives repository.

- Branch 1.19 in a few weeks.

- Sprint in the virtual USA scipy2020: do we want to participate? 
  - Matti will respond that we will participate.


- Google Season of Docs application: https://github.com/numpy/numpy/wiki/Google-Season-of-Docs-2020-Project-Ideas new proposals until May 4th.
  - Will probably be submitted May 1st!

- African Institute of Mathematical Sciences (AIMS) - Virtual NumPy workshop on Saturday, 5/2, 9-11 AM GMT+2 (Ross)
  * Presentation: https://github.com/BIDS-numpy/presentation-AIMS-2020

- Complex number behavior in various (order related) functions
  - Discussion on mailing list necessary still?


## Topics

- NumPy 1.18.4 release anything last minute?
  - Will happen any day now, only one backport remaining.


- Proposal to review/update Code of Conduct committee
  - Who would be happy to step in?
  - Short introductions?
  - Can we find a consensus on a proposed change of the CoC committee
  - Ralf will write an email with a concrete proposal of change.


- `force=True` argument for `np.asarray()` and friends (`__array__(force=False)`)?
  - Mailing list discussion is ongoing, some examples will probably.


- `shuffle`, `permutation` and `choice` (https://github.com/numpy/numpy/issues/5173)
  - In the new API they recently got `axis` similar to `take`
  - This is not the same meaning is in most cases (e.g. `np.sort`)
  - `out` argument and in-place is another design choice.


- NumPy survey
  * Link to the latest pretest: 
  https://umdsurvey.umd.edu/jfe/form/SV_8bJrXjbhXf7saAl
    - Main change: replace email collection with link to GH, twitter, mailing list
  * will go out today to translators
  * (Logo will be fixed in the final link) DONE
  * Please try it out!


- Website Update:
  - Last case study is complete, someone with cricket skill would be a great final reviewer!
    - Anirudh and Rakesh will have a look.
  - https://github.com/numpy/numpy.org 
  - No release blockers aside from tweaks
  - News section can have releases, what else, see: https://github.com/numpy/numpy.org/issues/219 https://github.com/numpy/numpy.org/pull/222


- Logo redesign:
  - May be picked up soon






## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * NEP 41 merged, next PR is open and waiting for 1.19, the followup about array-coercion is still in the making

- Ross
  * Some notes related to the update of [`np.polynomial`/`poly1d`](https://hackmd.io/1CUvnChwQmmpqrvmIbKDsA)

---

Please remember to archive this file and commit it to github.com/numpy/archive

