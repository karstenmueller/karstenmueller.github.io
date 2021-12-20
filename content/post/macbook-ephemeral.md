---
title: "MacBook as an ephemeral device"
date: 2020-03-19T15:26:40+01:00
tags: [code, macos]
---

## Bootstrap and configure a MacBook

Even my MacBook is becvoming more and more ephemeral. Years ago I spent hours to get started on a new hardware. Nowadays I want it to be done quick and reproducible. And the less dependencies the better.

So ask yourself if your MacBook does survice the 10th floor test: "Can I grab a random machine and throw it out the tenth-floor window without adversely impacting users for more than 10 minutes?" [Bootstrapping an Infrastructure](http://www.infrastructures.org/papers/bootstrap/bootstrap.html).

I am using opensource software like [strap.sh](https://github.com/MikeMcQuaid/strap), [dotfiles](https://github.com/ryanb/dotfiles) and [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh). See [karstenmueller/macos-bootstrap](https://github.com/karstenmueller/macos-bootstrap). This really should be more idempotent, but it is not so much. 

As always easy does it, so just get a [GitHub access token](https://github.com/settings/tokens) and setup some environment variables. Here we go:

First set some Environemnt variables (execute all following commands in one shell session):

~~~zsh
# used for configuring your box
export STRAP_GIT_NAME='John Doe'
export STRAP_GIT_EMAIL='john@example.com'
# used for accessing personal dotfiles repo
export STRAP_GITHUB_USER='johndoe'
export STRAP_GITHUB_TOKEN='gh_XXX'
~~~

Create a fork of my [dotfiles](https://github.com/karstenmueller/dotfiles) repository and clone it:
~~~zsh
git clone https://github.com/STRAP_GITHUB_USER/dotfiles .dotfiles
~~~

~~~zsh
git clone https://github.com/karstenmueller/macos-bootstrap.git .bootstrap
cd .bootstrap
bash run.sh
~~~

This will execute some tasks:
- create links of .dotfiles/ to $HOME
- configure macOS defaults
- install packages with [Homebrew](https://github.com/Homebrew/brew)
- setup zsh
- [ ... ] 

See [modules](https://github.com/karstenmueller/macos-bootstrap/tree/main/modules) for a complete list of tasks.

**Please** create pull requests on [karstenmueller/macos-bootstrap](https://github.com/karstenmueller/macos-bootstrap.git) if you want to change anything.

**Beware**: You should really fork my dotfiles repo and work from there to be able to keep changes you make in your personal repository.
