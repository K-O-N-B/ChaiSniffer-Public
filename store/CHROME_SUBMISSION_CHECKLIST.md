# Chrome Web Store — Submission Checklist (v0.9.16)

> **I cannot log into your Google account or pay the $5 fee for you.**  
> Everything below is ready to copy/upload. Follow this page top to bottom.

---

## A. What you must do yourself (AI cannot)

| # | Action | Link / path |
|---|--------|-------------|
| 1 | Register Chrome Web Store developer (**one-time USD $5**) | https://chrome.google.com/webstore/devconsole |
| 2 | Sign in with the Google account you want as publisher | — |
| 3 | Click **New item** → upload zip | see Package below |
| 4 | Fill Store listing / Privacy / Distribution / Test instructions | copy from files in this folder |
| 5 | Click **Submit for review** | — |

---

## B. Package (upload first)

```
G:\00_Develop-Projects-NZ\009_MPV_Bridge\MPV-Bridge\dist-release\ChaiSniffer-Extension-v0.9.16.zip
```

- Manifest V3, version **0.9.16**
- Same package that passed Edge review
- Root of zip contains `manifest.json` (no nested folder)

---

## C. Screenshots & icon (already 1280×800)

```
G:\00_Develop-Projects-NZ\009_MPV_Bridge\MPV-Bridge\dist-release\store-assets\v0.9.16-edge\
├── store-icon-128.png              ← Icon (128×128)
├── 01-popup-resource-list.png      ← Screenshot 1
├── 02-self-check-passed.png
├── 03-float-icon-on-video.png
├── 04-player-settings-mpv.png
└── 05-install-steps-extension-id.png
```

Chrome prefers **1280×800** screenshots (these are already resized for Edge).

Optional: Small promo tile **440×280** / Marquee **1400×560** — skip for first submission.

---

## D. Forms to fill (copy-paste)

| Dashboard tab | File |
|---------------|------|
| Store listing | [CHROME_STORE_LISTING.md](./CHROME_STORE_LISTING.md) |
| Privacy (single purpose + permissions + data) | [CHROME_PRIVACY_FIELDS.md](./CHROME_PRIVACY_FIELDS.md) |
| Test instructions | [CHROME_TEST_INSTRUCTIONS.md](./CHROME_TEST_INSTRUCTIONS.md) |
| Permission reference | [PERMISSIONS_JUSTIFICATION.md](./PERMISSIONS_JUSTIFICATION.md) |

---

## E. Recommended Distribution settings

| Field | Value |
|-------|-------|
| Visibility | **Public** |
| Pricing | **Free** |
| Regions | All countries (or All available) |

Uncheck “Publish automatically after review” only if you want to control go-live timing; otherwise leave checked.

---

## F. After approval — important

Chrome store **Extension ID ≠ Edge CRX ID**.

1. Open Chrome store listing → install → Settings → copy **Chrome Extension ID**
2. Users must paste **that** ID into `setup-bridge.cmd` (Host already supports both Chrome and Edge registries)
3. Update public README with Chrome Web Store URL

---

## G. Common rejection risks (already mitigated in copy)

- Broad host permissions → justified (media sniffing)
- Native Messaging + external Host → explained (not bundled)
- Cookies / webRequest → local download/player only, no upload
- No remote code → declare **No**
