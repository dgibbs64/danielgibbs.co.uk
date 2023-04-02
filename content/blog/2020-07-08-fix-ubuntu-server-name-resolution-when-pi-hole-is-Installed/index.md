---
title: "Fix Ubuntu Server Name Resolution when Pi-Hole is Installed"
date: 2020-07-07
categories:
  - gaming
tags:
  - pi-hole
  - ubuntu
  - server
authors:
  - dgibbs
image: pi-hole-screenshot.png
---

After installing Pi-Hole on an Ubuntu server, I discovered that the server itself could no longer resolve DNS. I was unsure how to fix this until I stumbled upon a similar issue while researching LAN Cache. It remains unclear if this problem affects the standard installation as well as the Pi-Hole docker container.

For reference, here is the solution provided by lancache.net to disable systemd-resolved's DNSStubListener:

Edit the file /etc/systemd/resolved.conf using a text editor such as nano or vi:

```bash
sudo nano /etc/systemd/resolved.conf
```

Change the line that starts with #DNSStubListener= to DNSStubListener=no (make sure to remove the #).

Remove the current resolv.conf file:

```bash
sudo rm /etc/resolv.conf
```

Create a symbolic link to systemd-resolved's resolv.conf file:

```bash
sudo ln -s /var/run/systemd/resolve/resolv.conf /etc/resolv.conf
```

Restart the systemd-resolved service:

```bash
sudo service systemd-resolved restart
```

Verify that DNS resolution is still working by using the nslookup command to check a domain of your choice, such as lancache.net:

```bash
nslookup lancache.net
```

By following these steps, systemd-resolved's DNSStubListener will be disabled, and your cache host should be able to bind to 0.0.0.0:53.
