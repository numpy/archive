# 2024-06-05 NumPy community meeting

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

**Present:** Ben Woodruff, Mateusz Sokol, Chuck Harris, Nathan Goldbaum, Sebastian Berg

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings

- (after rc1 and maybe rc2) How to announce 2.0?
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is in a few weeks.
  - Can also add a short snippet into the project readme "on github".

- Nathan did a global state refactor in response to Sebastian's suggestion, needs to be reviewed.

- Had a big discussion about semantics of re-enabling the GIL, motivated by https://github.com/numpy/numpy/issues/26622.
    * Currently you need to manually disable the GIL to run numpy without the GIL.
    * Need a prerelease pip to install the correct wheel.

- [name=rgommers] Roadmap update: https://github.com/numpy/numpy/pull/26505
    * Still moving forward, a few more people want to look.


## New topics

- Sebastian gave an update about the scientific-python meeting.

- Had a discussion about recognizing large funded efforts on the website or with some kind of label of pull requests.
    - Partially to recognize and thank funders and encourage future work but also for transparency. 

- [name=mtsokol] Array API compatibility for `np.ceil`, `np.floor`, and `np.trunc`:
  ```
    In [136]: np.ceil(np.ones(4, dtype=np.int32)).dtype
    Out[136]: dtype('float64')

    In [137]: np.floor(np.ones(4, dtype=np.float32)).dtype
    Out[137]: dtype('float32')

    In [138]: np.trunc(np.ones(4, dtype=np.uint8)).dtype
    Out[138]: dtype('float16')
  ```
- [name=mtsokol] To be backported: https://github.com/numpy/numpy/pull/26603


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
