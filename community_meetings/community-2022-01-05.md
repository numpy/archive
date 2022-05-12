# 2022–01-0519 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 7:00 pm UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Rohit, Ross, Inessa, Sebastian, Stefan, Ralf, Chuck, Mars, Alex de Siqueira, Melissa, Matti


## Follow-up from last meeting / discussions

* Moving to cibuildwheel (anything left to discuss here?)
  * statsmodel uses this now, so this can be stolen (only the deploy step is left to be done!)
  * Perhaps the [skimage workflow](https://github.com/scikit-image/scikit-image/blob/main/.github/workflows/wheel_tests_and_release.yml) is another useful reference

* Workflow policy about “abandoned” pull requests
  *Proposed draft:* https://docs.google.com/document/d/1k6mwWjgTMlQ-ykt1phTBRKhDMRDoHa_IwLD2IwMB1NA/edit?usp=sharing


* 2021 NumPy user survey
  * The analysis for the high level report is in the review stage.
  * Mars Lee will work on its graphic design.
  * "Detailed report" (the website) is updated but not available online yet (Ross should look into that).
  * The data set is ready for the release into the public domain.

* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  - tagged for 1.22.1, is this good enough?
      - [RG] yes should be fine. ship has sailed for 1.22.0 I think.

* Docs front-landing page redesign finished
    * [Live page](https://numpy.org/doc/stable/)

* Adding "saved reply" to follow up with a first-time contributor after merging their first PR:
    * Templated response: [https://docs.google.com/document/d/1lM0t6wwPZU_nJCwqkmBbq-a5tr1FCZ-JgnF36WWJ79Q/edit?usp=sharing](https://docs.google.com/document/d/1lM0t6wwPZU_nJCwqkmBbq-a5tr1FCZ-JgnF36WWJ79Q/edit?usp=sharing). Comments are welcome!
    * How to add it on GitHub: [https://docs.github.com/en/github/writing-on-github/working-with-saved-replies](https://docs.github.com/en/github/writing-on-github/working-with-saved-replies)
    * Inessa started adding the comment and will keep track of the results (e.g., second-time contributions, mailing list subscriptions, etc.)
* NumPy Triage Team
    * Everyone is welcome, policies on how to join and maintain membership will be decided by the founding members
    * For successful onboarding and retention, we need to clearly outline duties and responsibilities for this team. Inessa is working on a proposal, aiming to submit on Jan 10th.
    
* NumPy sprint schedule for 2022:
  3-4 mentored sprints and 1-2 maintainers sprints
    - April – mentored sprint at PyCon US
    - June – mentored sprint for Africa and LatAm in partnership with Data Umbrella
    - July – maintainers sprint at SciPy US
    - October – mentored sprint at PyData Global
    - November – maintainers sprint
    - ? mentored sprint with WiMLDS

  If you find issues that would be suitable for newcomers, you can list them here https://hackmd.io/@melissawm/H14qfHRZY or add a label
  - Rename sprint tag to sprintable, and start using it more.


## Topics

* Scripted reply for:
  * "can I work on this"
  * Thanks but no thanks – however, may be hard to generalize
  * Tell inessa about further replies that may be useful

* NumPy newsletter 
  – aiming to launch in late January
  – looking for content writers

* Next Newcomer's Hour is on **Jan 13th at 4 pm UTC**. Ganesh Kathiresan will cover how to:
  – Browse code with vim+ctags+cscope
  – How to debug core files (basics)

* Finances review 2022/01/05
 
* Dipping the toes: What are the thoughts on attacking value-based casting "soon"?

* NumPy 1.22.1 will be released soon to fix up issues found after the release?


---

Please remember to archive this file and commit it to github.com/numpy/archive



