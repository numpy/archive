# 2022-04-27 NumPy community meeting


- Time: 6:00 pm UTC
- [Numpy community events calendar](https://scientific-python.org/calendars/numpy.ics)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Sebastian Berg, Ross Barnowski, Charles Harris, Matti Picus, Mars Lee, Dilia, Mike McCarty, Melissa Mendonça, Rohit Goswami


## Follow-up from last meeting / discussions

   
* Apparently the fix for one of the CVEs is missing for 1.22.2
https://github.com/numpy/numpy/issues/19038#issuecomment-1048886879
  * The database seems to list <=1.19.0 which is incorrect, but it does not say that 1.22.2 is still affected. It also has the "disputed" note. Sebastian will send an update request.


* Discussion about NEP 50 work.
  * Followup, work still in progress, there was some discussion about the size of the change on the NEP pull request.  (Sebastian plan is still to go ahead with a switch logic to actually figure out _how_ disrupting it is.) 
  * Branching is as close as ~6 weeks (grrrrr)
  * Technical work may likely be doable (Sebastian), but we have no progress on the bigger problem: Making pandas transition.  And it is hard to say how hard that is.  (And at least _slow_ to get downstream to test broadly, unless it is exceedingly easy...)
  * Better plan probably: Make a feature flag to opt-in to the new behaviour.  And plan for the *next* release to be 2.0 and adopt it.  This gives time for projects to follow-up, testing, and generally fixing up any problems.
    * Downside: Annoying logic for switching
    * Upside: lets be pragmatic on merging... Errors will be OK, since you will have to opt-in to it (and it is clearly "experimental")


## Topics

- [name=Melissa] Short discussion on the calendar ics (*Moved over from Inessa's notes on the last documentation team meeting*)
    - Moving away from Google Calendar
    - Syncing problems
        - Need to subsribe to URL link to sync calendar
        - Download, import from file does not sync and therefore is not recommended
    - Currently only the HackMD link is present
    - Pros --> Even if people don't register through the web they can visit the page and get updates
    - Cons --> Kinda confusing sometimes, needs an additional layer of indirection
    - Possibility: implement calendar widget
        - [Jupyter uses in-browser, Google Calendar widget to show all their events](https://jupyter.org/community#calendar)
        - However, this brings us back to an implicit Google / Outlook / Other dependency
    - We should check that different
    - Make clearer instructions for syncing calendar across different services (Google Calendar, Outlook), [similar to this example](https://scientific-python.org/calendars/)
    - As of now, should subscribe by url +1
    - *Action item:* Inessa will communicate this info via all the existing channels.


- NumPy 2.0 NEP?
  - We have the wiki page: https://github.com/numpy/numpy/wiki/Backwards-incompatible-ideas-for-a-major-release
  
    
- [name=Melissa] PyCon US’22
    - Select a few issues and add a “sprint” label to them
    - Mentored sprints April 30, regular developer sprints May 2-3
    - **Mentored sprints**
        - Saturday, April 30th, 8:00 pm to 12:00 am UTC. [on your timezone](https://www.timeanddate.com/worldclock/fixedtime.html?msg=PyCon+US+2022+mentored+sprints&iso=20220430T14&p1=220&ah=4.)
        - Please confirm your availability and the time slot preferred by [entering your name in this document](https://docs.google.com/spreadsheets/d/1FWamp-R1OBCkBFJccg7-K3BK0SAMMsc-Jb1DOc4itbs/edit?usp=sharing) You may choose to mentor for 2 hours only or stay for the entire sprint.

- For the sprints: Reviewing doc things is a bit tricky, because CI is currently problematic.

- Melissa will try to fix gitpod for the sprint.

- The 1.22 docs should be rebuild with the latest docs to fix the intersphinx builds (Chuck can look into that).



---
Please remember to archive this file and commit it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)


