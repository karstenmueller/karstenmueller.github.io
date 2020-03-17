# Personal Github Pages blog with Hugo

![gh-pages](https://github.com/karstenmueller/karstenmueller.github.io/workflows/gh-pages/badge.svg?branch=master)

Edit, preview and publish Markdown Content as a website on GitHub pages.

## Initial Setup

### Create a new hugo site

~~~zsh
hugo new site .
~~~

### Setup Git repo

~~~zsh
rm -rf .git themes/bootstrap4-blog
git init
git add .
git commit -m 'initial commit'
git branch source
git co source
~~~

### Add a theme

I am using theme hugo-theme-bootstrap4-blog as a git submodule.

~~~zsh
git submodule add -f https://github.com/alanorth/hugo-theme-bootstrap4-blog.git themes/bootstrap4-blog
echo 'theme = "bootstrap4-blog"' >> config.toml
git commit -m 'added theme bootstrap4-blog'
~~~

## Setup GitHub Actions

Create a token and save it as a secret (Repo Setting -> Secrets). Use 'PUBLISH_TOKEN' as in [.github/workflows/gh-pages.yml](.github/workflows/gh-pages.yml)

Push it:

~~~zsh
git remote add origin https://github.com/karstenmueller/karstenmueller.github.io.git
git push -u origin source
~~~

## Configure Hugo

Either with one config.toml in the root directory or separated in environments in directory ./config.

## Create

Add a post "helloworld" as content/posts/helloworld.md

~~~zsh
hugo new posts/helloworld.md
~~~

Edit and review changes

~~~zsh
hugo server --buildDrafts
~~~

## Publish

Github Actions are used to run the deployment task. The remote run is triggered by pushing to the branch "source".
To trigger the deployment locally just type:

~~~zsh
./run deploy-local
~~~

## Requirements

- Publishing the website depends on [Hugo](https://github.com/gohugoio/hugo) and the [Bootstrap v4 theme](https://github.com/alanorth/hugo-theme-bootstrap4-blog)
- Local deployment depends on [act](https://github.com/nektos/act) which enables you to run your GitHub Actions locally.
