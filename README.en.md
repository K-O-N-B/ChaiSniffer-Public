# ChaiSniffer

**Languages:** [简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

ChaiSniffer is a browser extension + Windows helper app that discovers media URLs on web pages and opens them in an **external player** or downloads them locally.

> Install the extension from **Microsoft Edge Add-ons**; download the **helper app** from [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest).

---

## Why ChaiSniffer

In-browser players are often limited by the web page. **ChaiSniffer sniffs URLs and bridges them to your PC**; playback quality and features come from the player you install (we recommend **mpv**), such as:

- Better **picture quality and smooth playback** (upscaling, frame interpolation, shaders — depending on player setup)
- **AI translation, subtitles**, and other enhancements on the player side
- **Saving important videos** locally (only content you are authorized to save)

ChaiSniffer does **not** embed a player or bypass DRM. It only discovers addresses and hands them to local download/playback.

---

## Players

| Player | Recommendation |
|--------|----------------|
| **[mpv](https://mpv.io/)** | **Recommended today.** Primary test target; best HLS / Cookie / split-track compatibility. |
| **[NeoPlayer](https://github.com/K-O-N-B/NeoPlayer)** | Author’s daily player; **still in development.** Releases will be published later — use mpv for now. |
| PotPlayer / VLC / others | Can be added in Settings; **compatibility not fully verified.** |

Quality, AI translation, and subtitle styling are handled by **the player and its scripts**, not inside the extension.

---

## Quick start (Windows)

1. Install the **ChaiSniffer** extension.
2. Open **Settings** → copy **Extension ID**.
3. Download and extract the **helper app** (any folder is fine).
4. Run `native-host\setup-bridge.cmd` and paste the ID.
5. Click **Verify installation** in Settings.
6. Configure **[mpv](https://mpv.io/)** under **Player settings** (recommended). NeoPlayer will be released when ready.

Details → [docs/en/INSTALL_HOST.md](docs/en/INSTALL_HOST.md)

---

## Documentation

| Language | Install | Test env | Privacy |
|----------|---------|----------|---------|
| 简体 | [zh-CN](docs/zh-CN/INSTALL_HOST.md) | [TEST_ENV](docs/zh-CN/TEST_ENV.md) | [PRIVACY](PRIVACY.md) |
| 繁體 | [zh-TW](docs/zh-TW/INSTALL_HOST.md) | [TEST_ENV](docs/zh-TW/TEST_ENV.md) | [PRIVACY.zh-TW](PRIVACY.zh-TW.md) |
| English | [en](docs/en/INSTALL_HOST.md) | [TEST_ENV](docs/en/TEST_ENV.md) | [PRIVACY.en](PRIVACY.en.md) |

---

## Feedback

[GitHub Issues](https://github.com/K-O-N-B/ChaiSniffer-Public/issues)
