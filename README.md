# StrmFastPlay

StrmFastPlay 是 Jellyfin STRM 起播加速插件，支援各大網盤搭配 OpenList、AList 使用，縮短播放前等待時間，盡量達到秒播效果。

## 使用說明

- OpenList / AList 網頁內播放越快，Jellyfin STRM 越容易秒播；若來源本身很慢或無法播放，插件也無法改善網盤速度。
- 目前實測 PikPak 最穩定，通常可在 5 秒內起播，其他網盤會依來源當下速度而不同。
- 內嵌軟字幕需要額外載入字幕，起播可能比硬字幕稍慢。
- 影片已燒入硬字幕時不需另外載入字幕，來源順暢即可更容易達到秒播。

## 下載

請到 Releases 下載：

[StrmFastPlay.zip](https://github.com/SkillGodAk/StrmFastPlay/releases/latest/download/StrmFastPlay.zip)

## 安裝

下載 Releases 裡的 `StrmFastPlay.zip`，解壓縮到 Jellyfin 插件目錄：

```text
jellyfin/config/plugins/StrmFastPlay/
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
