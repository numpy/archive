---
tags: NumPy
---


# 2021-05-12 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Ralf, Bas, Sebastian, Chuck, Matti, Melissa, Ryan, Ross, Mars, Serge


## Follow-up from last meeting / discussions



## Topics

- WiMLDS Was a success :tada:


- The state of issues in our issue tracker
  - Can we write up better actionable issues for people looking for working on something impactful?
      - New features
      - What functions to add SIMD acceleration to
      - Systematic testing of classes of functions for empty/nan/inf, discontiguous arrays, etc.
      - ...

- Custom allocator: which approach should we take?
  - simple struct that holds the functions
  - simple struct that holds the functions and a void * ctx
  - PyObject
  - FromSpec


- Add `dtype.__class_getitem__`?
 
    *  Challenge: create something that is usable for static type checking as well runtime (_e.g._ for grabbing `dtype` subclasses).
    *  See [numpy/numpy#18935](https://github.com/numpy/numpy/pull/18935#issuecomment-834517359) for some prior discussion.
    *  Do we want examples such as these to work:
    `DTypeSeq = Sequence[np.dtype[T]]`
    `seq: DTypeSeq[np.int64] = ...`

- Quick Update: NumPy Docs Front Page Redesign: [Interactive Prototype](https://design.penpot.app/#/view/41890b30-934c-11eb-825c-a56ecc9e3fc1/e1ce3fc0-934c-11eb-bc52-e39ba1f3ae20?token=P8-a3msKJ73tEDHtfpC3Sg&index=0)
    - [Github issue](https://github.com/numpy/numpy/issues/18419#issuecomment-840078589)
    - This prototype exists as a low-cost, quick and iterative overview of how several pages could look and 'feel' together.
    - There is no direct 'translation' from prototype to code. Implementation will be through the current Sphinx theme
    - You can leave comments on Github instead of on Penpot (the prototyping platform)
    - If you have a suggestion, if possible, put in your experience as context. For example- 'As an experienced NumPy user, I would like to quickly reach the Reference. Could we put a link to the Reference in the left navigation bar?'
        - In UI/UX terms, this is a 'user profile' or 'user story'
    - The prototype looks great, Ross can look into starting a PR for it.

- Chuck release the next 1.20.3 :tada:

- GSoD deadline is close, the final decision is due on monday. Melissa is on top of it with Ross giving a hand.


---

Please remember to archive this file and commit it to github.com/numpy/archive
