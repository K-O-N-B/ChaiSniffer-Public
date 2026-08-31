# Edge 商店上架文案（审核用）

> 复制到 Partner Center 对应字段。英文版见文末。  
> 隐私政策 URL：`https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md`  
> 支持 URL：`https://github.com/K-O-N-B/ChaiSniffer-Public`

---

## 扩展名称

- 中文：**柴嗅**
- 英文：**ChaiSniffer**

---

## 简短描述（≤ 132 字符，中文）

嗅探网页媒体地址，在本机下载非 DRM 的 HLS，或交给 mpv/VLC 等播放器打开。需单独安装 Windows 本机组件。

---

## 详细描述（中文，≥ 250 字）

**柴嗅（ChaiSniffer）** 帮助您在浏览网页时发现页面中的流媒体地址（HLS m3u8、DASH mpd、直链等），并在 **本机** 完成下载或交给外部播放器播放。

**主要功能：**
- 自动识别当前标签页中的媒体资源，在弹出面板中列出；
- 支持将地址、Cookie、Referer 传递给本机 mpv、VLC、PotPlayer 等播放器；
- 配合 **Windows 本机 Host**（需从 GitHub 单独下载）可下载非 DRM 的 HLS（含 AES-128）及常见分轨内容；
- 内置 m3u8 解析工具、下载任务管理、环境自检；
- **明确拒绝** Widevine 等商业 DRM 内容。

**重要说明：**
1. 本扩展 **不包含** 下载合并程序。完整下载/播放能力需安装 **Windows 本机 Host**（见项目 GitHub Releases）。
2. 从商店安装后，请在扩展 **设置** 页复制 **扩展 ID**，运行 Host 安装包中的 `setup-bridge.cmd` 完成桥接。
3. **macOS** 上 Host 暂未完整支持，Mac 用户请勿依赖本机下载功能。
4. 请遵守版权与当地法律，仅处理您有权保存或离线观看的内容。

**测试环境：** Windows 10/11 + Microsoft Edge Stable + 本机 Host + ffmpeg + mpv。详见 GitHub 文档 TEST_ENV.md。

---

## Detailed description (English)

**ChaiSniffer** discovers streaming media URLs (HLS, DASH, direct links) on web pages and lets you open them in local players or download them on your PC.

**Features:**
- Lists sniffed media for the active tab;
- Passes URL, cookies, and referer to mpv, VLC, PotPlayer, etc.;
- With the separate **Windows Native Host** (download from GitHub Releases), downloads non-DRM HLS including AES-128;
- Built-in m3u8 tools, download tasks, and setup self-check;
- Refuses commercial DRM (Widevine, etc.).

**Important:**
1. The extension alone does **not** include ffmpeg or download workers. Install the **Windows Native Host** from GitHub.
2. After installing from the store, copy your **extension ID** from Settings and run `setup-bridge.cmd` from the Host package.
3. **macOS Host is not fully supported** yet.
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

本扩展使用 **Native Messaging** 与用户在本地安装的 Host 通信。审核完整下载流程需：

1. 安装扩展；
2. 从 https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest 下载 Windows Host zip；
3. 运行 `setup-bridge.cmd` 并粘贴设置页扩展 ID；
4. 设置 → **运行完整自检**；
5. 打开含公开 HLS 的测试页验证 Popup 与下载。

Host 为独立可执行组件，符合 Microsoft 政策 1.2.3（本机配套程序单独安装）。

---

## 截图文案建议（5 张）

1. Popup 资源列表 — 「发现页面中的流媒体地址」
2. 设置页自检 — 「一键检查 Host / ffmpeg / 播放器」
3. 下载任务 — 「本机 HLS 下载与进度」
4. 播放器选择 — 「mpv / VLC / PotPlayer 任选」
5. 安装说明 — 「商店扩展 + GitHub Host 分步安装」
