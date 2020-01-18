# NumPy Information Map

Objective
=========

There is loads of information about NumPy scattered across various sites, documents and articles besides several others that are created by the community at large. Our objective is to augment the ongoing NumPy website and documentation spruce-up efforts, through classification of key information related to NumPy. This will help in identifying inconsistencies, gaps and missing pieces that could be addressed as part of NumPy documentation (GSoD, others) and marketing, funding and other related initiatives. The eventual goal is to accelerate the process of on-boarding new NumPy users and make it easy for seasoned users to access relevant information about NumPy in crisp, digestible chunks. We plan to create and use NumPy Information Map to meet this objective.

What is an information Map?
===========================

An information map helps with analysis, organization, and visual presentation of information. It is a way of classifying and organizing information such as concepts, procedures, proposals, manuals such that it is available to the target audience in digestible chunks. An information map enables efficient information access by improving structure and readability. It also provides the much needed focus on target audience or the 'user', especially in the way information is generated, stored and accessed.

What problem does it solve?
===========================

Following is a list of some of the key problems that can be addressed by an information map. For more details on benefits gained by information mapping, see the reference section.

-   Too long content, TL;DR

-   Un-organized, scattered information in various logical and physical styles

-   Hard to read and find information about the topic users are typically interested in

-   Information inconsistencies and gaps

-   Time to completion of tasks takes longer due to information gaps, hard to locate data

-   Higher costs, lower productivity, expensive errors due to miscommunication and incorrect information

NumPy Information Map (Classification Chart)
============================================

Here is an early draft of the NumPy information map:

|  Information    | What it         | 
| ----------------|-----------------|
| some text       |  **bold text**  |

+-----------------+-----------------+-----------------+-----------------+
| **Information   | **What it       | **Key           | **Examples with |
| Type**          | contains?**     | information     | a focus on      |
|                 |                 | blocks**        | target          |
|                 |                 |                 | audience**      |
+=================+=================+=================+=================+
| NumPy Concepts  | Relationships,  | 1.  Names /     |                 |
|                 | key terms,      |     > Definitio |                 |
|                 | definitions,    | ns              |                 |
|                 | usage related   |                 |                 |
|                 | ideas           | 2.  Rules       |                 |
|                 |                 |                 |                 |
|                 |                 | 3.  Introductio |                 |
|                 |                 | ns              |                 |
|                 |                 |                 |                 |
|                 |                 | 4.  Examples    |                 |
|                 |                 |                 |                 |
|                 |                 | 5.  Diagrams    |                 |
|                 |                 |                 |                 |
|                 |                 | 6.  Syntax      |                 |
|                 |                 |                 |                 |
|                 |                 | 7.  Flow charts |                 |
|                 |                 |                 |                 |
|                 |                 | 8.  Related     |                 |
|                 |                 |     > infomap   |                 |
+-----------------+-----------------+-----------------+-----------------+
| NumPy Structure | Key components  | Physical as     | NumPy SW        |
|                 | of NumPy and    | well as logical | Components      |
|                 | how they work   | components with |                 |
|                 | together        | parts and       | NumPy Code      |
|                 |                 | distinct        | Components      |
|                 | Both - for end  | boundaries.     |                 |
|                 | user (binaries, |                 | NumPy           |
|                 | libraries,      |                 | History/Evoluti |
|                 | scripts,        |                 | on/About        |
|                 | command         |                 |                 |
|                 | references      |                 | -   NumPy       |
|                 | etc.) and for   |                 |     > Release   |
|                 | NumPy           |                 |     > and       |
|                 | Developers - in |                 |     > feature   |
|                 | terms of how    |                 |     > timeline  |
|                 | code is         |                 |                 |
|                 | organized,      |                 | NumPy Org       |
|                 | control flows,  |                 | Components      |
|                 | deployment      |                 |                 |
|                 | related         |                 | -   [[Steering  |
|                 | structures      |                 |     > Councils  |
|                 |                 |                 |     > &         |
|                 | \*This could    |                 |     > Partners] |
|                 | also include    |                 | {.underline}](h |
|                 | NumPy org       |                 | ttps://numpy.or |
|                 | structure (if   |                 | g/devdocs/dev/g |
|                 | it makes sense  |                 | overnance/peopl |
|                 | to share it     |                 | e.html)         |
|                 | with users -    |                 |                 |
|                 | say in About    |                 | -   Link to     |
|                 | kind of tab on  |                 |     > Teams     |
|                 | website)        |                 |     > page      |
|                 |                 |                 |     > (TBD)     |
|                 |                 |                 |                 |
|                 |                 |                 |     -   Develop |
|                 |                 |                 | ment            |
|                 |                 |                 |         > (Comm |
|                 |                 |                 | unity+dedicated |
|                 |                 |                 |         > core) |
|                 |                 |                 |                 |
|                 |                 |                 |     -   Packagi |
|                 |                 |                 | ng              |
|                 |                 |                 |                 |
|                 |                 |                 |     -   Learnin |
|                 |                 |                 | g/Education     |
|                 |                 |                 |         > (Trai |
|                 |                 |                 | ning?)          |
|                 |                 |                 |                 |
|                 |                 |                 |     -   TechPub |
|                 |                 |                 | s               |
|                 |                 |                 |                 |
|                 |                 |                 |     -   Website |
|                 |                 |                 |                 |
|                 |                 |                 |     -   Marketi |
|                 |                 |                 | ng              |
+-----------------+-----------------+-----------------+-----------------+
| NumPy Processes | Mostly recipes  | 1.  Name        | [For NumPy      |
|                 | which have a    |                 | Users]{.underli |
|                 | finite timeline | 2.  Stages      | ne}             |
|                 | and address     |                 |                 |
|                 | how-to-do-so-an | 3.  Steps       | -   [[NumPy     |
|                 | d-so            |                 |     > incident  |
|                 | with NumPy or   | 4.  I/O         |     > reporting |
|                 | how to          |                 |     > guideline |
|                 | contribute to   | 5.  Pre-requisi | s]{.underline}] |
|                 | NumPy           | tes             | (https://numpy. |
|                 |                 |     > (Both in  | org/devdocs/dev |
|                 |                 |     > terms of  | /conduct/code_o |
|                 |                 |     > other     | f_conduct.html# |
|                 |                 |     > dependenc | reporting-guide |
|                 |                 | ies             | lines)          |
|                 |                 |     > and NumPy |                 |
|                 |                 |     > usage     | -   Reporting a |
|                 |                 |     > skills)   |     > bug       |
|                 |                 |                 |                 |
|                 |                 | 6.  Cause-Effec | -   Reporting a |
|                 |                 | t-Procedures    |     > security  |
|                 |                 |                 |     > issue     |
|                 |                 |                 |                 |
|                 |                 |                 | -   Getting     |
|                 |                 |                 |     > help with |
|                 |                 |                 |     > NumPy     |
|                 |                 |                 |     > usage     |
|                 |                 |                 |                 |
|                 |                 |                 | [For NumPy      |
|                 |                 |                 | Contributors &  |
|                 |                 |                 | Developers]{.un |
|                 |                 |                 | derline}        |
|                 |                 |                 |                 |
|                 |                 |                 | -   [[Contribut |
|                 |                 |                 | ing             |
|                 |                 |                 |     > to        |
|                 |                 |                 |     > NumPy]{.u |
|                 |                 |                 | nderline}](http |
|                 |                 |                 | s://numpy.org/d |
|                 |                 |                 | evdocs/dev/inde |
|                 |                 |                 | x.html?highligh |
|                 |                 |                 | t=slack)        |
|                 |                 |                 |                 |
|                 |                 |                 |     -   [[Code  |
|                 |                 |                 |         > of    |
|                 |                 |                 |         > Condu |
|                 |                 |                 | ct]{.underline} |
|                 |                 |                 | ](https://numpy |
|                 |                 |                 | .org/devdocs/de |
|                 |                 |                 | v/conduct/code_ |
|                 |                 |                 | of_conduct.html |
|                 |                 |                 | )               |
|                 |                 |                 |                 |
|                 |                 |                 |     -   [[Devel |
|                 |                 |                 | oper            |
|                 |                 |                 |         > Guide |
|                 |                 |                 | lines]{.underli |
|                 |                 |                 | ne}](https://nu |
|                 |                 |                 | mpy.org/devdocs |
|                 |                 |                 | /dev/gitwash/in |
|                 |                 |                 | dex.html)       |
|                 |                 |                 |         > and   |
|                 |                 |                 |         > [[dev |
|                 |                 |                 |         > envir |
|                 |                 |                 | onment          |
|                 |                 |                 |         > setup |
|                 |                 |                 | ]{.underline}]( |
|                 |                 |                 | https://numpy.o |
|                 |                 |                 | rg/devdocs/dev/ |
|                 |                 |                 | development_env |
|                 |                 |                 | ironment.html)  |
|                 |                 |                 |                 |
|                 |                 |                 |     -   [[Devel |
|                 |                 |                 | oper            |
|                 |                 |                 |         > Workf |
|                 |                 |                 | low]{.underline |
|                 |                 |                 | }](https://nump |
|                 |                 |                 | y.org/devdocs/d |
|                 |                 |                 | ev/development_ |
|                 |                 |                 | workflow.html)  |
|                 |                 |                 |                 |
|                 |                 |                 |     -   [[C     |
|                 |                 |                 |         > Style |
|                 |                 |                 |         > Guide |
|                 |                 |                 |         > for   |
|                 |                 |                 |         > NumPy |
|                 |                 |                 | ]{.underline}]( |
|                 |                 |                 | https://numpy.o |
|                 |                 |                 | rg/devdocs/dev/ |
|                 |                 |                 | style_guide.htm |
|                 |                 |                 | l)              |
|                 |                 |                 |                 |
|                 |                 |                 |     -   [[NumPy |
|                 |                 |                 |         > Bench |
|                 |                 |                 | marking]{.under |
|                 |                 |                 | line}](https:// |
|                 |                 |                 | numpy.org/devdo |
|                 |                 |                 | cs/benchmarking |
|                 |                 |                 | .html)          |
|                 |                 |                 |                 |
|                 |                 |                 |     -   [[How   |
|                 |                 |                 |         > to    |
|                 |                 |                 |         > relea |
|                 |                 |                 | se              |
|                 |                 |                 |         > a     |
|                 |                 |                 |         > NumPy |
|                 |                 |                 |         > versi |
|                 |                 |                 | on]{.underline} |
|                 |                 |                 | ](https://numpy |
|                 |                 |                 | .org/devdocs/de |
|                 |                 |                 | v/releasing.htm |
|                 |                 |                 | l)              |
|                 |                 |                 |                 |
|                 |                 |                 | -   Others TBD  |
+-----------------+-----------------+-----------------+-----------------+
| NumPy Reference | Functions,      | Name            | Links to User   |
|                 |                 |                 | guide           |
|                 | APIs            | I/O             |                 |
|                 |                 |                 | FAQ             |
|                 | Others for end  | Usage Model,    |                 |
|                 | users           | workflow        |                 |
|                 |                 |                 |                 |
|                 | Tutorials       | Example code    |                 |
|                 |                 |                 |                 |
|                 | Presentations   |                 |                 |
|                 |                 |                 |                 |
|                 | Workshops -     |                 |                 |
|                 | media,          |                 |                 |
|                 | recordings      |                 |                 |
|                 | (latest ones)   |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| NumPy Showcase  | Case Studies    | 1.  Challenges  |                 |
|                 |                 |     > before    |                 |
|                 |                 |     > NumPy,    |                 |
|                 |                 |                 |                 |
|                 |                 | 2.  How NumPy   |                 |
|                 |                 |     > use       |                 |
|                 |                 |     > helped,   |                 |
|                 |                 |                 |                 |
|                 |                 | 3.  Use         |                 |
|                 |                 |     > Model,Int |                 |
|                 |                 | eresting        |                 |
|                 |                 |     > statistic |                 |
|                 |                 | s               |                 |
|                 |                 |     > such as   |                 |
|                 |                 |     > time      |                 |
|                 |                 |     > reduction |                 |
|                 |                 |     > for       |                 |
|                 |                 |     > processin |                 |
|                 |                 | g               |                 |
|                 |                 |     > image by  |                 |
|                 |                 |     > 50% etc., |                 |
|                 |                 |                 |                 |
|                 |                 | 4.  Distinctive |                 |
|                 |                 |     > NumPy use |                 |
|                 |                 |     > model say |                 |
|                 |                 |     > in terms  |                 |
|                 |                 |     > of scale  |                 |
|                 |                 |     > or type   |                 |
|                 |                 |     > of usage. |                 |
+-----------------+-----------------+-----------------+-----------------+
| NumPy Branding  | Logos,          | 1.  Infographic | -   [[Icons]{.u |
|                 | templates for   | s               | nderline}](http |
|                 | docs,           |                 | s://github.com/ |
|                 | proposals,      | 2.  Logos       | numpy/numpy/tre |
|                 | presentations,  |                 | e/master/brandi |
|                 | keynotes,       | 3.  Themes      | ng/icons)       |
|                 | talks, badges   |                 |                 |
|                 | (For Projects   | 4.  Color-font- | -   [[Color-sch |
|                 | using NumPy?)   | styling         | eme]{.underline |
|                 |                 |                 | }](https://user |
|                 |                 | 5.  Name-recall | -images.githubu |
|                 |                 |                 | sercontent.com/ |
|                 |                 |                 | 98330/63642399- |
|                 |                 |                 | 51f41480-c673-1 |
|                 |                 |                 | 1e9-8d22-20315b |
|                 |                 |                 | 71c83e.jpg)     |
|                 |                 |                 |                 |
|                 |                 |                 | -               |
+-----------------+-----------------+-----------------+-----------------+
| Misc (For NumPy | Could include   | 1.  How-to      | -   [[NumPy     |
| internal use?)  | internal NumPy  |                 |     > Governanc |
|                 | processes such  | 2.  Steps for   | e]{.underline}] |
|                 | as governance   |     > NumPy     | (https://numpy. |
|                 | or output of    |     > governanc | org/devdocs/dev |
|                 | those processes | e               | /governance/gov |
|                 | such as         |     > procedure | ernance.html)   |
|                 | reports,        |     > say xyz   |                 |
|                 | meeting minutes |                 | -   [[Reports]{ |
|                 |                 | 3.  Reports     | .underline}](ht |
|                 |                 |                 | tps://github.co |
|                 |                 | 4.  Plans       | m/numpy/archive |
|                 |                 |                 | /tree/master/re |
|                 |                 |                 | ports)          |
|                 |                 |                 |                 |
|                 |                 |                 | -   [[Meeting   |
|                 |                 |                 |     > minutes]{ |
|                 |                 |                 | .underline}](ht |
|                 |                 |                 | tps://github.co |
|                 |                 |                 | m/numpy/archive |
|                 |                 |                 | /tree/master/st |
|                 |                 |                 | atus_meetings)  |
+-----------------+-----------------+-----------------+-----------------+
| Archives        | This could      | 1.  Mailing     |                 |
|                 | include         |     > lists     |                 |
|                 | resources that  |     > archives  |                 |
|                 | are dated but   |                 |                 |
|                 | maybe useful    | 2.  StackExchan |                 |
|                 | for new users   | ge              |                 |
|                 | or historical   |     > (older    |                 |
|                 | purposes        |     > discussio |                 |
|                 |                 | ns              |                 |
|                 |                 |     > that are  |                 |
|                 |                 |     > relevant  |                 |
|                 |                 |     > even      |                 |
|                 |                 |     > today)    |                 |
|                 |                 |                 |                 |
|                 |                 | 3.  Key         |                 |
|                 |                 |     > decisions |                 |
|                 |                 |     > and       |                 |
|                 |                 |     > reasons   |                 |
|                 |                 |                 |                 |
|                 |                 | 4.              |                 |
+-----------------+-----------------+-----------------+-----------------+

References

1.  [[http://www.web.stanford.edu/\~rhorn/a/topic/stwrtng\_infomap/artclInfoMappingTraining.pdf]{.underline}](http://www.web.stanford.edu/~rhorn/a/topic/stwrtng_infomap/artclInfoMappingTraining.pdf)

2.  [[https://www.researchgate.net/figure/Example-of-an-information-map\_fig1\_232477925]{.underline}](https://www.researchgate.net/figure/Example-of-an-information-map_fig1_232477925)

3.  [[https://stc-techedit.org/tiki-index.php?page=Evaluating+the+Information+Mapping+Method]{.underline}](https://stc-techedit.org/tiki-index.php?page=Evaluating+the+Information+Mapping+Method)
