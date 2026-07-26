# Bookmarkora Privacy Policy

**Last updated:** June 22, 2026

Bookmarkora ("the Extension" or "the App") helps you sync browser bookmarks with storage you control: **GitHub Gist**, your own **Gitea** server, a **WebDAV** folder, or **S3-compatible** object storage. Optional **end-to-end encryption** keeps remote bookmark files encrypted; the passphrase stays in your browser session (extension) or in app memory (macOS) and is never sent to developers.

Optional **Tools** features (duplicate cleanup, broken-link check, snapshots, named **tab sessions**, and related utilities) run on your device. They use bookmark or tab data only when **you** open Tools and start an action—or when you enable scheduled tool scans.

## Summary

- Bookmarkora **does not operate developer-owned servers** for sync or analytics.
- Your bookmarks, credentials, tab sessions, and settings stay **on your device** and in **storage you configure**.
- We do **not** sell, rent, or share your data with third parties for advertising or analytics.
- The Extension does **not** collect your general browsing history. `tabs` / `webNavigation` are used only for Tools you explicitly use (e.g. tab sessions, broken-link check), not for background tracking.

## Data the Extension Handles

### Browser bookmarks

The Extension (or macOS App) reads and modifies bookmarks to upload, download, merge, restore, deduplicate, or remove them when **you** trigger those actions, use Tools, or when auto-sync is enabled.

### Tab sessions (browser extension only)

When you use **Tab Session** features in Tools, the Extension may read open tab URLs and titles in the current window to save a named session locally and optionally sync session JSON to your configured remote storage. Sessions are not collected in the background without your action.

### Sync configuration

Settings such as sync provider (GitHub / Gitea / WebDAV / S3), Gist ID, Gitea URL, WebDAV folder URL, S3 endpoint and bucket settings, file names, auto-sync mode, sync scope, E2E encryption toggle, notification preferences, and tool schedules are stored locally (`chrome.storage.sync` / `chrome.storage.local`, macOS UserDefaults, or iCloud config backup if you enable it).

### Credentials

If you provide credentials, they are stored on your device only:

- GitHub Personal Access Token  
- Gitea access token  
- WebDAV username and password (Basic authentication)  
- S3 access key and secret key  
- E2E encryption passphrase (session-only in the extension; in-memory on macOS when enabled)

These are used only to access **your** configured remote storage. They are **not** transmitted to Bookmarkora developers.

### Local snapshots and logs

Bookmark snapshots, configuration backups, sync logs, and tab session backups may be stored locally to support restore and troubleshooting. They are not uploaded unless **you** sync to your remote storage.

## Where Data Is Sent

When you sync, bookmark data, tab session files, and related JSON are sent only to:

- **GitHub** (`github.com`, `githubusercontent.com`) — when you configure GitHub Gist sync  
- **Your Gitea server** — only the origin you configure; the browser extension requests host permission at runtime  
- **Your WebDAV server** — only the origin/folder URL you configure; the browser extension requests host permission at runtime  
- **Your S3-compatible endpoint** — only the endpoint and bucket you configure; the browser extension requests host permission at runtime when needed  

Broken-link checks initiated in Tools may cause the Extension to open **background tabs** to URLs already present in **your bookmarks**. Those requests go directly to the target websites—not to Bookmarkora developers.

No bookmark, credential, or tab data is sent to the Bookmarkora author or any intermediary service operated for Bookmarkora.

## Permissions (Browser Extension)

| Permission | Purpose |
|------------|---------|
| `bookmarks` | Read/write bookmarks for sync and Tools (cleanup, import/export, link check on bookmark URLs, etc.) |
| `storage` | Save settings, credentials, snapshots, sync logs, config backups, and tab session data locally |
| `alarms` | Run scheduled auto-sync and optional periodic tool scans when you enable them |
| `notifications` | Optional sync success/failure notifications |
| `tabs` | Save/restore tab sessions; open background tabs when you run **Broken Link Check** on bookmark URLs |
| `windows` | Restore saved tab sessions into browser windows when you choose Restore in Tools |
| `webNavigation` | Detect navigation errors during user-initiated broken-link checks and tab session operations—not for browsing history tracking |
| GitHub host access (`github.com`, `githubusercontent.com`) | Access your configured Gist |
| Optional `*://*/*` | Requested at runtime when you configure a **Gitea**, **WebDAV**, or **S3** URL and click Test Connection or sync—limited to origins you specify |

## macOS App

The macOS companion app reads Safari bookmarks via `Bookmarks.plist` when you grant **Full Disk Access** or select the bookmarks file. Synced data goes only to remotes you configure (GitHub / Gitea / WebDAV / S3), same as the browser extension.

## Data Retention and Deletion

- **Uninstall the extension or app** — removes locally stored data (subject to OS/browser behavior).  
- **Clear remote data** — use in-app actions or delete files on GitHub / Gitea / WebDAV / S3 directly.  
- **Revoke credentials** — delete or rotate tokens, keys, or passwords on GitHub, Gitea, WebDAV, or S3 at any time.

## Children

Bookmarkora is not directed at children under 13, and we do not knowingly collect personal information from children.

## Changes

We may update this policy when the product changes. The "Last updated" date at the top will reflect the latest revision.

## Contact

For privacy questions, open an issue in the project repository or contact the publisher listed on the Chrome Web Store / Firefox Add-ons listing.

---

# Bookmarkora 隐私政策（中文）

**最后更新：** 2026 年 6 月 22 日

Bookmarkora（「本扩展」或「本应用」）帮助您将浏览器书签同步到您自行控制的存储：**GitHub Gist**、**私有 Gitea**、**WebDAV 目录**或 **S3 兼容**对象存储。可选 **端到端加密** 用于保护远程书签文件；加密口令保存在浏览器会话（扩展）或应用内存（macOS）中，**不会**发送给开发者。

可选 **工具中心** 功能（重复书签清理、死链检测、快照、**标签页会话**等）均在您的设备上运行，仅在 **您** 打开工具并执行操作时—or 在您启用定时工具扫描时—使用相关书签或标签页数据。

## 概要

- 书签同步与工具功能**不经过开发者服务器**，也不用于广告或分析追踪。
- 书签、凭据、标签页会话与设置保存在 **您的设备** 及 **您配置的远程存储** 中。
- **不会**为广告或分析目的出售、出租或共享您的数据。
- 本扩展 **不收集** 您的日常浏览历史。`tabs` / `webNavigation` 仅用于您主动使用的工具（如标签页会话、死链检测），不作后台追踪。

## 处理的数据

### 浏览器书签

仅在您手动操作、使用工具中心，或开启自动同步时，读取或修改书签（上传、下载、合并、恢复、去重、清空等）。

### 标签页会话（仅浏览器扩展）

使用工具中心的 **标签页会话** 时，扩展可能读取当前窗口中可保存标签页的 URL 与标题，在本地保存命名会话，并可选择将会话 JSON 同步到您配置的远程存储。不会在未经您操作的情况下后台收集标签页。

### 同步配置

同步方式（GitHub / Gitea / WebDAV / S3）、Gist ID、Gitea 地址、WebDAV 目录、S3 端点与存储桶、文件名、自动同步模式、同步范围、端到端加密开关、通知与工具定时任务等，保存在浏览器扩展存储、macOS 本地设置，或您开启的 iCloud 配置备份中。

### 凭据

以下凭据 **仅保存在本机**，用于访问您配置的远程存储，**不会**发送给 Bookmarkora 开发者：

- GitHub Personal Access Token  
- Gitea Token  
- WebDAV 用户名与密码（Basic 认证）  
- S3 Access Key 与 Secret Key  
- 端到端加密口令（扩展为会话级；macOS 启用时仅在内存中）

### 本地快照与日志

可能在本地保存书签快照、配置备份、同步日志与标签页会话备份，用于恢复与排查；除非您主动同步，否则不会上传至第三方。

## 数据去向

同步时，书签数据、标签页会话文件及相关 JSON 仅发送至：

- **GitHub**（`github.com`、`githubusercontent.com`）— 配置 Gist 同步时  
- **您指定的 Gitea 服务器** — 扩展在运行时按您配置的域名申请主机权限  
- **您指定的 WebDAV 服务器** — 扩展在运行时按您配置的地址申请主机权限  
- **您指定的 S3 兼容端点** — 仅访问您配置的端点与存储桶；需要时由扩展在运行时申请主机权限  

在工具中心发起 **死链检测** 时，扩展可能对 **书签中已有的 URL** 打开后台标签页进行检测；请求直接发往目标网站，**不经过** Bookmarkora 开发者。

不向 Bookmarkora 作者或任何中间服务传输书签、凭据或标签页数据。

## 权限说明（浏览器扩展）

| 权限 | 用途 |
|------|------|
| `bookmarks` | 同步与工具中心读写书签（清理、导入导出、对书签 URL 做死链检测等） |
| `storage` | 本地保存设置、凭据、快照、同步日志、配置备份与标签页会话 |
| `alarms` | 在您启用时执行定时自动同步与可选的周期性工具扫描 |
| `notifications` | 可选的同步成功/失败通知 |
| `tabs` | 保存/恢复标签页会话；在您运行 **死链检测** 时对书签 URL 打开后台标签页 |
| `windows` | 在工具中心选择恢复时，将已保存的标签页会话还原到浏览器窗口 |
| `webNavigation` | 在用户发起的死链检测与标签页会话操作中使用，用于判断导航错误；**不用于**浏览历史追踪 |
| GitHub 主机访问 | 访问您配置的 Gist |
| 可选 `*://*/*` | 配置 **Gitea**、**WebDAV** 或 **S3** 地址并测试/同步时，按您指定的源运行时申请 |

## macOS 应用

macOS 伴侣应用在您授予 **完全磁盘访问** 或手动选择书签文件后，读取 Safari 书签；远程同步目标与扩展相同（GitHub / Gitea / WebDAV / S3），数据同样只发往您配置的存储。

## 删除数据

- **卸载扩展或应用** — 清除本地数据（以系统/浏览器行为为准）  
- **清空远程** — 使用应用内功能，或在 GitHub / Gitea / WebDAV / S3 上直接删除对应文件  
- **撤销凭据** — 在 GitHub、Gitea、WebDAV 或 S3 账户中随时修改、轮换或删除 Token/密钥/密码  

## 儿童隐私

本应用不面向 13 岁以下儿童，也不会故意收集儿童个人信息。

## 政策变更

产品变更时我们可能更新本政策；文首「最后更新」日期将随之调整。

## 联系我们

如有隐私相关问题，请在项目仓库提交 Issue，或通过 Chrome 网上应用店 / Firefox 附加组件 listing 中的发布者信息联系。
