---
tags: NumPy
---


# 2021-03-17 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Inessa, Sebastian, Ross, Ralf, Ryan, Melissa, Mars, Chuck, Matti


## Follow-up from last meeting / discussions

- GSoD'21
  - [Project ideas](https://github.com/numpy/numpy/wiki/Google-Season-of-Docs-2021-Project-Ideas)
  - March 26th deadline


## Topics

* GSoC students interested in SciPy and look promising

- Brief pythran discussion: interesting, but probably no in NumPy.

- Strategy for reviewing/merging `numpy.array_api` (NEP 47) namespace
  - This will be tried on a "SciPy PR" (e.g., `scipy.stats.qmc`), when that runs smoothly, we can probably merge things into NumPy (as hidden API) for further testing.
  - This will not be in 1.21.x; for 1.22.x the goal is to get it stableand public.

* Can we expose an "experimental C-API"?
  - We will create a header file that uses a private `np.core._get_new_casting_api` 
  - What would the first use case be? `bfloat16`? `uint8_warn_on_overflow`?

- [YouTube Brand account has been created](https://www.youtube.com/channel/UCguIL9NZ7ybWK5WQ53qbHng) - who will be administrators?

- Next step for fundable projects
    - Ralf is going to set up a wiki page to gather ideas (around 5 each with someone willing to support it an estimate of how involved).

- CZI proposal(s): Next round letter of intent are due soon.

- For diversity: maybe think about interacting with free-code-camp? https://www.freecodecamp.org/news/search/?query=numpy





---

Please remember to archive this file and commit it to github.com/numpy/archive

