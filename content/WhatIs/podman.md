---
title: "What is Podman?"
date: 2023-01-23T00:00:00-00:00
tags: 
- guides
- selfHosted
draft: false
---
Podman and Docker are both containerization tools that allow developers to package and deploy applications in a portable and consistent way. However, there are some key differences between the two that make them better suited for different use cases.

One of the main differences between Podman and Docker is that Podman is a daemonless tool, while Docker requires a daemon to be running in order to function. This means that Podman does not require a daemon to be running in the background, making it more lightweight and easier to use in certain situations. Additionally, Podman does not require a root user to run, which can be a security benefit.

Another key difference between the two is that Podman supports rootless containers, which allows users to run containers without the need for root access. This can be useful for users who want to run containers on systems where they do not have root access. Docker, on the other hand, requires root access to run containers.

In terms of compatibility, Podman and Docker are largely interchangeable. Both tools use the same container image format, and both can use the same container registries. This means that users can easily switch between the two tools without having to rebuild their container images.

In terms of support, Docker is the more established of the two, with a larger community and more extensive documentation. However, Podman is gaining popularity and support, and is considered to be a more secure and efficient alternative to Docker.

Ultimately, whether you choose to use Podman or Docker will depend on your specific use case and requirements. Both tools have their own unique advantages, and it's worth experimenting with both to see which one works best for you.

In summary, Podman and Docker are both containerization tools, but Podman is a daemonless tool that can run without root access and supports rootless containers, while Docker requires a daemon to be running and need root access to run containers. Podman and Docker are largely interchangeable and both tools use the same container image format, but Docker is the more established of the two.