---
tags: NumPy
---


# 2021-02-17 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Inessa, Melissa, Stéfan, Chuck, Matti, Bas, Ralf, Ross, Ryan


## Follow-up from last meeting / discussions

- GSoC'21: 175 hrs (half the lenght of before), deadline 19 Feb. Do we want to participate?
  - Maybe we could mentor SciPy projects?
  - Over at NetworkX they have a section of the dev docs that are for projects. They should be ~175 hours and have the name of a mentor.
    * https://networkx.org/documentation/latest/developer/projects.html
    * To help mentor on SciPy projects (more approachable for students): https://github.com/scipy/scipy/wiki/GSoC-2021-project-ideas
    * We are considering extending that list of projects beyond just GSoC, and invite people from underrepresented backgrounds to apply (e.g., recent bootcamp graduates)


- Fundraising
    - https://opencollective.com/numpy
    - An example of what is possible: https://opencollective.com/webpack + [Webpack lead community developer interview](https://www.youtube.com/watch?v=AEtg5KYO22c)

- GSoD'21: we need an opencollective account and project ideas. Deadline for organizations to apply is March 26


## Topics

- proposed `atleast_nd` addition

- namespace reorganization?
    - Useful modules: fft, linalg, random, polynomial
    - We do have the `.lib.x` namespace, where we can be more liberal with adding new functions, as long as they do not bleed into the main namespace (by use of `__all__`)
   - Sebastian volunteers to add a `np.__getattr__` thingy so we can "hide" outdated functionality so it doesn't show up for tab completion.

- Pick up the ["configurable allocator"](https://github.com/numpy/numpy/pull/17582)  (what is needed there?)
    - Needs a small NEP

- `numpy.typing` and Transonic/Pythran/Cython
    - Possible standalone project: create the right `Protocol`s that we'd like people to use for new library code, e.g. an NDArray protocol and a DType protocol.




---

Please remember to archive this file and commit it to github.com/numpy/archive

