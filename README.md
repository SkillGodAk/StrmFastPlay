<p align="center">
  <img src="assets/strmfastplay-logo.png" alt="StrmFastPlay - Jellyfin STRM 起播加速插件" width="760">
</p>

# StrmFastPlay

**繁體中文** | [English](README_EN.md)

**StrmFastPlay 是專為 Jellyfin STRM 播放設計的起播加速插件。**
針對 OpenList / AList、PikPak、夸克網盤、迅雷網盤與其他遠端媒體來源的 STRM 使用情境，改善播放前等待時間，讓媒體更快開始播放。

適用情境包括：

- Jellyfin STRM 起播慢
- Jellyfin STRM 播放前等待時間過長
- OpenList / AList STRM 播放延遲
- PikPak STRM 播放延遲
- 夸克網盤 STRM 播放延遲
- 迅雷網盤 STRM 播放延遲
- 遠端影片在 Jellyfin 中起播速度不穩定
- Jellyfin remote media startup delay

> StrmFastPlay 最佳化的是 Jellyfin STRM 播放流程。實際起播速度仍會受到網盤、CDN、OpenList/AList、網路品質、字幕與媒體格式等因素影響。

## 主要功能

- 改善 Jellyfin STRM 播放前等待時間
- 最佳化遠端 STRM 媒體的起播流程
- 支援 OpenList / AList 直鏈與 302 使用情境
- 目前主要實測 PikPak
- 可預先準備下一集，降低連續播放等待
- 保留必要的 Jellyfin 相容性與安全回退機制
- 適用 Docker 與一般 Jellyfin Server 環境

## 適合誰使用？

如果你的 Jellyfin 媒體庫使用 `.strm` 指向 OpenList、AList、PikPak、夸克網盤、迅雷網盤或其他遠端媒體，而且經常遇到：

> 點擊播放後，需要等待數秒甚至更久才開始播放

StrmFastPlay 就是針對這類問題設計。

## 工作方式

StrmFastPlay 會在 Jellyfin 播放 STRM 時進行專用最佳化，減少不必要的播放前等待，同時在必要時保留 Jellyfin 原本的媒體處理流程。

本專案的公開文件僅說明功能、相容性與使用方式；核心最佳化演算法與實作細節不公開。

## 使用建議

- OpenList / AList 來源支援時，建議使用 302 / 直鏈模式。
- 來源本身在瀏覽器或 OpenList 中能快速播放，通常更容易獲得良好的 Jellyfin 起播體驗。
- 同一季劇集建議保持正確季數與集數資訊，以利下一集預先準備。
- 外掛字幕或軟字幕可能增加額外載入時間。

## 相容性

StrmFastPlay 以實際 Jellyfin 版本持續測試，並採 best-effort forward compatibility 設計。

Jellyfin 更新後，如果相關播放流程仍相容，插件可繼續使用；若 Jellyfin 核心發生重大變更，插件會盡量安全回退，而不是影響 Jellyfin Server 正常啟動。

請以最新 GitHub Release 的相容性說明為準。

## 下載

[前往 GitHub Releases 下載](https://github.com/SkillGodAk/StrmFastPlay/releases)

## 安裝

下載 Releases 中的 `StrmFastPlay.zip`，解壓縮到 Jellyfin 插件目錄：

```text
jellyfin/config/plugins/StrmFastPlay/
```

Docker 範例：

```text
/volume1/docker/jellyfin/config/plugins/StrmFastPlay/
```

完整重新啟動 Jellyfin 後即可載入插件。

建議安裝完成後，到 Jellyfin：

```text
控制台 -> 已排程的工作
```

執行一次 StrmFastPlay 提供的 STRM 媒體資訊相關工作（若目前版本提供）。

## PikPak 邀請碼

```text
34544273
```

## 試用與價格

首次安裝可免費試用 7 天，試用結束後需輸入授權碼。

- 月卡：5 RMB / 台幣 25 元
- 半年卡：25 RMB / 台幣 125 元
- 年卡：50 RMB / 台幣 250 元

聯絡作者：

- QQ 群：`1018495751`
- TG 群：[點此加入](https://t.me/+l1v_7ag4mJQ3NjI1)

## FAQ

### StrmFastPlay 是做什麼的？
它是一個 Jellyfin STRM 起播加速插件，主要用途是縮短遠端 STRM 在 Jellyfin 中點擊播放後的等待時間。

### 支援 OpenList / AList 嗎？
支援這類 STRM 使用情境，尤其適合搭配可正常直鏈或 302 的遠端媒體來源。

### 支援 PikPak、夸克網盤、迅雷網盤嗎？
目前主要以 PikPak 搭配 OpenList 的使用情境進行實測；夸克網盤、迅雷網盤等，只要能透過 OpenList / AList 正常提供 STRM、直鏈或 302 播放，也屬於 StrmFastPlay 的適用場景。實際起播效果仍取決於各網盤當下的直鏈速度、限制與可用性。

### 能讓網盤下載速度變快嗎？
不能。StrmFastPlay 最佳化 Jellyfin 播放流程，不會增加網盤、CDN 或網路頻寬。

### 為什麼不同影片起播速度還是不一樣？
遠端來源速度、媒體格式、字幕、CDN 狀態、網路品質與影片本身結構都可能影響起播時間。

### Jellyfin 更新後還能用嗎？
插件以持續相容為目標，但 Jellyfin 大版本可能改變內部行為。請以最新 Release 的相容性資訊為準。

### 核心技術是開源的嗎？
公開倉庫主要提供產品資訊、下載與使用文件。核心最佳化實作屬於商業版本的一部分，不在公開文件中揭露。

## Search keywords

`Jellyfin STRM` · `Jellyfin STRM slow startup` · `Jellyfin STRM playback speed` · `Jellyfin OpenList` · `Jellyfin AList` · `Jellyfin PikPak` · `Jellyfin Quark` · `Jellyfin 夸克網盤` · `Jellyfin Thunder` · `Jellyfin 迅雷網盤` · `Jellyfin remote media` · `Jellyfin plugin` · `STRM acceleration` · `Jellyfin startup delay`

## 商業與智慧財產聲明

StrmFastPlay 為商業軟體。除明確標示可公開使用的檔案外，核心演算法、最佳化策略、授權機制與實作細節均屬作者所有。

未經授權，不得對商業版本進行重新散布、破解、繞過授權或以其非公開實作建立衍生商業版本。

StrmFastPlay 是獨立第三方專案，並非 Jellyfin、OpenList、AList 或 PikPak 官方產品。
