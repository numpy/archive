# 2022-12-07 NumPy community meeting


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


**Present** *(add your name and GitHub handle)*: Chuck Harris, Sayed Adel, Michael Siebert, Rohit Goswami, Aaron Meurer, Anirudh Dagar, Melissa Mendonca, Ralf Gommers, Inessa Pawson, Sebastian Berg, Alex de Siqueira, Tyler Reddy, Mars Lee, Matti Picus

**Notes taken by:** Ralf Gommers, Sebastian Berg, Aaron Meurer 

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-11-23.md_

- [name=rgommers] Update on Meson build & merging it into `main`
  - Merged with CI now.
  - Windows, SIMD, BLAS/LAPACK still in progress

- [name=seberg] Creation of a new unit DType repo (partially just for organizational reasons)
  - It exists now: https://github.com/numpy/numpy-user-dtypes

- [name=seberg] "Road to NumPy 2.0" 
  - Slowly drafting a bit, but nothing to discuss for a while probably


## New Topics

- Welcome, Sayed! :tada: :clinking_glasses: 

- Dive into C++ (form and substance)

  The first step, Having a guide style imposed by a c++ linter. [gh-22710](https://github.com/numpy/numpy/issues/22710)
  - Even C++17 should be fine.
  - Add C++ linter to CI


- [name=Aaron] Feedback on implementing a few new functions (related to data-api's)
  - Useful/high-impact additions to NumPy
  - Proposals:
    - `np.linalg.matrix_transpose` function
    - add `ndarray.mT` attribute
    - namedtuples for `eigh`, `svd`, `qr`, etc. linalg functions
    - Other suggestions:
        - `vecdot` (stacked 1-D vector dot product) -> (Chuck says this was on the wish list for a long time)
        - `matrix_norm` / `vector_norm` -> helps to have these, can make them into gufuncs
        - `svdvals` (equivalent to `np.linalg.svd(compute_uv=False)`)
        - `permute_dims` (same as `transpose` except `axis` argument is required)
        - `copy` argument to `reshape` (https://github.com/numpy/numpy/issues/9818)
        - `copy=False` for `asarray` -> this is tricky, let's delay that one
        - a bunch of aliases (`acos` for `arccos` etc.) -> only useful in the context of array API standard compatibility, so needs a larger discussion and tracking issue
    - Some discussion on breaking changes: some really small ones maybe we should do at some point (e.g., return tuples of ndarray instead of lists of ndarray)

- [name=Rohit] Would we like to maintain an asv dashboard or look into say pyperf or more modular approaches for testing performance regressions
  - Pros:: no asv :)
  - Cons:: no dashboard (short term?) 




---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
