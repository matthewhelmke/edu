---
title: "Image Overview: configmap-reload"
type: "article"
description: "Overview: configmap-reload Chainguard Images"
date: 2022-11-01T11:07:52+02:00
lastmod: 2022-11-01T11:07:52+02:00
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
menu:
  docs:
    parent: "images-reference"
weight: 500
toc: true
---

`stable` [cgr.dev/chainguard/configmap-reload](https://github.com/chainguard-images/images/tree/main/images/configmap-reload)
| Tags         | Aliases                                            |
|--------------|----------------------------------------------------|
| `latest`     | `0`, `0.11`, `0.11.1`, `0.11.1-r0`                 |
| `latest-dev` | `0-dev`, `0.11-dev`, `0.11.1-dev`, `0.11.1-r0-dev` |



Kubernetes ConfigMap Reload

`configmap-reload` is a simple binary to trigger a reload when Kubernetes ConfigMaps or Secrets, mounted into pods, are updated.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/configmap-reload:latest
```

## Usage

This image is a drop-in replacement for the upstream image.
You can run it using the helm chart with:

```shell
$ helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
$ helm install my-release prometheus-community/alertmanager \
    --set configmapReload.enabled=true \
    --set configmapReload.image=cgr.dev/chainguard/configmap-reload \
    --set image.tag=latest
    <other configuration parameters here>
```
