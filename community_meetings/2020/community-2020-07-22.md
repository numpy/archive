---
tags: NumPy
---

# 2020-07-22
NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (18:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Sayed, Ross, Ralf, Melissa, Inessa, Chuck, Sebastian, Matti, Rakesh, Anirudh, Ryan Cooper, Ben


## Follow-up from last meeting / discussions

- Survey Ongoing
    - Just over 830 responses to date
    - Inessa reached out to South-American contacts
    - NumFOCUS newsletter will come out towards the end of the month
    - Inessa is thinking to close the survey ~5 days after that newsletter comes out
    - We will make the data available publicly, we can get an initial analysis from qualtrics as well. (and make sure it is anonymized as much as possible)

- New NumPy Logo:
  - Logo(s) can be found in https://github.com/numpy/numpy/tree/master/branding/logo
  - Still places left to update? ~~Twitter~~, ~~Slack~~, Wikipedia, NumFOCUS website?
  - --> Ralf updated Twitter and Slack, and emailed NumFOCUS who will make the updates on website, merchandise store and (if applicable) other places.
  - Any volunteer to take care of Wikipedia? --> Inessa - DONE

- Website translations (Crowdin)?
    - Wiki page with instructions created: https://github.com/numpy/numpy/wiki/Translations-of-the-NumPy-website
    - Korean, Chinese, Japanese, Spanish and Portuguese (Brazilian) are now enabled in the Crowdin interface.
    - Volunteer for Korean started, only 5% through so far.
    - Other languages not started yet, need another call for volunteers.




## Topics

- Thanks to Chuck for the 1.19.1 release! :tada:

- SIMD Discussion next week with Sayed
  - There was a meeting with David from IBM (original bounty on the issue)
  - Microsoft compilers have issues with auto-vectorizations (at least strided?), so we should focus on universal intrinsics more.
  - We support a few platforms, although AIX will remain problematic (IBM needs to move)

  - [Summary of current status](https://hackmd.io/EvwrkJAhRKedMMQKMkLQDA)
   * Best way to look at this?
     - 16397 is very technical, 16782 is the big one
     - 16782 should have some concrete examples

   * Important metrics that need to be considered:
     - benchmarks, accuracy test, executable size

   * The infrastructure has been merged (more work will probably be needed). Next steps will be to start using it for actual loops in `einsum` and ufuncs





- OpenBLAS do we actually need it: opencv seems to do without, so it may be a long-term goal to see if we can do without (parts) of it.  An advantage may be better strided-performance.





## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian

  - working on NEP 43
  - Looking into retrofitting a return value for casting (and potentially changing the metadata)

- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

