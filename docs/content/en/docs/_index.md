
---
title: "Welcome"
linkTitle: "Documentation"
weight: 20
menu:
  main:
    weight: 20
---

Welcome to the Kairos documentation!

Kairos is an open-source project which brings Edge, cloud, and bare metal OS lifecycle management into the same design principles with a unified Cloud Native API.

At a glance:

- Community Driven
- Open Source
- [Meta-Distribution](/docs/architecture/meta), distro agnostic
- [Immutable](/docs/architecture/immutable)
- Secure
- [Container-based](/docs/architecture/container)
- [P2P Mesh](/docs/architecture/network)

Kairos can be used to:

- Easily spin up a Kubernetes cluster with the Linux distribution of your choice.
- Create your Immutable infrastructure, with atomic upgrades no more infrastructure drift!
- Manage the cluster lifecycle with Kubernetes—from building to provisioning and upgrading.
- Create a multiple-node, single cluster which spans across regions.

To become familiar with Kairos, check out the [quickstart](/docs/getting-started).

## What is it ?

Kairos is a cloud native, meta-Linux distribution that can be built, managed, and runs on Kubernetes.

Why or when should I use it?

- Build your cloud on-premise, no vendor lock-in, completely open source.
- Brings the same convenience of public cloud on-premise.
- Node provisioning—bring your own image or use the Kairos releases.
- For appliances that doesn't have to be Kubernetes application specific, its design fits multiple use case scenarios.

## Features

- At the current state, Kairos can create multiple-node Kubernetes clusters with [K3s](https://k3s.io)—all K3s features are supported.
- Upgrade manually via CLI or with Kubernetes. Upgrade distributions are done via container registries.
- As an immutable distribution, configured to your needs, stays immutable.
- Node configuration via a single cloud-init config file.
- Handles airgap upgrades with in-cluster, container registries.
- Extends the image in runtime or builds time via Kubernetes Native APIs.
- Plans to support CAPI with full device lifecycle management.
- Plans to support up to RKE2, kubeadm, and much more!
- Nodes can optionally connect autonomously via a full-mesh P2P hybrid VPN network. It allows to stretch a cluster up to 10000 km!
  Kairos can create private virtual network segments to enhance your cluster perimeter without any SPOF.

## More than a Linux distribution

Kairos is available as ISO, qcow2 and Netboot artifact for user convenience based from Alpine and openSUSE, but it is actually more than that. It allows to turn any Linux distribution into a uniform, comformant distro with immutable design. As such, any distro which is "converted" will share the same, common feature set between all of them, and they are managed in the same way by Kubernetes Native API components.

Any input OS will inherit:

- Immutability
- A/B upgrades
- Booting mechanism Fallback
- Boot assessment
- Single image, container-based atomic upgrades
- Cloud init support
- All the Kairos feature-set

Kairos treats all the OSes homogeneously in a distro-agnostic fashion.

The OS is a container image. That means that upgrades to nodes are distributed via container registries.

Installations medium and other assets required to boot bare metal or Edge devices are built dynamically by the Kubernetes Native API components provided by Kairos.

![livecd](https://user-images.githubusercontent.com/2420543/189219806-29b4deed-b4a1-4704-b558-7a60ae31caf2.gif)

## Goals

The Kairos ultimate goal is to bridge the gap between Cloud and Edge by creating a smooth user experience. There are several areas in the ecosystem that can be improved for edge deployments to make it in pair with the cloud.

The Kairos project encompassess all the tools and architectural pieces needed to fill those gaps. This spans between providing Kubernetes Native API components to assemble OSes, deliver upgrades, and control nodes after deployment.

Kairos is distro-agnostic, and embraces openness: The user can provide their own underlying base image, and Kairos onboards it and takes it over to make it Cloud Native, immutable that plugs into an already rich ecosystem by leveraging containers as distribution medium.

## Contribute

Kairos is an open source project, and any contribution is more than welcome! The project is big and narrows to various degree of complexity and problem space. Feel free to join our chat, discuss in our forums and join us in the Office hours. Check out the [contribution guidelines](https://github.com/kairos-io/kairos/contribute) to see how to get started and our [governance](https://github.com/kairos-io/kairos/blob/master/GOVERNANCE.md).

We have an open roadmap, so you can always have a look on what's going on, and actively contribute to it.

Useful links:

- [Upcoming releases](https://github.com/kairos-io/kairos/issues?q=is%3Aissue+is%3Aopen+label%3Arelease)


## Community

You can find us at:

- [#Kairos-io at matrix.org](https://matrix.to/#/#kairos-io:matrix.org)
- [IRC #kairos in libera.chat](https://web.libera.chat/#kairos)
- [Github Discussions](https://github.com/kairos-io/kairos/discussions)

### Project Office Hours

Project Office Hours is an opportunity for attendees to meet the maintainers of the project, learn more about the project, ask questions, learn about new features and upcoming updates.

Office hours are happening weekly on Wednesday - 5:30 – 6:00pm CEST. [Meeting link](https://meet.google.com/aus-mhta-azb)

Besides, we have monthly meetup to participate actively into the roadmap planning and presentation which takes part during the office hours:

#### Roadmap planning

We will discuss on agenda items and groom issues, where we plan where they fall into the release timeline.

Occurring: Monthly on the first Wednesday - 5:30 – 6:30pm CEST. 

#### Roadmap presentation

We will discuss the items of the roadmaps and the expected features on the next releases

Occurring: Monthly on the second Wednesday - 5:30pm CEST.

## Alternatives

There are other projects that are similar to Kairos which are great and worth to mention, and actually Kairos took to some degree inspiration from.
However, Kairos have different goals and takes completely unique approaches to the underlying system, upgrade, and node lifecycle management.

- [k3os](https://github.com/rancher/k3os)
- [Talos](https://github.com/siderolabs/talos)
- [FlatCar](https://flatcar-linux.org/)
- [CoreOS](https://getfedora.org/it/coreos?stream=stable)

## Development

### Building Kairos

Requirements: Needs only Docker.

Run `./earthly.sh +all --FLAVOR=opensuse`, should produce a Docker image along with a working ISO.


## What's next?

See the [quickstart](/docs/getting-started) to install Kairos on a VM and create a Kubernetes cluster!
