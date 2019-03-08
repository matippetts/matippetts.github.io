---
title: Discovering Netlify
author: Mark Tippetts
date: 2019-01-10
tags:
  - meta
  - JAMstack
  - headlessCMS
---
On [GitHub](https://github.com/matippetts):
- I created a repository named _matippetts.github.io_.
- I created a Gemfile with the following content:

``` ruby
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins
```

- I saved the Gemfile to a new `gh-pages` branch, thereby opening a new **Pull Request**.
- From the repository **settings** tab, I set the **GitHub Pages** theme to `Midnight`, which had the effect of creating a file named `_config.yml` with a single line:
``` yaml
theme: jekyll-theme-hacker
```

On [Netlify](https://app.netlify.com):
- I created a new site from Git.
- From the site **settings**:
  - I changed the site name to `matippetts-netlify-cms-jekyll`
  - I enabled the Identity plugin

The Netlify **Continuous Deployment** engine failed with the following error:
```
4:15:08 PM:    GitHub Metadata: Error processing value 'title':
4:15:08 PM:   Liquid Exception: No repo name found. \
Specify using PAGES_REPO_NWO environment variables, \
'repository' in your configuration, \
or set up an 'origin' git remote pointing to your github.com repository. \
in /_layouts/default.html
```

A little research on this came up with [a solution to a closed issue](https://github.com/jekyll/jekyll/issues/4705#issuecomment-200991736) on the jekyll repository on Github, which suggested adding the repository name to the `_config.yml` file.

Here is [a link](file:///home/mark/workspaces/professional-website/matippetts.github.io/_posts/2019-01-13-open-in-browser-PR.md) that should work.
