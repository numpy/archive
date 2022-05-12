# 2021-09-29 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 16:30 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Sebastian, Melissa, Ross, Mars, Matti, Chuck, Rohit, Inessa, Bas van Beek, Tyler Reddy, Mukulika


## Follow-up from last meeting / discussions

* C++ inclusion into NumPy:
  * Discussion ongoing on the mailing list

* SVML:
  * PR https://github.com/numpy/numpy/pull/19478
  * Should be ready to give it a try/put in.

* 2021 User Survey
  * Stephanie has started cleaning the collected data. She will try to join one of the upcoming community meetings to give an update.
  * We are in talks with Dario Taraborelli from CZI to get their survey team on board for the 2022 survey. (Nothing official yet.)


## Topics

* [Experimental DType/UFunc API exposure](https://github.com/numpy/numpy/pull/19919):
  * Exposure only through a Pyton side API that checks for `NUMPY_EXPERIMENTAL_DTYPE_API=1`.  Or do we need more "safeguards"?  The C caller includes `numpy/experimental_dtype_api.h` and:
    ```
    if (import_experimental_dtype_api(version) < 0) {
        return NULL;
    }
    ```
  * This is not yet stable API, but the header is abundently clear about that.  And I would like to ask e.g. Numba if they want to give the new ufunc API a try.

* Add a new repo for larger benchmarks `numpyorg-benchmarks`. The impetus is the code for the nbody benchmark from a Quansight intern
  - Approved.
  - Ross: it would be nice if this turns into a pluggable system for additional benchmarks.

* Spam on mailing list
  * Someone from the mailing list is going to ask python.org to try to filter it

* [The issue template use seems mostly done?](https://github.com/numpy/numpy/pull/19814)
  * You would get this: https://github.com/Mukulikaa/numpy/issues/new/choose
  * Seems good to move forward here

* PyPy 3.8 has an RC already and should be out soon

* [Typing documentation discussion](https://github.com/numpy/numpy/issues/19875)
  * more docs are always welcome

* [DOC: Old scripted effort to generate C-API documentation with Doxygen #19993 ](https://github.com/numpy/numpy/issues/19993)
  * Old unused script: We should remove it.

* Replace LGTM with github security scan?



---

Please remember to archive this file and commit it to github.com/numpy/archive



