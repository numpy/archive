# 2019-09-23 NumPy Web Team Meeting

Time: 9 a.m. Pacific Time

Join Hangouts Meet: https://meet.google.com/trm-gvto-guz
<br> **note: Hangouts works best with Chrome*

Join by phone: +1 980-533-5653 PIN: 455 016 082#

[Slack workspace](https://numpy-team.slack.com)

[Meetings archive](https://github.com/numpy/numpy.org/tree/master/meetings-archive)

**Present:** Ralf, Inessa, Joe, Matti, Sebastian, Hameer



# Agenda

1. Status of the `newsite` branch
2. Website structure - site map: https://app.flowmapp.com/share/e1b61759a5f95f43d8907baedf42875d/
3. Status of content creation.
4. Status of translations with Crowdin.
5. GitHub Actions needs approval. 




# Minutes

**1. Hugo** website working and easy to set up try out:
    * Repo at github.com/numpy/numpy.org in the `newsite` branch
    * README explains how to run the new website (do not forget git submodule init and update)

**2. Website Structure:**
The structure of the individual pages (templates) is still under development, to be finalized after the content creation stage has been completed.

*Navigation of the second level pages:*
A side bar is a better UX choice, refrain from using drop down menus, which are not user friendly.

*NumPy Hall of Fame:*
The page NumPy Hall of Fame is a working title, could be changed to Contributor Spotlight or something similar. (E.g. GitHub has Maintainer Spotlight.)
Ask Travis and other present and past contributors if they would like to be featured. It could be a short bio or an interview (possible questions: why did they get involved with NumPy? how did it help them to advance their careers?).
Not everyone attending the call is convinced that the page is necessary.

*Get Help:*
Sidebar/section of Learn (it’s very short, refer to the sitemap).


**3. Content:**
<br>Ralf: 
<br>All the new content is available on github.com/numpy/numpy.org/tree/newsite/content. 

<br>Inessa:
- Suggested collaboration strategy: HackMD or Google Docs for the initial content generation and discussion, move to GitHub once finalized. 
- Contribute is far along, and some content for most of the pages, nothing pushed to GitHub yet.
        
**4. Translations:**
    <br>- Crowdin did not work with markdown.
    <br>- Get license to translate by paragraph so things work better (Ralf correct?)
    <br>- Focus on the website first.

**5. GitHub Actions:**
    Shekhar has been working on using it for deploying  

**6. Sphinx theme for documentation:** https://pr-19-scipy-sphinx-theme-v2.surge.sh/
    <br>- Same color-scheme and fonts as old one
    <br>- Make sure things are a bit unified between different sites. (Open an Issue)

**7. NumPy Logo:**
    A significant change to the logo should be postponed, maybe until the major release. Summer’s nontransparent version of the NumPy logo is viewed as satisfactory. The NumPy team appreciates everyone’s enthusiastic comments and contributions to this topic.


## Notes 
<!-- Other important details discussed during the meeting can be entered here. -->

