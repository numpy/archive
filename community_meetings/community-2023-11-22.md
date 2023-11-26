# 2023-11-22 NumPy community meeting

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

**Present:** Ralf, Sebastian, Stefan, Sayed, Steven Kell, Chuck, Rohit Goswami

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-11-08.md_


- Reviewing 2.0 board (as a recurring thing)
   - Updating [the 2.0 project board](https://github.com/orgs/numpy/projects/9/views/1)

- Completed giving talk about NumPy at PyData NYC conference
    - Talk title: Comics in NumPy? More Likely Than you Think!
    - Digital comic: https://heyzine.com/flip-book/3e66a13901.html
    - Recording will be uploaded in a few weeks at PyData's Youtube channel, will share when ready
    - Krita source files, printable PDF and talk slides in the [repository](https://github.com/MarsBarLee/gsod-numpy-2023/tree/main/source-files)
    - Next steps
        - Review with Mukulika, one of the project mentors
        - Community Review #3 of 10/16 pages so far
        - Uploading comic to NumPy website, currently on heyzine
        - Completion of last 6 pages
    - <img src="https://hackmd.io/_uploads/ryIHONKmp.png" width="400">


- Array API changes PRs open


- Cyclic garbage collection?
  - The hook used for it, would also be useful for string allocation management.

- Dropping Python 3.10:
  - Not yet, there is probably little gain anyway.


- Thoughts on new array conversion API (guessing internal for now):
  * still looking into this, but got a bit distracted with other things (and the whole wrapping)


## New topics

- Discussion about array API PRs:
  - `np.bool` and testing one should.
> [] ?
testing one should  - Let's add to the NEP that we move out `numpy.array_api` into its own package/repo. Especially if the main namespace is already compliant, there isn't much of a reason to have the separate namespace inside numpy.

- Would it be OK to make NEP 50 the only default (can start cleaning up a lot, might unlock some options also)?
  - Let's do if it becomes a real problem.

- f2py changes/failures/backports
  - bunch up f2py changes (maybe even copy it in a single commit from main).
  - Next 1.26.x will be an "f2py" release.

- Merge Highway Quick-sort pr https://github.com/numpy/numpy/pull/24018
    - Yes, all good. Let's go ahead with the merge, this supports Highway's high-level kernels.

- Supporting loongson[^loongarch] architecture (LSX)
  https://github.com/numpy/numpy/pull/25215
    - Has QEMU support since QEMU 7.1
    - Sayed is fine with adding it, as long as they support it. Others agree.

- Removing `PyArray_GetCastFunc`
  - PR: https://github.com/numpy/numpy/pull/25161

- Building/developing docs:
    - Remove "Git for development" section?
    - Trimming down https://numpy.org/devdocs/dev/index.html (it looks quite poor and hard to navigate)
    - Adding a mostly 1:1 copy of http://scipy.github.io/devdocs/building/index.html 

- Separating out `libnpymath`; also undoing the C++ addition there.
    
- dealing with git submodules:
    - `git config --global submodule.recurse true`
    - parallel fetch: `git config --global fetch.parallel 0`

https://github.com/numpy/numpy/pull/15457
- Really old but useful F2PY PR :)

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
