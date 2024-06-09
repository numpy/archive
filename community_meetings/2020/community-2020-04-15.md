---
tags: NumPy
---

# 2020-04-15 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Charles Harris, Guilherme Leobas, Sebastian Berg, Inessa Pawson, Melissa Weber Mendonca, Matti Picus, Warren Weckesser, Rakesh, Anirrudh, Marcelo Novaes, Hameer Abbasi, Ralf Gommers



## Follow-up from last meeting / discussions

- Website release
Mars Lee: the installation widget is in the works
Ralf: finishing writing the content
Shaloo: finalizing the case studies based on Ross’s input
Inessa: finalizing all the communication pertaining to the launch

- Community Survey update

    
  - The latest version of the questionnaire (v4) can be found here: https://docs.google.com/document/d/1MX3RqZyurlddFarV8ZAq9AHywzKUHd_AdenMn85CLgI/edit?usp=sharing 

  - TODO: Check what other Python surveys are out/coming out soon?
    **DONE:** there are no meaningful conflicts

  - Ross has been given the full permission rights to the questionnaire on Qualtrics. Now the team can continue with the project.

- [NEP 41 (dtype redesign)](https://numpy.org/neps/nep-0041-improved-dtype-support.html), deadline soon up, but I may bring up DType <-> Scalar split on the mailing list.

- Call about array protocols/`like=` argument (next tuesday) NEP 30, 31, 35, 37
  - Tell Sebastian if you are interested.



## Topics

- Moving numpy-wheels to anaconda.org
  - Matti opened [pr 78](https://github.com/MacPython/numpy-wheels/pull/78). It still needs some secrets to be added to the [pipeline](https://dev.azure.com/numpy/numpy/_apps/hub/ms.vss-build-web.ci-designer-hub?pipelineId=8&nonce=ojSEv15E9OGrmmh5iwMrKQ%3D%3D&branch=azure-pipelines2) (Variables button in the upper right corner).

- Branch 1.19 in a few weeks.

- Error message on import: instead of a wall of text link to a wiki page (Ross)

- Sprint in the virtual USA scipy2020: do we want to participate? Matti will respond that we will participate.

- Add a "obsolete" block to the top of the documentation on https://docs.scipy.org/doc . Matti made a [demo](https://docs.scipy.org/doc/numpy-1.3.x/genindex.html) based on [this diff](https://hackmd.io/cnvOU4R7Tv6No8WsBku02Q) that uses javascript to add a `div` to the top of the doc on loading. That means we only need to modify the `_static` theme and not all the pages in the 24 versions of docs there. We should also add a `<meta content="noindex" name="robots" />` header to prevent search engine indexing
  - New sphinx-theme has the version selector which will help with this as well.
  - sitemap can be used additionally to prioritize the newer/stable release.
  - Banner is a good idea.

- Proposal to review/update Code of Conduct committee and NumFOCUS/finance subcommittee.
  - Current CoC and Commitee: https://docs.scipy.org/doc/numpy/dev/conduct/code_of_conduct.html
  - pytest had issues with core developers leaving the project, ostensibly because of unresponsive(?) CoC
  - Sebastian will send email to the mailing list asking for interest.

- Google Season of Docs application: https://github.com/numpy/numpy/wiki/Google-Season-of-Docs-2020-Project-Ideas
    - [Good link for kinds of docs](https://documentation.divio.com/)
    - More other Proposals can be added until May 4th.

- African Institute of Mathematical Sciences (AIMS) - Virtual NumPy workshop on Saturday, 5/2, 9-11 AM GMT+2
  - Ross will hold a class and anyone is invited to help/join
  - NumPy Intro + AI machine learning use-cases


- Complex number behavior in various (order related) functions
  - sort, compare, clip, minimum/maximum
  - `np.isclose` with NaN and `equal_nan`
  - There may be many things to work on here, including adding tests, etc. to see where issues crop up?
  - Hameer will propose deprecations to the emailing list.





## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * NEP 37, etc. https://github.com/seberg/numpy-dispatch
  * Start organizing preparing meeting.

- Ross
  * Some notes related to the update of [`np.polynomial`/`poly1d`](https://hackmd.io/1CUvnChwQmmpqrvmIbKDsA)

---

Please remember to archive this file and commit it to github.com/numpy/archive

