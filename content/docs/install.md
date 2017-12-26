+++
date = 2016-04-20
lastmod = 2017-12-26
draft = false
# tags = ["academic", "hugo"]
title = "Install"
math = true
summary = """
Create a beautifully simple personal or academic website in under 10 minutes. 
"""

[menu.docs]
  parent = "setup"
  weight = 1

# [header]
# image = "headers/getting-started.png"
# caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"
+++

The following three methods describe how to install in the cloud using your web browser, how to install on your PC using the Command Prompt/Terminal app, and how to install with RStudio.

## Quick install using your web browser

1. [Install Academic with Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart)
    * Netlify will provide you with a customizable URL to access your new site
2. On GitHub, go to your newly created `academic-kickstart` repository and edit `config.toml` to personalize your site. Shortly after saving the file, your site will automatically update
3. Read the [Quick Start Guide]({{< ref "docs/get-started.md" >}}) to learn how to add Markdown content. For inspiration, refer to the [Markdown content](https://github.com/gcushen/hugo-academic/tree/master/exampleSite) which powers the [Demo](https://themes.gohugo.io/theme/academic/)

## Install on your PC

Prerequisites:

* [Download and install Git](https://git-scm.com/downloads)
* [Download and install Hugo](https://gohugo.io/getting-started/installing/#quick-install)

1. Clone (or [Fork](https://github.com/sourcethemes/academic-kickstart#fork-destination-box) or [download](https://github.com/sourcethemes/academic-kickstart/archive/master.zip)) the *Academic Kickstart* repository with Git:

        git clone https://github.com/sourcethemes/academic-kickstart.git My_Website
    
    *Note that if you forked Academic Kickstart, the above command should be edited to clone your fork.*

2. Initialize the theme:

        cd My_Website
        git submodule update --init --recursive

3. View your new website:
      
        hugo server

    Now you can go to [localhost:1313](http://localhost:1313) and your new Academic powered website should appear.
           
4. Read the [Quick Start Guide]({{< ref "docs/get-started.md" >}}) to learn how to add Markdown content, customize your site, and deploy it. For inspiration, refer to the [Markdown content](https://github.com/gcushen/hugo-academic/tree/master/exampleSite) which powers the [Demo](https://themes.gohugo.io/theme/academic/)

5. Build your site by running the `hugo` command and then [deploy it]({{< ref "docs/deployment.md" >}})

If you wish to initialise your site with the demo content, copy the contents of the `themes/academic/exampleSite` folder to your website root folder, overwriting existing files if necessary. The `exampleSite` folder contains an example config file and content to help you get started. The following command can be used to accomplish this:

        cp -av themes/academic/exampleSite/* .

## Install with RStudio

In RStudio IDE (v0.2+), install the *Blogdown* and *Hugo* dependencies:

```r
install.packages("blogdown")
blogdown::install_hugo()
```

Now restart RStudio and you can create an Academic project directly from the menu `File -> New Project -> New Directory` - see Figures 1 and 2 below:

{{< figure src="img/docs/rstudio-create-project.png" title="Create project" >}}
{{< figure src="img/docs/rstudio-project-type.png" title="Choose *website using Blogdown* as the project type" >}}

Enter `gcushen/hugo-academic` as the theme:

{{< figure src="img/docs/rstudio-theme.png" title="Choose the Academic theme" >}}

Then you will see a panel in RStudio named *Build* containing a *Build Website* button. When you click this button, RStudio will call `blogdown::build_site()` to build the website, automatically generating files in the `public/` folder.

Use `blogdown::serve_site()` to preview your site in your web browser. We recommend previewing your site in your normal web browser as the in-built RStudio web browser is very outdated and buggy.
