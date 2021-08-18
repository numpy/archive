# 2021-08-04 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Ryan, Raghuveer, Bas, Ralf, Inessa, Melissa, Matti, Sebastian, Ross, Aerik Pawson


## Follow-up from last meeting / discussions

* Survey status
  * 334 responses so far

* SVML addition - it's very large, how to review & deal with it?
  * Raghuveer made a PR to vendor SVML from intel (100+k lines of code) and almost 1MB in binary (12MiB currently, but before 30MiB).
  * Within NumPy or separate?
  * Intel specific (it will not give any advantage e.g. on AMD)
  * The function advertise 4 ULP error:
    * How much worse is the high precision (1 ULP)  (Chuck: comment on it)
    * Run this by the mailing list  (Sebastian)
  * Verification data is now a separate PR which is great
  * Vendor vs. submodule vs. something else?  (Ralf)



## Topics

- How to continue/settle the float-precision discussion?
  * The current responses seem pretty unspecific/unclear whether the high precision is just "desirable" or really needed for the use-case.
  * Testing against SciPy special to see how it affects them, may be interesting?
  * Trying the "low-accuracy mode", which seems to have pretty good accuracy
  * Add documentation?  Maybe not/difficult since 

* Git submodule vs. vendoring SVML?
  - lighter for the repository
  - requires an additional `git submodule init`
      - Lets try to create a clear error: "Run this command" if the submodule is not initialized
  - Lets try the submodule route, and vendor it if it turns out painful.
  - Create a copy in NumPy just in case the official repo moves, etc.

- Would it be useful to have a cross-project discussion forum/user forum?
  * Takes effort to monitor, etc. which may be hard for us
  * Putting the infrastructure in-place itself should be easy
  * If there is someone who wants to start it, we can link to it! (Get Hannah and Stéfan in touch
  * Jupyter had a contributor-in-residence, but not specifically for community management.

* Opinions on the `np.bit_count` addition?
  * General opinion: good addition, and uint8 seems a reasonable return value for a bit-count.



---

Please remember to archive this file and commit it to github.com/numpy/archive



