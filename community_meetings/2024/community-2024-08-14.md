---
title: NumPy community meeting
tags: [NumPy]

---

# 2024-08-14 NumPy community meeting

- Time: 18:00 (6:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Ralf Gommers, Matti Picus, Nathan Goldbaum, Tammy Lawson, Chuck Harris, Brigitta Sipocz, Tyler Reddy, Inessa Pawson

## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit:_ https://github.com/numpy/archive/tree/main/community_meetings 

- NumPy 2.1 release: Chuck has released 2.1.0rc1
    - OpenBLAS version for 2.1.0 final? -> yes, 3.27 + reduced number of kernels is in the `2.1.x` branch already.
    - Do we need to worry about `oldest-supported-numpy`: nope.
    - Release date? Ideally a week after rc1, unless problems get reported. It will help to get 2.1.0 out, because downstream needs it to release for Python 3.13 in time.
    - Up to 51 wheels + 1 sdist now ... it's getting heavier.


## New topics

- Lots of typing PRs. Is this critical for 2.1 (probably not). How can we get more people to help out with this?

- In case anyone wants to play around with `pixi` + `numpy` development: https://github.com/rgommers/pixi-dev-scipystack (content warnings: (1) it's changing daily, (2) it's addictive so be warned)


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
