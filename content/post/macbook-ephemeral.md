---
title: "MacBook as an ephemeral device"
date: 2020-03-19T15:26:39+01:00
tags: [code, macos]
---

## Bootstrap and configure a MacBook

Even my MacBook is becvoming more and more ephemeral. Years ago I spent hours to get started on a new hardware. Nowadays I want it to be done quick and reproducible. And the less dependencies the better.

I make use of opensource software [strap.sh](https://github.com/MikeMcQuaid/strap), [dotfiles](https://github.com/ryanb/dotfiles) and [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh). See [karstenmueller/macos-bootstrap](https://github.com/karstenmueller/macos-bootstrap).

As always easy does it, so just get a [GitHub access token](https://github.com/settings/tokens) and setup some environment variables. Here we go:

~~~zsh
git clone https://github.com/karstenmueller/macos-bootstrap.git .bootstrap
cd .bootstrap
# used for configuring your box
export STRAP_GIT_NAME='John Doe'
export STRAP_GIT_EMAIL='john@example.com'
# used for accessing personal dotfiles repo
export STRAP_GITHUB_USER='johndoe'
export STRAP_GITHUB_TOKEN='861bf1x18b3729152942c86164ad6d46898e3233'
bash macos-bootstrap/run.sh
~~~

This will execute some tasks:

- fork my [dotfiles](https://github.com/karstenmueller/dotfiles) repository and clone your fork to ~/.dotfiles
- copy my dotfiles to $HOME
- configure macOS defaults
- install packages with [Homebrew](https://github.com/Homebrew/brew)
- setup zsh

**Please** create pull requests on [karstenmueller/macos-bootstrap](https://github.com/karstenmueller/macos-bootstrap.git) if you want to change anything.

**Beware**: You should fork my dotfiles repo and work from there.
