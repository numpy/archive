---
title: NumPy community meeting
tags: [NumPy]

---

# 2026-09-23 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings) and [new meetings agenda](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)


**Code of Conduct** 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Inessa, Abhinay, Iason, Nathan, Pratham, Chuck, Matti, Stéfan, Sam, Joren, Maanas, Riaz, Sebastian, Swarom, Harsh, Tyler, Shoumik, Shreya

## Follow-up from previous meetings / discussions


## New topics

- Pratham: 
   - https://github.com/numpy/numpy/pull/32552 To be merged
   - https://github.com/numpy/numpy/pull/32641 Decision on breaking change
   We discussed these and will move forward with both PRs. Thanks Pratham!

- Inessa:
  - https://github.com/numpy/numpy/issues/23805 - needs decision to allow markdown in release notes. 
    We discussed this and would prefer to stay with RST for now. NEPS can be whatever they want, but the tooling around release notes should stay RST.
  - https://github.com/numpy/numpy/issues/24574 Add a `[docs only]` positive CI selector instead of the negative. 
    (mattip) This would now be an alias to `[skip actions]` since we only have github actions and circleci now, right?
    The discussion moved quickly to maybe having tags to not run SIMD or not to run BLAS. But too smart of a CI can also cause problems.    

- Joren: 
  - turning `np.poly1d` into a generic type, maybe?
  Working on typing it became Any. Can we do better?
  Probably. It is widely used but not really well
  maintained.

- [Transition to heap types](https://github.com/numpy/numpy/pull/32641#issuecomment-5788708580). Choices:
  - wrong meeting, move this to the triage meeting
  - warn already in 2.6 when subtyping a type exported by the API if the class is not a heaptype, make the change for 2.8. How would we do that?
  - Cannot warn. Document the change in 2.6, make a breaking 2.8 change with no direct warning.
  - Try to find consumers of the API classes, make sure they are using heap types.
  - Wait till NumPy3 and make the change all-at-once
  - Something else 
  This discussion was around the PRs above, and was decided to move forward making these heap types.

- Iason: 
  - histograms and base ndarrays: https://github.com/numpy/numpy/pull/32701
  histograms should convert everything to ndarray or preserve base classes? Against base classes: matrixes can not be bin edges. For: it would be nice to preserve units. The main problem is that histogramdd does something different from histogram. Concensus was to move to probably move to base ndarrays and expect users to use `__array_function__` or wrap themselves.
  - type resolver for minmax to raise no loop error if it would reach a loop via a safe cast for user dtypes: https://github.com/numpy/numpy/pull/32702
  Discussion: there are edge cases around promotion failing falling back to separate min/max instead of fast minmax.
  - for the C99 Annex G stuff, should I close all the issues and explain what the issue is and why we won't fix them?
  Discussion: yes, close all of them
  - stil got two PRs up about same-kind casting for np.put and np.repeat. Matti had a question which I had answered on the review. Would be good to just get them in so they don't sit in the queue.
  (mattip) yes, that answered my question. From my perspective they are good to go.

- Process for merging ByteStringDType / accepting NEP 58
  Discussion: Nathan will submit a large PR to implement the ByteStringDType and hopefully people will review it.

- Shoumik: 
  - I would like to discuss [PR 32589](https://github.com/numpy/numpy/pull/32589), fixes 24115. Failing CI job for default to utf 8 and the next steps towards it.
  Discussion: (mattip) we should close this PR as a learning excercise, and if Shoumik wants to, Shoumik should investigate internal numpy use of open without an encoding.

### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
