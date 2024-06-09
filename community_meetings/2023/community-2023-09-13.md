# 2023-09-13 NumPy community meeting

- Time: 5:00pm UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.


**Present:** Ralf, Matti, Chuck, Tyler, Raghuveer, Mars, Mateusz, Stefan, Nathan, Sayed, Ross, Brigitta


## Follow-up from the last meeting / discussions

_For the notes from the previous meeting, visit: https://github.com/numpy/archive/blob/main/community_meetings/community-2023-08-30.md_

- Short update on GSOD-NumPy 2023
    - Illustration stage: next Community Review #3 to come soon

- Follow up on leftover items for `bitwise_count` UFunc (added by Ganesh): https://github.com/numpy/numpy/pull/21429#
  * Sayed: SIMD optimization can be seamlessly applied by relocating the implementation of bitwise_count to [loops_autovec.dispatch.c.src](https://github.com/numpy/numpy/blob/main/numpy/core/src/umath/loops_autovec.dispatch.c.src)
  * Sayed has an update working that uses autovectorization, he'll push it to the PR.

- Inessa's CZI grant supporting her role as NumPy Contributor Experience Lead is ending on September 1st.
    - Australasia newcomers events could be good to keep going.
    - Video from presentation at SciPy US'23: https://youtu.be/uytmM0ulG6E?si=zoR2vXG0QiTpDujz
    - A report covering grant activities and outcomes will be ready in October.
    - We'd like to figure out later what activities that were grant-supported for the past two years to keep going and support as a team on a volunteer basis (or look for new funding for).

- Standalone benchmark script (https://github.com/numpy/numpy/pull/15987): it's useful for work on SIMD, but hard to integrate with `asv`. So we can merge it in its current form under `tools/`. But it is tricky since we need a c-extension module to get the inner loop.

## New Topics

- Ralf is working on moving pyodide to meson, still depends on distutils/setup.py
	- [pyodide/pyodide#4125](https://github.com/pyodide/pyodide/pull/4125)
	- [Further preliminary work](https://github.com/pyodide/pyodide/compare/main...rgommers:pyodide:update-numpy-meson?expand=1)

- Starting to make ABI breaks
  - mumble something about memory allocation tracking deprecation: we can remove the older allocation tracking interfaces.
  - there is some header cleanup we could do to move us closer to the limited API. There are some non-limited API uses in the public headers, and these should be hidden so that cython users can do `cimport numpy` with the limited API.

- Timing to remove `setup.py` files ([gh-24519](https://github.com/numpy/numpy/pull/24519))
	- Will have to disable Pyodide build, probably another month of work left on that (including work on pyodide itself)
	- Build using setup.py is OK today, but will rapidly degrade
	- Can we support all OpenBLAS configs?
		- No fundamental blocking issues / missing features.
	  - Missing checks for 2 known broken OpenBLAS versions, but mechanism is now available.
  - Everyone seems happy to remove `setup.py` files now.
    - Matti has OpenBLAS wheel; working to make it work with build.


- Numpy 2.0 API migration continues
    - `core` to `_core` rename
    - sctypesdict complaint from jax (https://github.com/numpy/numpy/pull/24376#issuecomment-1717908075)
    	- skimage did a [hacky workaround](https://github.com/scikit-image/scikit-image/pull/7122/files#diff-78d999eb449844b07ca2761ffc82275ec9b5eeb484913498f818ef4b2362c68bR28) for `sctype2char` disappearing; still have to investigate proper solution. Would be helpful to have migration messages to guide users on how to make such replacements.
    - recarray repr?

## Action Items



---

### Let's connect and keep the conversation going!
Join the NumPy contributor community **Slack workspace**: Please enquire in a meeting or by mail.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **Twitter**: [@numpy_team](https://twitter.com/numpy_team)

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
