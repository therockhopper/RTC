---
title: "Csv to Json"
date: 2022-05-12T17:46:39-03:00
---

```
# Install requirements
brew install jq && npm i -g csvtojson

# Convert the csv and save it as json
csvtojson ./myCsv.csv | jq . > myJson.json
```
