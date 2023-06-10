---
tags: NumPy
---
# 2023-06-07 NumPy community meeting


- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Sebastian, Raghuveer, Inessa, Stéfan van der Walt, Mike McCarty, Michael Siebert, Sayed, Chuck



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-05-24.md_

- Sayed Adel: Next move towards C++ support, there's a lot of SIMD work depending on it.
    - Two choices: SVE support from C++ (will require C++ ufuncs), or add sizeless support in universal SIMD.
        - option 2: https://github.com/numpy/numpy/pull/22265
        - option 1 (preferred by Sayed):
            - https://github.com/numpy/numpy/pull/21057
            - https://github.com/numpy/numpy/pull/19753
    - Either way it does/should not affect anyone externally.
    - Internal vs. external signatures will diverge more if internal is in C++ and external in C.
    - Inner loops for custom dtypes will still be able to be written in C, like now (so no backwards compatibility breaks for C API users).
    - NEP: C++ support in the ufunc machinery.
    - Sayed will write a summary of why the ufunc machinery needs C++ parts going forward. After that is done, we'll judge if it needs to be a full NEP (Ralf agrees to help writing if needed).
    - C++17 version is much better and lower-complexity than the older implementation that Sayed had.




## New Topics

- Discussion about sin/cos precision
  - [name=Raghuveer] Suggested to use lower precision for float32 but high accuracy for float64.

- SPEC discussion (endorsement)
  - https://scientific-python.org/specs/
  - Mainly 0 (replacing NEP 29) and 4 (CI infra) are interesting, a bit of history may be good.

- Changing string casts to bool
  - `np.asarray(["0", "1"]).astype(bool)` is currently ``[False, True]`` does it seem OK to change that to `[True, True]` (i.e. the `0`) for NumPy 2.0 or should it even then have.
      - Can lead to silently bad results 
      - old behavior: `np.asarray(["0", "1"]).astype(int).astype(bool)`
      - We can probably just change it for 2.0

- Context manager to control precision




## Action Items





---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
