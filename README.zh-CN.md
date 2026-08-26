# StrmFastPlay - Jellyfin STRM / 网盘播放加速插件

[繁體中文](README.md) | **简体中文** | [English](README_EN.md)

**StrmFastPlay 是专为 Jellyfin STRM 播放加速与网盘播放加速设计的插件。**
主要改善 **Jellyfin STRM 起播慢、网盘影片播放前等待时间过长、远程媒体起播不稳定** 等问题。

适用于通过 OpenList / AList 或其他兼容方式提供 STRM、直链或 302 播放的远程媒体来源。

## 常见网盘场景

PikPak、夸克网盘、迅雷网盘、115 网盘、123 网盘、光鸭网盘、阿里云盘、百度网盘、天翼云盘、中国移动云盘、中国联通云盘、UC 网盘、腾讯微云、蓝奏云、Google Drive、OneDrive、Dropbox、MEGA、TeraBox、Yandex Disk、FebBox、Seafile、Cloudreve、WebDAV、SMB 等。

以上仅代表常见适用场景，不等于全部来源都经过完整实测。

## FAQ

### Jellyfin 网盘播放很慢怎么办？
StrmFastPlay 针对 Jellyfin 远程 STRM / 网盘播放流程进行优化，目标是减少点击播放后的等待时间。

### 支持哪些网盘？
只要能通过 OpenList / AList 或其他兼容方式正常提供 STRM、直链或 302 播放，就属于适用场景。

## 安装

### Jellyfin 存储库安装（推荐）

在 Jellyfin 控制台依次打开“插件”→“存储库”→“新增”，填写：

- 名称：`StrmFastPlay`
- 存储库网址：`https://skillgodak.github.io/StrmFastPlay/manifest.json`

保存后到插件目录安装 StrmFastPlay，并完整重启 Jellyfin。后续新版本可通过 Jellyfin 插件更新功能安装。

### 手动安装

[前往 GitHub Releases](https://github.com/SkillGodAk/StrmFastPlay/releases) 下载 `StrmFastPlay.zip`，将 ZIP 内的 DLL 与 `meta.json` 解压到：

```text
jellyfin/config/plugins/StrmFastPlay/
```

完整重启 Jellyfin 后即可加载。

## 推广回馈

发布 StrmFastPlay 推广介绍文章后，联系作者并提供发布证明，可免费获得一张月卡（1 个月）。
