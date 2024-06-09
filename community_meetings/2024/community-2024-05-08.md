# 2024-05-08 NumPy community meeting

- Time: 7:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Sebastian Berg, Nathan Goldbaum, Ben Woodruff, Tyler Reddy, Brigitta Sipocz, Chuck Harris, Inessa Pawson, Mars Lee, Raghuveer Devulapalli, Ross Barnowski

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/tree/main/community_meetings

- (after rc1 and maybe rc2) How to announce 2.0?
  - Blog post on scientific python (probably)
  - Slightly longer news article on numpy.org
  - Not in a hurry, final release is a while away.
  - Can also add a short snippet into the project readme "on github".

- Release date: we are mainly waiting for other packages to release for compatibility. 
    - Let's do an RC2 in 1-2 weeks, after OpenBLAS 0.3.27 can be included (Matti is herding CI here at the moment)
    - Final release unlikely to be feasible before the second half of May; even that is optimistic.

- Next month there is a deadline for the NASA ROSES grant. Ralf will be sending out a proposal to the steering committee for a renewal of the grant.
    - Better is finally setting up the mailing list for all maintainers, and sending the request for input there.


## New topics

- NumPy accepted for 2024 Google Season of Docs
  - Work continuing and shared on May 6 Docs meeting

- [name=seberg] If anyone has comments on can-cast in `copyto` on scalars, that would be nice (but I don't really want to discuss it long, it needs thinking or just voicing opinion/expectations).
  - python float to float32? safe?)
  - python int to int8 safe?  What if it is 1000?
  - At least for copyto integer value-based makes most sense
  - For floats: Probably just call it safe, even if it isn't...


- Dropping Python 3.9 Discussion
  - [name=seberg] While there is a point with the `pip install` pain, the opposite of trickier builds seems also a potential issue to me now.  So I lean towards just sticking with what we have and supporting it.


- NumPy at PyConUS
    - [name=Mars] Giving a talk "Paint by Numbers: A Retrospective on the “NumPy Comics” and Under-Represented Skillsets in Documentation" at the Documentation Summit, May 19
    - Submit a sprint? Here's a description
        - "NumPy is a Python library widely used in science and engineering for numerical data manipulation. How then, are comic related? The "How to Contribute To NumPy" comics follows riveting story of three grad students as they learn not only how to use NumPy in their research, but also the emotional ups and downs!
        - Join us in making comics! Take a copy of the NumPy comics and give feedback. Take the challenge and try making your own comics for your open source projects! Bounce off story ideas, sketch, write a script. Pens, paper, and other tactile tools will be provided."
        - Could also point to sprintable issues list or resources such as [Contributing to numpy/numpy 101](https://hackmd.io/@inessapawson/B1wDQ-hxC?utm_source=preview-mode&utm_medium=rec)
        - Mars has given a sprint before, at SciPy 2022
        - Possible challenges: people coming to sprint expecting typical sprintable issues, which Mars does not have experience with
            - Solution: Mars can point to NumPy Slack
        - Clearly communicate that sprint is about graphic design and scientific communication


- Vendoring a small library for `PyMutex` on Python 3.13?



## Action items



---

### Let's connect and keep the conversation going!
Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **X**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
