---
title: Debugging Atom
author: Mark Tippetts
---
I want to clear up a possible source of confusion right at the start: the difference between debugging _in_ Atom and debugging Atom _itself_. Atom is a programmer's text-editor, with all the features of a traditional IDE available as extensions. This includes the ability to build, run, and debug applications and scripts in a number of languages. That is debugging _in_ Atom, and it is **not** what this article is about. Instead, I want to talk about debugging Atom _itself_, usually in the context of creating plugins for Atom.

The main interface for debugging Atom is [Chrome Dev Tools](https://developers.google.com/web/tools/chrome-devtools/). This makes sense given Atom's architecture as a collection of plugins for [Electron]. Electron gets its name from the fact that it's a _shell_ -- in two senses:
- In the first sense, Electron is a framework for applications that run inside a window in a desktop environment, where the outermost frame of the user interface is traditionally called a Shell.
- In the second sense, Electron is basically just a wrapper around two other applications, which are themselves containers. Inside the Electron shell are a Chromium web browser -- for running front-end code -- and a NodeJS server -- for running back-end code.

The architecture of Atom provides developers with access to a stack of APIs, where the higher-level members of the stack extend the functionality of lower-level members:
- [Atom API](https://atom.io/docs/api/v1.34.0/AtomEnvironment) (v1.34.0)
- [Electron API](https://electronjs.org/docs/api)
- [Node API](https://nodejs.org/dist/latest-v11.x/docs/api/) (v11.7.0)
- Web APIs:
  - [on MDN](https://developer.mozilla.org/en-US/docs/Web)
  - [at Google](https://developers.google.com/web/fundamentals/)
