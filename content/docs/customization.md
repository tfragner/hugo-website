+++
date = 2016-04-20
lastmod = 2017-09-03
draft = false
# tags = ["academic", "hugo"]
title = "Customization"
math = true
summary = """
Create a beautifully simple personal or academic website in under 10 minutes. 
"""

aliases = ["post/getting-started/"]

[menu.docs]
    parent = "setup"
    weight = 30

# [header]
# image = "headers/getting-started.png"
# caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"
+++

It is possible to carry out many customizations without touching any files in `themes/academic`, making it easier to update the framework in the future.

## Navigation menu

The `[[menu.main]]` entries towards the bottom of `config.toml` define the navigation links at the top of the website. They can be added or removed as desired.

To create a dropdown sub-menu, add `identifier = "something"` to the parent item and `parent = "something"` to the child item.

## Website icon

Save your main icon and mobile icon as square PNG images named `icon.png` (32x32 pixels) and `icon-192.png` (192x192 pixels), respectively. Place them in your root `static/img/` folder.

## Analytics

To enable [Google Analytics](http://www.google.com/analytics), add your tracking code in `config.toml` similarly to `googleAnalytics = "UA-12345678-9"`.

## Third party and local scripts (JS)

To add a third party script, create a file named `head_custom.html` in a `layouts/partials/` folder at the root of your website (not in the `themes` folder). Any HTML code added to this file will be included within your website's `<head>`. Therefore, it's suitable for adding custom metadata or third party scripts specified with the *async* attribute.

Whereas for your own local scripts, you can link your local JS assets (relative to your root `static/js`) from your `config.toml` using `custom_js  = ["custom.js"]`.

## Language and translation

The interface text (e.g. buttons) is stored in language files which are collected from Academic's `themes/academic/i18n/` folder, as well as an `i18n/` folder at the root of your project.

To edit the interface text, copy `themes/academic/i18n/en.yaml` to `i18n/en.yaml` (relative to the root of your website). Open the new file and make any desired changes to the text appearing after `translation:`. Note that the language files are formatted in YAML syntax.

To translate the interface text to another language, follow the above instructions, but name the new file in the form `i18n/X.yaml` where `X` is the appropriate [ISO/RFC5646 language identifier](http://www.w3schools.com/tags/ref_language_codes.asp) for the translation. Then follow the brief instructions in the *Language* section at the bottom of your `config.toml`. To change the default language used by Academic, set `defaultContentLanguage` to the desired language identifier in your configuration file.

To translate the navigation bar, you can edit the default `[[menu.main]]` instances in `config.toml`. However, for a multilingual site, you will need to duplicate all of the `[[menu.main]]` instances and rename the new instances from `[[menu.main]]` to `[[Languages.X.menu.main]]`, where `X` is the language identifier (e.g. `[[Languages.zh.menu.main]]` for Simplified Chinese). Thus, the navigation bar can be displayed in multiple languages.

To translate a content file in your `content/` folder into another language, copy the file to `filename.X.md` where `filename` is your existing filename and `X` is the appropriate [ISO/RFC5646 language identifier](http://www.w3schools.com/tags/ref_language_codes.asp) for the translation. Then translate the content in the new file to the specified language.

For further details on Hugo's internationalization and multilingual features, refer to the [associated Hugo documentation](https://gohugo.io/content/multilingual/).

## Permalinks

*Permalinks*, or *permanent links*, are URLs to individual pages and posts on your website. They are permanent web addresses which can be used to link to your content. Using Hugo's *permalinks* option these can be easily customized. For example, the blog post URL can be changed to the form *yourURL/2016/05/01/my-post-slug* by adding the following near the top of your `config.toml` (before `[params]` settings):

    [permalinks]
        post = "/:year/:month/:day/:slug"

Where `:slug` defaults to the filename of the post, excluding the file extension. However, slug may be overridden on a per post basis if desired, simply by setting `slug = "my-short-post-title"` in your post preamble.

**Example 2:** let's consider changing the URL path of posts from `post/` to `blog/`. First, add the following parameters right above the `[params]` section of your `config.toml`:
```
[permalinks]
    post = "/blog/:slug"
```
Then add `aliases = ["/blog/"]` to your post archive page `post/_index.md` so that it can be accessed from the */blog/* URL.

## Advanced style customization (CSS)

For advanced customization of the style, you can link custom CSS assets (relative to your root `static/css`) from your `config.toml` using `custom_css = ["custom.css"]`.

For example, let's override some of Academic's default styles. First, define `custom_css = ["override.css"]` in `config.toml`. Then we can create the file `static/css/override.css`, relative to your website root (i.e. **not** in the `themes` directory). Add your custom CSS to this file.
