# 2023-09-27 NumPy community meeting

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


**Present:** Ralf, Stefan, Matti, Tyler, Sebastian, Nathan, Chuck, Mateusz, Mars, YanLiang

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-09-13.md_


- Inessa's CZI grant supporting her role as NumPy Contributor Experience Lead is ending on September 1st.
    - We'd like to figure out later what activities that were grant-supported for the past two years to keep going and support as a team on a volunteer basis (or look for new funding for).


- Starting to make ABI breaks
  - there is some header cleanup we could do to move us closer to the limited API. There are some non-limited API uses in the public headers, and these should be hidden so that cython users can do `cimport numpy` with the limited API.


- Numpy 2.0 API migration continues
    - `core` to `_core` rename

## New Topics

[PR to speed up np.char](https://github.com/numpy/numpy/pull/24756) functions: should they be ufuncs?
  - against: the code is simple now and works. Having reductions would not make sense?
  - for: it would be more generic and support all the axis/out kwargs
      - summary: there is a strong sentiment for using ufuncs if we are already touching the code. They don't have to be public at this point. At some point, when NEP 55 kicks in, they will be exposed via the `np.strings` namespace

- (Ralf) working on adding BLAS/LAPACK CI jobs, `-Dblas=auto` and backporting that to 1.26.1/2 asap. [gh-24808](https://github.com/numpy/numpy/issues/24808) and [gh-24703](https://github.com/numpy/numpy/issues/24703) point to a bit of pain for downstream package devs.

- ufunc signature: we should make a decision to solidify it for 2.0
  - Move `auxdata` inside the context?
  - extend `get_loop()` to have more information?
  - need to solve the problem of not being able to have a pow() loop. 
  - allocate a buffer? You can do it today via the auxdata.




## Action Items



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: Please enquire in a meeting or by mail.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
