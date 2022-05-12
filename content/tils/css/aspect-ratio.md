---
title: "Aspect Ratio"
date: 2022-05-12T17:46:39-03:00
---
# Aspect Ratio now in Chrome Canary

new build of chrome canary v84ish enables the usage of the new `aspect-ratio` CSS property. Goodbye padding hacks for aspect ratios.

```css
/* Old hacky way */
.video {
  padding-top: 56.25%;
}

/* New cool way */
.video {
  aspect-ratio: 16 / 9;
}
```
