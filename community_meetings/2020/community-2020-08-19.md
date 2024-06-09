---
tags: NumPy
---

# 2020-08-19 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 13:00 Pacific Time (18:00 UTC)
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Clair Bowen, Inessa Pawson, Deji Suolang, Stephanie Mendoza, Ryan Cooper, Ross Barnowski, Warren Weckesser, Ralf Gommers, Matti Picus, Xiaoyi Deng, Sebastian Berg, Ben Nathanson


## Follow-up from last meeting / discussions

- Tests slow (migrate to Azure?)

  * side note: output of `pytest --durations=10`:
    ```
    14.09s call     numpy/lib/tests/test_io.py::TestSaveTxt::test_large_zip
    13.74s call     numpy/linalg/tests/test_linalg.py::TestCond::test_generalized_sq_cases
    9.29s call     numpy/core/tests/test_mem_overlap.py::test_may_share_memory_easy_fuzz
    8.27s call     numpy/core/tests/test_multiarray.py::TestBool::test_count_nonzero_all
    7.65s call     numpy/core/tests/test_mem_overlap.py::test_may_share_memory_harder_fuzz
    7.44s call     numpy/f2py/tests/test_compile_function.py::test_f2py_init_compile[extra_args0]
    7.41s call     numpy/f2py/tests/test_compile_function.py::test_f2py_init_compile[]
    7.37s call     numpy/f2py/tests/test_compile_function.py::test_f2py_init_compile[--noopt --debug]
    5.64s call     numpy/core/tests/test_mem_overlap.py::test_diophantine_fuzz
    4.93s call     numpy/lib/tests/test_format.py::test_large_archive
    ```


## Topics

- **NumPy Community Survey 2020**
1,144 responses as of Aug 19th. The survey is closing on Aug 20th.

  **Release of the collected data into the public domain**
  Discuss with Claire Bowen, the Lead Data Scientist on privacy and data security at the Urban Institute, how to strike a balance between open data and data privacy with the scientific methods and tools currently available. 
  
  - There's a balance between utility and privacy of the data.
  - Options include: an interactive sanitizer, generating and releasing a synthetic dataset, differential privacy approaches (hot because it can quantify privacy risk; it's a mathematical equation that has to be satisfied for an approach to be considered differential; not recommended because the application isn't well-developed), ...
  - Claire recommends going for a synthetic dataset.
  - We can release disjoint sets, like separating out the demographics info, the free-form text (which needs manual curation), and the responses to other questions.
  - In the survey itself we promised to release the data publicly, so yes we did commit to do that.

  **Data analysis**
  Schedule a meeting with the Survey Team   to discuss deliverables, timeline, and allocate responsibilities.

- [Policy on tools that share information with commercial firms](https://github.com/numpy/numpy/issues/17066)


- New Sphinx theme

- NEP process

    
- API standardization initiative




## Additional Details

- Warren

  - Work on a faster text reader is on github at [readtextstream](https://github.com/WarrenWeckesser/readtextstream).

- Sebastian


- Ross

---

Please remember to archive this file and commit it to github.com/numpy/archive

