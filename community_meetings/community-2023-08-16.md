# 2023-08-16 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Mars, Ralf, Chuck, Tyler, Matti, Ross, Sayed, Raghuveer, Ankur, Ganesh, Mateusz, Inessa


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-08-02.md_


- Meson module and NumPy work is in the final stages.
  - We are shipping a NumPy version of meson that does the SIMD discovery. It has been merged for 1.26. Thanks to Sayed and Ralf, this was a signinficant effort!
  
- Highway NEP is in the works. Google Highway has chaned its license and Matti should review the [PR](https://github.com/numpy/numpy/pull/24138) so we can merge a first version
  - A number of concerns: dispatch/discovery, c/c++ transition, actual kernels.
  - We should resolve the discussions and additionally ask Jan and Sayed to add their opinions, and merge the NEP soon.

- The Optimization Team (SIMD) had its first meeting
  - Start with using the #simd Slack channel.
  - Next meeting is Aug 28.
  - See https://hackmd.io/dVdSlQ0TThWkOk0OkmGsmw?view



## New Topics
- Community Review #2 for GSOD-NumPy 2023
    - **The script can be viewed here, as a [Google Doc](https://docs.google.com/document/d/1fjLTDqSkcKMxo8oSTRThllBFpjo5rXS9/edit?usp=sharing&ouid=110556856523158639329&rtpof=true&sd=true)**. You can comment either here on [Github](https://github.com/numpy/numpy/issues/24382) or on the Google Doc, whichever you prefer.
    - Both will be open for 2 weeks and close **Aug 23**.
    - For review, you can comment on any part, whether you like the idea of the comics, don't like a specific line or not sure what something means.
    - Themes: **NumPy is made by the people who use it: scientists**! Thus a group of grad students learn how to contribute to NumPy by creating an issue for a usability problem. By talking to community members, a PR is made to change the .npz file beheavior.
    - Some specific parts I would like feedback on:
        - **Themes**
          - [On Page 5, ](https://docs.google.com/document/d/1fjLTDqSkcKMxo8oSTRThllBFpjo5rXS9/edit?disco=AAAA3sVZK9Y)does this panel accurately show the tie between open source and open science?
        - **Story and Pacing**
          - Does this seem like a reasonable amount of content to cover in 16 pages?
          - Do the three students interacting together feel realistic?
            - eg Since they're beginners, they don't at answer immediately
            - eg not too mean-spirited? They argue, to show different approaches
        - **Accuracy**
          - [On Page 3](https://docs.google.com/document/d/1fjLTDqSkcKMxo8oSTRThllBFpjo5rXS9/edit?disco=AAAA3sVZK9c), how accurate is the .npz code?
          - [On Page 7](https://docs.google.com/document/d/1fjLTDqSkcKMxo8oSTRThllBFpjo5rXS9/edit?disco=AAAA3sVZK9k), does the visual metaphor of the NumPy issue tracker as a bulletin board make sense?
  - Feedback from the crowd: quite positive, folks are happy, the story flows well, and the scope is right.
  - Ross will have a much closer look again soon.
  - Can it be part of the docs page?
      - Depends on size of images. Probably circle back after completion


- CI restructure and moving all jobs over to Meson (https://github.com/numpy/numpy/issues/24410)
  - Cirrus CI changes: starting to pay for some compute credits? (see https://cirrus-ci.org/blog/2023/07/17/limiting-free-usage-of-cirrus-ci/ and https://github.com/numpy/numpy/issues/24280)
  - The approach is in general to pay $100-$200 for their service.
  
- Follow up on leftover items for `bitwise_count` UFunc (added by Ganesh): https://github.com/numpy/numpy/pull/21429#
  * Sayed: SIMD optimization can be seamlessly applied by relocating the implementation of bitwise_count to [loops_autovec.dispatch.c.src](https://github.com/numpy/numpy/blob/main/numpy/core/src/umath/loops_autovec.dispatch.c.src)

- [name=rossbar] NEP51 fallout with doctests - is `np.printoptions(legacy)` a viable recommendation?
  - Downstream issue for reference: https://github.com/networkx/networkx/issues/6846
  - Ross will file an issue



## Action Items



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: Please enquire in a meeting or by mail.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
