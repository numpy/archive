# 2022–02-02 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 6:00 pm UTC
- [Numpy community events calendar](https://calendar.google.com/calendar/r?cid=YmVya2VsZXkuZWR1X2lla2dwaWdtMjMyamJobGRzZmIyYzJqODFjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Sebastian, Chuck, Tyler, Alex, Inessa, Ross, Matti, Melissa, Ralf


## Follow-up from last meeting / discussions

* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  - For now pushed off to 1.23, needs a PRs that could still be backported 1.22.x
  - PR start: https://github.com/numpy/numpy/pull/20896

* Dispute was submitted for the CVEs
  - They had asked for more proof for rejection/adjusting, not sure what that would be.  But expect the "disputed".

* New loadtxt review discussion
  * The changes were merged.


## Topics

* Checking for NULL in C-API functions?
  * Do we really need to sanitize input (sebastian)? Consensus: yes

* Checking for the return value of `PyArray_Descr*`
  * Pretty useless, but needed to close the CVE, so we should put it in (mattip)

* There seem to be a lot of DOC PRs: Melissa is pinging people to get them moving.

* Data Umbrella LatAm/Africa sprint 2022
  * Important dates:
June 18, 2022:  Pre-sprint session (1 hour) 
June 25, 2022:  Day of Sprint (4 hours)
July 9, 2022:  Post-sprint follow-up (1 hour)
  * Call for contributions: 
In preparation for the sprint, we will need help with mainly administrative tasks, e.g., answering questions on Discord before and after the sprint, surveys, social media, and more. 
Spanish, Portuguese, and French speakers, we especially need you here! 
The work begins in late April 2022. Contact Inessa (via email or Slack) if you would like to help.

* Maintainers Summit at PyCon US 2022 – April, 29th
  * Important dates:
  March 20, 2022 Submission deadline for talks

* SciPy'22 conference (Austin, TX) – July 11-17th, 2022
  * Important dates:
  Feb 11, 2022 Submission deadline for Talks & Posters
  Feb 15, 2022 Submission deadline for Tutorials
  Feb 20, 2022 Program Committee Signup deadline (to review the proposals): https://docs.google.com/forms/d/e/1FAIpQLScWfVL3aWBAxu153qtzSJ_RhkWojTXls6eKmVYUKYkjfLU8fQ/viewform

* NumPy Newcomers' Hour – Feb 10th, 2022 at 4 pm UTC
  *Panel discussion:*  Finding your way in the NumPy codebase
  *Panelists:* Matti Picus, Sebastian Berg, Tyler Reddy
Submit your questions to Inessa via email or Slack

* Can we move forward with things like [extending the experimental DType API](https://github.com/numpy/numpy/pull/20904) opportunistically?

* Value-based casting thoughts, if we have lots of time.  We have 3 design axis (see also [here](https://hackmd.io/JseizFaBS5Otq9gCuPpN7w)):
  * Python scalars are weak vs. strong.
    * Strong: `123.0` is a float64, 1000 is an int64/int32 (maybe with object special case).
    * Weak: `float32_arr + 123.0` casts 123 to float.  `int8_arr + 1` casts `1` to uint8 (or tries to).
  * Python operators could be special: "weak scalars" only apply to Python operators
    * Good: Makes it a bit clearer to understand that `arr + 1` is special and different from `arr + np.asarray(1)`
    * Bad: Makes operators and ufuncs a bit more different.
  * Are our scalars special in how they interact with Python ones?
    * Good: Solves the biggest issue that `uint8_arr1d[0] + 123 -> int64` currently, but with weak scalars it would be `uint8` (lose precision, also for float32 vs. float64)
    * Bad: Solidifies a difference between 0-D arrays and scalars.  Plus, we convert 0-D arrays to scalars everywhere currently...
    * All scalar operations could warn on integer overflows to help a bit with the original problem, is that enough? (Maybe?)  Note that `uint8_arr1d[0] + 1000` can be an error.


---

Please remember to archive this file and commit it to github.com/numpy/archive


