# 2023-10-11 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Chuck Harris, Sebastian Berg, Ralf Gommers, Tyler Reddy, Raghuveer Devulapalli, Matt Haberland, Inessa Pawson, Ross Barnowski, Nathan Goldbaum, Mateusz Sokol, Mars Lee

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-09-27.md_
- Starting to make ABI breaks
  - there is some header cleanup we could do to move us closer to the limited API. There are some non-limited API uses in the public headers, and these should be hidden so that cython users can do `cimport numpy` with the limited API.

- Numpy 2.0 API migration continues
    - `core` to `_core` rename
    - Direct import of `core` will continue to work to support pickle.

## New topics

- `core.submodule` will still be directly importable to avoid the warnings on pickling after the noticeable push-back on the mailing list.
  - `_core` stays around.
  - New pickle files will use new names, so will break on <1.26.x

- BLAS/LAPACK detection ([gh-24893](https://github.com/numpy/numpy/pull/24893)) & NumPy 1.26.1 release
    - Leaving `allow-noblas` at `false` for this release to ensure that we get reports if anything is not working, rather than silent performance regressions.
    
- Presentation about GSOD NumPy Project is accepted to the PyData NYC program.
    - '[Comics in NumPy? More Likely than You Think!](https://nyc2023.pydata.org/cfp/talk/MTUFNQ/)' on Nov 2 2023, 10:55–11:35am, Microsoft Conference Center
    - Aim to hand out rescoped comics with 10/16 pages

- Remove upper version pin on Python?
  - Decision: Yes, we should remove them.

- Working around uint > -1
  - Started via `resolve_dtypes_raw` which is passed the info: bunch of hacks and lots of templates, but will work...

- NumPy finance review meeting is moved to November 2023.

- Cirrus CI costs:
  - About one month for about $45 (NumPy), SciPy spend $17 for half a month.

- `intp` as default integer discussion (64bit on 64bit machiens, 32bit on 32bit). Should we remove `np.int_` "default integer" and tell users to use `intp`?

  - Decision: change the definition of `intp` to be an `ssize_t`.

## Action items



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: Please enquire in a meeting or by mail.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
