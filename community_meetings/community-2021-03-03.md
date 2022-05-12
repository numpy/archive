---
tags: NumPy
---


# 2021-03-03 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 12:00 Pacific Time (20:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)

**Present:** Charles Harris, Melissa Mendonça, Ralf Gommers, Inessa Pawson, Ross Barnowski, Matti Picus, Ryan Cooper


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
    - [Draft for project ideas](https://hackmd.io/@melissawm/rkRhYd5zu)
    - Melissa will move to wiki next week, start publicizing
    - The point about gathering external documents should be removed; we can think about a "minimum set of documents" that should be maintained 


## Topics

- Did the "ABI" change actually cause cython issues? https://github.com/numpy/numpy/pull/16938
  - (mattip) No but... We should have more "best practices" guidance for `oldest-supported-numpy`: where can we publish this information? --> https://numpy.org/devdocs/user/depending_on_numpy.html

- Spending funds NEP (https://github.com/numpy/numpy/pull/18454), are people generally happy with the shape of that and starting to think about some concrete ways of defining fundable projects/activities?
  - Accessibility might be an area we could fund
  
- NumPy sprint with WiMLDS
    - May 8th, 2021 is a proposed date. May 9th is better for the NumPy team.
    - Setup for the sprint: 
*     - WiMLDS Berlin is suggesting a meetup prior to the main event to help participants set up correctly.
*     - Creating virtual machines would be best for a virtual sprint.
    - Duration of the sprint: 4 hours might be enough. 
    - Due to a noticeable time zone difference with North America (e.g., 9 hours with CA), perhaps, it would be best for mentors to work in shifts.
    - Identify issues for the sprint. Melissa already has a list. 

- EOSS Diversity and Inclusion Grants RFA
    - Applications due March 30th
    - Multi-project ideas are welcome




---

Please remember to archive this file and commit it to github.com/numpy/archive

