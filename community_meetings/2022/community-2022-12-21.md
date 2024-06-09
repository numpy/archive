# 2022-12-21 NumPy community meeting


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


**Present** *(add your name and GitHub handle)*: Inessa Pawson, Brigitta Sipocz, Charles Harris, Ross Barnowsky, Mars Lee, Melissa Mendonca, Tyler Reddy, Matti Picus, Sebastian Berg, Ralf Gommers



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-12-07.md_

- [name=seberg] "Road to NumPy 2.0" 
  - https://hackmd.io/rCw5kXszQMqA51diS43mQQ 

- [name=Rohit] Would we like to maintain an asv dashboard or look into say pyperf or more modular approaches for testing performance regressions
  - Pros:: no asv :)
  - Cons:: no dashboard (short term?) 


## New Topics

- `copy=False` discussion:
  - Chuck: Why don't we add a flag to the array like "never copy".
  - No library current implements such a flag
  - reshape would require the `copy=False`

- NumPy 1.24.0 is now available.
The release continues the ongoing work to improve the handling and promotion of dtypes, increase execution speed, and clarify the documentation. There are a large number of new and expired deprecations due to changes in dtype promotion and cleanups.
The supported Python versions are 3.8-3.11.
A total of 177 people contributed to this release, including 107 of them contributed for the first time.
  - Thanks Chuck!
  - Lots of breakage: do we need to discuss?
  - New release this weekend: it won't fix everything, but the big matplotlib (etc.) stuff would be fixed.

- Cirrus offers FreeBSD, should we test on it?  (There are recent failures there.)
  - There may be a limit and it is unclear if we would hit it easily?

- Windows jobs seem duplicated.
  - also in github pipelin

- We could clean up our CI matrix to not run (fully at least) on merges
  - Can lead to errors not being seen immediatly (if main change din the meantime)
  - ... but practically, we usually notice it when the new PR fails anyway.

- Can we have a Doc only label?
  - refguidecheck runs are inconsistent between CircleCI and macOS

- Holiday schedule
The NumPy team is on holidays.
Dec 28th triage meeting is canceled.
Dec 29th Newcomers Hour is canceled.

- CI: adding Musl job.

- When do we drop Python 3.8?
    - NEP 29 says April
    - With release of NumPy 1.25
    - Most tests could probably be moved to 3.10 directly
    - Some CI default images seem to have bumped recently (github actions and circle ci):  The "ubuntu latest" image is actually latest :)




---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
