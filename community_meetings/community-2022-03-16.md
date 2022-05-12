# 2022–03-16 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://calendar.google.com/calendar/r?cid=YmVya2VsZXkuZWR1X2lla2dwaWdtMjMyamJobGRzZmIyYzJqODFjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings minutes archive](https://github.com/numpy/archive/tree/master/status_meetings)
- [Triage meetings minutes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings minutes archive](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Ralf, Melissa, Namami Shanker, Bhavuk Kalra, Stéfan, Sebastian, Ross, Chuck


## Follow-up from last meeting / discussions

   
* Apparently the fix for one of the CVEs is missing for 1.22.2
https://github.com/numpy/numpy/issues/19038#issuecomment-1048886879
  * The database seems to list <=1.19.0 which is incorrect, but it does not say that 1.22.2 is still affected. It also has the "disputed" note. Sebastian will send an update request.

* **NumPy Newcomers' Hour** – March 10th, 2022 at 4 pm UTC 
*Speaker:* Mukulika Pahari
*Topic:*  Presentation of the tutorial <i>Analyzing the impact of the lockdown on air quality in Delhi, India</i> (https://numpy.org/numpy-tutorials/content/tutorial-air-quality-analysis.html)
A video recording of the presentation has been posted on the NumPy YouTube channel: https://youtu.be/5bfFI2WuuMA.


## Topics

* [name=Bhavuk] The numpy/numpy issue tracker has a lot of incoming issues about python installation via VSCode. Common notable points in all:
 1) Python version 3.10
 2) Numpy version - 1.22.2 But downgrading to Python - 3.9 seems to solve all the issues.
Refer to:
  - https://github.com/numpy/numpy/issues/21198
  - https://github.com/numpy/numpy/issues/21175
  - https://github.com/numpy/numpy/issues/21168
  - https://numpy.org/devdocs/user/troubleshooting-importerror.html

It appears to be an issue with the default configuration of VSCode on Mac OS.

* [name=Sebastian] We have two "value based" behaviours:
  * [NEP 50 draft](https://github.com/numpy/numpy/pull/21103)
  * The casting promotion/addressed in NEP 50: `np.uint8(3) + 3 -> np.uint8(6)`
  * The "integer ladder of precision", where given `np.asarray(python_int)`, NumPy tries:
    `long -> int64 -> uint64 -> object`  (often `long == int64`).
    * Proposed options: `int64 -> END`, `int64 -> uint64 -> END`, `intp -> ...`
  * Question: Do you think we need to address that "together"? (I suppose as a separate but synchronized proposal.)
  * This could be combined with a proposal to change the default integer: Most likely choice is `intp` (32bit on 32bit, 64bit on 64bit, the advantage is that it fits indexing and indexing-like functions).
  * Consensus here seems to be that it'd be good to do this. And get rid of `long` and auto-promotion to `object` as much as possible.
  * Last wish (Ralf): get rid of `long double`. Separate discussion, but that's already four desired changes.  Longdouble is problematic for some linking issues also, e.g. on windows, aside from platform dependence like double-double.
    (We have this: https://github.com/numpy/numpy/wiki/Backwards-incompatible-ideas-for-a-major-release, not that all of this is "major release" necessarily)
  
* [name=rossbar] Survey schedule + update
  - rossbar will deploy the details site sometime in the next few days. Hold off on announcement until the pdf report is ready.

* [name=Sebastian] Approach for [scalar math](https://github.com/numpy/numpy/pull/21188)?


- [name=Ralf] Revisiting 32-bit Windows support once more ...
  - Right now it is unclear that there are users, scipy is aiming to drop it (unless there is pushback)
  - There will be a discussion/proposal on https://discuss.scientific-python.org/
  - Chuck says that in 1.22.0 the 32-bit Windows wheel for Python 3.10 was missing, and there was only a single complaint because of that. He did upload a new wheel, because Azure DevOps started supporting 32-bit Python again so it wasn't much trouble.

- Discussion about the logic checking for existence of math/C99 functions in `numpy/core/setup.py`.
  * We also have the backup functions, many of which we probably don't need.
  * We should probably just do a release that may fail on some niche platforms (with the new build system), and then see if it actually fails much.



---

Please remember to archive this file and commit it to github.com/numpy/archive


