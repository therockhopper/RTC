---
title: "Waht is Plex Debrid?"
date: 2023-01-23T00:00:00-00:00
tags: 
- guides
- selfHosted
- mediaserver
draft: false
---

What is Plex Debrid and Why You Should Use It

If you're a Plex user, you've probably heard of Debrid services, but may not be entirely sure what they are or why you should use them. In this post, we'll explain what Plex Debrid is and why it's worth considering for your media streaming needs.

What is Plex Debrid?

Debrid services, also known as "premium link generators," allow you to access high-quality streaming links for your media content. These links are typically faster and more reliable than the free links that are available through regular streaming sources.

When you use a Debrid service with Plex, it enhances the capabilities of the Plex Media Server by allowing it to access these premium links. This means that when you're streaming content through Plex, the quality of the video and audio will be significantly better. Additionally, Debrid services often provide access to a wider range of content options, including new releases and hard-to-find titles.

Why Use Plex Debrid?

There are several reasons why you might want to consider using a Debrid service with Plex:

-   Improved streaming quality: As mentioned, Debrid links offer better quality video and audio than free streaming sources. This means that you'll have a more enjoyable viewing experience with less buffering and other issues.
    
-   Wider content options: Debrid services often provide access to a wider range of content options than free streaming sources, so you'll have more choices when it comes to what to watch.
    
-   Faster streaming speeds: Because Debrid links are generally faster and more reliable than free links, you'll have a smoother streaming experience.
    
-   Better organization: Many Debrid services offer features like automatic sorting and tagging of content, which can make it easier to find what you're looking for.
    
-   Enhanced security: Debrid services offer a level of security that free streaming sources can't match. You'll be less likely to run into malware, viruses, or other security threats.
    

How to Set Up Plex Debrid

Setting up Plex Debrid is relatively straightforward. First, you'll need to sign up for a Debrid service, such as Real-Debrid or AllDebrid. Once you have an account, you'll need to enter your login credentials into the Plex Media Server settings. From there, you'll be able to access the premium links provided by the Debrid service.

In conclusion, Plex Debrid is a great way to enhance your streaming experience and access a wider range of content options. With improved streaming quality, faster speeds, better organization, and enhanced security, it's definitely worth considering for your media streaming needs.

Learn more from the [Github Repo](https://github.com/itsToggle/plex_debrid)

TL;DR notes:
##### Windows setup
`rclone.exe cmount realdebrid: X: --dir-cache-time 10s --no-console`
`python ./main.py`