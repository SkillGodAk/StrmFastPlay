# StrmFastPlay

[繁體中文](README.md) | **English**

**StrmFastPlay is a commercial Jellyfin plugin designed to reduce STRM startup delay.**
It is intended for remote STRM libraries using OpenList, AList, PikPak, Quark Cloud Drive, Xunlei/Thunder Cloud Drive and similar media sources.

## What it does

- Improves Jellyfin STRM startup time
- Optimizes remote STRM playback flow
- Designed for OpenList / AList direct-link and HTTP 302 scenarios
- Primarily tested with PikPak; also intended for Quark Cloud Drive and Xunlei/Thunder Cloud Drive when exposed through compatible OpenList/AList STRM or direct-link workflows
- Supports next-episode preparation for smoother continuous playback
- Uses compatibility safeguards for Jellyfin updates

> StrmFastPlay optimizes the Jellyfin playback workflow. Actual startup speed still depends on the cloud provider, CDN, network quality, subtitles and media format.

## Who is it for?

StrmFastPlay is intended for users who experience long delays between pressing Play and seeing video when Jellyfin libraries use `.strm` files pointing to remote media.

Common search scenarios include:

- Jellyfin STRM slow startup
- Jellyfin STRM playback delay
- Jellyfin OpenList slow playback
- Jellyfin AList STRM
- Jellyfin PikPak
- Jellyfin Quark Cloud Drive
- Jellyfin Xunlei / Thunder Cloud Drive
- Jellyfin remote media startup delay

## How it works

StrmFastPlay applies dedicated playback optimizations for STRM items while preserving Jellyfin's normal media handling when required.

Public documentation intentionally describes behavior at a product level. The proprietary optimization algorithm and implementation details are not disclosed.

## Compatibility

The plugin is continuously tested against practical Jellyfin releases and uses a best-effort forward-compatibility design. Check the latest GitHub Release notes before major Jellyfin upgrades.

## Download

https://github.com/SkillGodAk/StrmFastPlay/releases

## Installation

Extract the release package into:

```text
jellyfin/config/plugins/StrmFastPlay/
```

Then fully restart Jellyfin.

## Trial and pricing

A new installation includes a 7-day free trial.

- Monthly: 5 RMB / TWD 25
- 6 months: 25 RMB / TWD 125
- Yearly: 50 RMB / TWD 250

## FAQ

### What problem does StrmFastPlay solve?
It reduces the waiting time before remote Jellyfin STRM playback begins.

### Does it support OpenList / AList?
It is designed for these STRM scenarios, especially when the remote source supports healthy direct-link or HTTP 302 playback.

### Does it support PikPak, Quark Cloud Drive and Xunlei/Thunder Cloud Drive?
PikPak with OpenList is one of the primary tested scenarios. Quark Cloud Drive and Xunlei/Thunder Cloud Drive are also target use cases when OpenList/AList can expose a working STRM, direct link or HTTP 302 playback path. Actual startup performance still depends on each provider's current link speed, restrictions and availability.

### Does it increase cloud-drive bandwidth?
No. It optimizes Jellyfin-side playback behavior and does not increase upstream bandwidth.

### Are the core optimization details open source?
The public repository focuses on product information, downloads and documentation. The core optimization implementation is proprietary.

## Search terms

`Jellyfin STRM` · `Jellyfin STRM slow startup` · `Jellyfin STRM playback speed` · `Jellyfin OpenList` · `Jellyfin AList` · `Jellyfin PikPak` · `Jellyfin Quark Cloud Drive` · `Jellyfin Xunlei` · `Jellyfin Thunder Cloud Drive` · `Jellyfin remote media` · `Jellyfin plugin` · `STRM acceleration`

## Commercial / IP notice

StrmFastPlay is commercial software. Proprietary optimization logic, licensing components and non-public implementation details remain the property of the author.

StrmFastPlay is an independent third-party project and is not an official Jellyfin, OpenList, AList or PikPak product.
