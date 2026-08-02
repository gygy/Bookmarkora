# Bookmarkora

> 原名 **BookmarkSync**。远程默认同步文件仍为 `BookmarkSync.json`（兼容已有仓库）。

**跨浏览器书签云同步** — 在 Chrome、Firefox、Edge、Safari 之间同步书签，远程存储由**你自己**掌控。

当前版本：**1.1.107**

[English](README.md)

---

## v1.1.107 更新说明

```
v1.1.107

新增：同步 HTML 备份在 BookmarkSync/_snapshots_html/ 保留带日期的 bak-*.html（同时覆盖最新文件）；保留策略与远程快照一致
改进：日/韩/德/法/西/意/葡/俄/阿/繁中等语言界面文案全量补译
```

---

## Bookmarkora 是什么？

Bookmarkora 把浏览器书签备份、同步到**你自己的**远程存储。数据**不经过** Bookmarkora 开发者服务器，只保存在本机或你配置的账号里。

**支持的远程存储**

- **GitHub Gist** — 用 Personal Token 或设备码登录，上手简单  
- **私有 Gitea** — 自建 Git 仓库（兼容 GitLab / Gitee）  
- **WebDAV** — Nextcloud、群晖 NAS 等任意 WebDAV 目录  
- **S3 兼容存储** — AWS S3、Cloudflare R2、MinIO 等（浏览器扩展完整支持；macOS 应用同步支持 S3 与端到端加密）

**扩展独有功能（可选）**

- **工具中心** — 健康面板、重复/死链检测、远程快照、合并预览、版本历史、HTML/JSON 导入导出、标签页会话  
- 端到端加密（E2E）— 远程文件为密文，口令仅存于当前浏览器会话  

**两种使用方式**

| | 浏览器扩展 | macOS 应用 |
|---|------------|------------|
| **适用** | Chrome、Firefox、Edge | Mac 上的 Safari |
| **安装** | 浏览器扩展商店 | 下载 `.app` |
| **同步** | 该浏览器内的书签 | Safari 书签 |

可以只用扩展、只用 Mac 应用，或两者同时用 — 配置**同一套**远程存储（单目标：GitHub / Gitea / WebDAV / S3 择一），即可跨浏览器保持一致。

---

## 安装

### 浏览器扩展

1. 从浏览器扩展商店安装 **Bookmarkora**：  
   - [Chrome 网上应用店 — Bookmarkora](https://chromewebstore.google.com/detail/mdilbiflbhofoeokchmohbkdbobbegab?hl=zh-CN)（Edge 也可安装 Chrome 扩展）  
   - [Firefox 附加组件 — Bookmarkora](https://addons.mozilla.org/zh-CN/firefox/addon/bookmarksync-cloud-sync/)  
2. 将扩展图标固定到工具栏，方便打开。  
3. 点击图标 → **设置**（齿轮）→ 配置远程存储。

### macOS 应用（Safari）

1. 从发布页下载 **Bookmarkora.app**（或复制到「应用程序」文件夹）。  
2. 打开应用。  
3. 按提示授予**完全磁盘访问权限**，以便读取 Safari 书签：  
   **系统设置 → 隐私与安全性 → 完全磁盘访问 → 添加 Bookmarkora**  
   也可在应用内使用「选择书签文件」手动指定 `Bookmarks.plist`。  
4. 若与浏览器扩展一起使用，请配置**相同**的远程存储。

### Safari 扩展（可选）

若提供 Safari 版本，安装配套 Mac 应用后，在 **Safari → 设置 → 扩展** 中启用 Bookmarkora。

---

## 首次配置

1. 打开**设置**（扩展弹窗 → 齿轮，或 Mac 应用 → 设置标签）。  
2. 进入 **连接** 标签。  
3. 选择存储类型：**GitHub Gist**、**Gitea**、**WebDAV** 或 **S3**。  
4. 填写对应字段（见下文）。GitHub 可使用 **设备码登录** 获取 Token。  
5. 点击 **测试连通性**。  
   - 使用 Gitea 或 WebDAV 时，浏览器会询问是否允许访问你的服务器地址，请选择允许。  
6. 返回主界面，尝试 **同步书签**（合并）或 **上传**。

---

## 远程存储配置

### GitHub Gist

1. 创建 [Personal Access Token](https://github.com/settings/tokens/new)，勾选 **gist** 权限。  
2. 新建 [Gist](https://gist.github.com/)，从 URL 中复制 Gist ID。  
3. 在 Bookmarkora 设置中填写：  
   - **GitHub Token** — 粘贴 Token  
   - **Gist ID** — 粘贴 ID  
   - **文件名** — 默认 `BookmarkSync`（需与 Gist 内文件名一致）  
4. **测试连通性** → 若尚无文件，首次上传会自动创建。

### 私有 Gitea

1. 在 Gitea 上创建仓库，并生成具有仓库写入权限的 Token。  
2. 在 Bookmarkora 设置中填写：  
   - **Gitea 地址** — 如 `https://gitea.example.com`  
   - **Token**、**所有者**、**仓库**、**分支**（默认 `main`）  
3. 书签保存在仓库根目录的 `BookmarkSync.json`。  
4. **测试连通性** → 在浏览器弹窗中允许访问你的 Gitea 域名。

### WebDAV

1. 在 WebDAV 服务上准备或创建一个目录。  
2. 在 Bookmarkora 设置中填写：  
   - **WebDAV 目录地址** — 完整文件夹 URL，例如  
     `https://cloud.example.com/remote.php/dav/files/用户名/bookmarks/`  
   - **用户名**、**密码**（Basic 认证）  
   - **文件名** — 默认 `BookmarkSync.json`  
3. **测试连通性** → 允许浏览器访问你的 WebDAV 主机。

**常见 WebDAV 服务**

| 服务 | 说明 |
|------|------|
| Nextcloud | 在「文件」设置中查看 WebDAV 路径 |
| 群晖 NAS | 在套件中心启用 WebDAV，使用共享文件夹 URL |
| 其他 | 需可通过 HTTPS 访问的目录 URL |

---

## 日常使用

### 扩展弹窗

| 操作 | 作用 |
|------|------|
| **同步书签** | 合并本地与远程（日常推荐） |
| **上传** | 将本地书签推送到远程 |
| **下载** | 用远程书签覆盖本地 |
| **清空本地** | 删除所有本地书签（会先自动快照，需确认） |
| **清空远程** | 仅清空远程，本地保留（需确认） |

底部显示**本地 / 远程**书签数量及当前推送目标。

### 推送目标（设置 → 同步）

可同时勾选**多个**后端（例如 GitHub + WebDAV）：

- 勾选 **GitHub**、**Gitea**、**WebDAV** 中的任意组合。  
- **上传**、**合并**、**清空远程** 会作用于所有已选目标。  
- **下载**、**合并** 读取远程时以**主目标**为准（多选时可指定）。

### 自动同步（设置 → 同步）

各后端可独立开启：

- **书签变更时** — 修改书签后自动上传或合并  
- **定时** — 每隔 N 分钟上传、下载或合并  

自动同步默认不弹出成功通知；手动操作可按需开启通知。

### macOS 应用

Mac 应用提供与扩展相同的 Safari 书签操作：上传、下载、合并、清空本地/远程、快照与设置。下载或合并后，若界面未刷新，可重启 Safari 或重新打开书签侧边栏。

---

## 快照与安全

- 在**清空本地**、**清空远程**或大规模覆盖前，Bookmarkora 会尽量先创建**快照**。  
- 在 **设置 → 数据**（扩展）或 **数据** 标签（Mac 应用）中查看、恢复快照。  
- **配置备份** 可恢复之前的连接设置。


---

## 下载安装包

**Chrome：** 请从 [Chrome 网上应用店 — Bookmarkora](https://chromewebstore.google.com/detail/mdilbiflbhofoeokchmohbkdbobbegab?hl=zh-CN) 安装。

**Firefox：** 请从 [Firefox 附加组件 — Bookmarkora](https://addons.mozilla.org/zh-CN/firefox/addon/bookmarksync-cloud-sync/) 安装。

开发者模式或离线安装时，可从本仓库 [dist/](dist/) 获取最新安装包（当前 v1.1.107）：

- [Bookmarkora-1.1.107-chrome.zip](dist/Bookmarkora-1.1.107-chrome.zip)

产品截图见 [screenshots/](screenshots/)（英文根目录、zh_CN/ 中文）。

---

## 隐私

Bookmarkora 不运营同步服务器。书签与凭据仅保存在本机或你配置的 GitHub / Gitea / WebDAV / S3 中。

完整说明：[隐私政策](PRIVACY.md)

---

## 常见问题

**Chrome 和 Safari 能一起同步吗？**  
可以。在 Chrome 扩展和 Mac 应用里配置**同一个** Gist / Gitea / WebDAV，在两边分别执行**合并**即可。

**Token 安全吗？**  
Token 和密码保存在浏览器同步存储或 Mac 本地设置中，不会发送给 Bookmarkora 开发者。可随时在 GitHub / Gitea / WebDAV 侧撤销或修改。

**下载和合并有什么区别？**  
**合并**会综合本地与远程书签，更安全。**下载**会用远程书签**完全替换**本地。

**为什么 Mac 要「完全磁盘访问」？**  
Safari 书签存放在受系统保护的文件中，Mac 应用需要读写权限才能同步。

---

## 许可证

MIT — 见 [LICENSE](LICENSE)
