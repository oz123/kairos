---
title: "Customizing the system image"
linkTitle: "Customization"
weight: 2
description: >
---

Kairos is a container-based OS, if you want to change Kairos and add a package, it is required to build only a Docker image.

For example:

```docker
FROM quay.io/kairos/kairos:opensuse-latest

RUN zypper in -y ...

RUN export VERSION="my-version"
RUN envsubst '${VERSION}' </etc/os-release
```

The image can be then used with `kairos upgrade` or with system-upgrade-controller for upgrades within Kubernetes.
