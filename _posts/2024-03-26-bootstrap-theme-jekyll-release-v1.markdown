---
title: "Released NOCC Jekyll Bundle"
layout: post
comments: true
date: 2024-03-26 11:10:45 +0200
categories: jekyll bootstrap theme
tags:
- nocc
- theme
- bootstrap
background: '/assets/images/bg-post.webp'
---

{:.text-center}
![NOCC Jekyll Bundle webshots](/assets/images/nocc-showcase.webp){:.img-fluid}

[NOCC Jekyll Bundle](https://bootstrap-theme.notesoncloudcomputing.com/). A fully featured bundle site for [Jekyll](https://jekyllrb.com/){:target="_blank"} created by [Carles Loriente](https://github.com/carlesloriente).
Containing a homepage, about page, tags cloud page, gallery of images page, examples post pages with comments powered by [Disqus](https://disqus.com/){:target="_blank"}, and a contact form powered by [Formspree](https://formspree.io/){:target="_blank"}.
Using the [NOCC Bootstrap theme](https://www.npmjs.com/package/nocc-bootstrap-theme) npm package.

## Features

1. **A complete website ready to roll out**
2. **It uses a theme build for Bootstrap 5**
3. **Local and remote environments built-in**
4. **Extensive use of SVG and WeBP**
5. **Static site with dynamic features**

## Installation

Just follow the instructions below, and then you can change the content of the pages and site settings.

- [Download the package](https://github.com/carlesloriente/bootstrap-theme-jekyll/archive/refs/heads/main.zip) or clone the project running the command:

{% include code_block.html lang="bash" content='git clone --recursive git@github.com:carlesloriente/bootstrap-theme-jekyll.git' %}

- Install the NOCC npm package, run the command:

{% include code_block.html lang="bash" content='npm install nocc-bootstrap-theme --save' %}

- Install Ruby Gems and other dependencies, run the command:

{% include code_block.html lang="bash" content='sh bin/install.sh' %}

## Configuration

1. Update with your settings the configuration file `_config.yml`:
   - `landing` (Setting for the theme landing site, please set to `false`)
   - `title`
   - `author`
   - `url`
   - `timezone`
   - `description`
   - `full_description` (Setting for the theme landing site, please set to `false`)
   - `gh_repository` (Optional; if not needed, comment it out)
   - `email` (Set to a working email address, and then if you want to enable the contact form, create a free account at [Formspree](https://formspree.io){:target="_blank"})
   - `formemail` (fill in with your Formspree code; after that, fill out and send the form on the contact page, check your email and verify if you are receiving the messages)
   - `twitter_username` (Optional; if not needed, comment it out)
   - `github_username` (Optional; if not needed, comment it out)
   - `facebook_username` (Optional; if not needed, comment it out)
   - `instagram_username` (Optional; if not needed, comment it out)
   - `linkedin_username` (Optional; if not needed, comment it out)
   - `kofi` (Optional; if not needed, comment it out)
   - `google_site_verification` (Optional; if not needed, comment it out)
   - `google_analytics` (Optional; if not needed, comment it out)
   - `disqus_shortname` (To enable the comments feature, create a free account at [Disqus](https://disqus.com){:target="_blank"}, and fill in with your disqus shortname, if not needed, comment it out)

### Add your content

You need to create new posts/articles inside the folder named `_posts`. The files should be in markdown format. Use one of the sample files to learn more about the syntax and [Front Matter](https://jekyllrb.com/docs/front-matter/) settings. Remove the unwanted files.

### Test your site locally

Use the Jekyll build and web server command `bundle exec jekyll serve` or set up the local development environment (*recommended*).

#### Configure local environment

Suppose you want to use HTTPS in your environment and eliminate browser warnings when developing. In that case, the bundle comes with handy pre-generated certs.

Navigate to folder `bin/certs` and execute the following command to validate certs and update the CA trust DB.

{% include code_block.html lang="bash" content='openssl verify -CAfile ca_selfsigned.crt wildcard.local.crt && sudo cp ca_selfsigned.crt /etc/pki/ca-trust/source/anchors/ && sudo update-ca-trust' %}

- Modify your /etc/hosts file adding `127.0.0.1 bootstrap-theme.local`. Depending on your setup, there will already be an entry for 127.0.0.1; add bootstrap-theme.local after the last argument.
- Execute the command `sh bin/build-local.sh`, which will build the site files, launch the Webrick web server using the `_site_local` folder as webroot, and open your browser.
- For the first time only, you must make your browser trust the wildcard domain cert.
  - Mozilla Firefox: After opening the URL `https://bootstrap-theme.local:8000`, the message "Warning: Potential Security Risk Ahead" is shown; click the `Advanced` button and then `Accept Risk & Continue`.

> **&#9432;** Check this gist to create your own CA and wildcard cert.

### Host your site

#### in GitHub-Pages

You can host your site using GitHub Pages. Follow the [official guide](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

> **&#9432;** GitHub Pages hosting is free; you need an account and repository.

#### in Amazon S3 bucket

You can host the site using an S3 Bucket; please follow the [AWS guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html).

## Bugs and Issues

Have a bug or an issue with this template? [Open a new issue](https://github.com/carlesloriente/bootstrap-theme-jekyll/issues) here on GitHub!

## Contributing

New contributors are always welcome! Check out [CONTRIBUTING.md](https://github.com/carlesloriente/bootstrap-theme-jekyll/blob/main/CONTRIBUTING.md) to get involved.

## About

**[Carles Loriente](https://www.linkedin.com/in/carles-loriente/)** is the creator and maintainer of the NOCC Jekyll Bundle and the NOCC Bootstrap theme.

- [Linkedin](https://www.linkedin.com/in/carles-loriente)
- [Twitter](https://twitter.com/godarthvader)
- [GitHub](https://github.com/carlesloriente)

[Bootstrap 5](https://getbootstrap.com/) framework created by [Mark Otto](https://twitter.com/mdo) and [Jacob Thorton](https://twitter.com/fat).

## Copyright and License

Copyright (c) 2024 Carles Loriente. The code released under the [MIT](https://github.com/carlesloriente/bootstrap-theme-jekyll/blob/main/LICENSE) license.
