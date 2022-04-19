# 2022-04-13 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/numpy.ics)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Ralf Gommers, Inessa Pawson, Rohit Goswami, Mars Lee, Rajasekaran Karunanithi, Matti Picus, Ross Barnowski, Charles Harris, Yashi (Yashasvi), Alex de Siqueira, Bhavuk Kalra


## Follow-up from last meeting / discussions

   
* Apparently the fix for one of the CVEs is missing for 1.22.2
https://github.com/numpy/numpy/issues/19038#issuecomment-1048886879
  * The database seems to list <=1.19.0 which is incorrect, but it does not say that 1.22.2 is still affected. It also has the "disputed" note. Sebastian will send an update request.


* Discussion about NEP 50 work.
  * Branching is as close as ~6 weeks (grrrrr)
  * Technical work may likely be doable (Sebastian), but we have no progress on the bigger problem: Making pandas transition.  And it is hard to say how hard that is.  (And at least _slow_ to get downstream to test broadly, unless it is exceedingly easy...)
  * Better plan probably: Make a feature flag to opt-in to the new behaviour.  And plan for the *next* release to be 2.0 and adopt it.  This gives time for projects to follow-up, testing, and generally fixing up any problems.
    * Downside: Annoying logic for switching
    * Upside: lets be pragmatic on merging... Errors will be OK, since you will have to opt-in to it (and it is clearly "experimental")
    
* [name=Melissa] Contributor interviews for NumFOCUS CDR project
  - For more info: https://numpy.org/news/
  - We discussed this at the April 13th meeting.
  - Mars was interviewed today for this project.

* [name=Inessa Pawson] April 7th NumPy Newcomers’ Hour
Presenter: Mars Lee
Topic: Making NumPy accessible with community workshops: how we can involve more people with disabilities in data science.
A video recording is available on the NumPy YouTube channel: https://youtu.be/jI4pax8HX6c


## Topics

* NumPy 1.21.6 is released
Details will be discussed at the next triage meeting on April 20th.

* [name=Rohit] What's the long-term plan w.r.t. `dev.py` work going on over [at SciPy](https://github.com/scipy/scipy/pull/15959)?
    * [name=Ralf] Eventually, we'd like to reunify the two, say maybe in 9 months
* [name=Chuck] What about moving to markdown?
    * Probably not for a while, since its by construction less expressive than ReST (maybe MYST someday?)
* [name=Chuck] What about `meson`?
    * --> NASA grant has support
    * Maybe eventually with the right person
* [name=Ralf] NASA grant, short update:
    - Paperwork was just finalized. Submitted in Jan 2021; NASA notification of award in Aug/Sep 2021.
    - An announcement and blog post are coming.

- [name=Ralf] Numba compatibility: see https://github.com/numpy/numpy/issues/13718
    - Matti: one thing we could do is a Numba CI run perhaps (or the opposite).
    - Let's revisit this once there's a plan. It'd be great to get that wish list from the Numba team, or pings if we merged something in `main` which breaks something for Numba.





---
**IMPORTANT** The NumPy community Google calendar will be deprecated on June 1st, 2022. Please subscribe to https://scientific-python.org/calendars/numpy.ics to keep track of all NumPy community events.

---
Please remember to archive this file and commit it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


