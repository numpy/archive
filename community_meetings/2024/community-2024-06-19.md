# 2024-06-19 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian Berg, Ralf Gommers, Chuck Harris, Luiz Amaral, Nathan Goldbaum, Mateusz Sokol, Ben Woodruff, Tyler Reddy, Inessa Pawson, Stefan van der Walt

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings

- Had a discussion about recognizing large funded efforts on the website or with some kind of label of pull requests.
    - Partially to recognize and thank funders and encourage future work but also for transparency. 


## New topics

- Release 2.0.1 with Python 3.13?
  - Python RC is coming in July, we should try to have a release around that time/soon after.
  - Branching 2.1 would have to be very soon.
  - That may also be fine: align us to the old release version.
  - It usually takes about 2 weeks to receive feedback on a new release. Let's hold of decisions for the next release until the next community call.
  - Nathan is already testing against Python 3.13 on main.
  - Dropping distutils: wait until the support for 3.11 ends.

- Discussion that we have to use Python 3.11 for docs build because otherwise distutils docs doesn't work.

- User annoyance reported:
  ```
  In [4]: np.clip(np.array([0, 255], dtype=np.uint8), 0, 455)
  ```
  Fails due to no promotion (Python integer) of the uint8 but 455 doesn't fit uint8.
  - Clip is implemented in Python, so if the input is a Python integer and the dtype is integral, we could check and just ignore the bound!

- POSSEE NumPy GenAI update: Ben will submit reviewed PRs to Chuck

- Discussion on numpy typing stubs
  - Refer to: https://github.com/numpy/numpy/issues/26747
  Conclusion: let's treat strings as scalars.
  

- SciPy US'24 conference: Nathan is hosting a NumPy development sprint and a NumPy 2.0 community feedback (BoF) session.




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
