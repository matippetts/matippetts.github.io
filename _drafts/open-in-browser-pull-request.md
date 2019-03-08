---
title: Opened Pull Request for open-in-browser Atom plugin
author: Mark Tippetts
date: 2019-01-13
tags: meta
---
Software bugs. Nobody loves them. Not users, and not programmers. One of the oft-touted advantages of Open Source software is the principle that, "Many hands make light work." Because anybody can read the code, and in principle anybody can improve the code, bugs will get zapped early and often. This was [codified](http://www.catb.org/~esr/writings/cathedral-bazaar/cathedral-bazaar/ar01s04.html) by Eric Raymond in his famous manifesto _The Cathedral and the Bazaar_ as [Linus's Law](https://en.wikipedia.org/wiki/Linus%27s_Law): "given enough eyeballs, all bugs are shallow."

This almost-as-oft-disputed principle has its detractors, especially among security analysts.


While working on this blog, I've repeatedly encountered [an open issue](https://github.com/magbicaleman/open-in-browser/issues/47). I'll be using Atom to edit a markdown file, such as the one I'm writing right now. (`tags: meta`) If I right-click a link in Markdown Preview and then


This is not a problem in open-in-browser. It's a

Here's the (entirely typical) description of the problem in the initial bug report:

> [Enter steps to reproduce:]
>
> 1. ...
> 2. ...

It's funny because it's true. You may recognize this text from `./github/ISSUE_TEMPLATE/bug_report.md`.

As [the above stack-trace](https://github.com/magbicaleman/open-in-browser/issues/47#issuecomment-444527365) demonstrates, the problem occurs when `atom.workspace.getActiveTextEditor()` returns `undefined` in [`lib/open-in-browser.coffee:15`](https://github.com/magbicaleman/open-in-browser/blob/0ab814320f8f27ab22624a590b84d96dd55e14bf/lib/open-in-browser.coffee#L15):
``` coffee
getFilePath: -> atom.workspace.getActiveTextEditor().getPath()
```
