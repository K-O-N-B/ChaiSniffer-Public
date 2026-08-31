# 輔助應用程式安裝說明

> **語言：** [简体中文](../zh-CN/INSTALL_HOST.md) | [繁體中文](INSTALL_HOST.md) | [English](../en/INSTALL_HOST.md)

> **柴嗅 / ChaiSniffer** 分兩部分：**瀏覽器擴充功能**（嗅探）+ **輔助應用程式**（下載、合併、開啟播放器）。  
> 從 Edge 商店安裝擴充功能後，仍需單獨安裝輔助應用程式。

---

## 下載

| 內容 | 連結 |
|------|------|
| **Windows 安裝包** | [Releases · 最新版](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) |
| 測試環境 | [TEST_ENV.md](./TEST_ENV.md) |

安裝包通常包含：`native-host/` 資料夾、`setup-bridge.cmd`、內建 `bin/ffmpeg.exe`。

---

## 安裝步驟（Windows）

1. 從 [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) 下載 zip。
2. **解壓到任意資料夾**（如下載、`D:\Apps\ChaiSniffer` 等），位置不限。
3. 開啟柴嗅 **設定**，複製 **擴充功能 ID**。
4. 進入解壓後的 `native-host` 資料夾，雙擊 `setup-bridge.cmd`，貼上擴充功能 ID。
5. 回到設定頁，點 **檢查是否安裝成功**，各項為 ✓ 即可使用。

> **商店版擴充功能 ID 與測試版不同**，安裝時必須使用設定頁顯示的 ID。

---

## 播放器

在擴充功能 **播放器設定** 中填寫 **[mpv](https://mpv.io/)**（**目前推薦**）、VLC、PotPlayer 等路徑。  
**NeoPlayer**（作者自用）仍在開發中，之後會發布 Release；現階段請優先使用 mpv。

**浮動圖標：** 設定 → 嗅探 → **顯示視頻浮動圖標**（v0.9.16+，預設開啟，可關閉）。

---

## macOS

擴充功能嗅探可能可用；輔助應用程式（下載/播放）**尚未完整支援**，請使用 Windows。

---

## 常見問題

**Q：輔助應用程式可以裝在任何磁碟嗎？**  
A：可以。解壓到任意資料夾後，在該資料夾內執行 `setup-bridge.cmd` 即可；腳本會登記實際路徑。

**Q：為什麼商店擴充功能還要再裝輔助應用程式？**  
A：商店只能裝瀏覽器部分；下載、寫檔、呼叫播放器需要本機程式。

**Q：連線失敗？**  
A：確認擴充功能 ID 一致、已執行安裝腳本，並在設定頁重新檢查。
