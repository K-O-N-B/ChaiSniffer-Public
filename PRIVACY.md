# 柴嗅（ChaiSniffer）隐私政策

**最后更新：** 2026-08-31  
**语言：** [简体中文](PRIVACY.md) | [繁體中文](PRIVACY.zh-TW.md) | [English](PRIVACY.en.md)

---

## 概述

柴嗅在设计上 **不收集、不上传、不出售** 您的个人数据。媒体嗅探、下载、播放请求均在 **您的本机** 完成。

---

## 扩展处理的数据

| 数据类型 | 用途 | 是否离开本机 |
|----------|------|--------------|
| 当前页面的媒体 URL（m3u8、mpd、直链等） | 显示在资源列表，供您选择下载或播放 | **否**（仅本地扩展与 Host 通信） |
| 当前页面的 Cookie / Referer / User-Agent | 写入本机下载或播放请求头 | **否** |
| 扩展设置（嗅探开关、播放器路径等） | 保存在浏览器 `chrome.storage` 或本机 `bridge-settings.json` | **否** |
| 疑似 AES 密钥候选（深度搜索，默认关闭） | 仅在页面内存中收集，供您手动试钥 | **否** |

扩展 **不会** 向开发者服务器发送上述数据。扩展未内置分析 SDK 或广告追踪。

---

## 本机 Host 处理的数据

Host 程序在您电脑上运行，用于：

- 调用 ffmpeg 下载/合并媒体；
- 读写下载目录（默认 `%USERPROFILE%\Downloads\mpv-bridge`）；
- 启动您配置的本地播放器；
- 保存 `bridge-settings.json`（播放器路径、ffmpeg 路径等）。

Host **不会** 主动连接开发者服务器。网络请求仅发往 **您选择的媒体 CDN**（与浏览器访问相同）。

---

## 权限说明（摘要）

扩展申请的浏览器权限均用于上述本地功能，例如：

- `webRequest` / `host_permissions`：观察页面媒体请求以嗅探地址；
- `cookies`：读取当前站点 Cookie 供本机下载/播放；
- `nativeMessaging`：与已安装的本机 Host 通信；
- `storage`：保存您的设置。

完整权限对照见仓库内 [store/PERMISSIONS_JUSTIFICATION.md](store/PERMISSIONS_JUSTIFICATION.md)（供商店审核）。

---

## 第三方

- **ffmpeg**（随 Host 分发或用户自备）：按媒体 URL 下载数据，遵守各站点服务条款。
- **mpv / VLC / PotPlayer** 等：由用户自行安装，柴嗅仅启动并传参。

---

## 儿童

本产品不面向 13 岁以下儿童，亦不会故意收集儿童信息。

---

## 政策变更

重大变更将在本文件与 GitHub Releases 说明中更新「最后更新」日期。

---

## 联系

通过 [GitHub Issues](https://github.com/K-O-N-B/ChaiSniffer-Public/issues) 联系维护者。
