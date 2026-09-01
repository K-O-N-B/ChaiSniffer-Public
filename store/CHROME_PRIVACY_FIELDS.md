# Chrome Web Store — Privacy tab (copy-paste)

Dashboard → **Privacy** tab. Use English.

---

## Single purpose description

```
ChaiSniffer has one purpose: on web pages the user opens, discover streaming media addresses (HLS, DASH, direct links) and let the user download them locally or open them in an external player (e.g. mpv). All processing stays on the user's device. The extension does not bypass DRM, does not track users, and does not upload browsing or media data to the developer.
```

---

## Permission justifications

**nativeMessaging**
```
Required to communicate with the user's locally installed Windows helper app (installed separately from GitHub). The helper runs ffmpeg downloads, writes files, and launches the user's chosen player. No cloud service is involved.
```

**webRequest**
```
Observes network requests in the active tab to detect media URLs (m3u8, mpd, mp4, etc.) for the resource list. Data is processed locally only and is not sent to the developer.
```

**storage**
```
Stores user preferences in the browser (e.g. sniffing on/off, site allow/deny list, player settings, float icon toggle). Data stays in chrome.storage sync/local on the user's device.
```

**cookies**
```
Reads cookies for the current website only when the user downloads or opens media that requires login. Cookies are passed to local download/player requests on the user's PC, not uploaded to any developer server.
```

**contextMenus**
```
Adds items to the extension toolbar menu (e.g. open Settings, open project home page).
```

**tabs**
```
Gets the active tab ID to associate sniffed resources with the correct page and to open the Settings or tools pages when the user clicks menu actions.
```

**webNavigation**
```
Refreshes sniffing context when the user navigates so the resource list matches the current page.
```

**alarms**
```
Keeps the background service worker responsive for low-frequency local tasks (e.g. download status polling). No user data is collected via alarms.
```

**scripting**
```
Injects bundled content scripts when needed to detect media elements and optional user-enabled features (e.g. deep key search, off by default). All script code is included in the extension package.
```

**downloads**
```
Assists with browser-initiated downloads where needed; primary HLS download is handled by the local helper app via native messaging.
```

**declarativeNetRequest**
```
Used only when the user enables optional mobile User-Agent spoofing in Settings (off by default) so some sites may serve mobile stream URLs.
```

**declarativeNetRequestWithHostAccess**
```
Same as declarativeNetRequest: optional mobile UA rules require host access. Feature is user-controlled and off by default.
```

**Host permission (http://*/* https://*/*)**
```
Broad http(s) access is required because users may visit any site where they want to discover media. The extension only inspects requests on pages the user opens. Users can optionally restrict sniffing via a site deny/allow list in Settings. No page content is transmitted to the developer.
```

**file:///* (if listed)**
```
Allows sniffing on locally opened HTML files (file://) for testing and offline pages. No remote data collection.
```

---

## Remote code

Select: **No, I am not using remote code**

Justification (if required):
```
All JavaScript and assets are bundled inside the extension package. No remote scripts are loaded at runtime.
```

---

## Data usage (checkboxes)

Check **only**:

- ✅ Authentication information (current-site cookies for local download/player; not uploaded)
- ✅ User activity (observe network requests on the active tab to find media URLs; local only)
- ✅ Website content (media URLs / video sources; processed locally only)

Leave unchecked: PII, health, financial, personal communications, location, web history.

---

## Certifications

Check **all three**:

- ✅ I do not sell or transfer user data to third parties, outside of the approved use cases
- ✅ I do not use or transfer user data for purposes that are unrelated to my item's single purpose
- ✅ I do not use or transfer user data to determine creditworthiness or for lending purposes

---

## Privacy policy URL

```
https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md
```
