# StrmFastPlay

StrmFastPlay 是 Jellyfin STRM 起播加速插件，目標是讓 STRM 影片播放前等待時間更短，達到接近秒播的效果。

適合 OpenList、AList、WebDAV、HTTP 302、網盤直鏈等 STRM 使用情境。

只要 OpenList / AList 網頁內播放本身能秒播，STRM 起播才有機會做到秒播；如果網頁內播放也很慢，通常代表遠端網盤或掛載來源本身速度不穩。

目前實測最穩的是 PikPak，多數情況可做到 5 秒內起播。迅雷、夸克等來源速度會依網盤端與 OpenList / AList 回應狀況而不同。

## 下載

請到 Releases 下載：

[StrmFastPlay.zip](https://github.com/SkillGodAk/StrmFastPlay/releases/latest/download/StrmFastPlay.zip)

## 安裝

下載 `StrmFastPlay.zip`，解壓縮到 Jellyfin 插件目錄：

```text
jellyfin/config/plugins/StrmFastPlay/
```

資料夾內應只有：

```text
Jellyfin.Plugin.StrmFastPlay.dll
```

安裝後重新啟動 Jellyfin。

## 試用與授權

- 首次安裝可免費試用 3 天
- 月卡：5 RMB / 25 台幣
- 半年卡：25 RMB / 125 台幣
- 年卡：50 RMB / 250 台幣

購買方式請聯絡作者：

- 微信：MONflykeep
- LINE：flykeep

## 相容性

StrmFastPlay 不寫死只能在單一 Jellyfin 版本使用。新版 Jellyfin 若仍相容核心播放流程，插件會盡量繼續可用；若 Jellyfin 核心結構改變，插件會安全停用加速，不應影響 Jellyfin 啟動。
