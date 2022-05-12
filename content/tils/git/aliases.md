---
title: "Git Aliases"
date: 2022-05-12T17:46:39-03:00
---
Git allows you to setup aliases to reduce the amount of charcheters you have to type to execute a command or even to create some commands you might think git is missing

Below are some super common alias I like to use in my own git configs
```
// Create a global alias for checkout
git config --global alias.co checkout

// Create a global alias for branch
git config --global alias.br branch

// Create a global alias for branch
git config --global alias.last 'log -1 HEAD'

// alias to make unstaging files easy
// `git unstage file` is now the same
// as `git reset HEAD file`
git config --global alias.unstage 'reset HEAD'

```

But what if you want to run an external command?
you then start the command with `!`

```
git config --global alias.visual "!gitk"
``
