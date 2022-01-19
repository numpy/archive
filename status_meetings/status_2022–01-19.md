# 2022–01-19 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 6:00 pm UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Matti, Tyler, Mars, Sebastian, Ross, Alex de Siqueira, Chuck, Stéfan van der Walt


## Follow-up from last meeting / discussions

* Moving to cibuildwheel (anything left to discuss here?)
  * statsmodel uses this now, so this can be stolen (only the deploy step is left to be done!)
  * Perhaps the [skimage workflow](https://github.com/scikit-image/scikit-image/blob/main/.github/workflows/wheel_tests_and_release.yml) is another useful reference


* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  - For now pushed off to 1.23, needs a PRs that could still be backported 1.22.x 

* Decide on where to store saved replies on GitHub for all maintainers to refer to.
  - Wiki seems to be the best place: it's easy to find and followers will not get notified of the changes.
[name=Inessa] will submit the document.

* Better docs on filing issues: https://github.com/numpy/numpy.org/issues/72
Case study: https://github.com/OctoPrint/OctoPrint/blob/master/CONTRIBUTING.md

* Reducing the number of open issues and PRs
References: https://blog.jessfraz.com/post/the-art-of-closing/
  
* Finances review 2022/01/05. There is not much to report. We have a nice positive balance.
 
* Dipping the toes: What are the thoughts on attacking value-based casting "soon"?

* NumPy 1.22.1 was released to fix up issues found after the release. Thanks, Chuck!


## Topics

* Dispute was submitted for the CVEs

* New loadtxt review discussion
  * Skip all the error paths that current fail in PyPy to make CI pass (the next PyPy release will not have this problem.)

* Subscribe to the NumPy YouTube channel: https://www.youtube.com/channel/UCguIL9NZ7ybWK5WQ53qbHng
  - Ganesh's presentation for the Newcomers Hour has been posted: https://youtu.be/VXxa3G4BtEc
  - There is also some new channel custsomization (open for comments)
  - Add a link to numpy.org to the NumPy YouTube channel 

* numpydoc could use a release
  - Makes sense, hopefully Eric Larson will take this (and Jarrod may help). 

* Weighted quantiles inclusion in NumPy and [PRs](https://github.com/numpy/numpy/issues/8935)
  - Invite Aoun Abel to the triage meeting to see if we can push it forward (and what is necessary exactly)

* 1.22.2 there are some issues, but there is probably no big urge.

* There was some interest in a Unit DType but it petered out a bit because the prototype was not faster than astropy.Quantile.  Sebastian still wants to look into a better/more realistic protoype.



---

Please remember to archive this file and commit it to github.com/numpy/archive


