---
tags: NumPy
---


# 2021-01-06 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Inessa, Chuck, Melissa, Sebastian, Matti, Danuta, Ralf



## Follow-up from last meeting / discussions


- Community Survey: processing the data is finished. How to publish? 

- Delay 1.20 release (probably mid-end January) for PyArrow? See [numpy issue](https://github.com/numpy/numpy/issues/17913) and [PyArrow fix](https://github.com/apache/arrow/pull/8834) summary of the issue: 
    - We release by the end of the month independendly from pyarrow.

## Topics


- Adding new dtypes: `float128` (quad precision) and `complex32`? Should they start outside of NumPy

* Sponsorship NEP - any feedback? Would like to implement soon.
  - All looks good to everyone. One comment from Matti to address in the document, then it can be merged with Draft status, and quickly after Ralf can propose to move it to Accepted.
  - We discussed how to determine who to put on the funding committee. Four people (Stefan, Danuta, Inessa, Ralf) have a good amount of experience with obtaining and handling funding, so would be good candidates. Should be an open process though, anyone should be able to volunteer to join this committee. To formalize teams, Ralf will write up a separate NEP, based on the project structure that we talked about at both SciPy'19 and the last in-person sprint in Berkeley.


- Melissa Weber: Intro to Sphinx for Python Documentation - presentation for Data Umbrella 
  - Jan 28th   
  - https://www.meetup.com/data-umbrella/events/275518677/

- CZI grant for f2py, Pearu has  now ~8hours per week on average.



## Additional Details

- Warren

  - Work on a faster text reader is on github at [npreadtext](https://github.com/WarrenWeckesser/npreadtext).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

