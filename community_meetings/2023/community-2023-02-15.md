# 2023-02-15 NumPy community meeting


- Time: 7:00 pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Inessa Pawson, Sayed Adel, Sebastian Berg, Tyler Reddy, Matti Picus, Charles Harris, Tatiane, Ross Barnowsky, Melissa, Brigitta, Raghuveer



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-02-01.md_


- Discussion about array clearing.

- Status of "exotic" CI jobs & their maintenance burden
  - Some discussion about CI platforms: Azure is the most problematic platform - can we get rid of it? Ralf volunteers to deduplicate some jobs, and Brigitta volunteers to work on moving jobs to GitHub Actions.


## New Topics

- inessapawson/rossbar: Google Season of Docs 2023
    - The new season has been [announced](https://groups.google.com/g/season-of-docs-announce/c/-wfcYZ9UYwc/m/gotnfJ0OCgAJ?pli=1).
    - Read about last season's successful projects [here](https://developers.google.com/season-of-docs/docs/2022/participants).
    - Mukulika and Ross are available for mentoring.
    Melissa will be mentoring Matplotlib (if the proposal is accepted.)
    - Important dates: 
Feb 15th - applications open 
March 24th at 18:00 UTC - deadline for organization applications
For the full GSOC timeline, visit https://developers.google.com/season-of-docs/docs/timeline
   - Google doesn't pay directly, payments are made via OpenCollective. A participating technical writer will be submitting their invoices through Open Collective. The infrastructure for distributing funding is already set up and can be used for future GSOC projects.
   -  Budget proposal can range $5k-$15k in total, 40% upfront, 60% on completion.
   -  A project can have multiple tech writers.

- Topics for a GSoD:
  - Tutorials or how-to-guides on best practices for using numpy functions or performing certain tasks?

- Adding copyright to code like in [PR 223171](https://github.com/numpy/numpy/pull/23171): do we have a policy? Is there one we can adopt and add to the guidelines somewhere?
*Discussion:* Introduce a policy for not including copyright notices in the code base. Possible exception: for complete files that can be used stand-alone in a different code base. 
By contributing code to NumPy you agree to the license of the project. We could add this reminder to a PR template to make it more explicit.
Ask the NumFOCUS legal team for assistance drafting this policy.
 
- adding `types` to `np` or `np.lib`
  - Mainly used for DType classes, but available to other internal classes that would not end up in the main namespace (except exceptions).
  - `np.dtype[np.int64]`
  - Sebastian will make a poll (and then potentially abide by the result).

- seberg: `_is_numeric` attribute to DType classes?
  - Alternative: go to full abstract hierarchy immediately?
  - Should `bool` be considered "numeric"?
  - Nathan is not around, so maybe to defer

- seberg: Just  noticed that Travis CI seems MIA for the past 2 weeks. It is complaining about missingi credits, but we still have credits?!
  - mattip: I sent a mail to Travis support. They already got back to me  that the issue should be solved.

- Inessa: NumPy 2.0 team meeting
Let's start planning. Inessa will email the Steering Council.

- Inessa: https://github.com/numpy/numpy.org/issues/614
Please submit your feedback.
https://www.tensorflow.org is a good example of solving the issue.


## Action Items

- [] Inessa: Add a copyright notice to PR templates for nummpy/numpy and numpy/numpy.org.

- [] Melissa: ask the NumFOCUS legal team for help draft policy for not including copyright notices in the code base.
- 
---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
