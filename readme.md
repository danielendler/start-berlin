[![Netlify Status](https://api.netlify.com/api/v1/badges/61edd30c-8a04-4bc5-9e52-b10361bb39f4/deploy-status)](https://app.netlify.com/sites/unruffled-kepler-1b05f1/deploys)

# About

This mini page is hoasted on https://berlin.endler.cc.
It is based on [Hugo](https://gohugo.io/) and deployed via [Netflify](https://www.netlify.com/).

As a theme, it uses [Jane](https://github.com/xianmin/hugo-theme-jane).

# Installation

On a Mac:

1. Install hugo:  `brew install hugo`
2. Clone this repo `git clone https://github.com/danielendler/start-berlin`
3. Start hugo with draft mode on: `hugo server -D`
4. Navigate to http://localhost:1313/ to access your site

For more details please read [getting started on Hugo](https://gohugo.io/getting-started/quick-start/).

# Content 
Hugo creates static websites based on markdown files.

## Content structure

The content of the page is multi-lingual, namely in `en` and in `de`.
The content is structured in the `content` folder.
All the files need to exist in both folders, for the multi-lingual set-up to be identified.

```
.
├── content
│   ├── de
│   │   ├── _index.md
│   │   ├── donate.md
│   │   ├── family.md
│   │   ├── legal
│   │   │   ├── imprint.md
│   │   │   └── privacy-policy.md
│   │   ├── project.md
│   │   ├── sponsors.md
│   │   └── updates
│   └── en
│       ├── _index.md
│       ├── donate.md
│       ├── family.md
│       ├── legal
│       │   ├── imprint.md
│       │   └── privacy-policy.md
│       ├── project.md
│       ├── sponsors.md
│       └── updates
├── data
├── layouts
├── static
├── themes
└──...

```

## Content pieces

Each content piece (each markdown file) has a header and then the content itself.
As an example, the file (`de/project.md`) has the following header:
```
---
title: "Projekt"
date: 2021-09-08
menu: "main"
weight: -10
---

# Wie es anfing
--> content here
```

Just place your content under the `---` area.

## Links between content pieces

You can add links to others peices of content through this code: 
```
[Sponsors]({{< ref "sponsors" >}} )
  └ Name link          └ File name
```

You can slo link directly to an achor on a site by using:
```
[Sleman's]({{< ref "sponsors#sleman" >}} ) 
   └ Name link        └ File    └ anchor
```

# Deployment
Netflify is configured to always deploy on every push to the `main` branch. The badge above shows if the deployment was successful.