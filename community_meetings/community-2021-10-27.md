# 2021-10-27 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 16:30 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Tyler, Mukulika, Melissa, Bas, Mars, Sebastian, Matti, Inessa, Chuck, Ross, Ralf, Rohit


## Follow-up from last meeting / discussions

* 2021 Community Survey
  The data from the free form responses on the project priorities is available for review and/or analysis.


* Moving to cibuildwheel. And to not having a separate `numpy-wheels` repo (?).
  * related to https://github.com/numpy/numpy/pull/20102
  * Questions were a bit 'open ended".
  * Two question: 
    * We would like a way to trigger builds without additional commits in the main repo.
    * It would be good to control access, but is this possible with a "github actions" button?
      (It should be limited to "commit" bits at least) 
  * We should move forward
  * Put it in for testing, but 1.22 will still be NumPy wheels

## Topics

* Deprecate `MachAr` ([numpy/numpy#20201](https://github.com/numpy/numpy/pull/20201))
  * Do need to keep the information `ibeta==2`, `irnd` (rounding mode info as an integer), `ngrd` (guard digits) around?  Normally users should have IEEE floats and this seems well defined? (and very hidden)

* NumPy mailing list moderation
  * Matti, Sebastian, and Inessa are now moderators/owners along with Didrik Pinte from Enthought.
  * [PR to numpy.org](https://github.com/numpy/numpy.org/pull/487#discussion_r737513542): is that the appropriate place?
    * No. We can tuck in in to one of the governance docs and we can also extend the [list description](https://mail.python.org/mailman3/lists/numpy-discussion.python.org/) with much of the info 
  * Private repo to record mediator actions under github/numpy?
    * it is up to the moderators to manage this as they see fit

* 1.22.0 release timeline and important PRs/features/issues?
    * Current plan is to fork mid November
    * [Ralf] I'd like to get the `numpy.array_api` module as well [DLPack](https://github.com/dmlc/dlpack/blob/master/include/dlpack/dlpack.h) support completed.
        * Yes we'd like these. Ralf to post a tracking issue.
        * DLPack yes. Sebastian has a few concerns. Discussed: let's not put it into `asarray`, just as a separate `from_dlpack` function. Let's start simple and raise errors in corner cases if needed. `readonly` is one corner case to discuss on the PR, probably okay to raise an error, but there's some history there.
    * [Ralf] any deprecations we want to get into 1.22 in order to be able to push the `numpy.lib` namespace reorganization forward? SciPy 1.8.0 will have a large amount of private-but-missing-underscores deprecations, we may want to do something similar for NumPy (perhaps in 1.23 though, in case we're risk averse and want to see if there are complaints for SciPy?)
        * No: better to merge early into the release cycle for `1.23.x`. 
    * [Sebastian] I would like to merge the current DType (and probably some other smaller followups), but overall:  It probably just doesn't matter too much, most testing will happen on `main` anyway...


- PyData Global sprints: **this Saturday, October 30** Numpy + Scipy | 2pm UTC
    - All participating developers will have free access to the conference. You only need to register via this link (*Note: kindly ensure that every maintainer that will participate in your project sprint signs up to the conference using a link* that I can share in private if you need it).
    - https://pydata.org/global2021/sprints/#numpy

- [moving from `refguide_check.py` to pytest](https://github.com/numpy/numpy/issues/15846#issuecomment-948051075)
  * Distill the existing refguide_check issues/discussion on the issue tracker to get the conversation all in one place.


- Temperature reading: applying for a NumFOCUS Small Development Grant for C++ enabling in NumPy?
  - Yes, let's draft this. Will be helpful also to clarify what the next steps are.
  - Bringing PocketFFT in sync with the SciPy version would be useful, nice side benefit of allowing C++.



---

Please remember to archive this file and commit it to github.com/numpy/archive



