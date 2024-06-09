# 2021-12-22 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 7:00 pm UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Chuck, Inessa, Sebastian, Rohit


## Follow-up from last meeting / discussions

* Moving to cibuildwheel (anything left to discuss here?)

* Workflow policy about “abandoned” pull requests
  *Proposed draft:* https://docs.google.com/document/d/1k6mwWjgTMlQ-ykt1phTBRKhDMRDoHa_IwLD2IwMB1NA/edit?usp=sharing


* 2021 NumPy survey results
  * There are volunteers for each section to perform an analysis (and review it), first iteration should be done soon (~1 week).
  * After that, analysis needs to be put together into a report.
  * "Detailed report" (the website) is updated but not available online yet (Ross should look into that)
  * "public use" data; clean data enough so there is no disclosure risk:
    - classify data based on sensitivity, threshold. 

* [Modify/Revert changes to unique NaN handling?](https://github.com/numpy/numpy/issues/20326)
  - tagged for 1.22.1, is this good enough?
      - [RG] yes should be fine. ship has sailed for 1.22.0 I think.

* Docs front landing page with sphinx-panels almost ready
    * [CircleCI preview](https://23834-908607-gh.circle-artifacts.com/0/doc/build/html/index.html) (recommended to view in Firefox to see all images, will not show in Chrome)
    * Trying to land before next release (late December) and backport candidate label
    * Need to change link to current Getting Started page
    * We have a least a few days (backport label should be used)



## Topics


* Adding "saved reply" to follow up with a first-time contributor after merging their first PR:
– Template of the reply: [https://docs.google.com/document/d/1lM0t6wwPZU_nJCwqkmBbq-a5tr1FCZ-JgnF36WWJ79Q/edit?usp=sharing](https://docs.google.com/document/d/1lM0t6wwPZU_nJCwqkmBbq-a5tr1FCZ-JgnF36WWJ79Q/edit?usp=sharing). Comments are welcome!
– How to add it on GitHub: [https://docs.github.com/en/github/writing-on-github/working-with-saved-replies](https://docs.github.com/en/github/writing-on-github/working-with-saved-replies)
– How to find PRs submitted by first-time contributors: e.g., modify the `tools/changelog.py` to look for such PRs so we do not forget for a while.

* NumPy Triage Team – everyone is welcome, policies on how to join and maintain membership will be decided by the founding members
  – For successful onboarding and retention, we need to clearly outline duties and responsibilities for this team.

* NumPy sprint schedule for 2022: 
  * Look for a short survey on NumPy Slack:  https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A
 


---

Please remember to archive this file and commit it to github.com/numpy/archive


