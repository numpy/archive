---
tags: NumPy
---

# 2020-05-13 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Ryan Cooper, Rakesh, Matti, Sebastian, Melissa, Warren, Ralf, Chuck, Themistoklis, Ross



## Follow-up from last meeting / discussions

- Branch 1.19 in a few weeks. (This weekend probably)
  - Arm wheels ready to go (some trig functions are inaccurate for longdouble on them, tests skipped, but good in the notes)
  - Ralfs open PR should be merged (we could also backport it for the release).

- Google Season of Docs application: https://github.com/numpy/numpy/wiki/Google-Season-of-Docs-2020-Project-Ideas new proposals until May 4th.
  - Accepted! Next deadline: June 8
  - We should formulate a template response to the applications on the mailing list, perhaps encourage them to reach out to the mentors at numpy-scipy-gsod@googlegroups.com

- Complex number behavior in various (order related) functions
  - Please ping @seberg if there are some specific issues.

- `shuffle`, `permutation` and `choice` (https://github.com/numpy/numpy/issues/5173)
  - Warren or sebastian may take this up.

- NumPy survey:
  * The latest version of the questionnaire: https://umdsurvey.umd.edu/jfe/form/SV_8bJrXjbhXf7saAl
  * Translations are underway, aiming to complete the forward translation stage by 06/01/2020.


- Website update:
  - Sports Analytics case study has been reviewed. Thank you, Anirudh!
  - The latest on the homepage design: https://github.com/numpy/numpy.org/pull/221




## Topics

- What to do about shipping a `__init__pxd` without tests?
  - Cython has tests, but they are quite large/slow?
  - We should check the impact, but should probably try to test and leave it (Matti will take a look)

- Any reason not to accept a [PyInstaller hook](https://github.com/numpy/numpy/issues/16163)?
  - Adding seems simple, but we need to test it too?
  - The author is willing to contribute this.
  - We are not opposed, and would like to see the PR.

- NumPy logo redesign
Isabela submitted some ideas, feedback is needed. https://github.com/numpy/numpy.org/issues/37#issuecomment-624348230


- Discussion of GSoD potential projects

- NumPy 1.19, there are some open xfails on odd architectures
  - We should look into xfailing them (but it may be a bit tricky to be specific to software floating point error support)

- Distutils debugging symbol stripping
  - We can think about upstreaming
  - Lets not change it, the wheels are stripped (which makes it smaller)


## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * Incorrect broadcasting, and reduction axis in the iterator https://github.com/numpy/numpy/pull/15162
  * Look into rewrite of array-coercion, a good prototype is finished at: https://github.com/numpy/numpy/pull/16200
  

- Ross
  * Some notes related to the update of [`np.polynomial`/`poly1d`](https://hackmd.io/1CUvnChwQmmpqrvmIbKDsA)

---

Please remember to archive this file and commit it to github.com/numpy/archive

