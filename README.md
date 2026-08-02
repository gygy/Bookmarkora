# Bookmarkora

> Formerly **BookmarkSync**. Default remote sync file remains `BookmarkSync.json` for existing repos.

**Cross-browser bookmark sync** — keep bookmarks in sync across Chrome, Firefox, Edge, and Safari using storage **you** control.

Version **1.1.108**

[简体中文](README_cn.md)

---

## What's new in v1.1.108

```
v1.1.108

FIXED: Privacy policy updated for Microsoft Edge Add-ons (clear personal-information disclosure and user controls; HTML policy URL)
```

---

## What is Bookmarkora?

Bookmarkora backs up and syncs your browser bookmarks to **your own** remote storage. Your data never passes through a Bookmarkora server — it stays on your device or in accounts you configure.

**Supported remote storage**

- **GitHub Gist** — simple cloud backup via a personal token  
- **Private Gitea** — self-hosted Git repository  
- **WebDAV** — Nextcloud, Synology NAS, or any WebDAV folder  
- **S3-compatible** — AWS S3, Cloudflare R2, MinIO  

**Extension highlights (v1.1.108)**

- **Tools hub** — health panel, duplicates, broken links, snapshots, merge preview, version history, tab sessions  
- Optional **end-to-end encryption** for remote bookmark files  

**Two ways to use it**

| | Browser extension | macOS app |
|---|-------------------|-----------|
| **For** | Chrome, Firefox, Edge | Safari on Mac |
| **Install** | Browser add-on store | Download `.app` |
| **Syncs** | That browser’s bookmarks | Safari bookmarks |

You can use the extension alone, the Mac app alone, or both — point them at the **same** Gist / Gitea / WebDAV / S3 to stay in sync across browsers.

---

## Install

### Browser extension

1. Install **Bookmarkora** from your browser’s extension store:  
   - [Chrome Web Store — Bookmarkora](https://chromewebstore.google.com/detail/mdilbiflbhofoeokchmohbkdbobbegab) (also works for Edge)  
   - [Firefox Add-ons — Bookmarkora](https://addons.mozilla.org/firefox/addon/bookmarksync-cloud-sync/)  
2. Pin the extension icon to the toolbar for quick access.  
3. Click the icon → **Settings** (gear) to connect your remote storage.

### macOS app (Safari)

1. Download **Bookmarkora.app** from the release page (or copy to `/Applications`).  
2. Open the app.  
3. When prompted, grant **Full Disk Access** so the app can read Safari bookmarks:  
   **System Settings → Privacy & Security → Full Disk Access → add Bookmarkora**  
   Alternatively, use **Choose bookmark file** inside the app to pick `Bookmarks.plist` manually.  
4. Configure the same remote storage as in the browser extension (if you use both).

### Safari extension (optional)

If a Safari version is provided, install the companion app from the Mac App Store or developer build, then enable it in **Safari → Settings → Extensions**.

---

## First-time setup

1. Open **Settings** (extension popup → gear, or macOS app → Settings tab).  
2. Go to **Connection**.  
3. Choose a storage type: **GitHub Gist**, **Gitea**, **WebDAV**, or **S3**.  
4. Fill in the fields (see below).  
5. Click **Test Connection**.  
   - For Gitea or WebDAV, allow access when the browser asks for permission to your server URL.  
6. Return to the main screen and try **Sync bookmarks** (merge) or **Upload**.

---

## Remote storage setup

### GitHub Gist

1. Create a [Personal Access Token](https://github.com/settings/tokens/new) with **gist** access.  
2. Create a new [Gist](https://gist.github.com/) and copy its ID from the URL.  
3. In Bookmarkora settings:  
   - **GitHub Token** — paste the token  
   - **Gist ID** — paste the ID  
   - **File name** — default `BookmarkSync` (must match the file in the Gist)  
4. **Test Connection** → first upload creates the file if it does not exist yet.

### Private Gitea

1. Create a repository on your Gitea server and generate an access token with repo write access.  
2. In Bookmarkora settings:  
   - **Gitea URL** — e.g. `https://gitea.example.com`  
   - **Token**, **owner**, **repo**, **branch** (default `main`)  
3. Bookmarks are saved as `BookmarkSync.json` in the repository root.  
4. **Test Connection** → allow browser access to your Gitea domain when prompted.

### WebDAV

1. Create or choose a folder on your WebDAV server.  
2. In Bookmarkora settings:  
   - **WebDAV folder URL** — full path to the folder, e.g.  
     `https://cloud.example.com/remote.php/dav/files/username/bookmarks/`  
   - **Username** and **password** (Basic auth)  
   - **File name** — default `BookmarkSync.json`  
3. **Test Connection** → allow browser access to your WebDAV host when prompted.

**Common WebDAV services**

| Service | Notes |
|---------|--------|
| Nextcloud | Use the WebDAV path from Files settings |
| Synology | Enable WebDAV in Package Center; use the shared folder URL |
| Other | Folder URL must be reachable over HTTPS |

---

## Daily use

### Extension popup

| Action | What it does |
|--------|----------------|
| **Sync bookmarks** | Merge local and remote (recommended for daily use) |
| **Upload** | Push local bookmarks to remote |
| **Download** | Replace local bookmarks with remote |
| **Clear local** | Remove all local bookmarks (snapshot created first; confirmation required) |
| **Clear remote** | Clear remote copy only; local bookmarks kept (confirmation required) |

The footer shows **local** and **remote** bookmark counts and which storage targets are active.

### Push targets (Settings → Sync)

You can sync to **more than one** backend at once (e.g. GitHub + WebDAV):

- Check **GitHub**, **Gitea**, and/or **WebDAV** under push targets.  
- **Upload**, **merge**, and **clear remote** apply to all checked targets.  
- **Download** and **merge** read from the **primary** target (choose when multiple are enabled).

### Auto-sync (Settings → Sync)

Turn on auto-sync per backend:

- **When bookmarks change** — upload or merge after edits  
- **On a schedule** — upload, download, or merge every N minutes  

Auto-sync runs silently (no success notifications). Manual actions can still show optional notifications.

### macOS app

The Mac app offers the same sync actions for **Safari** bookmarks: upload, download, merge, clear local/remote, snapshots, and settings. After a download or merge, restart Safari or reopen the bookmarks sidebar if counts look stale.

---

## Snapshots & safety

- Before **clear local**, **clear remote**, or large overwrites, Bookmarkora creates a **snapshot** when possible.  
- View and restore snapshots in **Settings → Data** (extension) or the **Data** tab (Mac app).  
- Config backups let you restore previous connection settings.


---

## Downloads

**Chrome:** Install from the [Chrome Web Store — Bookmarkora](https://chromewebstore.google.com/detail/mdilbiflbhofoeokchmohbkdbobbegab).

**Firefox:** Install from [Firefox Add-ons — Bookmarkora](https://addons.mozilla.org/firefox/addon/bookmarksync-cloud-sync/).

For manual load (developer mode), get the latest packages (v1.1.108) from [dist/](dist/):

- [Bookmarkora-1.1.108-chrome.zip](dist/Bookmarkora-1.1.108-chrome.zip)

Product screenshots: [screenshots/](screenshots/) (English at root, zh_CN/ for Chinese).

---

## Privacy

Bookmarkora does not operate sync servers. Bookmarks and credentials are stored on your device or in storage you configure (GitHub, Gitea, WebDAV, S3).  

Full policy: [Privacy Policy](PRIVACY.md)

---

## FAQ

**Can I sync Chrome and Safari together?**  
Yes. Use the same Gist / Gitea / WebDAV in the Chrome extension and the macOS app. Run **merge** on each side when switching devices.

**Is my token safe?**  
Tokens and passwords are stored in browser sync storage or local Mac settings — not sent to Bookmarkora developers. Revoke tokens anytime on GitHub/Gitea/WebDAV.

**Download vs merge?**  
**Merge** combines local and remote (safer). **Download** replaces local bookmarks entirely with remote.

**Why does macOS ask for Full Disk Access?**  
Safari stores bookmarks in a protected file. The Mac app needs read/write access to sync them.

---

## License

MIT — see [LICENSE](LICENSE)
