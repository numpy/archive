---
tags: NumPy
---



# 2020-11-11 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (21:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Maia, Melissa, Ryan, Bas, Ralf, Matti, Sebastian, Chuck



## Follow-up from last meeting / discussions

**We discussed quite a lot last week (not sure we should go through all of these):**

- Community Survey (no news currently expected)


- Travis CI: Most things were moved now, astropy and NumFOCUS discussion is ongoing
  - We may be able to move to shippable (but scipy can't)


- Data umbrella: 12/2/2020
  - Finding "sample issues" is difficult but would be good, we have to sit down find issues.
  - Test related improvements could be good projects, e.g. using parametrize


- Plan for video content for "onboarding": https://github.com/BIDS-numpy/planning-onboarding-materal/issues
  * We probably need a few more concrete ideas about what to make videos of


- Pydata mentored sprints
  * Still awaiting details, likely in December
  * Melissa is looking into this possibility (we will review )

- "Mentor available" or live hacking (work on issue XY and invite others to come along if they are interested)?
  - Lets look into Office hours first (Melissa will look for time)



## Topics

- Areas where projects/newcomes could work on:
  - Tests (adding tests that are missing for, e.g., empty arrays, infs/nans, complex dtypes; parametrize; untested checking for code coverage)
  - Go into less heavily used parts of the code base and find new issues (for particular purposes, like Data Umbrella)

- Tensor API standardization project:
  - Blog post: https://data-apis.org/blog/array_api_standard_release
  - Array API standard document: https://data-apis.github.io/array-api/latest/
  - Repo: https://github.com/data-apis/array-api/


- NEP 42: DType restructure, mainly casting:
  - PR should move forward, since there are a couple of more steps necessary:
    - Change the actual casting loop setup
    - Fix the casting loop signature (requires to adapt all code callign it)

- NumPy 1.20 cut:
  - Mainly OpenBLAS decision open. (lets discuss next week?)
  - Release aim for branching in 1.5 weeks
  - Remaining typing PRs should maybe be merged (Bas can milestone the ones that would be good to land)
  - NEP 35 needs to be decided on.
    - Need to decide whether the `like=` argument should be strict

- timestamp64
    - Noam Raphael would like to suggest to implement a  data type to hold a proper timestamp
    - Noam was in the "early call", ironicaly due to a timezone mess. In discussion, it turns out that (as I understood) he wants is to make the [epoch official](https://numpy.org/devdocs/reference/arrays.datetime.html?highlight=epoch#datetime-units). The documentation there is (maybe intentionally?) vague what exactly epoch a datetime64 represents. 
    - Matti will write a mail to the mailing list asking if we should anchor `datetime64` to UTC at a particular epoch, or if that is a bad idea. This would make `datetime64` "atomic time": an exact count of the time since the epoch, rather than "unix time" which is adjusted by a second or so every decade.

- CZI grant is about to end (this means deprecation NEP, etc. will be ready for review soon)


## Additional Details

- Warren

  - Work on a faster text reader is on github at [npreadtext](https://github.com/WarrenWeckesser/npreadtext).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive
