---
title: "Loading Javascript can stop your CSS animation from running"
date: 2022-07-10T12:46:39-03:00
tags: 
- CSS
- OTT
draft: true
---

I mean, put a <script> tag on your page, and the CSS animation stops

It is a CSS keyframe animation.

Yeah, we load a <script> that takes ~15s to parse eval and finish on our TV.

I thought CSS animations for some reason were run on a different thread.

will-change: background-position didn't work.

From what I read, anything that requires coordination to repaint will not work.


So only properties that can be recomposed without requiring a repaint will work if the JS thread is busy.

So things like opacity, transformation, etc.

And the reason why is that one of the components that is asked and everything waits on for repainting, is the JS engine.

Which is why "long tasks" is such a warned about thing in the developer console.

