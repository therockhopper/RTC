---
title: "Lightning ES5 Regenerator Runtime Error"
date: 2022-05-12T17:46:39-03:00
---

When running `lng dist --es5` the Lightning SDK might spit back an error like regenerator runtime is undefined. To resolve this issue you need to install the "regenerator-runtime" package via `npm i regenerator-runtime`.

Simple error simple fix, just no docs for it. It is only an issue when targeting ES5 builds. So unless you are doing a Tizen 2017 build you may never have to do a ES5 build with Lightning.
