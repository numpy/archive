---
tags: NumPy
---
# 2023-05-24 NumPy community meeting


- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://us06web.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://us06web.zoom.us/u/kbGQI0hHSd)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** May Ireland, Ralf Gommers, Chuck Harris, Sebastian Berg, Ross Barnowski, Sayed Adel, Mars Lee



## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-05-10.md_

- Now at Outlining stage for GSOD-NumPy 2023 (May 15-26)
    - Completed Gathering community input stage and 3 brainstorming sesions
        - At Newcomer (May 4) NumPy Docs (May 8), Commmunity (May 10)
        - [Link to Google Jamboard](https://jamboard.google.com/d/1j_rEIslOh59N9cLGU1VGc7rTc88SuLTi7l4YqTqAULc/edit?usp=sharing)
    - [Summary from Brainstorming Sessions](https://github.com/MarsBarLee/gsod-numpy-2023/blob/main/outlining/summary-from-brainstorming-sessions.md)
    - Next steps
        - Narrow down [User Personas](https://github.com/MarsBarLee/gsod-numpy-2023/blob/main/outlining/user-persona-contributor-pathways.md)
        - Draw [Concept Art Prompts](https://github.com/MarsBarLee/gsod-numpy-2023/blob/main/outlining/concept-art.md)
    - Had [conversation in NumPy Docs](https://github.com/numpy/archive/blob/main/docs_team_meetings/docs-2023-05-22.md), this is the written update for the NumPy Community meeting
        - Main discussion points from NumPy Docs meeting
            - Metaphor should not make core topic (contributor workflow) make more complicated
            - Reviews stage open for 2 weeks (late May-early June)
            - Letting go making full ‘comic book style’
    - Talked about overlap (formalizing contributor workflows) with group and May Ireland

- Inessa: Presentation by May Ireland, DEI consultant on the CZI DEI grant, at the PyConUS’23 Maintainers Summit on her findings from the discovery stage of developing a DEI action plan for four CZI-funded projects (NumPy, SciPy, Matplotlib, and pandas): https://www.youtube.com/watch?v=nno7B6jI0wY

- Inessa: DEI report by May Ireland: https://contributor-experience.org/docs/posts/dei-report/
Members of the broader open source and open science communities are invited to participate in a series of the Culture Labs to discuss and actively work on improving communication, conflict mediation, and creating a culture of belonging in our communities.
If you are interested, join us on Zulip: https://contributor-experience.zulipchat.com/join/ckihfnw42e25xsfevmzdv5sc/


## New Topics

- May Ireland: DEI report & next steps
    - May shared some context around [this blog post and report](https://contributor-experience.org/docs/posts/dei-report/)
    - The audience likes the report!
    - Question on how May sees differences between projects, and what we can learn from other similar open source projects. 
    - Different perspectives on how community evolves. 
    - Who and How people spend volunteer time
    - Role formalization without constricting

- Ralf Gommers: Release schedule, Meson progress & Python 3.12 support

- Ralf Gommers: Platform support status, and 32-bit Windows in particular (see [gh-23717](https://github.com/numpy/numpy/issues/23717))



- Sayed Adel: Next move towards C++ support, there's a lot of SIMD work depending on it.
    - Two choices: SVE support from C++ (will require C++ ufuncs), or add sizeless support in universal SIMD.
        - option 2: https://github.com/numpy/numpy/pull/22265
        - option 1 (preferred by Sayed):
            - https://github.com/numpy/numpy/pull/21057
            - https://github.com/numpy/numpy/pull/19753
    - Either way it does/should not affect anyone externally.
    - Internal vs. external signatures will diverge more if internal is in C++ and external in C.
    - Inner loops for custom dtypes will still be able to be written in C, like now (so no backwards compatibility breaks for C API users).
    - NEP: C++ support in the ufunc machinery.
    - Sayed will write a summary of why the ufunc machinery needs C++ parts going forward. After that is done, we'll judge if it needs to be a full NEP (Ralf agrees to help writing if needed).
    - C++17 version is much better and lower-complexity than the older implementation that Sayed had.

- Chuck Harris: Can we merge the open NEP drafts please? -> yes, Sebastian will have a look




## Action Items





---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: https://join.slack.com/t/numpy-team/shared_invite/zt-1gokbq56s-bvEpo10Ef7aHbVtVFeZv2w

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
