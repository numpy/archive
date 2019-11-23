# 2019-09-23 NumPy Web Team Meeting

**Present:** Ralf, Inessa, Joe, Matti, Sebastian, Hameer



# Agenda

1. Status of the `newsite` branch.
2. Website structure - site map: https://app.flowmapp.com/share/e1b61759a5f95f43d8907baedf42875d/
3. Status of content creation.
4. Status of translations with Crowdin.
5. GitHub Actions needs approval. 




# Minutes

**1. NumPy.org (Hugo generated):**
<br>The latest version is stored here: https://github.com/numpy/numpy.org/tree/newsite

README.md explains how to run the new website. Don't forget *git* submodulee in it, make sure to update.
    
The current graphic design elements are copyrighted by freepikcompany.com, licensed to NumPy for free. For full details please refer to freepikcompany.com/legal#nav-freepik, Section 8 *License Agreement for Freepik Content*.

**2. Website Structure:**
The structure of the individual pages (templates) is still under development, to be finalized after the content creation stage has been completed.

*Navigation of the second level pages:*
A side bar is a better UX choice, refrain from using drop-down menus, which are not user friendly.

*NumPy Hall of Fame:*
The page NumPy Hall of Fame is a working title, could be changed to Contributor Spotlight or something similar (e.g. GitHub has Maintainer Spotlight).
Ask Travis and other present and past contributors if they would like to be featured. It could be a short bio or an interview (possible questions: why did they get involved with NumPy? how did it help them to advance their careers?).
Not everyone attending the call is convinced that the page is necessary.

*Get Help:*
Sidebar/section of Learn (it’s very short, refer to the sitemap).


**3. Content:**

Ralf: 
<br>All the new content is available on github.com/numpy/numpy.org/tree/newsite/content. 

Inessa:
- Suggested collaboration strategy: HackMD or Google Docs for the initial content generation and discussion, move to GitHub once finalized. 
- Contribute is far along, and some content for most of the pages, nothing pushed to GitHub yet.
        
**4. Translations:**

- Crowdin did not work with markdown. A possible solution: to purchase a subscription to translate by paragraph for better results.
    
- Focus on the website high-level content first.

**5. GitHub Actions:**
    Approved for the deployment. Shekhar is already using it.  

**6. NumPy Documentation (Sphinx generated):** 

The latest version is available here: https://pr-19-scipy-sphinx-theme-v2.surge.sh/

Uniformity in the Hugo and Sphinx template design of numpy.org is desired. At the very least the same color scheme (https://user-images.githubusercontent.com/98330/63642399-51f41480-c673-11e9-8d22-20315b71c83e.jpg) and fonts must be used.
Opened issue #48 (github.com/numpy/numpy.org/issues/48).
    

**7. NumPy Logo:**
    A significant change to the logo should be postponed, maybe until the major release. Summer’s nontransparent version of the NumPy logo is viewed as satisfactory. The NumPy team appreciates everyone’s enthusiastic comments and contributions to this topic.
