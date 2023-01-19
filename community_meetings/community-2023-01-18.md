# 2023-01-18 NumPy community meeting


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


**Present:** Inessa Pawson, Charles Harris, Craig Peters, Ross Barnowski, Ralf Gommers, Tyler Reddy, Matti Picus, Julian, Mars Lee, Sayed, Brigitta



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-01-04.md_


## New Topics

- Melissa/Inessa: Docs Team leadership transition
    - Thank you, Mukulika and Ross, for stepping up!
See the announcement on the mailing list: https://mail.python.org/archives/list/numpy-discussion@python.org/thread/CINO52S7PCQG7D472MGLEQKLI6SLIOXT/

- Inessa: NumPy Documentation Team handbook: https://github.com/numpy/archive/blob/main/numpy_docs_team_handbook/README.md
Feel free to file issues and submit PRs to expand it.

-  Craig Peters: Has anyone tried Codespaces with the updated devcontainer configuration?
     - The latest PR: https://github.com/numpy/numpy/pull/22785
     - Feedback from new users may be best (e.g. lets announce on the mailing list?)
Inessa will make the announcement.
     - Relationship with Gitpod: in parallel, at least for a while to determine what is easier to maintain.


- Feedback (or lack thereof on the mailing list) on the NumPy 2.0 proposal
    - Hesitance to reply due to long development history, maybe missing too much context to feel like have valuable feedback 
    - Holding a vote? 
    - According to the document, there should be a commitment from 2 champions for each feature. There is not enough maintainer bandwidth for it.

- Can we decide on doing a feature flag to start on small things?  Thinking of a small change (returning tuples rather than lists from `np.gradient` or so)
  - Ok, we can do this.
  - Flag more likely to get feedback than a branch
  - Annouce on twitter "try your code with this feature flag"?

- Cython 3 should not be planned right now, which means descriptor and array ABIs are mostly frozen.

- Discussion on state of meson.
  - Docs are still a big thing, since we describe distutils everywhere.  (Before Python 3.12)
  - Works, but SIMD is open (Sayed working) and blas/lapack support is functional but not magical yet.  This needs to be in meson (by April 2023)
  - More CI jobs moved to meson.
  - Wheel building works nicely for SciPy, it should be easy to move over there to meson.

- Lets rip out all the nose remnents, it has been many years!


---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
