---
title: "NPM Reverse search Dependencies"
date: 2022-05-12T17:46:39-03:00
---


I specifically wanted to find what package used a dependency that was breaking an initial install. This may help somebody out trying todo the same:
```
find ./node_modules/ -name package.json | xargs grep <the_package_name>
```
