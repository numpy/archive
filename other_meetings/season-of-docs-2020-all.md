---
tags: documentation, season of docs
---

# 2019 Google Season of Docs Meetings

---

## Notes from 2 Mar '20

Rescheduling this meeting & moving to once every 3 weeks. Open it up more widely; announce on mailing list.

New numpy.org website launch plan: March 15th roll-out.

Question on Crowdin: is there a glossary (for consistent translation of a term)?

---

## Notes from 18 Feb '20

### Shekhar

* Travis re-setup: https://github.com/numpy/numpy.org/pull/166. All green but still an issue on the Surge side.
* Refactoring [versions](https://github.com/Shekharrajak/versions), [scipy-sphinx-theme-v2](https://github.com/scipy/scipy-sphinx-theme-v2/)
* Crowdin: numpy.crowdin.org public project got deleted, unsure why. Shekhar will set it up again, and add Chinese (to start real translations) and Dutch (to verify before deletion)

### Anne


### Melissa

Linalg SVD 

[NEP 44 on doc restructuring](https://github.com/numpy/numpy/pull/15554) submitted.

---

## Notes from 21 Jan '20

Anne's "absolute beginners" tutorial was merged today!

Melissa's linalg tutorial is about ready.

We discussed translations; for now let's see how they work with the new website. If that goes as expected, then figuring out how we can split off part of the user guide and translate that as well could be very useful.

---

## Notes from 7 Jan '20

* Introduction from Melissa
* Anne's PR
* Maja's [PR](https://github.com/scipy/scipy/pull/11143)

### Shekhar

* Worked on open issues in [scipy-sphinx-theme-v2](https://github.com/scipy/scipy-sphinx-theme-v2). Discussing in issue and fixing one by one. Labelled the issue for someone who wants to work on it. 
* Travis setup for numpy.org [#124](https://github.com/numpy/numpy.org/pull/124).
* Discussing with crowdin team for the transaltion and auto PR for new updated master branch files.
* Tried out sphinx based numpy.org/doc site https://github.com/Shekharrajak/versions
* Working on surge auto deployment per PR for [versions](https://github.com/Shekharrajak/versions) - instead of github action moving to travis [#1](https://github.com/Shekharrajak/versions/pull/1).
* Refactored the scipy-sphinx-theme-v2.

### Brandon
- iterate on numpydoc.validate, revalidate scipy.stats for new errors
- finish interlink conversion: https://github.com/scipy/scipy/pull/11129
- create PR for new intersphinx mapping: https://numpy-team.slack.com/archives/CNLCCUBQV/p1574830518003000
- finish code examples for scipy.stats: https://github.com/scipy/scipy/pull/11148
- participate in stats.fisher discussion (see https://github.com/scipy/scipy/issues/11131)
- participate in kstwo discussion (see https://github.com/scipy/scipy/issues/10963)
- triage daily practice and/or guide
- software documentation style guide, will collaborate with Maja

### Melissa
* linear algebra tutorials (SVD, etc.)

### Ralf
* possible new volunteer writer
* merge PRs from Anne and Shekhar

---

## Notes from 10 Dec

A short meeting, we just decided to continue these bi-weekly calls from Jan 7th onwards.

---

## Notes from 26 Nov

### Maja
 
* I've finally solved the problem of embedding the trees in the documentation (recall that the main obstacle was the font size). The solution is easy (and universal) enough to make future maintenance manageable:
    * convert the PDF with the tikzpicture with pdftocairo to SVG
    * insert links to appropriate documentation parts by means of a simple script (provided by me)
    * rescale the SVG accordingly using common (visual) sense
    * insert the SVG file in the documentation like so: 
    ```
    .. raw:: html
       :file: linalg.svg
    ```
* I'm preparing a comprehensive 'trees' pull request.
* I've revised the website contents with respect to stylistic consistency, punctuation and updated certain information (see [PR #324](https://github.com/scipy/scipy.org/pull/324)).
* I've also revised the first half of the API documentation (see [PR #11075](https://github.com/scipy/scipy/pull/11075)). The second part will be complete tomorrow at the latest.
* The (rather subjective) priority list is available [here](https://github.com/mkg33/GSoD/blob/master/priority_list) - as usual, all comments and modification welcome!
* Right now, I'm also writing a concise final report and guidelines for future maintenance (regarding the trees, stylistic revisions, tips on punctuation).
* And yes, I'll definitely meet the deadline :raised_hands: :smiley: 
* Discussed https://github.com/scipy/scipy.org/issues/117, browser-dependent rendering issue. Low-prio at the moment, discussion on the issue.


### Brandon
* Examples on their way for:
    * `anderson`, `ansari`, `bartlett`, `combine_pvalues`, `epps_singleton_2samp`, `fligner`, `friedmanchisquare`, `kstatvar`, `levene`, `ranksums`, `trim1`
    * https://gist.github.com/brandondavid/98859e6f6357b7177ba8ba762d0c961a
* Interlink conversion:
    * https://github.com/scipy/scipy/issues/10366
    * https://github.com/scipy/scipy/pull/11129
* stats.fisher_exact: 
    * https://github.com/scipy/scipy/issues/11131
    * https://hackmd.io/AAmCAcryRWu2BKGZfc9wew
* numpydoc, nan_policy, [kstest/ks_2samp](https://github.com/scipy/scipy/issues/10963), notes/references

### Anne

* I think things are looking pretty good on the tutorial front! I'm looking for any additional spots to add links and combing through for inconsistencies and typos. I'd love any and all feedback you have! You can find the tutorial here: https://github.com/bonn0062/GSoD/blob/master/absolute_beginners.rst
* We also decided to release the tutorial as a Medium article to see if we could get any additional feedback from beginners and the tech community as a whole. I added a few images and gifs to make it a little more Medium-friendly and published it on Towards Data Science on 11/17. So far, we've had almost 7K views with more than 500 claps and no negative comments! 🎉😄 (Pretty good for a post that has a 34 minute read time...) https://towardsdatascience.com/the-ultimate-beginners-guide-to-numpy-f5a2f99aef54

### Shekhar

* Worked on CI/CD fixes and scipy-sphinx-theme. Generated new docs for `numpy` documentation devdocs and `neps` : PR [#14648](https://github.com/numpy/numpy/pull/14648), [#42](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/42). _All green, needs review_

* Surge deployment issue - github secrets is not getting picked sometime (or may be for some user) in github actions. Related PR [#74](https://github.com/numpy/numpy.org/pull/74), talking to surge and github action team. Using travis those issue don't come. May be we should add travis CI as well. It will not need much changes.

* [numpy/doc #1](https://github.com/numpy/doc/pull/1): Working on numpy/doc repo to make it align with the new theme. One idea is to make it sphinx based doc just like numpy/neps.

* [numpy/doc #2](https://github.com/numpy/doc/pull/2): Generated docs put in doc/beta repo for the review from everyone. It should be available on numpy.org/doc/beta once review is completed.

* Passed the ownership of new theme repo [Shekharrajak/scipy-sphinx-theme-v2](https://github.com/Shekharrajak/scipy-sphinx-theme-v2) to Ralf, so that we can continue use of github actions and workflow. Refer: [comment-557909094](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/42#issuecomment-557909094).

* Making configuration for the new theme simple by adding color, font options in configuration options. So they just have to set in conf.py file for different documentation site.


## Finalizing projects

The end of November, which is the official end of Season of Docs, is rapidly approaching (submission deadline is 29 Nov). Let's discuss what needs to happen still.

---

## Notes from 12 Nov

### Maja

* Regarding the graphical guides: I ran into an unexpected problem, i.e., the font size turned out to be too small for the website. I am now redisigning all the trees.

* The results of our user survey are out. You can consult the full report [here](https://github.com/mkg33/GSoD/blob/master/user_survey_summary.pdf).

User survey results and summary can be published.
Maja is also preparing a prio list for the feedback
people gave.

* I am also finishing the revision of the existing documentation (viz. stylistics, punctuation, rephrasing, consistency, etc.).

### Brandon

* PR#11017 merged (numpydoc validation of morestats.py): https://github.com/scipy/scipy/pull/11017

* #244 RT02 enforces the pandas docstring guide, not the numpydoc docstring guide: https://github.com/numpy/numpydoc/issues/244

* stats.fisher_exact: https://hackmd.io/s8BHudE6Qfa2yoUGgojH4A

* nan propagate:
    https://github.com/scipy/scipy/issues/9815
    https://github.com/scipy/scipy/issues/9947
    https://github.com/scipy/scipy/issues/9948
    https://github.com/scipy/scipy/issues/9955
    https://github.com/scipy/scipy/pull/10519

Apparently consensus on `nan_policy` behavior was
reached in March. Brandon will summarize this and
bring some coherency/consistency in the discussions
on the various issues.

### Anne
 
 * I've been  focusing on putting something more readable together. You can check it out [here](https://github.com/bonn0062/GSoD/blob/master/absolute_beginners.rst)!

95% through, and Anne expects it to be ready for review
towards the end of this week.

### Shekhar

* Spend time to understand the Hugo features: [multilingual](https://gohugo.io/content-management/multilingual/), [Hugo example](https://github.com/gohugoio/hugo/tree/master/examples/multilingual).
* Setup crowdin for numpy.org - `newsite` branch.
* Worked on Hugo site translation (numpy.org `newsite` branch) to implement Multilingual feature: [#61](https://github.com/numpy/numpy.org/pull/61), [#62](https://github.com/numpy/numpy.org/pull/62). 
* Removed the crowdin from sphinx theme: [#40](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/40)

* Reading about versioning in custon Sphinx theme but still think that numpy.org/doc is good for selecting different versions.
* Working on better UI/UX for custom sphinx theme and fixing bugs like [#38](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/38).

Discussion on what to focus on merging first: Shekhar
prefers to merge the Sphinx theme first. We can deploy
it to a separate site and link it from the docs front
page as a beta version, to get some end user feedback.

---

## Notes from 22 Oct

### Brandon
* Reflections on being just past the midpoint:
    * Learning workflow, tools, environment
    * Learning to work in the open and be willing to make mistakes in public
    * Appreciation for the responsiveness of the community
    * Using the Slack workspace for greater team cohesion
* This week:
    * PR#10863 merged (PEP257+numpydoc standardization): https://github.com/scipy/scipy/pull/10863
    * kstest, ks_2samp issue opened: https://github.com/scipy/scipy/issues/10963
        Also: https://hackmd.io/3Gj_8GsYTuCa-xGBD9KHog
    * Work on numpydoc validation script well underway: https://github.com/numpy/numpydoc/pull/238
* Next week:
    * stats.fisher conditional -vs- unconditional MLE: https://stats.stackexchange.com/questions/288641/odds-ratio-mle-calculation-unconditional-vs-conditional
    * Coordinate with PR#10519 (docstrings for nan `policy='propagate'`): https://github.com/scipy/scipy/pull/10519
    * Script to wrap numpydoc/validate.py for scipy(.stats)
    * WIP PR for SciPy docstyle guide
    * WIP PR for "Examples" section updates

### Maja

* The graphical guides are now 99% complete. I had to spend much more time on the stats and mstats pages (they are rather extensive and difficult to render graphically).

* Actually, I had to split the stats API content into two trees. Not a very pretty solution but the only logical one I could think of.

* Here's an example of the first part (stats API); notice the novel tertiary branching solution: ![](https://i.imgur.com/cGupLhi.jpg)

* As of today, we have 167 responses to our survey (you can consult the interim results [here](https://docs.google.com/spreadsheets/d/149Zie4unVkmyVKuc6X-RmWkaaOrxOyEy3j7sn-Ayz-c/edit?usp=sharing)).

* Here is a brief summary of the interesting comments left by the respondents: 

    * most people wish there were more code samples and better explanations
    * they'd also appreciate better navigation and graphical guides
    * the examples ought to be more basic and avoid scientific jargon
    * quite a few people emphasise the need for improved navigation (they mention it in the open-ended questions).

* The problematic [pull request](https://github.com/scipy/scipy/pull/10823) has already been merged.

* I've started to correct the minor inconsistencies in the graphical guides (only certain subtle layout issues).

* I will now resume the task of revising the current documentation and, at the same time, take care of integrating the graphical guides with the documentation (plus adding the necessary cross-references to the trees).

### Shekhar

* Worked on Hugo-Surge deployment: [#46](https://github.com/numpy/numpy.org/pull/46), [#58](https://github.com/numpy/numpy.org/pull/58)

* [Scipy Sphinx theme v2](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/) continue: Fixed the Search box issue and did changes for the copybutton feature from old sphinx theme. 

* Tried Translation using sphinx by refering [readthedoc](https://docs.readthedocs.io/en/latest/localization.html#project-with-multiple-translations), [Talk on Sphinx](https://www.youtube.com/watch?v=Nz8zutA55fI), [PR](https://github.com/readthedocs/sphinx_rtd_theme/pull/405/files), [Google group discussion](https://groups.google.com/forum/#!topic/sphinx-users/Xmbs5AbnVKY)

* Tried to understand docusaurus multilingual feature, but it very specific to the framework and implementation were looking bit complex to me. How to redirect to the same page when user select the specific language and all the links changed to that specific language page? i.e. if page is `/about.html` then for Hindi language it should be `hi/about.html` with all other ref links.

* Working on versioning dropdown part using [#12097](https://github.com/numpy/numpy/pull/12097/). Looking at javascript code written for [Python doc](https://github.com/python/cpython/blob/master/Doc/tools/static/switchers.js)

* Working on Hugo-Crowdin setup. Previously done in [Scipy Sphinx theme v2](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/).
 
### Anne
 
 * I've been working less on the outline this week and am now focusing on putting something more readable together. You can check it out [here](https://github.com/bonn0062/GSoD/blob/master/absolute_beginners.rst)!

---

## Notes from 8 Oct

### Maja

* The graphical guides are being developed [here](https://github.com/mkg33/GSoD). All remarks are, as usual, very welcome. However, at this stage, I won't be able to make any major changes (because I've already implemented this layout in a significant part of the project). I'll still be able to accomodate any minor corrections/wishes, though.

* As of now, there do exist certain (minor) inconsistencies in the graphical guides (i.e., spacing) but I'll correct them very soon.

* Here's an example of what the layout looks like right now (this is supposed to be the final version):

![](https://i.imgur.com/5hCg4r8.jpg)

* As of today, we have 55 responses to our user survey. 

* Next week: I'll open a new pull request regarding the integration of the graphical guides with the documentation and I'll also resume the task of revising/correcting the stylistic issues in the current documentation.

* Just for reference, here's a screenshot of the 'sub-sub-categories'.

![](https://i.imgur.com/nsIRfYR.jpg)


### Shekhar

* Testing the new Sphinx theme with numpy docs: https://github.com/numpy/numpy/pull/14648

* beautified and better UX: https://github.com/Shekharrajak/scipy-sphinx-theme-v2 

* User will be able to select previous version of the docs. It will be using numpy.org/doc : https://github.com/numpy/doc/pull/1

* Tab for choosing the historical and PDF versions of the doc: https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/29

* Hugo and Surge for newsite branch: https://github.com/numpy/numpy.org/pull/46

* Working on crowdin: Testing and trying out the crowdin machine translation : https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/28
* 

### Anne
* Still working on the absolute beginner's guide! You can find it officially here: https://github.com/bonn0062/numpy/blob/absolute-beginners/doc/source/user/absolute-beginners-outline.rst and I'm playing with it over here (before submitting it) https://github.com/bonn0062/GSoD/blob/master/absolute_beginners_outline.rst


### Brandon

- Numpydoc validation waiting on merging with Pandas tool (Marc Garcia)
- Consistency of docstrings, e.g. `a` : "input array" has many different ways of spelling it.
- Working on KS-test. Undocumented behavior, e.g. `N > 2666` `approx` behavior.

---

## Notes from 24 Sep

### Maja

* The user survey is finally online, you can access it [here](https://docs.google.com/forms/d/e/1FAIpQLSeBAO0UFKDZyKpg2XzRslsLJVHU61ugjc18-2PVEabTQg2_6g/viewform). You're most welcome to take part in it and spread the word, so that we can reach a wider audience.

* The 'official' colour scheme appears to be a bit too dark for the tree guides. Here's the original version: ![](https://i.imgur.com/rfMnhBw.jpg)

Here are two lighter alternatives: ![](https://i.imgur.com/mZBnIod.jpg)
 

![](https://i.imgur.com/l0p9SEW.jpg)

* I've also broken a few things (see [here](https://github.com/scipy/scipy/pull/10823)) :-) I'm working on revising the docs and my recent commits don't pass the CI checks - I've been unable to find the mistake but Ralf has kindly offered to help.
    
### Anne
* Working on tone and content for introductory materials. Interested in sounding casual and approachable, but wiithout being too informal. 

* If you want to check out the working outline, you can find it [here](https://github.com/bonn0062/numpy/blob/absolute-beginners/doc/source/user/absolute-beginners-outline.rst)

### Shekhar

* Styling and better UX for the sphinx theme: [PR-25 demo](https://pr-25-scipy-sphinx-theme-v2.surge.sh). More details in the [repo](https://github.com/Shekharrajak/scipy-sphinx-theme-v2).

* Trying [crowdin machine translator beta version](https://support.crowdin.com/pre-translation-via-machine/). automatic PR by crowdin: [PR 28](https://github.com/Shekharrajak/scipy-sphinx-theme-v2/pull/28) 

* Versioning system in sphinx docs - numpy/doc is currently servering the same purpose. So we can use the same numpy.org/doc for version change. 

---

## Notes from 10 Sep

### Maja

Some points I'd like to discuss with everyone:

* Shall we put, for example, 'linalg.logm' or just 'logm' in the graphical guides? There seems to be some inconsistency in the tutorials, hence the question. Compare the relevant parts below:

![](https://i.imgur.com/8EwdiOI.jpg)

![](https://i.imgur.com/1UlkF4p.jpg)

* Language used in the docs: American or British English? I'd go for the former because it seems to be the preferred choice of about 90% of the docs. I'm correcting things like '-isation' -> 'ization' or 'behaviour' -> 'behavior' and wanted to get a green light from the community.

* Would you like me to include any specific questions in the survey?


* My suggestions on the stylistic issues in the docs can be found in the pull request [#10800](https://github.com/scipy/scipy/pull/10800).

* One of the most important issues: shall we use the convention '1-D', 'one dimension', etc. - there are lots of inconsistencies in the docs, hence the question.

1-D was the goal, see numpydoc


### Shekhar

- Discussion about deployment: [#39](https://github.com/numpy/numpy.org/issues/39)
- [Found Crowdin + Google translation API (Need billing info to use it)](https://support.crowdin.com/configuring-machine-translation-engines/#google-translate)
- Worked on [scipy-sphinx-theme-v2](https://github.com/Shekharrajak/scipy-sphinx-theme-v2)
- Stable PR: 18 - [demo link](https://pr-18-scipy-sphinx-theme-v2.surge.sh/)
- Github CI/CD used in [scipy-sphinx-theme-v2](https://github.com/Shekharrajak/scipy-sphinx-theme-v2) and surge is integrated.
- Using Github Actions we can automate various process like: surge integration, github push/commit, deploy in github gh-pages , etc. [Refer](https://github.com/sdras/awesome-actions).


### Harivallabha

- Started coding up an end-to-end tutorial using scipy.stats
- Search Engine based on Topic Modeling with Latent Dirichlet Allocation; Inferencing - Collapsed Gibbs Sampler
- Testing it on a financial-tweets-dataset from Kaggle. Seems to work fine on the nltk Brown corpus
- Will polish it off and put it up for review soon. Can be integrated with the other tutorials for scipy.stats when they come out.

---

## Season of Docs meeting 27 Aug

Time: 27 Aug 2019, 3pm UTC (=8am PST, 5pm CEST)
Hangouts link: https://hangouts.google.com/call/khTLgOVXuYRbE-8TrFs-AEEI
_note: Hangouts works best with Chrome, Firefox is troublesome_

Zoom link for next meeting: https://berkeley.zoom.us/j/7722186582 It will time out after 40 minutes, then we will have to restart it (or stop the meeting :smile: ) 

### Notes from Aug 27

### Agenda

-  Hangouts to Zoom?
   - Matti put in a link at the top of this document, people should make sure they have a zoom client before the meeting.
- Publishing project plans
- Blogs
- Updates on Community Bonding period

**- Shekhar**: 

* 
    - Hugo sample site: https://github.com/Shekharrajak/poc-hugo having surge integrated. In every PR we will be having a deployed URL.
        something like (pr-<prnumber>-<sitename>.surge.sh). 
    - Sample PR: https://github.com/Shekharrajak/poc-hugo/pull/2, CI/CD tool will use docker to build and trigger the surge for deployment 
        of static site: https://github.com/Shekharrajak/poc-hugo/blob/master/Dockerfile
    - So we can manage docker service in any CI/CD tool so we don't need to configure it for different CI/CD tool. We just have to change
        out install, build and deploy script as per the tool (Hugo, Sphinx).
    - Understanding Crowdin:
        - Trying to get tool for translator because crowdin need manual work :
            1. translation has to be done by contributors
            2. Download the translated version and put in server.
            3. We can translate line by line (subline will be picked at end of line).
        - Find out google translator: https://translate.google.com/#view=home&op=translate&sl=auto&tl=en 
        - Sample site repo: https://github.com/Shekharrajak/google-translate-site
        - URL for sample hosted site: https://shekharrajak.github.io/google-translate-site/
        - Since we will be generating the static page using the SSG tool (Hugo) and our footer will be configured for google translator
          dropdown. So it will translate the current page as per the user option (refer : https://nitw.ac.in)
  
- Maja
  - Started providing a graphical guide 
  - Sample user survey Maja is currently developing (comments welcome!): https://docs.google.com/forms/d/e/1FAIpQLSeBAO0UFKDZyKpg2XzRslsLJVHU61ugjc18-2PVEabTQg2_6g/viewform Maybe we should send out to a alpha community
  - Color [scheme for numpy.org](https://github.com/numpy/numpy.org/issues/33) Anne: [contrast checker](https://hangouts.google.com/_/elUi/chat-redirect?dest=https%3A%2F%2Fwebaim.org%2Fresources%2Fcontrastchecker%2F)
  
- Brandon
  - SciPy stats [reference documentation](https://hangouts.google.com/_/elUi/chat-redirect?dest=https%3A%2F%2Fgist.github.com%2Fbrandondavid%2F98859e6f6357b7177ba8ba762d0c961a)
  - Half of a blog post about building SciPy on windows. There is old information hanging around that needs to be taken out. Will try to interface with Matt Haberland (sp?)
  
- Anne
  - Wrote first [blogpost](https://towardsdatascience.com/what-do-you-want-to-see-in-the-numpy-docs-de73efb80375). Would like to attract responses: people who want to contribute or are interested
  - Looking at introductions to NumPy/SciPy, interacted with Jay (? person with great graphical intro stuff)
  - I'd love to get project proposals from each of the writers so I can feature you individually!
  - If you have thoughts/ideas/updates/assorted awesomeness (Brandon...) please send it my way when you can! Regular updates are best.
  - It would also be great to be able to reach out to Christina for her info. Feel free to send her my info if that's better!
  
- Ralf:
  There was some confusion about scipy.org (which is about "the SciPy ecosystem") vs. scipy.org/scipylib (which is about SciPy the project/package). We may just want to get rid of some of the (outdated) ecosystem content and make scipy.org only about SciPy the project.

---

## Season of Docs kickoff meeting Aug 13

Time: 13 Aug 2019, 3pm UTC (=8am PST, 5pm CEST)
Hangouts link: https://hangouts.google.com/call/koNrrNfwZSJ5fdzWFEjkAEEE
_note: Hangouts works best with Chrome, Firefox is troublesome_

### Agenda

1. Introductions
2. Overviews of projects (would be great if Anne, Maja, Brandon and Shekhar could give a short (~2-3 min?) summary)
  - Anne: beginner documentation of basic concepts in NumPy as a stepping stone for people who want to *use* it, not necessarily *study* it. Much of the material exists, it is a matter of reorganizing and enhancing it for first-time users
  - Maja: (1) Top-level overview and guidelines, diagrams, trees, for getting into SciPy. (2) User survey of what people want, where are there holes in the documentation. (3) Creating and editing tutorials.
  - Brandon: Scipy stats reference docs. Fill out missing functions and add examples, internal links. Clear up ambiguity and work through issues on github. 
4. Summary of mentoring and other documentation/website activities (Ralf)
 - Ralf: Everyone will be working according to the GSOD timeline. We should develop a communication channel/mentoring that will ensure prompt replies to questions/problems/decisions.
6. Discuss next steps:
  - communication channels: github issues/pull requests. There is also a slack channel. The mailing lists are widely distributed and may not be appropriate for "stupid" questions, depending on how thick your skin is. We will set up a slack channel for this project.
  - community bonding period
  - triaging rights for the scipy/numpy teams on github
  - publishing proposals on the wiki at www.github.com/scipy/scipy/wiki or www.github.com/numpy/numpy/wiki
  - Medium channel for progress and protocols
  - Documentation sprints??
  - How often should we do a team meeting? 1 hour every two weeks.


## Notes

Github Repos:
github.com/numpy/numpy - main numpy repo code and docs
github.com/numpy/numpy.org - "front page" of numpy, will be expanded
github.com/scipy/scipy
github.com/scipy/scipy.org - "front page" of scipy
github.com/scipy/docs.scipy.org - one page TOC for documentation
https://github.com/scipy/scipy-sphinx-theme - theming for sphinx use

Getting started with building documentation: https://www.numpy.org/devdocs/docs/index.html
