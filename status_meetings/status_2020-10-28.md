---
tags: NumPy
---

# 2020-10-28 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Ryan Cooper, Bas van Beek, Sebastian Berg, Matti Picus, Ross, Branowski, Melissa Mendonca, Inessa Pawson, Charles Harris, Al-Baraa El-Hag, Madhuilka Chambers, Michael Forbes, Danuta Dzierzanowska 



## Follow-up from last meeting / discussions

- **Community Survey** analysis (not much development, defer to next meeting)
  - repo: https://github.com/rossbar/numpy-survey-results
  - rendered: https://rossbar.github.io/numpy-survey-results/
  - Narrative Text
  - Freeform field analysis (roadmap related)



## Topics

- Newsletter 

* [Travis CI move to .com](https://github.com/numpy/numpy/issues/17656): Probably just need to go ahead with it
  * Move is done and it seems working.
  * Close/reopen on PR will trigger the new build.

- News for the NumFOCUS newsletter (due tomorrow)
  - The new [discourse forum](https://numpy.discourse.group/)?

- Should we publicise the [discourse](https://numpy.discourse.group/) more and also make use it for user support?
  - We need to be sure that we have the bandwidth to moderate if we do this.

* Re: Test improvements (e.g. with hypothesis) discussion: Should we mark "project" labels? I.e. things that should be fairly uncontroversial, but may require deeper understanding and/or long, but hopefully a managable/predictable amount of work.
  - Maybe rather: "Mentor available"
  - Or: We will work on this issue at ... join us!
  - Take an issue, and solve it in a video.

- Plan for video content for "onboarding": https://github.com/BIDS-numpy/planning-onboarding-materal/issues


- Data umbrella: likely 12/2/2020
  * Matti taking lead on it
  * It would be nice to have more intro material for how to contribute to numpy ready for the presentation


- Pydata mentored sprints
  * Still awaiting details, likely in December

* Order of generic types for ndarray ([numpy/numpy#16547](https://github.com/numpy/numpy/issues/16547)):
   * We're approaching the point where `ndarray` can be made Generic w.r.t. its dtype and shape (the latter being a placeholder until proper shape support).
   * Open question: `ndarray[Dtype, Shape]` or `ndarray[Shape, Dtype]`?


- Can we extend the array struct part III:
  * (Sebastian) my opinion is that we should strive for this, even if we may need to back out.
  * What *blockers* would have to be removed?
    * Cython: Is *not* a blocker, ask @scoder to make sure
    * Ecosystem: No known library would have issues.
    * ...?




## Additional Details

- Warren

  - Work on a faster text reader is on github at [npreadtext](https://github.com/WarrenWeckesser/npreadtext).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

