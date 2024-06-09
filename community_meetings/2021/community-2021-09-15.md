# 2021-09-15 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Tyler, Sebastian, Bas, Ross, Mars, Stéfan, Melissa, Serge


## Follow-up from last meeting / discussions

* The 2021 survey is closed. We have collected 520 responses. The next steps will be announced by Stephanie shortly.

* SVML progress

## Topics

* Consider alternating times for this meeting to allow more people from eastern timezones to join.
  * The same time as the triage meeting is probably good.
  * Sebastian: send an email to the mailing list: probably move to the same time as the triage meeting currently.

* NASA [ROSES-21](https://science.nasa.gov/researchers/sara/grant-solicitations/roses-2021/schedule-research-opportunities-space-and-earth-sciences-roses-2021) grants went out, and NumPy, scipy, pandas, sklearn proposal was funded.

* C++ inclusion into NumPy
  * Serge Guelton (Pythran dev, author of incremental C++ move PR -https://github.com/numpy/numpy/pull/19713) will join this meeting.
    - [xsimd](https://github.com/xtensor-stack/xsimd)
      - No PPC support in xsimd currently
      - x86 (SSE2, SSE3, SSSE3, SSE4.1, SSE4.2, AVX, FMA3, AVX2, AVX512), x86 AMD (SSE4A, FMA4, XOP), ARM (ARMv7, ARMv8)
      - Few extra math functions, such as exponential logarithm ([ldexp](https://github.com/xtensor-stack/xsimd/blob/master/include/xsimd/types/xsimd_api.hpp#L857))
    - Removing the C-symbol export by integrating more into C++ seems worthwhile, but not incremental?
    - We could have clang-tidy checks to make sure we only use a subset of C++
    - The introduction of `integer_tag` might be confusing?
    - The disabled travis CI warnings might be nice to restart?
    - Sebastian: Ping the mailing list again the coming week, hopefully we can push this forward soon.

* [`npreadtext`](https://github.com/BIDS-numpy/npreadtext) is testable (the idea is to replace `np.loadtxt`):
  * Announcement later today (it should be possible to `pip install` it and use `from npreadtext import monkeypatch_numpy` to try.)

* [PyCon India](https://in.pycon.org/2021/) sprint (September 20)


---

Please remember to archive this file and commit it to github.com/numpy/archive



