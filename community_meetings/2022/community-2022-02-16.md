# 2022–02-16 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 6:00 pm UTC
- [Numpy community events calendar](https://calendar.google.com/calendar/r?cid=YmVya2VsZXkuZWR1X2lla2dwaWdtMjMyamJobGRzZmIyYzJqODFjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Rohit, Kody Rogers, Inessa, Tyler, Sebastian, Mars, Ross, Charles, Melissa, Matti, Sayed


## Follow-up from last meeting / discussions

* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  - For now pushed off to 1.23, needs a PRs that could still be backported 1.22.x
  - PR start: https://github.com/numpy/numpy/pull/20896


## Topics

* **SciPy'22 conference** (Austin, TX) – July 11-17th, 2022
  Now in hybrid format.
  If you are planning on attending, sign up to volunteer. Current needs:
– moderating online networking sessions,
– moderating online chats during live presentations,
– reviewing talk and poster proposals (Program Committee Signup deadline is Feb 20th, 2022): https://docs.google.com/forms/d/e/1FAIpQLScWfVL3aWBAxu153qtzSJ_RhkWojTXls6eKmVYUKYkjfLU8fQ/viewform

* **NumPy Newcomers' Hour – Feb 10th, 2022**
  *Panel discussion:*  Finding your way in the NumPy codebase
A video recording has been uploaded to the NumPy YouTube channel:
https://www.youtube.com/watch?v=mTWpBf1zewc
Please subscribe!

* **2021 Survey**
  - Need to change URL: currently `user-survey-2020-details`, want to drop the "2020". Is a repo name change sufficient or does there need to additional changes to e.g. CNAME?
  - 2021 results are (mostly) ready to go live: https://rossbar.github.io/user-survey-2020-details/index.html
    * List of outstanding issues: https://github.com/numpy/user-survey-2020-details/issues
    * Please add to the list if you happen to have a chance to review and notice anything that can be improved!
      - Milestoning blockers
  - Data in CI: include encrypted data and de-encrypt during workflow with secrets - any thoughts?

* **GSoC 2022** discussion (cross-discussed at the [SciPy Meeting](https://hackmd.io/pyhudrC5TgSwdJtpPldHgQ))
    * Mentoring organization application deadline – Feb 21st, 2022 18:00 UTC (https://developers.google.com/open-source/gsoc/timeline)
    * Joint proposal? [Ralf]
    * If anyone is interested in checking NumFOCUS org vs. PSF, ping Mridul from Networkx

* **GSoD 2022**
    * Updating https://scipy-lectures.org/, https://scipy-cookbook.readthedocs.io/?
    * https://developers.google.com/season-of-docs/docs/timeline

* **doctests** seem to be broken (and the documentation about it as well)
  - refguide check runs on the `.rst` files, but not the function (etc.) docstrings, maybe non-ufunc ones?
  - There is also a large skiplist

* **Update from Sayed:**
– met with IBM,
– will be looking into complex numbers.


---

Please remember to archive this file and commit it to github.com/numpy/archive


