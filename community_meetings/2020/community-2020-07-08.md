---
tags: NumPy
---

# 2020-07-08
NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (18:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Ben, Isabela Presedo-Floyd, Ross, Warren, Anirudh, Ralf, Inessa, Matti, Sebastian, Ryan Cooper, Chuck, Rakesh


## Follow-up from last meeting / discussions

- SciPy recap:
  * plenary/maintainer track NumPy talks were great :tada: 


## Topics

- Survey Released :tada: 

  The survey is offered in 8 additional languages: Bangla, French, Hindi, Japanese, Mandarin, Portuguese,   Russian, and Spanish. 
  *   **531 responses so far**
  * Mailing list posts resulted in ~250 responses, mostly from US
  * So far ~75% of responses are from the US
  * Japan is 2nd in # of responses
  * Remaining communication channels:
    - News bar of numpy.org
    - numfocus newsletter
    - pydata mailing lists
    - Subreddits? (r/numpy, r/python)
  * PSF survey responses (first one in ~2017): about 9k
  * French translation was accomplished within 48 hours of mailing-list request (many thanks to all the fantastic volunteers!)



- New NumPy logo finalized :tada: 
  * Add logo to manifest?
    - General consensus - yes
  * New stickers! Point numfocus to the new logo
    - 2 stickers: small and elongated versions (with text)
    - Ralf will ping
  * Other places where logo needs to be updated?
    - [ ] Twitter
    - [ ] Slack
    - [ ] Wikipedia
    - [ ] NumFocus site


- NumPy Sprint:
  * HackMD: https://hackmd.io/r4pcf4CQRMOUY2VXOWk5_Q
  * Kick-off on crowdcast
  * Create new zoom rooms (Sebastian or Ross)
  * Announce on mailing list prior to the weekend (Sebastian)
  - https://github.com/scipy/scipy/issues/9030
    * Set up a similar issue for the upcoming NumPy sprint
    * Add checklist of good issues for sprint


- SIMD PRs merging status?
  - The [next PR 16397](https://github.com/numpy/numpy/pull/16397) will provide universal intrinsics for all the platforms
  - Then the [next PR 16782](https://github.com/numpy/numpy/pull/16782) will start to use them for actual ufuncs
  - There is also [PR 16395](https://github.com/numpy/numpy/pull/16395) to verify the configuration
  - Still needed: merge documentation [PR 15551](https://github.com/numpy/numpy/pull/15551) which was approved, post-merging cleanup of rst documentation, docstrings, and C comments, fix fallout ([issue 13516](https://github.com/numpy/numpy/pull/13516) ...)

 * Best way to look at this?
   - 16397 is very technical, 16782 is the big one
   - 16782 should have some concrete examples
 
 * Important metrics that need to be considered:
   - benchmarks, accuracy test, executable size

 * Timeline for merging: within the next few weeks would be ideal

- Array coercion (16200)
  * Anirudh is done reviewing - ready for merging sooner rather than later

- How will translations work (for the website)?
  * Crowdin platform for translations
    - Has ML-based autotranslation, but maybe turn off to start
  * Same workflow for Spyder, Jupyter (soon)
  * About 80-90% in place, but not quite ready to start accepting translations
    - try the workflow with a few languages
    - sprint topic

- Tutorials update
  * Tutorials meeting on Monday, some developments:
    - Signed off on a "new tutorial" template



## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian

  - working on NEP 43
  - Looking into retrofitting a return value for casting (and potentially changing the metadata)

- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

