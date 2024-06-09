---
tags: NumPy
---

# 2020-03-18 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 11am Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Matti, Ross, Warren, Chris Meyer, Melissa, Irio Musskopf, Ralf, Stéfan, Anirudh Subramanian, Chuck, Guilherme Leobas, Rakesh Vasudevan


## Follow-up from last meeting / discussions

- Website release plan
   - Launch date was planned to be 15 March, we didn't make it because `<crazy week>`. Hopefully next weekend.
   - We did make good progress, including a full install guide, and revising the majority of content pages.
   - Translations dropdown was disabled, will be re-enabled after launch; translations can only start once content is finalized.

- Survey update

- Documentation and a numpy.org/doc/latest link
  - We should have a `stable` label that points to the last release, and `latest` points to HEAD.
  - Ross will try it with Stéfan's help.



## Topics

- 1.18.2 Released 🎉

- [NEP 41 (dtype redesign)](https://numpy.org/neps/nep-0041-improved-dtype-support.html): Should we give one week deadline?
  - Some more high-level documentation would help the discussion, and will be needed as the project continues
  - Sebastian will send out a notice in a few days

- Change time of community and/or triage meeting to encompass Australia more reasonably?
  - Create a poll: when2meet (Sebastian) maybe we can shift a bit later will send out the Mailing list.

- Creating a Jupyter notebook tutorials repo
  * Executable book project organization: https://github.com/ExecutableBookProject
    - [MyST](https://github.com/ExecutableBookProject/MyST-Parser): a markdown syntax that supports rST roles and directives - integrates with sphinx
  - Will go ahead with creating the Repo

- [numpy-stubs](https://github.com/numpy/numpy-stubs) typing work status?
  - SciPy is planning to have type annotations in their code base.
  - Scikit-image also interested, because of Napari integration
  - Stage 1 of the plan in README of the numpy-stubs repo would be useful on its own, would want to release that.
  - 

- poly1d vs Polynomial
    - Will urge users to move towards Polynomial, and not try too hard to fix poly1d behavior

- Question w.r.t. storing arrays where axes that represent scales 
  - [`xarray`](http://xarray.pydata.org/en/stable/) may solve these (partially?)
  - "Xarray introduces labels in the form of dimensions, coordinates and attributes on top of raw NumPy-like multidimensional arrays"
  - Also see the [Pangeo examples](https://pangeo.io/use_cases/)



## Additional Details

- Matti
  - Work on other architectures
    - The gcc compiler in aarch64 is 8.3.1 which has a [known bug](https://github.com/pypa/manylinux/issues/494). It was fixed in April 2019 but has not percolated into a yum package.
    - ppc64le uses [longlong doubles](https://github.com/numpy/numpy/issues/15763) for np.float128, we need to adjust the routines that assume it is 80-bit doubles.
    - s390x has a [resource starvation](https://travis-ci.community/t/no-space-left-on-device-for-system-z/5954/11) problem on travis. Hopefully IBM/travis will fix it.
    - Full tests on PyPy were failing, [PR](https://github.com/numpy/numpy/pull/15750) is waiting for review
  - Rakesh onboarding
    - held a 1/2 hour session to choose a few topics

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * NEP 41 is up for discussion (not much yet)
  * Some smaller PRs looking at milestoned issues (longdouble confusion)

- Ross
  * Some notes related to the update of [`np.polynomial`/`poly1d`](https://hackmd.io/1CUvnChwQmmpqrvmIbKDsA)

---

Please remember to archive this file and commit it to github.com/numpy/archive

