---
title: "What is Syncthing?"
date: 2022-08-17T00:00:00-00:00
tags: 
- guides
- selfHosted
draft: false
---
What is Syncthing and How to Use it for File Synchronization

Syncthing is an open-source, peer-to-peer file synchronization tool that allows you to easily share and sync files across multiple devices. It's a great alternative to cloud-based file syncing services like Dropbox, Google Drive, and OneDrive, as it allows you to keep your data on your own devices and under your own control.

What is Syncthing?

Syncthing is a decentralized file syncing tool that runs on Windows, Mac, Linux, and other platforms. It allows you to easily share and synchronize files across multiple devices, without the need for a centralized server or cloud service. Instead, Syncthing uses peer-to-peer technology to connect devices directly, which means that your data is always under your own control.

One of the key features of Syncthing is that it allows you to specify which folders you want to sync, and with which devices. This means that you can set up different sync relationships for different devices and folders, giving you fine-grained control over your data.

Why Use Syncthing?

There are several reasons why you might want to consider using Syncthing for your file syncing needs:

-   Keep your data under your own control: With Syncthing, your data is always stored on your own devices, rather than on a centralized server or cloud service. This means that you have complete control over your data, and don't have to worry about it being accessed or used by a third party.
    
-   Fine-grained control over syncing: Syncthing allows you to specify which folders you want to sync, and with which devices. This gives you greater control over your data and allows you to set up different sync relationships for different devices.
    
-   Cross-platform support: Syncthing runs on Windows, Mac, Linux, and other platforms, so you can use it to sync files between different types of devices.
    
-   Open-source: Syncthing is open-source software, which means that it's free to use and can be modified and distributed by anyone.
    

How to Set Up Syncthing

Setting up Syncthing is relatively straightforward. First, you'll need to download and install the Syncthing software on all the devices that you want to sync. Once you have it installed, you'll need to create an account and sign in to Syncthing on each device.

Once you're signed in, you'll be able to specify which folders you want to sync and with which devices. To do this, you'll need to create a "folder" on one device, and then "share" it with the other devices. The shared folder will then be synced across all the devices that have access to it.

In conclusion, Syncthing is a great alternative to cloud-based file syncing services that allows you to keep your data under your own control. With its cross-platform support, fine-grained control over syncing and open-source nature, it is a versatile and powerful tool that can be used by anyone to keep their files in sync across multiple devices.

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

