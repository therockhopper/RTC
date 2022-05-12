---
title: "Git Tags"
date: 2022-05-12T17:46:39-03:00
---

## Git has two types of tags
- lightweight (pointer to commit, nothing more)
- annotated (contains author,checksum,GPG)

A lightweight tag is very much like a branch that doesn’t change—it’s just a pointer to a specific commit

Annotated tags, however, are stored as full objects in the Git database. They’re checksummed; contain the tagger name, e-mail, and date; have a tagging message; and can be signed and verified with GNU Privacy Guard (GPG).

It’s generally recommended that you create annotated tags so you can have all this information; but if you want a temporary tag or for some reason don’t want to keep the other information, lightweight tags are available too

```
// Creating a annotated release tag
// '-m' specifies a tagging message
git tag -a v1.0.0 -m "my first release"
```

```
// Creating a lightweight release tag
// don't use -a,-s or -m option
git tag -a v1.0.0-RC
```

```
// View a certain tag
git show v1.0.0
```

Sometimes you release you should have tagged a release
a few commits ago. here is how you can tag a release based on an old commit
```
// Tag an old commit using its commit hash
git tag -a v1.0.1 abcde04
```

When you push your branch, your tags are not pushed with it.
You need to push your tags separately
```
// push all the tags we have created
git push origin --tags

// push one of the tags we have created
git push origin v1.0.0
```

Now anyone who clones or pulls from your remote repo will get all your tags as well.
