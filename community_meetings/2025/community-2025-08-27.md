---
title: NumPy community meeting
tags: [NumPy]

---

# 2025-08-27 NumPy community meeting

- Time: 17:00 (5:00 pm) UTC
- [NumPy community events calendar](https://scientific-python.org/calendars/)
- Join via Zoom at https://numfocus-org.zoom.us/j/83278611437?pwd=ekhoLzlHRjdWc0NOY2FQM0NPemdkZz09 (To dial in, find your local number: https://numfocus-org.zoom.us/u/kekDGNWmRa.)
- [Community meetings notes archive](https://github.com/numpy/archive/tree/main/community_meetings)
- [Triage meetings notes archive](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings notes archive](https://github.com/numpy/archive/tree/main/docs_team_meetings)

**Code of Conduct**
The NumPy Steering Council has made a strong commitment to creating an open, inclusive, and positive community. 
All attendees of NumPy community events must adhere to the NumPy Code of Conduct (https://numpy.org/code-of-conduct/). 
If you see violations, take a screenshot, intervene in a respectful manner, and report it to the CoC Committee via email. For more information, refer to the Reporting Guidelines section on https://numpy.org/code-of-conduct/.

**Present:** Matti, Chuck, Nathan, Joren, Sam Morley, Amelia Thurdekoos, Melissa, Tyler, Sebastian, Maanas, Britney Whittington


## Follow-up from the last meeting / discussions

- Sebastian: Discussion about [sort PR](https://github.com/numpy/numpy/pull/28516)
  - Discussion about python API, C-API and lower level struct of the context. Chuck suggests we start with the C-API, get it called from python, and then modify the other parts to support the new parameters. Maanas suggests shrinking the PR to special-case string dtype. It seems in the end Chuck will try to submit a PR to do the high-level things.

- [Same-value casting](https://github.com/numpy/numpy/pull/29129) in asarray
  The PR is almost ready, plus/minus some last comments from Martin. What do people think?


## New topics

- (mattip) More complete benchmark coverage for `np.unique` [PR 29621](https://github.com/numpy/numpy/pull/29621) drives up the benchmark time from 5-6 minutes to 8 minutes. This is after the author cut down the combinations of parameters. I wonder if we could use [a `@skip_benchmark_if` marker](https://asv.readthedocs.io/en/latest/writing_benchmarks.html#skipping-benchmarks) to have a kind of pytest fast/slow marker behaviour. Then we could run the CI with the `fast` marker. (tyler) `sklearn` has such a mechanism. Tyler will add a comment to the PR.

### Let's connect and keep the conversation going!

Please enquire in a meeting or via email how to join the NumPy contributor community on **Slack**.

Sign up to the NumPy **mailing list**: mail.python.org/mailman/listinfo/numpy-discussion

Subscribe to the NumPy **YouTube** channel: https://www.youtube.com/c/NumPy_team

Follow us on **LinkedIn**: https://www.linkedin.com/company/numpy/

---
Remember to archive this file by committing it to [github.com/numpy/archive/community_meetings](https://github.com/numpy/archive/tree/main/community_meetings)
