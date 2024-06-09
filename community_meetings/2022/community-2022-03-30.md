# 2022-03-30 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/numpy.ics)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Rohit, Ralf, Sebastian, Chuck, Bhavuk Kalra, Jake VanderVaate, Mars, Ross


## Follow-up from last meeting / discussions

   
* Apparently the fix for one of the CVEs is missing for 1.22.2
https://github.com/numpy/numpy/issues/19038#issuecomment-1048886879
  * The database seems to list <=1.19.0 which is incorrect, but it does not say that 1.22.2 is still affected. It also has the "disputed" note. Sebastian will send an update request.


* [name=Sebastian] Approach for [scalar math](https://github.com/numpy/numpy/pull/21188)?


## Topics

* Discussion about NEP 50 work.
  * Branching is as close as ~6 weeks (grrrrr)
  * Technical work may likely be doable (Sebastian), but we have no progress on the bigger problem: Making pandas transition.  And it is hard to say how hard that is.  (And at least _slow_ to get downstream to test broadly, unless it is exceedingly easy...)
  * Better plan probably: Make a feature flag to opt-in to the new behaviour.  And plan for the *next* release to be 2.0 and adopt it.  This gives time for projects to follow-up, testing, and generally fixing up any problems.
    * Downside: Annoying logic for switching
    * Upside: lets be pragmatic on merging... Errors will be OK, since you will have to opt-in to it (and it is clearly "experimental")


* [name=Inessa Pawson] Revisiting the policy: https://docs.google.com/document/d/1k6mwWjgTMlQ-ykt1phTBRKhDMRDoHa_IwLD2IwMB1NA/edit?usp=sharing
Replace *“abandoned”* for *“inactive”* to avoid giving a negative connotation to the work by the contributors who decided to step down from the project. 
    - (Ralf) LGTM with the change


* [name=Inessa Pawson] PyCon US 2022 – NumPy sprint (mentored or development?)

Date of the mentored sprints: Sat, April 30, 2022
For more info: https://us.pycon.org/2022/events/mentored-sprints/
We will need to provide 3-4 mentors.
- I'd be happy to help (Rohit)
- Chuck may be physically present, but not mentoring
- Sebastian: Not sure I will have time, but probably can give a hand.

Date of the development sprints: Mon, May 2 and Tuesday May 3, 2022
For more info: https://us.pycon.org/2022/events/development-sprints/
- Sebastian: Will go if we do it
- Will also show up if it happens (Rohit)

* [name=Inessa Pawson] NumPy Newcomers’ Hour – April 7th, 2022 at 4 pm UTC
Presenter: Mars Lee
Topic: Making NumPy accessible with community workshops: how we can involve more people with disabilities in data science.

* [name=Melissa] Contributor interviews for NumFOCUS CDR project
  - The website https://www.mdanalysis.org/2022/03/02/NF-CDR-Interview-Call/ asks for whether anyone is interested in potential 30 minutes interviews.


* [name=Rohit Goswami] Suggestion: recording public NumPy meetings
    * We can upload them to the YouTube channel
    * Useful for archival purposes
    * Also done by other communities, e.g. [Fortran-Lang](https://www.youtube.com/channel/UCTYRAlVmMCGGcrMkKxQLurw) ([sample announcement](https://fortran-lang.discourse.group/t/fortran-monthly-call-february-2022/2717))
Meeting discussion summary: Not clear that it would help much, what's more it may change the nature of meetings. We do have the archive.

* CI timeouts and general flakeyness e.g. [timeout on azure](https://dev.azure.com/numpy/numpy/_build/results?buildId=23388&view=results) and on [Travis](https://app.travis-ci.com/github/numpy/numpy/jobs/565149162)?
    * Policy needed for merging PRs which don't turn green?
[name=Rohit]
    * We should probably should just bump the timeout.

* [name=Ralf] tracking whether an array has a view on it? (conceptual discussion)



---
**IMPORTANT** The NumPy community Google calendar will be deprecated on June 1st, 2022. Please subscribe to https://scientific-python.org/calendars/numpy.ics to keep track of all NumPy community events.

---
Please remember to archive this file and commit it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


