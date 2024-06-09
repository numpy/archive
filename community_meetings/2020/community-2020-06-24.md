---
tags: NumPy
---

# 2020-06-24 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (18:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Ben, Ross, Warren, Sebastian, Anirudh, Rakesh, Matti


## Follow-up from last meeting / discussions


## Topics



* What to do with failing python3.9, s390x in CI?

  * We will delete the dead code branch tripping Py3.9 (but may need to disable due to cython)
  * Ping Tyler re: s390x CI run?

* Array-coercion, should we aim to not allow `np.array([array_like, array_like])`:
  - Syntax is slightly elusive and `subok=True` param ignored (the list is not a subclass)
    (Works only for `np.array(subclass, subok=True)`)
  - Many (but not all) array-likes are also nested-sequences, so they work, just slow.
  - Enshrining, effectively disallows array-likes containing sequence objects (I think we
    effectively already do this, because we get the shape from the array-like, at least in
    almost all cases).
  - But: 0-length dimensions do not work with nested arrays

* Anyone up for a UFunc brainstorming session?
  - There are four potential to define ufunc loop:
    - Direct loop match.
    - "Promoted" `f32 + f64` simply uses `f64 + f64 -> f64`  (special enough)
    - Use inner-loop function, but replace dtypes used for allocation:
      - May need to call back with different dtypes, requires two sets of dtypes:
        (one for inner-loop, one for allocation; normally these are the same)
      - `Unit[float64]`` uses `Float64` addition internally
      - Could be defined ahead of time.
    - Unit(float64) uses Float64 loop, but needs to figure that out after promotion (i.e. which exact loop to reuse is only decided at run-time)

    Possibly we don't need the last one (from python, an inner-loop can just call the whole ufunc again, its slow but likely fine).  For the 3rd case, it may be nice to support re-using a loop from a _different_ ufunc.

**Website** 
Milestone - 1 month since the launch of the new version.
**Some statistics:**

*Geography*
![](https://i.imgur.com/kW13qVo.png)

*Languages*
![](https://i.imgur.com/iRiHIaY.png)

*Most visited pages*
![](https://i.imgur.com/qaOCYDe.png)

For more info visit #numpy-dot-org channel on Slack.

**Community Survey update**
English, Spanish, Russian, Mandarin, Japanese, Hindi, and Portuguese versions of the survey have been uploaded on Qualtrics, pretested by native speakers and ready to go.

* Launch date 2nd of July.


**Logo update**

* Please vote at:  https://github.com/numpy/numpy.org/issues/ (the top 3 issues)
* Write an email to the mailing list about the logo! (Inessa will do)


**SciPy’20 networking sessions**
Moderators are needed.
**Dates:** July 8th and July 10th 
**Time:** 5-6 pm CDT
    
*Topics of the sessions:*
* Future of work: is remote the answer?
* I’m a PhD. What’s next?
* The tech writers studio.
* Python in the time of COVID-19.
* Python in FinTech.
* Python in Engineering Research.
* Let’s talk about burnout.
* PyParents.
* Leadership in open source. 
* Diversity, equity, and inclusion in open source. 
* *your topic*

Contact Inessa Pawson if you are interested to sign up as a moderator.


**Sprint for NumPy**

 - Need to figure out what platform NumPy will use to host the sprint
   * Zoom is not approved by organizers (some organization cannot use)
   * Use Jitsi for the sprints. Server needs? investigate beforehand




## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian

  - working on NEP 43
  - Looking into retrofitting a return value for casting (and potentially changing the metadata)

- Ross

  * Upload 1.19 docs?

---

Please remember to archive this file and commit it to github.com/numpy/archive

