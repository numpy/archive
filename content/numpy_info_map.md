# NumPy Information Map

## Objective
=========

There is loads of information about NumPy scattered across various sites, documents and articles besides several others that are created by the community at large. Our objective is to augment the ongoing NumPy website and documentation spruce-up efforts, through classification of key information related to NumPy. This will help in identifying inconsistencies, gaps and missing pieces that could be addressed as part of NumPy documentation (GSoD, others) and marketing, funding and other related initiatives. The eventual goal is to accelerate the process of on-boarding new NumPy users and make it easy for seasoned users to access relevant information about NumPy in crisp, digestible chunks. We plan to create and use NumPy Information Map to meet this objective.

## What is an Information Map?
===========================

An information map helps with analysis, organization, and visual presentation of information. It is a way of classifying and organizing information such as concepts, procedures, proposals, manuals such that it is available to the target audience in digestible chunks. An information map enables efficient information access by improving structure and readability. It also provides the much needed focus on target audience or the 'user', especially in the way information is generated, stored and accessed.

## What problem does it solve?
===========================

Following is a list of some of the key problems that can be addressed by an information map. For more details on benefits gained by information mapping, see the reference section.

-   Too long content, TL;DR

-   Un-organized, scattered information in various logical and physical styles

-   Hard to read and find information about the topic users are typically interested in

-   Information inconsistencies and gaps

-   Time to completion of tasks takes longer due to information gaps, hard to locate data

-   Higher costs, lower productivity, expensive errors due to miscommunication and incorrect information

## NumPy Information Map (Classification Chart)

Here is an early draft of the NumPy information map:


| Information Type 	| What it contains? | Key information blocks	| Examples with a focus on target audience 	|
|:-------	|:----------	|:--------	|:---------	|
| NumPy Concepts | Relationships, key terms, definitions, usage related ideas 	|* Names / Definitions<br>* Rules<br> * Introductions <br>* Examples<br>* Diagrams<br>* Syntax<br> * Flow charts<br>Related infomap| |
| NumPy Structure | Key components of NumPy and how they work together<br><br>Both - for end user (binaries, libraries, scripts, command references etc.) and for NumPy Developers - in terms of how code is organized, control flows, deployment related structures<br><br>*This could also include NumPy org structure (if it makes sense to share it with users - say in About kind of tab on website)|Physical as well as logical components with parts and distinct boundaries.|NumPy SW Components<br><br>NumPy Code Components<br><br>NumPy History/Evolution/About<br><br> * NumPy Release and feature timeline<br><br>NumPy Org Components<br> * [Steering Councils & Partners](https://numpy.org/devdocs/dev/governance/people.html)<br> * Link to Teams page (TBD)<br><br>   - Development (Community+dedicated core)<br>   - Packaging<br>   - Learning/Education (Training?)<br>  - TechPubs<br>  - Website<br>   - Marketing |
|NumPy Processes|Mostly recipes which have a finite timeline and address how-to-do-so-and-so with NumPy or how to contribute to NumPy<br><br>|* Name<br>* Stages<br>* Steps<br>* I/O<br>* Pre-requisites (Both in terms of other dependencies and NumPy usage skills)<br>* Cause-Effect-Procedures| 1. _For NumPy Users_ <br><br> * [NumPy incident reporting guidelines](https://numpy.org/devdocs/dev/conduct/code_of_conduct.html#reporting-guidelines)<br> * Reporting a bug<br> * Reporting a security issue<br> * Getting help with NumPy usage<br><br> 2. _For NumPy Contributors & Developers_ <br><br> a.) [Contributing to NumPy](https://numpy.org/devdocs/dev/index.html?highlight=slack)<br>- [Code of Conduct](https://numpy.org/devdocs/dev/conduct/code_of_conduct.html) <br>- [Developer Guidelines and dev environment setup](https://numpy.org/devdocs/dev/gitwash/index.html)<br>- [Developer Workflow](https://numpy.org/devdocs/dev/development_workflow.html)<br>- [C Style Guide for NumPy](https://numpy.org/devdocs/dev/style_guide.html)<br>- [NumPy Benchmarking](https://numpy.org/devdocs/benchmarking.html)<br>- [How to release a NumPy version](https://numpy.org/devdocs/dev/releasing.html)<br><br> b.) Others TBD|
|NumPy Reference| Functions,APIs meant for end users, Tutorials, Presentations, Workshops - media, recordings (latest ones)|* Name<br>* I/O<br>* Usage Model, workflow<br>* Example code|* Links to User guide<br>* FAQ|
|NumPy Showcase|Case Studies|* Challenges faced before NumPy was adopted,<br> * How NumPy use helped,<br> * Use Model,Interesting statistics such as time reduction for processing image by 50% etc.,<br> * Distinctive NumPy use model say in terms of scale or type of usage.|Marquee Case Studies such as:<br><br>1. First Black Hole Image<br>2. LIGO - Gravitational Waves Detection and reporting in real time<br> 3. NumPy in Sports data analytics (Maybe)|
|NumPy Branding|Logos, templates for docs, proposals, presentations, keynotes, talks, badges (For Projects using NumPy?)|* Infographics<br> * Logos<br> * Themes<br> * Color-font-styling<br> * Name-recall|1. [Icons](https://github.com/numpy/numpy/tree/master/branding/icons)<br>2. [Color-scheme](https://user-images.githubusercontent.com/98330/63642399-51f41480-c673-11e9-8d22-20315b71c83e.jpg)|
|Misc (For NumPy internal use?)|This could include internal NumPy processes such as governance or output of those processes such as reports, meeting minutes|1. How-to (some NumPy internal process)<br>2. Steps for NumPy governance procedure say xyz<br>3. Reports<br>4.Plans| [NumPy Governance](https://numpy.org/devdocs/dev/governance/governance.html)<br>[Reports](https://github.com/numpy/archive/tree/master/reports)<br>[Meeting minutes](https://github.com/numpy/archive/tree/master/status_meetings)|
|Archives|This could include resources that are dated but maybe useful for new users or historical purposes|* Mailing lists archives<br>* StackExchange (older discussions that are relevant even today)<br>* Key decisions and reasons|TBD|

## References

1.  [Information Mapping](http://www.web.stanford.edu/\~rhorn/a/topicstwrtng\_infomap/artclInfoMappingTraining.pdf)

2.  [Example of an Information Map](https://www.researchgate.net/figure/Example-of-an-information-map\_fig1\_232477925)

3.  [Evaluating Information Mapping methods](https://stc-techedit.org/tiki-index.php?page=Evaluating+the+Information+Mapping+Method)
