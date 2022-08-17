---
title: "Syncthing"
date: 2022-08-17T00:00:00-00:00
tags: 
- guides
- selfHosted
draft: false
---

[Syncthing](https://syncthing.net/)

# Mac
Install from [HomeBrew](https://brew.sh/)
```bash
brew install syncthing
```

Once Syncthing has been installed, run the following command to install it as a service and run automatically.
```bash
brew services start syncthing
```

In a web browser, type the following address to access the Syncthing Web GUI:
```bash
127.0.0.1:8384
```

