# Notes for Microsoft Edge Add-ons certification

**Product:** ChaiSniffer (柴嗅) v0.9.16  
**Type:** Manifest V3 browser extension + separately installed Windows Native Host

---

## Summary for reviewers

ChaiSniffer **sniffs media URLs** on web pages the user visits and optionally **downloads non-DRM HLS** or **opens streams in local players** (mpv recommended). Processing is **local only**; no user media or browsing data is sent to the developer.

The extension uses **Native Messaging** to talk to a **helper app the user installs separately** from GitHub (not bundled in the store package). This matches Microsoft policy for companion native software installed outside the store.

---

## How to test end-to-end (Windows)

1. Install the extension from this submission package (or sideload for pre-review).
2. Open extension **Settings** → copy **Extension ID**.
3. Download **Windows helper app** from:  
   https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest  
   File: `ChaiSniffer-Host-Windows-x64-v0.9.14.1.zip` (or newer).
4. Extract zip anywhere → run `native-host\setup-bridge.cmd` → paste Extension ID.
5. In Settings → **Run full self-check** → all items should pass (Host, ffmpeg, player path if configured).
6. Visit a page with **public non-DRM HLS** (e.g. Apple HLS sample or any site with `.m3u8` in network tab).
7. Click toolbar icon → verify media list in popup.
8. Optional: hover video → floating ChaiSniffer icon → open in player (requires mpv path in Settings).
9. Optional: Settings → disable **Show floating video icon** → icon should disappear without page reload.

---

## Native Messaging

- Host ID: `com.browser_mpv_bridge`
- Host is registered by `setup-bridge.cmd` under the user's Chrome/Edge native messaging registry.
- Extension never downloads or installs the Host automatically; user must get it from GitHub Releases.

---

## Permissions (why broad host access)

- `webRequest` + `host_permissions` for all http(s) sites: required to **observe network requests** and detect m3u8/mpd/media URLs on pages the user browses.
- User can restrict via **site allow/deny list** in Settings (optional).
- `cookies`: read cookies for the **current page only** to pass to local download/player requests when sites require login.
- `declarativeNetRequest`: optional mobile User-Agent spoofing (off by default).
- Content scripts: sniff media; **deep key search** and **MSE capture** are **off by default**.

Full table: https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/store/PERMISSIONS_JUSTIFICATION.md

---

## DRM / legal

The extension **refuses** Widevine and other commercial DRM. It does not bypass encryption beyond user-authorized non-DRM AES-128 HLS where applicable.

---

## Privacy policy

https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md

---

## Support

https://github.com/K-O-N-B/ChaiSniffer-Public/issues

---

## macOS

Helper app (download/playback) is **not fully supported** on macOS. Windows is the supported platform for full functionality.
