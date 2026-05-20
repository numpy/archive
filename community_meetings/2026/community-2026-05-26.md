# 2026-05-06 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Joren, Chuck, Inessa, Nathan, Tyler, Maanas, Honi Sanders, Aniket

## Follow-up from previous meetings / discussions

- Followup discussion with Honi about `maxlag` keyword argument. Seems to be a soft consensus to add at least a maxlag keyword argument. Tried to reach out to other projects and haven't heard back. Maintainers think that this was a sufficient amount of outreach for downstream libraries.

## New topics

- Do we want to enforce Zizmor in CI? (https://github.com/zizmorcore/zizmor)  (sebastian: +1 should definitely add)
  - New check on PRs, might fail if the PR touches github actions CI config.
  - People seem mostly ok with this.
  - Maybe also add cooldowns for CI steps that install dependencies. Only allow dependencies older than 1 week.


- Sebastian (async):
  - [DLPack support via registration](https://github.com/numpy/numpy/pull/31256)
  - [Backwards compatibility new DType API]()
    - Tested by duplicating many/most rational tests (I should glance through that myself, but it's pretty straightforward).
    - I would prefer testing more in ml_dtypes, I think (but happy if someone suggests a nice path in NumPy).
  - https://github.com/numpy/numpy/pull/31364
    - Test failure on x86-MacOS looks like a Python bug, I am tempted to skip it (and post on the Python issue) :/.
    - Otherwise, I think this is rather straight-forward


- [Descending/Reverse sorting PR](https://github.com/numpy/numpy/pull/31345): If there is no-one who wants to review it closer or has concerns, that should be almost ready to go in, and we may just put it over the finish line in the next days.
  - The large diff is unfortunate, but due to splitting templates and the fallback implementation into `.hpp`/`.cpp` (to remove explicit instantiation from the templates).
  - Follow-up to figure out fast SIMD sorts (but if that isn't straight forward right now, that seems OK to me (Sebastian))


### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
