---
title: "Random String (GUID,UUID)"
date: 2022-05-12T17:46:39-03:00
---
UUIDs (Universally Unique IDentifier), also known as GUIDs (Globally Unique IDentifier), according to RFC 4122, are identifiers designed to provide certain uniqueness guarantees.

Here is a oneliner to create one in JS

```javascript
Math.random().toString(36).substring(2, 15) + Math.random().toString(36).substring(2, 15);
```

But there are several pitfalls to this JS only approch

* Invalid id format (UUIDs must be of the form "xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx", where x is one of [0-9, a-f] M is one of [1-5], and N is [8, 9, a, or b]
* Use of a low-quality source of randomness (such as Math.random)
