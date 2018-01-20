+++
title = "Overview"

date = 2017-12-24
lastmod = 2018-01-20
draft = false

[menu.docs]
    parent = "deploy"
    identifier = "deployment"
    weight = 1
+++

Sites built using Academic can be deployed in a large variety of ways due to the static nature of the generated website. The recommended deployment method alongside a few of the other most popular techniques are described below.

If using Netlify, your site will be built automatically, otherwise run the `hugo` command in your terminal to generate your site in the `public/` folder - now it is ready to copy across to your host.

## Netlify

We recommend deploying your site with Netlify. Netlify is free and provides fast global access, automated deployment when you add or modify content, and one-click HTTPS security. [Check out our guide to deploy with Netlify]({{< ref "docs/install.md" >}}).

## GitHub Pages

Follow the instructions on deploying with GitHub Pages toward the end of [this blog post](https://georgecushen.com/create-your-website-with-hugo/).

## Amazon S3

By uploading the contents of your `public` folder to [Amazon S3](https://aws.amazon.com/s3/), your site can be served with dynamic scaling to almost unlimited traffic. This approach has the benefit of being one of the cheapest and most reliable hosting options available as you only pay for what you use.

## Web host via FTP

Use an FTP client to upload the contents of your `public` folder to a web host. This may be especially convenient for academic students and staff who are provided with university web space. 
