i---
tags: NumPy
---

# 2020-04-01 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Ross, Warren, Mars, Ralf, Rakesh, Inessa, Sebastian, Anirudh, Matti, Guilherme, Melissa, Brian, Hameer


## Follow-up from last meeting / discussions

- Website release plan:
  - Very close to release, what's left is: content editing for case studies (Shaloo, Ross), editing down text in tabs and array computing page(Ralf), writing the release announcement (Inessa), and deploying (Ralf, Joe). 

- Survey update

  The SurvMeth670 spring semester is over. The students created the following documents for the Community Survey project:

  - Survey distribution/ analysis: discusses survey distribution procedure, alternative sampling procedures,  sample monitoring methods, and post-survey analysis/adjustments.  

  - Translation considerations: discusses certain considerations to take when translating the survey into different languages.



  - Codebook: provides a guide for coding responses and serves as documentation of the variables on the data file.

  - Security and data confidentiality: documents Qualtrics security policies and provides recommendations for data confidentiality.

  - Translations lined up: Japanese, Chinese Mandarin, Spanish, Russian, Portuguese, decided not to do Hindi.

  - The latest version of the questionnaire (v4) can be found here: https://docs.google.com/document/d/1MX3RqZyurlddFarV8ZAq9AHywzKUHd_AdenMn85CLgI/edit?usp=sharing 

  - TODO: Check what other Python surveys are out/coming out soon?
  - [Anaconda](https://www.surveymonkey.com/r/CTDDMJ6) has come out now
  - Pycharm usually does one around Feb, couldn't find it on the website
  - Stackoverflow - probably does not conflict


- Documentation and a numpy.org/doc/latest link
  * PR for "stable" link : https://github.com/numpy/doc/pull/4

- Creating a Jupyter notebook tutorials repo:
  - https://github.com/numpy/numpy-tutorials
  - Melissa is working on guidelines for what content to write and how to organize the content. Probably split between tutorials about NumPy concepts we need, and educational material (wider range of topics, e.g. an ODE solver from scratch)
  - TBD Jupytext, Myst etc for the toolchain
  - nbdime? for command line tools (not CI/github)
  - Notebooks that render for users on github can be nice for end-users.
  - Getingt content must be the priority (not the format)

- [NEP 41 (dtype redesign)](https://numpy.org/neps/nep-0041-improved-dtype-support.html), deadline as soon as I get feedback from Eric probably.


## Topics

- NumPy 1.18.3 release

- [numpy-stubs](https://github.com/numpy/numpy-stubs) typing work status?
  - Was also discussed previous meeting
  - There is quite a bit of activity here right now, for now being developed in numpy-stubs, but eventually will move into NumPy.
  - There is work on typing `np.ndarray` with a DType.
    - https://github.com/numpy/numpy-stubs/pull/48

- Funding plan SciPy ecosystem
  - See slide 25 of the [Inside NumPy](https://www.slideshare.net/RalfGommers/inside-numpy-preparing-for-the-next-decade) presentation at SciPy'19
  - Work on this project is ongonig/started.
  - Roadmap should be updated (in any case)
  - NumPy will need representation

- Help with macOS and clang [PR 15648](https://github.com/numpy/numpy/pull/15648)

- Peter Entschev may be available to make a call about protocols/`like=` argument in a few weeks.
  - Tell Sebastian if you are interested.

- AWS hired a small team for NumPy (one more opening)

- Docs restructuring: now have a "under the hood" docs section. Melissa would like feedback on what should go there.
  - E.g. how do we deal with MKL/OpenBLAS? How does API/ABI versioning work?
  - Topic suggestions? Warren: writing ufuncs/gufuncs, and custom dtypes -> that would be great.
  - https://numpy.org/devdocs/reference/internals.html
  - Docteam meeting on Monday.

- Faster text reader
  - Work still in progress
  - Plan: New faster version, hopefully current (loadtxt, genfromtext) will mostly use this one.


## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * NEP 41 still being discussed
  * Working on new array-coercion (based on NEP 41 assumption)

- Ross
  * Some notes related to the update of [`np.polynomial`/`poly1d`](https://hackmd.io/1CUvnChwQmmpqrvmIbKDsA)

---

Please remember to archive this file and commit it to github.com/numpy/archive

