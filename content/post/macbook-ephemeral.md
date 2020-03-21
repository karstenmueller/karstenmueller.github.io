---
title: "MacBook as an ephemeral device"
date: 2020-03-19T15:26:39+01:00
tags: [code, macos]
---

## Bootstrap and configure a MacBook

Even my MacBook is becvoming more and more ephemeral. Years ago I spent hours to get started on a new hardware. Nowadays I want it to be done quick and reproducible. And the less dependencies the better.

I am using [strap.sh](https://github.com/MikeMcQuaid/strap), [dotfiles](https://github.com/ryanb/dotfiles) and [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh).

As always easy does it, so just setup some environment variables and run [install.sh](https://raw.githubusercontent.com/karstenmueller/dotfiles/master/script/install.sh)

~~~zsh
# used for configuring your box
export STRAP_GIT_NAME='John Doe'
export STRAP_GIT_EMAIL='john@example.com'
# used for accessing personal dotfiles repo
export STRAP_GITHUB_USER='johndoe'
export STRAP_GITHUB_TOKEN='861bf1x18b3729152942c86164ad6d46898e3233'
~~~

~~~zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/karstenmueller/dotfiles/master/script/install.sh)"
~~~

This will execute some tasks:

- clone my [dotfiles](https://github.com/karstenmueller/dotfiles) repository to ~/.dotfiles
- copy my dotfiles to $HOME
- install some packages with [Homebrew](https://github.com/Homebrew/brew)
- configure some macOS defaults
- setup zsh

**Beware**: you better fork my dotfiles repo and work from there.
