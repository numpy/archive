# 2023-12-06 NumPy community meeting

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

**Present:** Inessa Pawson, Sayed Adel, Chuck Harris, Matti Picus, Mars Lee, Nathan Goldbaum, Meteusz Sokol, Stefan van der Walt

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-11-22.md_

- Review of [the NumPy 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)

- Community Review #3 of GSOD-NumPy project
    - You can comment either here on [Github](https://github.com/numpy/numpy/issues/25318) or on [the PDF viewer](https://drive.google.com/drive/folders/1Ie-oYAbWqBcuOuPVow379WYotaRa_I5K), whichever you prefer.
    - Both will be open for 2 weeks and close Dec 20.
    - I can also take comments during this call
    - Feedback from call:
        - Timeline:
            - Dec: Community Review #3, thumbnailing last 6 pages
            - Jan-Feb: 1 page a week
            - March-April: Last community review, uploading on numpy.org
        - Enjoying flow of story
        - How to link to issues, PRs in a comic?
            - List URL or QR code in PDF and print comic
            - Link will be clickable in numpy.org version
        - Sharing with family and friends
        - Interest from people in bioinformatics eg from Biotech without Borders, a community lab in NYC
    - Other updates
        - [Video of talk at PyData NYC 2023](https://youtu.be/Gv_Ea94wquM?si=drLkjdN_0A75Jshn&t=40) uploaded
        - [Case study](https://github.com/numpy/numpy/wiki/Google-Season-of-Docs-2023:-NumPy-case-study) submitted back to GSOD website
    - Next steps
        - Thumbnailing last 6 pages
        - Uploading comic to NumPy website, currently on heyzine
    - <a href="https://drive.google.com/file/d/1F1pLhpVNRuMnVdmZ50QmeDMCDT0rdTFo/view?usp=sharing"><img src="https://hackmd.io/_uploads/ryIHONKmp.png" width="400"></a>

- Array API PRs status updates:
    -  4 (out of 9) PRs merged this week
    - Easy way to check if object is a dtype scalar type? (https://github.com/numpy/numpy/pull/25054#discussion_r1415982589)

- Thoughts on new array conversion API (internal for now):
  * still looking into this, but got a bit distracted with other things (and the whole wrapping)

- Would it be OK to make NEP 50 the only default (can start cleaning up a lot, might unlock some options also)?
  - Let's do if it becomes a real problem.

- f2py changes/failures/backports
  - bunch up f2py changes (maybe even copy it in a single commit from main).
  - Next 1.26.x will be an "f2py" release.

- Supporting loongson[^loongarch] architecture (LSX)
  https://github.com/numpy/numpy/pull/25215
    - Has QEMU support since QEMU 7.1
    - Sayed is fine with adding it, as long as they support it. Others agree.
    - The optimization team should discuss the implications of adding a new architecture

- Building/developing docs:
    - Remove "Git for development" section?
    - Trimming down https://numpy.org/devdocs/dev/index.html (it looks quite poor and hard to navigate)
    - Adding a mostly 1:1 copy of http://scipy.github.io/devdocs/building/index.html
    - Inessa would be willing to work on this, should coordinate with Ralf

- Separating out `libnpymath`; also undoing the C++ addition there.
    
## New topics
- Inessa: NumFOCUS Infrastructure Committee is currently working on a proposal for the NF Board of Directors to request infrastructure resource allocations for 2024. What infrastructure needs would we like the Board to consider funding (or facilitating discounts for)?

- Nathan: How to implement `isdtype` [from the array API](https://data-apis.org/array-api/2022.12/API_specification/generated/array_api.isdtype.html)? Accepts scalar types - is there a global mapping from scalar types to dtypes, including even dtypes defined in downstream code? Is `issubclass(scalar_type, np.generic)` sufficient? See https://github.com/numpy/numpy/pull/25054.
  - Basically this is an ArrayAPI question, so (mattip suggests) the answer should be "is this an array-api recognized dtype" and document the behaviour

- Stefan / Inessa: updates on numpy.org
  - Unifying the Hugo theme with the sphinx theme. The pydata-sphinx-theme styling was adopted for the keyfeature boxes, URL links, some coloring, headings sizes, and tabbed interfaces.

  - The reasoning behind this decision is that pydata-sphinx-theme is already widely-used by the SciPy community, has a larger pool of maintainers, and has many accessibility improvements (the latter is supported by the funding from CZI to QS Labs).

  - There will always be differences between numpy.org and the websites that fully rely on pydata-sphinx-theme due to the differences between the themes.

- Inessa: NumPy sprints schedule for 2024
  - Brigitta is interested to host Grace Hopper OSD 2024. Inessa could help.
  - Inessa will ask on #sprint-mentors if anyone is interested to host sprints in 2024

- Inessa: moving the deadline for numpy 2.0
  - move 2.0 to Feb 1, 2024
  - could also release 1.27 to push 2.0 even further but really don't want to do that.
  - regular timeline: 6 weeks from .rc to a public release


## Action items

- **LoongArch** is a new RISC ISA, which is a bit like MIPS or RISC-V. There are currently 3 variants: a reduced 32-bit version (LA32R), a standard 32-bit version (LA32S) and a 64-bit version (LA64). There are 4 privilege levels (PLVs) defined in LoongArch: PLV0~PLV3, from high to low. Kernel runs at PLV0 while applications run at PLV3. This document introduces the registers, basic instruction set, virtual memory and some other topics of LoongArch. — https://www.kernel.org/doc/html/v6.4-rc7/loongarch/introduction.html

---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
