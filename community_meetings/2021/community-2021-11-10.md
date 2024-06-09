# 2021-11-10 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 16:30 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Bas, Melissa, Tyler, Sebastian, Ross, Stephanie, Rohit, Abel, Mars, Mukulika, Chuck, Michael Siebert


## Follow-up from last meeting / discussions

* Moving to cibuildwheel. And to not having a separate `numpy-wheels` repo (?).



## Topics

* Move meeting time, please fill in: http://whenisgood.net/hhy4hk8

* 1.22.0 release current timeline: Fork next weekend
  * Lets wait a bit between branching and rc or any last-minute fixes?  (I think we normally do, just I remembre one or two releases ago we had a few things that should have been noticed earlier)
  * TODO: Aarons arrya-api Prs will go in.
  * The long-double needs fixing before the release: https://github.com/numpy/numpy/issues/20348


* NumPy survey 2021 results
  * Basic updates on the detailed report by Ross (reading in/analyzing the new data now), should be done in the next few days!
  * Need some more people in for the detailed report after that
  * (Previous ones were here: https://github.com/numpy/user-survey-2020-details) will be renamed and include both then.

* [Percentile/Quantile changes](https://github.com/numpy/numpy/pull/20327): rename `interpolation` to `method` and deprecate the former?
  * Pandas is a possible issue, they would see DeprecationWarnings (and have to follow)
  * Sebastian: Send an email to the pandas mailing list to ask them.
  * "interpolation" is not horrible, so we could stick with it, but nobody has reservations about switching and it is somewhat more specific.
  * We would make it DeprecationWarning -> VisibleDeprecationWarning -> error (slowly)
  * There are useful applications for "lower" and "higher" modes (used also as a bias correction)
    * Sebastian: I think I will rephrase the "discouring note" a bit.

* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  * Multiple NaNs are considered identical currently
    * Actually is what R also chooses
  * Previously, multiple NaNs were considered distinct.
  * Array-API chose the multiple NaNs, because some libraries seem to have difficulties implementing this behaviour.
  * Seems like we can agree on the keyword, it is not clear which one should be the default.

* Allocator changes:
  * `get_handler_version` and `get_handler_name` should get annotations?
  * They are hidden away in `np.core` right now.

* Npy appender:
  * There was also this: https://github.com/numpy/numpy/pull/20327
    * adds an `append=True` (but that), difficulty: You need to know that you want to append ahead of time to be certain you can update the header.
    * Unless we just always add this?
  * No need for new header (just ensure extra padding)
  * Multiple users modifying the file is a user-problem (no locking)
    * Maybe small advantage of an `.append()` method as a class.
  * Check also a version with an argument, and ping the mailing list again.



---

Please remember to archive this file and commit it to github.com/numpy/archive



