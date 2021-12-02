---
tags: NumPy, triage
---

# 2021-12-01 NumPy Development Meeting -- Triage

Note: we alternate between [community meetings](https://hackmd.io/76o-IxCjQX2mOXO_wwkcpg) and triage meetings.

- Time: 16:30 UTC (8:30am Pacific Time)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)


**Present:** Chuck, Sebastian, Ivan González, Inessa, Tyler, Matti


## Triage

* [PRs and issues labelled with "Triage-Review"](https://github.com/numpy/numpy/labels/Triage-review) (please add)

* [PRs and issues labeled with "needs decision"](https://github.com/numpy/numpy/labels/54%20-%20Needs%20decision) (50 open)

* [Open PRs (>250 open)](https://github.com/numpy/numpy/pulls) can we get this below 200?


## Followup

- `np.float128` - let's deprecate the name and leave `np.longdouble`. At some point we may be able to deprecate `np.longdouble`
- `ndarray.__format__` implementation for numeric dtypes [GH#19550](https://github.com/numpy/numpy/pull/19550)

## Topics

* Removal of stack-allocated arrays? See https://github.com/numpy/numpy/pull/20456
  - Should be discussed directly with the HPy people

* It would be nice to get rc2 out this weekend, the weekened after should be OK.

* old proposal for `__format__`: https://gist.github.com/gustavla/2783543be1204d2b5d368f6a1fb4d069
  * new PR: https://github.com/numpy/numpy/pull/19550
  * Sebastian: Will try to float it to the mailing list, I am not sure there was a good reason this got stuck, except the question of "should containers format with {:f}", and there is probably no prior art for this? 

- Inessa is now a Contributor Experience Lead for the NumPy project.:tada: Her work is funded by a supplemental CZI EOSS grant (https://figshare.com/articles/online_resource/Advancing_an_inclusive_culture_in_the_scientific_Python_ecosystem/16548063). The grant is awarded to 4 projects: numpy, scipy, matplotlib, and pandas. 
More info about the grant: https://cziscience.medium.com/advancing-diversity-and-inclusion-in-scientific-open-source-eaabe6a5488b.

- We should look into closing old PRs or floating them up (merging them).

- Discussion about how to make maintainers lives easier, e.g. communication on PRs is sometimes bad.



---

Please remember to archive this file and commit it to github.com/numpy/archive