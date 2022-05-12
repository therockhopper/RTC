---
title: "Async Await Timeout"
date: 2022-05-12T17:46:39-03:00
---
sometimes you want to pause for a few seconds in a async
for loop to avoid hitting a rate limit. To do this easily we can create a async version of setTimeout to help us.

```javascript
const wait = time =>
  new Promise(resolve =>
    setTimeout(() => {
      return resolve(true)
    }, time),
  )

// Use the wait in a async loop etc
await wait(1000)
```
