# 2021-01-20 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Ross, Matti, Ralf, Melissa, Sebastian, Chuck, Mars Lee



## Follow-up from last meeting / discussions




## Topics

- NumFOCUS "one pager" (due today)
  - > Please provide a short description of three (3) future or planned features/upgrades for your project.  These would be things that you have outlined in your project roadmap and/or next steps for your project.
    > 
    > Please provide a 1-2 sentence description.
    > 
    > We will display these in a bulleted list in the one-pager.
    > 

  - > One of the intentions of these one-pagers is to be shown to potential funders.
    > 
    > Funders want to have a quick understanding of the needs of a project so they can see where there may be alignment with their mission and identify places where they may be able to provide support.
    > 
    > Please describe three (3) project needs PLUS a high-level cost and/or "hours-to-complete" estimate.
    > 
    > These will be displayed in table format so try to keep the description as condensed as possible.
    > 


* 1.20 Release any blockers
  * Sebastian: I will look at the int deprecation release note text.
  * Not a blocker but would be nice to have: newer version of OpenBLAS

* Accelerate - do we have any interest in re-enabling it?
    * Backporting to older macOS? Otherwise we may need multiple wheels.
    * We'd like them to do the work, since there is quite a bit (e.g., fiddling with CI).

* Website update
  * Our setup uses undocumented github-pages features. We shouldn't try to change the CNAME in the numpy/numpy.github.io repo, it is brittle.
  * NumPy icon: will be available with SVG and unified colors and line thicknesses.





---

Please remember to archive this file and commit it to github.com/numpy/archive

