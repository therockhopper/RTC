---
title: "WSL Copy to Clipboard"
date: 2022-05-12T17:46:39-03:00
---

When running commands in WSL sometimes you want to copy the output to the clipboard.

```
# Copy contents of the file to windows clipboard
cat myfile.txt | clip.exe
```

using xclip would just copies it to the linux clipboard
