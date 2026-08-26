# StrmFastPlay - Jellyfin STRM / Cloud Drive Playback Acceleration Plugin

[繁體中文](README.md) | [简体中文](README.zh-CN.md) | **English**

**StrmFastPlay is a Jellyfin STRM and cloud-drive playback acceleration plugin.**
It is designed to reduce slow startup and long waiting times before remote media playback begins.

Typical scenarios include OpenList / AList and remote sources such as PikPak, Quark Cloud Drive, Xunlei/Thunder Cloud Drive, 115, 123Pan, GuangYaPan, Aliyun Drive, Baidu Netdisk, Tianyi Cloud, China Mobile Cloud, China Unicom Cloud, UC Drive, Google Drive, OneDrive, Dropbox, MEGA, TeraBox, Yandex Disk, WebDAV and SMB.

These are common target scenarios, not a claim that every provider has been fully tested.

## Installation

### Jellyfin repository (recommended)

Add this URL to your Jellyfin repositories:

```text
https://skillgodak.github.io/StrmFastPlay/manifest.json
```

Then open Dashboard → Plugins → All, search for `StrmFastPlay`, and install it. Fully restart Jellyfin after installation. Future releases can be installed through Jellyfin's plugin update feature.

### Manual installation

[Open GitHub Releases](https://github.com/SkillGodAk/StrmFastPlay/releases), download `StrmFastPlay.zip`, and extract the DLL and `meta.json` to:

```text
jellyfin/config/plugins/StrmFastPlay/
```

Fully restart Jellyfin to load the plugin.
