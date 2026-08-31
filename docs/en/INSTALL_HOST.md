# Helper App Installation

> **Languages:** [简体中文](../zh-CN/INSTALL_HOST.md) | [繁體中文](../zh-TW/INSTALL_HOST.md) | [English](INSTALL_HOST.md)

> **ChaiSniffer** has two parts: the **browser extension** (sniffing) and the **helper app** (download, mux, launch players).  
> Store installs still require the helper app separately.

---

## Download

| Item | Link |
|------|------|
| **Windows package** | [Releases · latest](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest) |
| Test environment | [TEST_ENV.md](./TEST_ENV.md) |

The zip usually includes: `native-host/`, `setup-bridge.cmd`, and bundled `bin/ffmpeg.exe`.

---

## Setup (Windows)

1. Download the zip from [Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest).
2. **Extract anywhere** (Downloads, `D:\Apps\ChaiSniffer`, etc.).
3. Open ChaiSniffer **Settings** and copy your **Extension ID**.
4. Open the extracted `native-host` folder and run `setup-bridge.cmd`; paste the ID when prompted.
5. Back in Settings, click **Verify installation** until all checks show ✓.

> **Store extension IDs differ** from sideload builds—always use the ID on the Settings page.

---

## Player

In **Player settings**, set the path to mpv, VLC, PotPlayer, or **NeoPlayer**. [NeoPlayer](https://github.com/K-O-N-B/NeoPlayer/releases/latest) is recommended (release pending).

---

## macOS

Sniffing may work; the helper app (download/playback) is **not fully supported**—use Windows.

---

## FAQ

**Q: Can I install the helper app anywhere?**  
A: Yes. Extract to any folder and run `setup-bridge.cmd` inside it; the script registers that path.

**Q: Why install a helper app after the store extension?**  
A: The store ships only the browser part. Downloads and player launch need a local program.

**Q: Connection failed?**  
A: Check the extension ID, rerun the setup script, and verify again in Settings.
