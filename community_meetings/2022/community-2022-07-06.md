# 2022-07-06 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present** *(please add your name and GitHub handle, it’s completely optional)*: Daniel Wesloh, Ralf Gommers, Melissa (@melissawm), Charles Harris, Sebastian Berg, Inessa Pawson (@inessapawson), Mars Lee (@marsbarlee), Ricardo Prins (@ricardoprins)


## Follow-up from last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2022-06-22.md_

* [name=seberg] Pushing forward the [NEP 50 "prototype"](https://github.com/numpy/numpy/pull/21626)
    * (merged) Next step in progress as PR

* [name=inessa] stats on inactive PRs
Action item for Inessa: Move this from Google Docs to Github
https://github.com/numpy/numpy/projects/16 (COMPLETED)

* video from the June 30th NumPy Newcomers’ Hour: https://youtu.be/lHDEr2eCjAM
Speaker: Ryan C. Cooper
Topic: NumPy in the classroom
If you'd like to help with creating timestamps and reviewing/editing/translating subtitles, reach out to Inessa Pawson


 
## New Topics

* [name=rgommers]: Windows on ARM request (https://mail.python.org/archives/list/numpy-discussion@python.org/message/QVVY24CHAQFLREKO26LUX4LN6J4AJ7BQ/) & supported platforms
  - ARM on Windows discussion was resolved on the mailing list; it would still be good to discuss if/how we want to approach supported platforms
      - For an example, see [PEP 11 - CPython platform support](https://peps.python.org/pep-0011/#unsupporting-platforms)
      - Seems useful, Ralf may ask Matti about getting it started
 
 - NumPy development sprint at SciPy'22: July 16-17th
If you are attending the conference in person, please join us.

- LinkedIn account for NumPy: feedback from scikit-learn
  - Should we grab the IDs/handles (even if we don't use them)?
  - No strong opinions: Go ahead and try (only announcements, no interactions, just like twitter). Inessa will take charge/care of the account.
  - Document access at https://gitlab.com/numpy/logistics


- [name=rgommers] Do we need a doc/policy on (non-)reproducibility and accuracy of floating-point computations?
    - People don't seem to understand this well (example: https://github.com/numpy/numpy/issues/20988), and I've heard more grumbling about it; some justified and most not.
    - More SIMD usage is going to yield more issues when numerical results aren't identical for the same binary across machines (which is fine, but having a doc to point to is useful)
    - When merging SVML support we had some discussion on accuracy vs. performance, however that's only captured in the mailing list thread
    - http://www.cudahandbook.com/2013/08/floating-point-cpu-and-gpu-differences/ makes a good point about multithreaded code, which we use in linalg functionality under the hood, meaning there's even run-to-run variations for the same binary on the exact same machine.
    - SVML PR had comments with detailed accuracy vs. performance benchmarks that will be useful
    - Seems interesting: Ralf will post a draft outline in an issue
    - A scripted response may also be useful sometimes (could link to docs or have its own information).


- [name=Melissa] Wiki: [proposal](https://hackmd.io/@melissawm/r1ZhQves5) +1
Decision: restrict access to "maintainers only". (DONE)

- next triage meeting (July 13th) is CANCELLED.

- NumPy 1.23.1 will happen soon (may happen this weekend)
  - Generally not too many problems with the release.


---
### Let's connect and keep the conversation going!
Join our **Slack** workspace: https://join.slack.com/t/numpy-team/shared_invite/zt-e2d24txg-w3Mq1OJZ2nEAAcGgQOoC0A

Sign up to our **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Subscribe to our **YouTube** channel: https://www.youtube.com/c/NumPy_team

---
Please remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
