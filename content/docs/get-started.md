+++
date = 2016-04-20
lastmod = 2017-09-03
draft = false
# tags = ["academic", "hugo"]
title = "Getting started"
math = true
summary = """
Create a beautifully simple personal or academic website in under 10 minutes. 
"""

aliases = ["post/getting-started/"]

[menu.docs]
    parent = "setup"
    weight = 20


# [header]
# image = "headers/getting-started.png"
# caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"
+++

In this section, we will explore some of the common options for customizing your site.

## Core parameters

The core parameters for the website can be edited in the `config.toml` configuration file:

- Set `baseurl` to your website URL (we recommend [GitHub Pages](https://georgecushen.com/create-your-website-with-hugo/) for free hosting)
- Set `title` to your desired website title such as your name
- The example Disqus commenting variable should be cleared (e.g. `disqusShortname = ""`) or set to your own [Disqus](https://disqus.com/) shortname to enable commenting
- Edit your details under `[params]`; these will be displayed mainly in the homepage *about* and *contact* widgets (if used). To disable a contact field, simply clear the value to `""`. 
- Place a square cropped portrait photo named `portrait.jpg` into the `static/img/` folder, overwriting any defaults. Note that you can edit the `avatar` filepath to point to a different image name or clear the value to disable the avatar feature. Alternatively, set `gravatar` to `true` to use the Gravatar/Wordpress avatar associated with your `email` address.
- To enable LaTeX math for your site, set `math = true`
- Social/academic networking links are defined as multiples of `[[params.social]]`. They can be created or deleted as necessary.

## Introduce yourself

Edit your biography in the *about* widget `content/home/about.md` that you copied across from the `themes/academic/exampleSite/` folder. The research interests and qualifications are stored as `interests` and `education` variables. The academic qualifications are defined as multiples of `[[education.courses]]` and can be created or deleted as necessary. It's possible to completely hide the interests and education lists by deleting their respective variables.

## Customize the homepage

Refer to our guide on using [widgets]({{< ref "widgets.md" >}}) to customize your homepage.

## Add your content

Refer to our guide on [managing content]({{< ref "docs/managing-content.md" >}}) to create your own publications, blog posts, talks, and projects.

## Remove unused widgets and pages

[How to remove unused widgets and content pages]({{< ref "docs/managing-content.md#removing-content" >}}).

## Themes

Check out the [available color themes]({{< ref "themes.md" >}}) and set the theme using  the `color_theme` option in `config.toml`.

The following font styles are available and can be set by the `font` option in `config.toml`:

- default (modern)
- classic (original Academic v1 style)
- playfair (serif)
