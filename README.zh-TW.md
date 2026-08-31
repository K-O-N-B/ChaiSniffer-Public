# 柴嗅 / ChaiSniffer

**語言：** [简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

**柴嗅** 是一款瀏覽器擴充功能 + Windows 輔助應用程式：在網頁上發現媒體位址，在本機下載或交給**外部播放器**開啟。

> 擴充功能可從 **Microsoft Edge 載入項目** 安裝（**v0.9.16 審核準備中**）；**輔助應用程式需單獨下載**（見 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest)）。

**目前版本：** 擴充功能 **0.9.16** · 輔助應用程式 **host-v0.9.14.1+** · [更新說明](RELEASE_NOTES/v0.9.16.md)

---

## 為什麼做柴嗅

瀏覽器內建播放器常受網頁限制，畫質、流暢度、字幕與 AI 翻譯等能力有限。**柴嗅負責嗅探影片位址並橋接到本機**；實際播放體驗交給您安裝的播放器（如 mpv），由播放器提供：

- 更好的 **畫質與流暢度**（超分、插帧、著色器等，取決於播放器設定）
- 播放器端的 **AI 翻譯、字幕** 等增強能力
- 對 **重要、有意義的內容** 進行本機保存（請僅保存您有權保存的影片）

柴嗅 **不內建** 播放器功能，也不繞過 DRM；只做「發現位址 → 本機下載或交給播放器」。

---

## 播放器說明

| 播放器 | 建議 |
|--------|------|
| **[mpv](https://mpv.io/)** | **目前推薦。** 主要測試環境，HLS / Cookie / 分軌橋接相容性最好。 |
| **[NeoPlayer](https://github.com/K-O-N-B/NeoPlayer)** | 作者自用播放器，**仍在開發中**，之後會上傳 Release。現階段請先使用 mpv。 |
| PotPlayer / VLC 等 | 可在設定中新增，但 **相容性未全面驗證**。 |

畫質增強、AI 翻譯、字幕樣式等由 **播放器及其外掛/腳本** 負責，不在柴嗅擴充功能內實作。

---

## 快速開始（Windows）

1. 安裝 **柴嗅** 擴充功能。
2. 開啟 **設定** → 複製 **擴充功能 ID**。
3. 下載並解壓 **輔助應用程式**（可解壓到任意資料夾）。
4. 執行 `native-host\setup-bridge.cmd`，貼上擴充功能 ID。
5. 設定頁 **檢查是否安裝成功** → 全部 ✓。
6. 在 **播放器設定** 中設定 **[mpv](https://mpv.io/)**（推薦）。NeoPlayer 開發完成後會另行發布。

詳細說明 → [docs/zh-TW/INSTALL_HOST.md](docs/zh-TW/INSTALL_HOST.md)

---

## 文件

| 語言 | 安裝 | 測試環境 | 隱私 |
|------|------|----------|------|
| 简体 | [INSTALL_HOST](docs/zh-CN/INSTALL_HOST.md) | [TEST_ENV](docs/zh-CN/TEST_ENV.md) | [PRIVACY](PRIVACY.md) |
| 繁體 | [INSTALL_HOST](docs/zh-TW/INSTALL_HOST.md) | [TEST_ENV](docs/zh-TW/TEST_ENV.md) | [PRIVACY.zh-TW](PRIVACY.zh-TW.md) |
| English | [INSTALL_HOST](docs/en/INSTALL_HOST.md) | [TEST_ENV](docs/en/TEST_ENV.md) | [PRIVACY.en](PRIVACY.en.md) |

---

## 回饋

[GitHub Issues](https://github.com/K-O-N-B/ChaiSniffer-Public/issues)
