---
title: "Cron Task Loop"
date: 2022-05-12T17:46:39-03:00
---

When writing a cron/task it can be helpfull to batch
the task and run muitiple smaller runs.

```javascript
  static async start(docs]) {

      if (!docs) {
        docs = await this.getDocs()
      }

      // Cron Logic

      // Do we need to run again?
      docs = await this.getDocs()
      if (docs.length > 0) {
        console.log('More docs to process')
        this.start(docs)
      }
  }

```
