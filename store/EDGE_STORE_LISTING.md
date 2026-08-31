# Edge 商店上架文案（审核用）

> **扩展版本：** 0.9.16  
> 复制到 Partner Center → 见 [EDGE_PARTNER_FIELDS.md](./EDGE_PARTNER_FIELDS.md)（字段级复制）  
> 提交步骤 → [EDGE_SUBMISSION_CHECKLIST.md](./EDGE_SUBMISSION_CHECKLIST.md)  
> 认证说明 → [EDGE_REVIEW_NOTES.md](./EDGE_REVIEW_NOTES.md)  
> 隐私政策 URL：`https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md`  
> 支持 URL：`https://github.com/K-O-N-B/ChaiSniffer-Public/issues`

---

## 扩展名称

- 中文：**柴嗅**
- 英文：**ChaiSniffer**

---

## 简短描述（≤ 132 字符，中文）

嗅探网页媒体地址，在本机下载非 DRM 的 HLS，或交给 mpv 等播放器打开。需单独安装 Windows 辅助应用。可在设置中关闭视频浮动图标。

---

## 详细描述（中文，≥ 250 字）

**柴嗅（ChaiSniffer）** 帮助您在浏览网页时发现页面中的流媒体地址（HLS m3u8、DASH mpd、直链等），并在 **本机** 完成下载或交给外部播放器播放。

**主要功能：**
- 自动识别当前标签页中的媒体资源，在弹出面板中列出；
- **可选视频浮动图标**：悬停视频时显示，一键用播放器打开（设置中可关闭）；
- 支持将地址、Cookie、Referer 传递给本机 **mpv**（推荐）、VLC、PotPlayer 等播放器；
- 配合 **Windows 辅助应用**（需从 GitHub 单独下载）可下载非 DRM 的 HLS（含 AES-128）及常见分轨内容；
- 内置 m3u8 解析工具、下载任务管理、环境自检；
- **明确拒绝** Widevine 等商业 DRM 内容。

**重要说明：**
1. 本扩展 **不包含** 下载合并程序。完整下载/播放能力需安装 **Windows 辅助应用**（见 [GitHub Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest)）。
2. 从商店安装后，请在扩展 **设置** 页复制 **扩展 ID**，运行辅助应用包中的 `setup-bridge.cmd` 完成桥接。
3. **macOS** 上辅助应用暂未完整支持，Mac 用户请勿依赖本机下载功能。
4. 请遵守版权与当地法律，仅处理您有权保存或离线观看的内容。

**测试环境：** Windows 10/11 + Microsoft Edge Stable + 辅助应用 + ffmpeg + mpv。详见 [TEST_ENV.md](../docs/zh-CN/TEST_ENV.md)。

---

## Detailed description (English)

**ChaiSniffer** discovers streaming media URLs (HLS, DASH, direct links) on web pages and lets you open them in local players or download them on your PC.

**Features:**
- Lists sniffed media for the active tab;
- Optional **floating icon on videos** (toggle in Settings);
- Passes URL, cookies, and referer to **mpv** (recommended), VLC, PotPlayer, etc.;
- With the separate **Windows helper app** (GitHub Releases), downloads non-DRM HLS including AES-128;
- Built-in m3u8 tools, download tasks, and setup self-check;
- Refuses commercial DRM (Widevine, etc.).

**Important:**
1. The extension alone does **not** include ffmpeg or download workers. Install the **Windows helper app** from GitHub.
2. After installing from the store, copy your **extension ID** from Settings and run `setup-bridge.cmd` from the helper package.
3. **macOS helper app is not fully supported** yet.
4. Use only on content you are authorized to access.

Tested on Windows 10/11 with Microsoft Edge Stable.

---

## 分类建议

- 主要：**生产力** 或 **开发人员工具**
- 次要：**实用程序**

---

## 年龄分级

建议：**青少年及以上**（涉及用户自行访问的第三方媒体内容）

---

## 认证说明（给审核员）

完整英文步骤见 [EDGE_REVIEW_NOTES.md](./EDGE_REVIEW_NOTES.md)。摘要：

1. 安装扩展；
2. 从 https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest 下载 Windows 辅助应用 zip（建议 v0.9.14.1+）；
3. 运行 `setup-bridge.cmd` 并粘贴设置页扩展 ID；
4. 设置 → **运行完整自检**；
5. 打开含公开 HLS 的测试页验证 Popup、浮动图标（可选）与下载。

辅助应用为独立可执行组件，符合 Microsoft 政策（本机配套程序单独安装）。

---

## 截图文案建议（5 张）

详见 [SCREENSHOT_CAPTIONS.md](./SCREENSHOT_CAPTIONS.md)。

1. Popup 资源列表 — 「发现页面中的流媒体地址」
2. 设置页自检 — 「一键检查辅助应用 / ffmpeg / 播放器」
3. 视频浮动图标 — 「可选浮动图标，一键交给播放器」
4. 播放器设置 — 「推荐 mpv，多播放器配置」
5. 扩展 ID — 「商店安装后需桥接辅助应用」

---

## v0.9.16 相对 0.9.14 的商店说明增量

- 新增设置项 **显示视频浮动图标**（默认开启），**无新增 manifest 权限**
- 播放器文案改为 **推荐 mpv**；NeoPlayer 标注开发中
