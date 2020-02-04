---
tags: NumPy
---

# 2020-01-22 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 11am Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)


**Present:** Hameer, Inessa, Matti, Stéfan, Ross, Sebastian, Tyler, Ralf, Mars Lee, Melissa, Chuck


## Follow-up from last meeting / discussions

- SIMD progress
  - [Draft NEP](https://github.com/numpy/numpy/pull/15119) -- wrong link?
  - Can we merge the infra cpu detection without approving universal intrinsics?

- Report on the [Twitter account](https://twitter.com/numpy_team) progress
  - Melissa and Ralf tweeting out some content?
  - Need to enable team tweets
  - RT [Anne's tweet](https://twitter.com/annebonnerdata/status/1219778893537669121)

- UMich Presentations
  * [EECS Presentation](https://github.com/BIDS-numpy/presentation-uofm-2020/) close to done - feel free to check it out.
  * Practice talk on Friday 2-3PM PST [zoom link](https://berkeley.zoom.us/j/762261535)
  * Presentation for SurvMeth670:
Talking points: https://github.com/numpy/numpy-surveys/blob/master/SURVMETH670-presentation.md
Slide deck: https://github.com/numpy/numpy-surveys/blob/master/NumPy_SURVMETH670.pptx
Infographic to be added to the presentation: https://github.com/numpy/numpy-surveys/blob/master/NumPy_info3.jpg
*Please note*: the documents require some minor tweaking. I’m sharing to get some feedback before everything is finalized. - Inessa

- NumPy events calendar for 2020 (conferences, sprints, etc.)
  * NumPy workshop at AIMS, Kigali (Rwanda); Tensor Developer Summit, March 19/20 + (perhaps) a NumPy sprint; PyCon Italy, April 2-5; PyCon US, April 15–23; SciPy'20 sprint; EuroSciPy'20 sprint; SciPy LatAm, September
  * Note new #events channel on Slack


## Topics

- NumPy Logo revisit: will happen in the next months.

- Adding a content section to numpy/archive [PR 15](https://github.com/numpy/archive/pull/15)

- [New tutorial](https://numpy.org/devdocs/user/absolute_beginners.html), yay! What do we do with the [old quickstart](https://numpy.org/devdocs/user/quickstart.html)
   - will be part of a general documentation site redesign

- [Community calendar](https://calendar.google.com/calendar?cid=YmVya2VsZXkuZWR1X2lla2dwaWdtMjMyamJobGRzZmIyYzJqODFjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20) or [ical](https://calendar.google.com/calendar/ical/berkeley.edu_iekgpigm232jbhldsfb2c2j81c%40group.calendar.google.com/public/basic.ics) — currently only has community/triage meetings on it
  - Anyone who wants access to modify, please let Stéfan know

- Update on paper
  - first draft is up and moving forward 

- [NEP 37](https://numpy.org/neps/nep-0037-array-module.html) proposal for ``np.get_array_module``

- `uarray`/`unumpy` Release

- [Tensor Developer Summit website](https://xd-con.org/tensor-2020/) is up
    - Program is still in flux; likely will include more discussion / collaborative time


## Additional Details

- Matti
  - working on wheels for aarch65, ppc64le, s390x. CI now tests "standard" OpenBLAS 0.3.8dev builds on all architectures, 64- and 32- bit OpenBLAS builds. Next up: get multibuild to work with many architectures.
  - NEP 34 merged (again)
  - lots of churn around removing python2 

- Warren
      
  - My repo [ufunclab-wheels](https://github.com/WarrenWeckesser/ufunclab-wheels) is a test of using multibuild in a GitHub Actions workflow to build wheels.

- Sebastian
  * Spring cleanup with Py3K keeping up with PRs
  * Start on dtype NEP restructuring

- Ross

