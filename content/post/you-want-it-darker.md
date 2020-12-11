---
title: "You Want it Darker"
date: 2020-12-11
tags: [tools]
---

Most of my work involves using a terminal application on macOS. Having used iTerm2 for quite a long time I recently switched to [Alacritty](https://github.com/alacritty/alacritty). Why? Because it is very sleak simple and fast!

My favorite color theme [nord](https://github.com/arcticicestudio/nord-iterm2) is quite dark so it's easy to the eyes and matches the 'mood of 2021' too 😒

Looks like this:
![image alt text](/2021/12/darker.png)

You need a thing or two to make this work:

- Install alacritty and a decent font

~~~shell
brew install alacritty
brew install --cask font-source-code-pro-for-powerline
~~~~

- Create a config file at `~/.alacritty.yaml`. Here is my config:

{{< gist karstenmueller 48595c3c43673583ebc8c766ce2f0847 >}}
