---
title: "Evaluation of Javascript can stop your CSS animation from running"
date: 2022-08-09T00:00:00-00:00
tags: 
- CSS
- OTT
draft: false
---
When building a splash screen for a OTT application we decided to try switching from a canvas animation to a CSS keyframe animation that would
be replaced by our app running in a canvas after the animation was complete.

Problem was when the browser would take ~15s to evaluate our script (large player deps), so our keyframe CSS animation would pause until the evaluation was complete.
This is because certain CSS props (opacity, transformation, etc.) force a browser re-paint.

Which is why "long tasks" is such a warned about thing in the developer console.

