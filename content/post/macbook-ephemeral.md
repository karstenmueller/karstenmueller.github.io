---
title: "MacBook as an ephemeral device"
date: 2020-03-19T15:27:40+01:00
tags: [code, macos]
---

## Bootstrap and configure a MacBook

Even my MacBook is becoming more and more ephemeral. Years ago I spent hours to get started on a new hardware. Nowadays I want it to be done quick and reproducible. And the less dependencies the better.

So ask yourself if your MacBook does survive the 10th floor test: "Can I grab a random machine and throw it out the tenth-floor window without adversely impacting users for more than 10 minutes?" [Bootstrapping an Infrastructure](http://www.infrastructures.org/papers/bootstrap/bootstrap.html).

I am using opensource software like [strap.sh](https://github.com/MikeMcQuaid/strap), [dotfiles](https://github.com/ryanb/dotfiles) and [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh). See [karstenmueller/macos-bootstrap](https://github.com/karstenmueller/macos-bootstrap). This is idempotent in some ways but could be improved. See the [modules](https://github.com/karstenmueller/macos-bootstrap/tree/main/modules) for a complete list of tasks.

As always easy does it, so
- Get a [GitHub access token](https://github.com/settings/tokens)
- Follow the [README](https://github.com/karstenmueller/macos-bootstrap/blob/main/README.md)

**Please** create pull requests on [karstenmueller/macos-bootstrap](https://github.com/karstenmueller/macos-bootstrap.git) if you want to change anything.

**Beware**: You should really fork my dotfiles repo and work from there.
