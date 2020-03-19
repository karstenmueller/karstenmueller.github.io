---
title: "Build a production ready serverless blog"
date: 2019-08-20
tags: [code]
---

## Setup with Hugo and GitHub Actions

Publishing a website has come a long way since the days of handcrafted HTML pages. Here is how to setup it 'serverless' :smirk:

Just by using an editor and install little tool it is possible to preview and publish a pretty decent website. And best of all: its blazingly fast. From pushing changes to published pages in about 10 seconds!

The workflow looks like this:

- create content by editing markdown files
- optionally preview changes locally just `hugo server --buildDrafts`
- push changes to github repo
- publish with Github Actions (see my [gh-pages.yml](https://raw.githubusercontent.com/karstenmueller/karstenmueller.github.io/source/.github/workflows/gh-pages.yml)) which renders HTML by using [hugo](https://gohugo.io) (my preferred static site generator)
- serve static pages with Github Pages

See my [karstenmueller.github.io](https://github.com/karstenmueller/karstenmueller.github.io) repo for the code.

It's quite fancy to blog from my iPad with [Working Copy](https://workingcopyapp.com)!
