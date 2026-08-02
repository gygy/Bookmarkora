# Bookmarkora Privacy Policy

**Last updated:** August 2, 2026

This privacy policy applies to the **Bookmarkora** browser extension available on **Microsoft Edge Add-ons** (and the same product on other Chromium/Firefox stores), plus the optional macOS companion app.

Bookmarkora helps you sync browser bookmarks with **storage you control** (for example GitHub Gist, Gitee, GitLab, self-hosted Gitea, WebDAV, S3-compatible object storage, Google Drive, or OneDrive). Optional end-to-end encryption keeps remote bookmark files encrypted; the passphrase stays on your device and is never sent to the developer.

## Summary

- Bookmarkora **does not operate developer-owned servers** for sync, analytics, or advertising.
- Bookmarks, credentials, tab sessions, and settings stay **on your device** and in **storage you configure**.
- We do **not** sell, rent, or share your data with third parties for advertising or analytics.
- The extension does **not** collect your general browsing history.

## Personal information we access

Bookmarkora may access or transmit the following information **only** to provide sync and Tools features you use:

| Category | Examples | Where it stays / goes |
|----------|----------|------------------------|
| Website content | Bookmark URLs, titles, folder names | Your device; your configured remote |
| Authentication information | Tokens, passwords, API keys you enter | Device storage only; used to talk to **your** remote |
| Tab session data (optional) | Open tab URLs/titles when you save a session | Device; optionally your remote if you sync sessions |

We do **not** collect health, financial, location, or general web-history data.

## How data is used

- Sync (upload / download / merge / auto-sync) reads and writes bookmarks as you configure.
- Tools (duplicates, broken-link check, snapshots, hygiene, tab sessions) run on your device when you start them or enable schedules.
- Broken-link checks may open background tabs to URLs **already in your bookmarks**; those requests go to the target sites, not to the developer.

## Where data is sent

When you sync, data is sent **only** to remotes **you** configure:

- GitHub / Gitee / GitLab / your Gitea instance  
- Your WebDAV server  
- Your S3-compatible endpoint and bucket  
- Google Drive or OneDrive (when you choose those providers and grant access)

No bookmark, credential, or tab data is sent to Bookmarkora developers or any Bookmarkora intermediary service.

## User controls (access, sharing, opt-out)

You control all processing:

1. **Stop sync / Tools** — turn off auto-sync and scheduled Tools, or do not use those features.  
2. **Remove credentials** — clear tokens/keys in Settings, or revoke them at the provider (GitHub, Gitea, Google, Microsoft, etc.).  
3. **Delete local data** — uninstall the extension/app (subject to browser/OS behavior), or clear local snapshots/logs in Settings/Tools.  
4. **Delete remote data** — delete sync files on your remote, or use in-app clear/restore actions.  
5. **Revoke host access** — deny optional host permissions for remotes you no longer use.

There is no developer-side account to request deletion from: we do not host your data.

## Permissions (browser extension)

| Permission | Purpose |
|------------|---------|
| `bookmarks` | Sync and Tools that read/write bookmarks |
| `storage` | Local settings, credentials, snapshots, logs, sessions |
| `alarms` | Scheduled auto-sync / Tools when enabled |
| `notifications` | Optional sync success/failure alerts |
| `tabs` / `windows` / `webNavigation` | Tab sessions and broken-link checks you start—not browsing tracking |
| Host access | Only origins needed for remotes you configure (GitHub fixed hosts; others requested at runtime) |

## macOS companion app

With Full Disk Access (or a file you select), the macOS app may read Safari bookmarks and sync to the same class of remotes. Data handling matches this policy.

## Children

Bookmarkora is not directed at children under 13. We do not knowingly collect personal information from children.

## Changes

We may update this policy when the product changes. The “Last updated” date above reflects the latest revision.

## Contact

Privacy questions: open an issue at [github.com/gygy/Bookmarkora](https://github.com/gygy/Bookmarkora), or contact the publisher listed on the **Microsoft Edge Add-ons** product page for Bookmarkora (also listed on Chrome Web Store / Firefox Add-ons where published).

---

# Bookmarkora 隐私政策（中文）

**最后更新：** 2026 年 8 月 2 日

本政策适用于 **Microsoft Edge 扩展商店**上的 Bookmarkora 扩展（及其他浏览器商店中的同款产品），以及可选的 macOS 伴侣应用。

Bookmarkora 将书签同步到 **您自行配置** 的远程存储（如 GitHub Gist、Gitee、GitLab、自建 Gitea、WebDAV、S3 兼容存储、Google Drive、OneDrive）。可选端到端加密口令仅保存在您的设备上，不会发送给开发者。

## 概要

- **没有**开发者运营的同步/分析/广告服务器。  
- 书签、凭据、会话与设置保存在 **本机** 与 **您配置的远程**。  
- **不**出售或出租数据。  
- **不**收集日常浏览历史。

## 可能访问的个人信息

| 类别 | 示例 | 去向 |
|------|------|------|
| 网站内容 | 书签 URL、标题、文件夹名 | 本机；您的远程 |
| 身份验证信息 | 您输入的 Token/密码/密钥 | 仅本机；用于访问您的远程 |
| 标签页会话（可选） | 您保存会话时的标签 URL/标题 | 本机；若同步会话则可到您的远程 |

不收集健康、财务、位置或一般网页历史。

## 用户控制（访问、共享与退出）

1. 关闭自动同步与定时工具，或不使用相关功能。  
2. 在设置中清除凭据，或在各服务商处撤销授权。  
3. 卸载扩展/应用，或清理本地快照与日志。  
4. 在远程存储删除同步文件，或使用应用内清空/恢复。  
5. 拒绝不再使用的远程主机权限。

开发者侧 **不托管** 您的数据，故无“向开发者申请删号”流程。

## 联系我们

请在 [github.com/gygy/Bookmarkora](https://github.com/gygy/Bookmarkora) 提交 Issue，或通过 **Microsoft Edge 扩展商店**产品页中的发布者信息联系（其他商店 listing 同样适用）。
