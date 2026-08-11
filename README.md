# StrmFastPlay

StrmFastPlay 是 Jellyfin STRM 起播加速插件，目標是讓 STRM 播放前等待時間更短，盡量達到秒播效果。

適用於 OpenList、AList、WebDAV、HTTP 302 直鏈、各類網盤 STRM 來源。

## 重要說明

StrmFastPlay 主要加速 Jellyfin 播放前等待，不是網盤加速器。

如果 OpenList / AList 網頁內播放本身就很慢、不能播放、拖進度條會卡，Jellyfin STRM 也可能無法秒播。

拖進度條是否順暢，主要看網盤直鏈的 Range / seek 速度。PikPak 目前最穩，通常可在 5 秒內起播；迅雷、夸克等來源會依當下直鏈速度而不同。

內嵌軟字幕影片通常比硬字幕影片更吃來源速度。若來源拖拉很慢，軟字幕影片拖進度條也可能比較慢。

## 下載

請到 Releases 下載：

[StrmFastPlay.zip](https://github.com/SkillGodAk/StrmFastPlay/releases/latest/download/StrmFastPlay.zip)

## 安裝

下載 Releases 裡的 `StrmFastPlay.zip`，解壓縮到 Jellyfin 插件目錄：

```text
jellyfin/config/plugins/StrmFastPlay/
```

資料夾內應包含：

```text
Jellyfin.Plugin.StrmFastPlay.dll
```

安裝後重新啟動 Jellyfin。

## 試用與價格

首次安裝可免費試用 3 天。試用結束後需輸入授權碼。

- 月卡：5 RMB / 台幣 25 元
- 半年卡：25 RMB / 台幣 125 元
- 年卡：50 RMB / 台幣 250 元

購買方式請聯絡作者：

- 微信：MONflykeep
- LINE：flykeep
