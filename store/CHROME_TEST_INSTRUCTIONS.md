# Chrome Web Store — Test instructions

Dashboard → **Test instructions** (or similar “notes for reviewers” field).

Select that **no credentials are needed**, then paste:

```
ChaiSniffer sniffs media URLs on pages the user opens and optionally downloads non-DRM HLS or opens streams in local players. No developer login or test account is required.

To test full functionality on Windows 10/11:

1. Install this extension from the submission package.
2. Open Settings and copy the Extension ID shown on the page.
3. Download the Windows helper app from:
   https://github.com/K-O-N-B/ChaiSniffer-Public/releases/latest
   (file: ChaiSniffer-Host-Windows-x64-v0.9.14.1.zip or newer)
4. Extract the zip anywhere, run native-host\setup-bridge.cmd, paste the Extension ID.
5. In Settings, click Run full self-check — Extension, Helper app, ffmpeg should show OK.
6. Optional: add mpv.exe path under Player settings (recommended player).
7. Visit a page with public non-DRM HLS (e.g. any page with .m3u8 in network requests).
8. Click the toolbar icon — media list appears in the popup.
9. Optional: hover a video — floating ChaiSniffer icon (can be disabled in Settings → Sniffing).

Native Messaging host ID: com.browser_mpv_bridge. The helper app is NOT bundled in the extension; users install it separately from GitHub.

Note: setup-bridge.cmd registers both Chrome and Edge native messaging. Use the Chrome store Extension ID when testing the Chrome build.

Privacy policy: https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md
Support: https://github.com/K-O-N-B/ChaiSniffer-Public/issues

macOS helper app is not fully supported; Windows is the supported platform for download/playback.

This same package (v0.9.16) was approved on Microsoft Edge Add-ons.
```
