---
title: "do-release-upgrade: command not found"
date: 2022-04-21
authors:
  - dgibbs
image: /images/blog/2022-04-21-jammy-jellyfish-wallpaper-840x473.jpg
---

If you encounter the error `do-release-upgrade: command not found` while attempting to upgrade from _Ubuntu 20.04_ to _Ubuntu 22.04_, you can use the following command to resolve the issue:

```
sudo apt install sudo do-release-upgrade
```

This will install the necessary package to enable you to perform the upgrade. Once the package is installed, you can use the following command to upgrade to Ubuntu 22.04:

```
sudo do-release-upgrade -d
```
