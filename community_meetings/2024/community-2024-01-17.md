# 2024-01-17 NumPy community meeting

- Time: 6:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian, Matti, Ross, Stefan, Raghuveer, Maanas, Sayed, Chuck, Ralf, Nathan


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2024-01-03.md_

- Review of [the NumPy 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)
  - Improve NumPy-Numba compatibility - nice to have, but not a blocker
  - https://github.com/numpy/numpy/issues/23999 - documentation is pending

- NumPy 2.0:
  - Chuck would like to prepare for branching
  - A few things are still open. The biggest points are:
    - Array API NEP (and maybe implementation)
    - Breaking dtype struct
    - Exposing new dtype API


## New topics

- How to announce 2.0?
  - Put a link into the release notes
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is a while away.
  - We should try to add more links out from the release notes to docs.
  - Can also add a short snippet into the project readme "on github".


- SciPy'24: CFP is open https://www.scipy2024.scipy.org.
  - Tacoma WA (near Seattle)
  - Who would like to give a 3-min talk on NumPy updates (the presenter has to be attending in person)?


- Cython's `numpy.math` ([gh-25594](https://github.com/numpy/numpy/pull/25594))
  - We would prefer that Cython deprecate it. Mattip will repurpose the PR to avoid using `numpy.math.pxd` in `numpy.random`.


- scikit-image also uses `lookfor`. should we just restore it?
  - Can be it's own small library or ipython search.
  - Will keep it removed, and S will make proposal/PR to IPython.


- The very very long ABI mismatch for `_ARRAY_API` and `pybind11` issue is confusing
    - We'd like to get a traceback so it is clear from which package the warning is coming (that package used an old pybind11 to build its binaries) (Sebastian will have a look).
    - We need a new pybind11 release! (Ralf to poke)

- [String DType PR](https://github.com/numpy/numpy/pull/25347) is ready for review, planning to update [NEP](https://numpy.org/neps/nep-0055-string_dtype.html) and propose to accept it.
  - Deepdives into the PR are welcome and Nathan is happy to help with it.
  - A bit longer discussion about the string dtype design.





## Action items


---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
