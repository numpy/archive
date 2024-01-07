# 2024-01-03 NumPy community meeting

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

**Present:** Ralf, Sebastian, Arman, Chuck, Lucas, Ross, Inessa, Nathan, Tyler, Mateusz, Raghuveer

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-12-20.md_

- Review of [the NumPy 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)
  - Improve NumPy-Numba compatibility - nice to have, but not a blocker
  - https://github.com/numpy/numpy/issues/23999 - documentation is pending


- Inessa: Moving forward on [ENH: add cov parameter to numpy.polynomial.polynomial.polyfit](https://github.com/numpy/numpy/pull/20889)
  - advanced users, especially from academia keep asking about it
  - Related issue: https://github.com/numpy/numpy/issues/20871
  - Chuck will review the related PRs and issues


## New topics

- Arman: Inviting a NumPy maintainer / experienced contributor to host an in-person sprint at PyData Armenia 2024. Travel and accommodation will be covered by the conference.
  - Arman will follow up with Ralf via email and send his invitation via the NumPy mailing list.

- NumPy 2.0:
  - Chuck would like to prepare for branching
  - A few things are still open. The biggest points are:
    - Array API NEP (and maybe implementation)
    - Breaking dtype struct
    - Exposing new dtype API

- Inessa: removing links to the communication channels that are not actively monitored and moderated by the NumPy team. Refer to https://github.com/numpy/numpy.org/issues/700
  - Let's just remove them, Inessa will submit a PR.

- Lucas: What's the plan for `fft` API changes for 2.0? One of the changes is at [gh-25495](https://github.com/numpy/numpy/pull/25495). There's also adding `device` as a parameter to the array creation functions `(r)fftfreq`.

- Use SciPy's FFT implementation?
  - There are some subtle difference (but beyond float32 support maybe only slight precision changes due to what happens under the hood)
  - In general: of course, not much reason not to (for the C++ implementation) 

- Lucas: `numpy.array_api.linalg.cholesky` is still broken for `upper=True` - does this need to be fixed in `array-api-tests` first? [gh-24777](https://github.com/numpy/numpy/pull/24777) has a 5-line fix.

- mattip: Anyone know what happened to https://about.codecov.io/ ? The integrations still exists in numpy/numpy, but I haven't seen reports for quite a while. Does anyone remember who has login credentials?
  - The service is no longer free. We should explore alternatives. The reports are useful.

- mattip: C++/Highway draft NEP was merged: next steps?

- mattip: Redoing the [team page](https://numpy.org/teams/)
  - images are too large
  - should be formatted in more than one column
  - some names repeat
  - are the lists current?
  - The names are pulled from github. Matti will file an issue in the Hugo scientific-python theme about the rendering. 


## Action items


---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
