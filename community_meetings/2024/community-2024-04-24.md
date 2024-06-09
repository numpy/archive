# 2024-04-24 NumPy community meeting

- Time: 7:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Nathan Goldbaum, Mars Lee, Brigitta Sipocz, Ralf Gommers, Matti Picus, Mateusz Sokol, Tyler Reddy, Sebastian Berg


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2024-02-28.md_

- (after rc1 and maybe rc2) How to announce 2.0?
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is a while away.
  - Can also add a short snippet into the project readme "on github".

- (idea) Targeting the NumPy C API with a header-only install.
    - We're down to only this for platform/build-dependent code: [numpy/_core/include/numpy/_numpyconfig.h.in](https://github.com/numpy/numpy/blob/main/numpy/_core/include/numpy/_numpyconfig.h.in)
    - Seems feasible indeed, no one sees a real blocker right now at least

- NumPy accepted for 2024 Google Season of Docs
    - Publishing question: Could the finished comics be sold under a formal publisher?
        - Scenario: Comic available on NumpPy website and sold paper copies
        - Not sure about licensing
        - With GSOD, produced work is udner an open license and copyright under Mars. As long as source is still available, comics can be sold 
        - Similar to source software available and selling packaging and installation
        - Conflict: if publisher requests exclusivity agreement
    - For the next NumPy Community survey, after the comics are put on the NumPy website, could we add questions about the effectiveness of the "How to Contribute to NumPy" comics? 
        - Mars will ask Inessa

- Release date: we are mainly waiting for other packages to release for compatibility. 
    - Let's do an RC2 in 1-2 weeks, after OpenBLAS 0.3.27 can be included (Matti is herding CI here at the moment)
    - Final release unlikely to be feasible before the second half of May; even that is optimistic.

- Next month there is a deadline for the NASA ROSES grant. Ralf will be sending out a proposal to the steering committee for a renewal of the grant.
    - Better is finally setting up the mailing list for all maintainers, and sending the request for input there.


## New topics


- Making the test suite separately installable:
    - See https://github.com/numpy/numpy/issues/26289
    - Motivation is binary size reductions (touched on in a previous community , see [gh-25737](https://github.com/numpy/numpy/issues/25737))
        - Also eliminating unnecessary kernels from OpenBLAS distribution

- StringDType SciPy talk accepted


## Action items



---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
