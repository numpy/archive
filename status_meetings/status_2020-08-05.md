---
tags: NumPy
---

# 2020-08-05
NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (18:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present: Ben, Warren, Melissa, Inessa, Ralf, Matti, Anirudh, Rakesh, Sebastian, Chuck** 


## Follow-up from last meeting / discussions

- Survey (about to close?): currently 985 responses
  * Upcoming meeting with a survey data privacy expert

- SIMD Discussion last week with Sayed: he is interested in continuing to contribute to NumPy past the first SIMD bounty.
  * Universal intrinsics for add, sub, mult, div on non-x86 platforms
  * Initial returns positive


## Topics

- `numpy.doc` namespace:
  - Can it be deleted (at least particular files, such as the glossary here: https://github.com/numpy/numpy/pull/17010) (I think this is the right PR https://github.com/numpy/numpy/pull/16996)
  - E.g. Debian does not even ship `numpy.doc` in the default install at least
  - Most users probably would only find it using `np.info`, but `np.info` seems rarely used?
  - Consensus: We can delete it (after scanning for the interesting bits)
    - Ross will look into this.

- meta: can we enable the GitHub feature that automatically removes a PR approval when a new commit is pushed?
  * Alternatively: does anyone know how to remove an approval *without* re-requesting review?
    - Consensus: no, leave as-is. It is the responsibility of the merger to make sure any changes that occur after approvals are good

  * Result of discussion: a maintainers guide would help clear up the policy here.
    - Use scikit-image guide as a template

- 3.9 Python release will mean some multibuild docker images need updating (beginning November)
  - Matti can take a look at that.

- Doc meeting update:
  - NumPy tutorials repo is moving (switch to binder)


- Tests (at least Travis CI) seem to be slow, migrating some of them to Azure may help.


## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

