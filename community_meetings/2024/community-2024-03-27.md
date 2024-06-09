# 2024-03-27 NumPy community meeting

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

**Present:** Ralf Gommers, Mars Lee, Lysandros Nikolaou, Nathan Goldbaum, Tyler Reddy, Sayed Adel, Chuck Harris, Matti Picus


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2024-02-28.md_

- (after rc1 and maybe rc2) How to announce 2.0?
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is a while away.
  - Can also add a short snippet into the project readme "on github".

- UMATH C++ interface a kiss of life from Marten, https://github.com/numpy/numpy/pull/19753.
  -  When to merge? After the branching of NumPy 2.0
  -  Changing the signature of the inner loop is problematic, especially around dispatching. But Sayed suggests making the wrapper around the changed signature into be meta-objects that will mitigate much of the problem.

   
- (idea) Targeting the NumPy C API with a header-only install.
    - We're down to only this for platform/build-dependent code: [numpy/_core/include/numpy/_numpyconfig.h.in](https://github.com/numpy/numpy/blob/main/numpy/_core/include/numpy/_numpyconfig.h.in)
    - Seems feasible indeed, no one sees a real blocker right now at least


## New topics

- Any objections to making `numpy.version` officially public API?
No, it makes sense. Might need more documentation and tests. We should probably add more strict API tests that nothing creeps into a top-level namespace

- Meta nogil project
    - Ralf, Nathan, and Lysandros began work on a contract from Meta to add support in the pydata stack for the nogil python build.
    - Will start contributing PRs towards that goal
        - CI build probably won't happen until 3.13b1
        - Initially, work on migrating global state to thread-local state.
        - Some work on migrating the new CPython C API constructs that play nicely with the GIL
        - Heap type conversion not needed


- Sketches for last 6 pages of "How to Contribute to NumPy comics"
    - [Link to sketch (4/6 pages)](https://raw.githubusercontent.com/MarsBarLee/gsod-numpy-2023/main/Last%206%20pages.png)
    - Accessing my (Mars) scope creep: script had 6, not 4 pages of story left
    - Possible additional page with credits and links to original issue and PR
    - Coming back after doing some graphic design gigs, so have a better accessment of hours remaining pages would take
    - Will talk to Mukulika
    
- pybind11 and NumPy2
Pybind11 has merged a PR to reduce the warning to a single line. Since it was only 10 hours ago, asking for a release is a bit premature. But maybe we could get matplotlib to build a wheel gainst pybind11 HEAD, although it would be messy (need to get cibuldwheel to use the HEAD from github)

- eigenpy: They use the NumPy headers and make them public, and also import the function table. So if you compile eigenpy with NumPy1 and load it with NumPy2
  - Summary: There should be an eigenpy issue we can point people to and we should link to it in the NumPy issue. The solution we prpose is that people include NumPy and import the NumPy API before including eigenpy. 


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
