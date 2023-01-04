---
title: "Fix dnf/yum repo failing after CentOS 8 EOL"
date: 2022-02-14
categories:
  - centos
  - linux
authors:
  - dgibbs
image: /images/centos-cloudlinux.jpg
---

Centos 8 reached its End of Life on December 31, 2021 and the associated repositories were shut down. This means that it is no longer possible to download anything from these repositories, and attempting to do so may result in errors such as:

```
Error: Failed to download metadata for repo 'BaseOS': Cannot prepare internal mirrorlist: No URLs in mirrorlist
```

Although Centos 8 is no longer supported, there is a solution for those who need to access its repositories. The Centos 8 repository has been moved to a "frozen" state and can be accessed at [https://vault.centos.org](https://vault.centos.org/). While it is generally recommended to upgrade to a newer operating system such as [RHEL](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux), AlmaLinux](https://almalinux.org/), or [Rocky Linux](https://rockylinux.org/), accessing the frozen repository at [https://vault.centos.org](https://vault.centos.org/) may be a suitable option if an immediate upgrade is not possible.

To do this you will need to change the urls in `yum.repos.d`. Using the below `sed` commands you can do this quickly.

```
sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
```

Once done run `dnf update` and you will be able to install packages again.
