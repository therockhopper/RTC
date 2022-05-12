---
title: "List Git Conflicts"
date: 2022-05-12T17:46:39-03:00
---

Ever needed to list all the conflicted files in your repo after attempting a merge?

```
git diff --name-only --diff-filter=U
```
