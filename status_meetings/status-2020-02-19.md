---
tags: NumPy
---

# 2020-02-19 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 11am Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)


**Present:** Chuck, Matti, Ross, Ralf, Sebastian, Stéfan, Brigitta, Melissa, ZJ, Inessa

## Follow-up from last meeting / discussions

- SIMD progress
  - [NEP 38](https://numpy.org/neps/nep-0038-SIMD-optimizations.html) is accepted. Now to implement useful ufuncs in terms of universal intrinsics.
      - Identified some corner cases in the AVX implementations. glibc less accurate than avx; issue when fallback to glibc is enacted.

- IEEE quad precision support? What should we change the name of float128 to? Proposals: floatdouble, then floatquad for true 128?
  - We should aim for a very small NEP proposing new names/warnings, etc.
  - Probably better alternative: summary the discussion and move on for now, it's low priority.

## Topics

- Update on NumPy paper
  - [first draft](https://github.com/bids-numpy/numpy-paper) is up and moving forward

- [Tensor Developer Summit website](https://xd-con.org/tensor-2020/) is up
  - Now is the time to register
  - Have speakers from all major projects in this space
  - Will there be some coordination for housing?
  - Up to 36 people registered; room for ~10 more
  - NumPy sprint on the Saturday following.

- Website release plan
    - March 15th launch! (Et tu, NumPy)
    - CloudFlare in front of GitHub pages
    - Community input would be appreciated on the two completed case studies
    - NumPy newsletter - input/ideas welcome. Coordinating issue in repo shortly

- Survey update/plan
    - First [draft](https://docs.google.com/document/d/1OEu4qStk2NBmyE9yVpywlJi8R-88djaOsQWgI-PWQhY/edit) from SURVMETH670 team is in - hoping to turn around quickly! All NumPy community members are invited to contribute to the document by using the GoogleDocs “Commenting/Suggesting” feature.

    - Plan to do a dry-run at a community meeting sometime in the near future

- NEP 41: https://github.com/numpy/numpy/pull/15506
  - Can we move NEP 41 forward fairly quickly
  - Agree (as proposed) that the first step [PR-15508](https://github.com/numpy/numpy/pull/15508) can and *should* be added without a finalized full API proposal. Even if the direct use and usage is very limited.
  - Input from downstream projects (e.g. pandas, particularly units example) would be very valuable
  - Feedback on the NEP process itself
    * Port the "sponsor" mechanism over from PEP - have a person who is responsible for editting/status changes

- Documentation and a numpy.org/doc/latest link
  People are in favor of using this, even if they change 
  - API links: it is important to know that the links change
  - Narrative links: we don't really care
  - We should have a `stable` label that points to the last release, and `latest` points to HEAD.

- Storing unicode strings as UTF-8: can the new dtype system support it? What do you do about unicode points vs byte points? Do we need a latin-1 encoded dtype?
  - (Sebastian) Of course it can support it. The only slightly fun thing is that it is unintuitive vs. storing a string will actually work. I.e. a dtype is limited compared to a unicode string (it can only store unicode strings up to a certain byte length). For strings that is a bit less weird, because ``len(string)`` gives a good idea, for unicode the limit is not directly obvious from the value.
    -  (Eric) note there are two different use cases here: reading encoded files without a copy, and compactly storing constrained strings. Having UCS1 and UCS2 storage available would solve the second problem without introducing unpredictable length semantics, and is consistent with how python handles compact Unicode storage. I suspect we eventually want both solutions available though.
  - (Eric) if we allow parameterizing the encoding in the dtype, we should also parameterize the `errors` argument to `decode` and `encode` as well.

- Would appreciate help pushing [scipy sphinx theme v2](https://github.com/scipy/scipy-sphinx-theme-v2) over the line

## Additional Details

- Matti
  - working on wheels
  - Example of using cython with the new random API almost merged: decision needed
  - Looking for test failures and segfaults on linux32, windows
  - Some movement with cython: [6 blockers](https://github.com/cython/cython/issues?q=is%3Aopen+is%3Aissue+milestone%3A3.0) left for 3.0 

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian
  * NEPs, see above.

- Ross
  * Updated 1.17 and 1.16 docs on site yesterday - if you have a second, check them out and make sure nothing looks fishy to you: numpy.org/doc

---

Please remember to archive this file and commit it to github.com/numpy/archive

