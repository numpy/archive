---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-09-10 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Ralf, Nathan, Chuck, Sayed, Maanas, Tyler, Britney, Joren, Matti, Inessa

## Follow-up from the last meeting / discussions

- Sebastian: Discussion about [sort PR](https://github.com/numpy/numpy/pull/28516)
  - Discussion about python API, C-API and lower level struct of the context. Chuck suggests we start with the C-API, get it called from python, and then modify the other parts to support the new parameters. Maanas suggests shrinking the PR to special-case string dtype. It seems in the end Chuck will try to submit a PR to do the high-level things.
  - 9 Sep discussion: Chuck's PR got merged, Maanas will make a new PR with some of the basic infrastructure, and then get input from Sebastian. 

- [Same-value casting](https://github.com/numpy/numpy/pull/29129) in asarray
  The PR is almost ready, plus/minus some last comments from Marten. What do people think?

- npymath: we should expose the float16 routines from the NumPy C-API itself, and not require downstream users to link to 


## New topics
- Inessa: numpy.org traffic statistics
  
- Inessa: make the numpy.org Plausible dashboard public?
  - Sure! Unfortunately the stats do not include the docs. Could we get that info? Inessa willl follow up at the next meeting.

- RNG test thread safety and limitations of pytest-run-parallel. https://github.com/numpy/numpy/pull/29671
  - this led to a general discussion about best practices and tests. We should update [the test recommendations](https://numpy.org/doc/stable/reference/testing.html#easier-setup-and-teardown-functions-methods) to avoid `setup_class` and `setup_method`
      - Make RNGs local to the test to avoid threading problems.

- [name=rgommers] Touch on platform support (macOS x86-64, ppc64le, ...)
    - Discussion about ppc64le wheels: CI is useful, but not too much enthusiasm from maintainers about releasing wheels for a platform that has perhaps (based on conda-forge download numbers) ~0.2% of the usage of x86-64 Linux. O(2,000) downloads for ppc64le vs. O(1,000,000) for x86-64. Another feeling was that most users are HPC users, and they'd get better performance when building from source (e.g., using Spack).

- Some discussion on 2.3.3 release process: there's an "unverified details" part in the left sidebar, would be nice to investigate.
- numpy-simd-routines: Dynamic/Precise SIMD Control, and testing unit based on buffer protocol.
  * Currently static, 1~ulp(F64), 4~ulp(F32), https://github.com/numpy/numpy/pull/29699
  * To enable independent testing, npsr intrinsics are mapped to support the buffer protocol, allowing Python projects to reuse them without low-level access. Could NumPy be one of the potential users?




### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
