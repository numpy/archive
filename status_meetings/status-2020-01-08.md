---
tags: NumPy
---

# 2020-01-08 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 11am Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)


**Present:** Chuck, Ross, Stéfan, Warren, Ralf, Melissa, Inessa, Sebastian, Hameer, Brigitta Sipocz


## Follow-up from last meeting / discussions

- `numpy.dual` deprecation 👍
  - Rip it out of SciPy/Statsmodels first (and let them release) so that there is less user-facing noise

- [cygwin compilation](https://github.com/numpy/numpy/issues?utf8=%E2%9C%93&q=is%3Aopen+cygwin+) There are a few open issues with this platform. Is it a priority?
  - Let's make a list of all the platforms we support and what does/doesn't work
  - prio: no

- Ragged arrays: modified [NEP](https://numpy.org/neps/nep-0034.html). Is `np.compat.allow_ragged` the best we can do?
    - https://github.com/matplotlib/matplotlib/pull/15833
    - https://github.com/pandas-dev/pandas/pull/30035
    - 

- SIMD progress
  - [Draft NEP](https://github.com/numpy/numpy/pull/15119) now open PR


## Topics

- How to run [Twitter account](https://twitter.com/numpy_team)

  - See e.g. Matplotlib: tweets updates, usage examples, announcements
  - Melissa and Ralf will have a first go at tweeting out some content.

- A datasets package to use for docs/examples
  - `scikit-image` is about to [integrate Pooch for data downloading](https://github.com/scikit-image/scikit-image/pull/3945)
  - Would probably want this external to NumPy so it can also be used by SciPy and others.
  - Agreed to add small dependency (package) to docs that will fetch data as necessary (tiny files could also live inside the repo, having the fetcher grab it directly from the package).

- numpy.org redesign update (Ralf, Inessa)
    - Content is nearing completion; more after next team meeting.
    - Will organize a sprint to do some final polishing (Inessa & Ralf to pick a date, say 1-2 weeks from now).

- Update on the presentation at UMich Survey Research Center (Ross, Inessa)
UMich - Community Survey meeting minutes https://hackmd.io/4sAhygrmS8mr7_BZmqXuKA

  * Client presentation to UM SURVMETH 670 class on 1/28/2020 (Ross B)

- Update on the presentation at UMich Computer Science and Engineering Department (Ross)
  * Logistics:
    - Presentation: Thursday 1/30/2020, 1:30 PM EST
    - Round-table discussion afterwards
    - Open time M, W, F - 1-on-1 meetings by sign-up
  * Presentation repo [here](https://github.com/BIDS-numpy/presentation-uofm-2020). Feedback welcome. Title ideas? 
    * Rough draft in `outline.ipynb` (\# and \#\# roughly correspond to slide breaks)

- NumPy events calendar for 2020 (conferences, sprints, etc.)
  * (Ross B)Interest in a NumPy workshop at AIMS, Kigali (Rwanda)?
    * Ross B will follow up with organizers
  
  * Tensor Developer Summit, March 19/20 + (perhaps) a NumPy sprint
  * PyCon Italy, April 2-5
  * PyCon US, April 15–23
  * SciPy'20 sprint
  * EuroSciPy'20 sprint
  * SciPy LatAm, September

  - [Community calendar](https://calendar.google.com/calendar?cid=YmVya2VsZXkuZWR1X2lla2dwaWdtMjMyamJobGRzZmIyYzJqODFjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20) or [ical](https://calendar.google.com/calendar/ical/berkeley.edu_iekgpigm232jbhldsfb2c2j81c%40group.calendar.google.com/public/basic.ics) — currently only has community/triage meetings on it
      - Anyone who wants access to modify, please let Stéfan know

- (mattip – defer to next meeting) Are we ready to start testing OpenBLAS 0.3.8? The [NumpyWheels/openblas-lib](https://github.com/MacPython/openblas-libs) repo now builds various OpenBLAS32 and OpenBLAS64 tarballs, including for aarch64 and ppc64le. It is pinned to a post 0.3.7 version of OpenBLAS. [PR-15279](https://github.com/numpy/numpy/pull/15279) proposes using these for our CI runs, but that means updating the CI to 0.3.8dev. OK?
  - Tyler has offered to build v0.3.7 stable tarballs if we prefer.

- Update on paper

- [NEP 37](https://numpy.org/neps/nep-0037-array-module.html)


## Additional Details

- Matti

- Warren
      
  - My repo [ufunclab-wheels](https://github.com/WarrenWeckesser/ufunclab-wheels) is a test of using multibuild in a GitHub Actions workflow to build wheels.

- Sebastian
  * Spring cleanup with Py3K keeping up with PRs
  * Cleanup of old own PRs
  * Start on dtype NEP restructuring

- Ross
  * Exploring GitHub GraphQL API for NumPy: https://github.com/rossbar/github_graphql


---

Please remember to archive this file and commit it to github.com/numpy/archive

