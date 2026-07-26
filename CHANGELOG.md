# Changelog

All notable changes to Bookmarkora are documented here.

## [Unreleased]

## [1.1.97] - 2026-07-26

### Changed
- **GitHub**: public repo renamed to [`gygy/Bookmarkora`](https://github.com/gygy/Bookmarkora); official site / privacy / release scripts updated. Local sync still uses `BookmarkSync.json` paths.

## [1.1.96] - 2026-07-26

### Fixed
- **Rebrand leftovers**: restore Firefox AMO store slug `bookmarksync-cloud-sync` (display name remains Bookmarkora); Mac Keychain service `com.bookmarksync.macos` and local snapshot dir `BookmarkSync/Snapshots`; Safari extension bundle id `com.bookmarksync.extension`; README Gist default filename `BookmarkSync`; gist verify placeholder examples.

## [1.1.95] - 2026-07-26

### Changed
- **Brand**: product display name **BookmarkSync → Bookmarkora** (extension title, UI, docs, package artifacts). Store-oriented titles keep sync keywords (e.g. `Bookmarkora · 书签同步` / `Bookmarkora — Bookmark Sync`).
- **Compatibility**: remote sync filenames (`BookmarkSync.json`, `BookmarkSync/_snapshots/`), Firefox id `bookmarksync@gygy`, and Mac bundle id `com.bookmarksync.app` are **unchanged** so existing installs keep syncing.

## [1.1.94] - 2026-07-26

### Changed
- **Organize (extension)**: General settings card title 「整理偏好」→「智能整理(实验)」across locales; Mac N/A

## [1.1.93] - 2026-07-23

### Changed
- **Organize (extension)**: planning-first flow — intensity (gentle/balanced/bold), confidence default selection, preview-only CTA, clearer apply confirm with snapshot/no-delete; Mac N/A (organize is extension-only)

## [1.1.92] - 2026-07-23

### Changed
- **整理助手体验**：按易用性 / 吸引力 / 交互反馈 / 去 AI 痕迹四维迭代——助手语气问候、主按钮「帮我整理」、生成中轮播提示、健康分可读文案、周小结有内容才出现、去掉重复空态与「AI/模型」主文案。Mac：仅同步版本号。

## [1.1.91] - 2026-07-23

### Changed
- **整理页入口**：去掉重复的「API 设置」，仅在主操作旁保留一处「模型设置」；通用页卡片改为「整理 · AI 模型」。Mac：仅同步版本号。

## [1.1.90] - 2026-07-23

### Changed
- **整理提速**：本地方案目标 &lt;6s；AI 增强软超时 4s（超时自动回退本地）；缩小 LLM 样本；enrich 仅对推荐方案全量算 impact；近重复检测与主题扫描降复杂度；树只读一次。Mac：仅同步版本号。

## [1.1.89] - 2026-07-22

### Added
- **整理 · 文件夹智能总览**：基于全部书签深度分析——内容主题、现有文件夹合理性（判定/分数/理由）、建议目录与证据说明、认知模型与深度元信息。Mac：仅同步版本号（整理为扩展独有）。

## [1.1.88] - 2026-07-22

### Changed
- **文案**：设置页 Tab「标签智能整理」改为「整理」（`optionsTabOrganize`）。Mac：仅同步版本号。

## [1.1.87] - 2026-07-22

### Fixed
- **多语言完整性**：整理相关 UI/错误/探测文案覆盖全部 12 种语言；去掉中文硬编码回退；AI 方案与实时建议语言跟随「应用语言 / 系统语言」；服务商名称按所选语言显示；补齐 diff/会话/向导等遗留英文串。Mac：仅同步版本号，无功能对齐项。

## [1.1.86] - 2026-07-22

### Changed
- **AI 服务商验证**：对全部预设端点做了可达性探测（DeepSeek/通义/智谱/Kimi/硅基/火山/百川/MiniMax/OpenAI/Claude/Gemini/OpenRouter/OpenCode/Groq/Mistral/Together 均可达并进入鉴权门）；补齐 Anthropic `max_tokens` / Gemini `x-goog-api-key` / OpenRouter Referer；更新 Claude 与 OpenCode 模型列表。


## [1.1.85] - 2026-07-22

### Changed
- **文案**：Tab / 页面 / 设置标题统一为「标签智能整理」，去掉重复双标题。


## [1.1.84] - 2026-07-22

### Fixed
- **OpenCode Go 连通性**：最小请求体（user-only + stream:false）、探测时轮询备用模型、先验 /models；错误文案明确为服务商上游故障并建议改用 Zen 免费模型或直连。


## [1.1.83] - 2026-07-22

### Changed
- **文案**：将「智能整理」统一改为「整理」（Tab / 主按钮 / 标题）。


## [1.1.82] - 2026-07-22

### Fixed
- **OpenCode Go/Zen**：连通性测试与调用不再发送 temperature（避免 Console Go Upstream request failed）；模型 id 去掉 provider 前缀；错误提示更明确；Zen 默认推荐免费模型。


## [1.1.81] - 2026-07-22

### Changed
- **智能整理AI**：精品扩展级 UX 演进——统一命名、三步流程、空态引导、应用下沉与成功态、周建议可操作、筛选/应用分层、历史建议可采纳。


## [1.1.80] - 2026-07-22

### Fixed
- **测试 AI 连通性**：结果改在 AI 设置区显示；使用当前表单配置；在设置页请求主机权限；正确处理失败返回。


## [1.1.79] - 2026-07-22

### Changed
- **AI 服务商**：下拉列表不再区分「中国 / 通用」分组，改为统一列表。


## [1.1.78] - 2026-07-22

### Changed
- **整理 / AI**：去掉「仅本地规则」选项与「关闭（仅本地规则）」服务商；有模型则走 AI，未配置时仍自动回退本地引擎。

## [1.1.77] - 2026-07-22

### Added
- **兼容 OpenCode**：新增 OpenCode Zen / Go 预设（https://opencode.ai/zen/v1）；支持导入本机 opencode.json 自动填充服务商、Base URL 与模型。

## [1.1.76] - 2026-07-22

### Changed
- **AI 模型设置**：扩充中国常用（DeepSeek / 通义 / 智谱 / Kimi / 硅基流动 / 豆包等）与通用（OpenAI / Claude / Gemini / OpenRouter / Groq 等）预设；支持自定义 OpenAI 兼容网关与任意模型名；切换服务商自动填入 Base URL 与推荐模型。

## [1.1.75] - 2026-07-16

### Changed
- **文件夹对照表**：方案预览先展示「旧文件夹 → 新文件夹」一一对照，可改新夹名、逐条/全部采纳；未采纳行不进入应用范围。

## [1.1.74] - 2026-07-16

### Changed
- **方案预览可读性**：每条显示「原文件夹 → 新文件夹」；顶部汇总文件夹数前后对比与移动/归档/保留/待定数；明确归档不等于删除。

## [1.1.73] - 2026-07-16

### Fixed
- **智能整理无反应**：未配置 API 时误走云端权限校验导致失败且 UI 未提示；现默认本地规则即可生成方案，并正确展示后台错误。


## [1.1.72] - 2026-07-16

### Changed
- **整理 · 一键智能**：主路径改为「智能整理」——自动诊断并按健康度选保守/平衡/重构；诊断摘要展示已选方案；仅在有依据时提示「也可以」减负/场景；场景·项目·减负收到「更多」。

## [1.1.71] - 2026-07-16

### Changed
- **整理 · 目标向导**：去掉含糊的模式下拉，改为「你想做什么？」四选一（优化目录 / 按场景 / 按项目 / 减负归档），每项一行说明；切换目标会清空旧方案。场景/项目/减负在本地规则与 LLM 提示中差异更明确。

## [1.1.70] - 2026-07-16

### Changed
- **整理 · 新增建议 UI**：顶部结构化卡片（标题/URL/当前·建议路径/标签），支持采纳移动、忽略、清空；保留最近 12 条历史并可折叠查看。

## [1.1.69] - 2026-07-16

### Changed
- **菜单树图标**：设置页外观为「菜单树」时，左侧导航显示与标签一致的图标。
- **整理页 · AI书签顾问**：统一命名；方案预览改为多行卡片，动作/目标文件夹/标题/URL 一眼看全；精简文案与交互。
- **通用 · 智能整理AI**：设置标题改为「智能整理AI」；新增「新增书签时给出归档建议」（目标夹 / 子夹 / 臃肿 / 合并拆分 / 重复相似），写入整理页并可通知。

## [1.1.68] - 2026-07-16

### Added
- **书签 IA 架构顾问**：整理页「智能分析」升级为 Information Architecture 诊断——多维评分（命名/分类/层级/重复/可维护/可发现/扩展）、万能目录与认知模型混乱检测，并固定输出**保守 / 平衡（推荐）/ 重构**三套可预览方案；默认不直接改库，确认后再应用。
  - 扩展：`aiOrganizeLibrary.ts`、`aiOrganizeIaSchemes.ts`、Organize 评分卡与方案卡。
  - **Mac 无需对齐**。
  - 后续：新增书签时的持续 IA 建议（放哪 / 是否新建 / 是否臃肿）将在后续版本接入。

## [1.1.67] - 2026-07-15

### Added
- **书签整理 · 智能分析（推荐）**：对标 Raindrop Stella 等能力——先诊断现有文件夹（空夹、近名夹、过深、主题混杂、根目录散落），再结合全部书签生成可预览归类方案；健康库优先复用现有目录名，问题库在保留熟悉命名的前提下建议浅层重组。本地规则可离线运行；配置 LLM 时把文件夹清单与诊断一并送入模型。
  - 扩展：`aiOrganizeLibrary.ts`、模式 `library`、Organize 面板诊断卡。
  - **Mac 无需对齐**（平台独有 AI 整理）。

## [1.1.66] - 2026-07-15

### Fixed
- **经典设置页 CSP 报错**：移除 `options.html` 内联脚本，改为打包模块在 React 渲染前添加 `options-embedded` 类，符合 MV3 `script-src 'self'`。

## [1.1.65] - 2026-07-15

### Changed
- **打开方式立即生效**：切换经典 / 标签 / 弹窗后立刻同步工具栏行为并按新方式打开（无需重载扩展）。

## [1.1.64] - 2026-07-15

### Fixed
- **经典模式设置窗过小**：同窗切换到设置时固定为与图标浮窗相同的 540×520–580，避免 Chrome 按内容把窗缩得很小。

## [1.1.63] - 2026-07-15

### Changed
- **经典模式 · 设置同窗切换**：点击扩展图标打开浮窗后，再点设置/展开，在当前窗口内打开并切换到设置页，不再另开浏览器标签页。

## [1.1.62] - 2026-07-15

### Changed
- **打开方式文案**：选项「经典（1.1.47）」改为「经典」。

## [1.1.61] - 2026-07-15

### Changed
- **打开方式默认恢复 1.1.47 经典体验**：新增「经典」选项并作为默认——工具栏图标用轻量浮窗（`popup.html`），设置用浏览器标签页；外观默认「标签」，窗口大小记为「紧凑」（仅弹窗模式生效）。下拉顺序：经典 / 标签 / 弹窗。已保存为标签或弹窗的用户不受影响。
  - 扩展：`uiOpenMode: classic | tab | popup`、`syncToolbarActionPopup`、`classicUiPreset`。
  - **Mac 无需对齐**（平台独有 UI）。

## [1.1.60] - 2026-07-15

### Fixed
- **图标窗与设置窗大小不一致**：工具栏图标改为打开同一 `options.html` 壳（`?tab=home`），与设置共用同一弹窗尺寸与靠右位置，不再使用独立 `popup.html` 导致宽高观感不同。

## [1.1.59] - 2026-07-15

### Fixed
- **同步窗与设置窗尺寸不一致**：弹窗模式共用同一个窗口；图标 ↔ 设置切换时只换页面并套用同一偏好尺寸/靠右位置，不再新开第二个不同大小的窗。

## [1.1.58] - 2026-07-15

### Fixed
- **快照列表「合并前」串语言**：标签在渲染时按当前语言解析，避免列表加载早于语言覆盖时冻住中文。
- **图标弹窗与设置弹窗位置统一**：弹窗模式一律靠当前主浏览器窗口右侧（以 normal 窗为准，避免以旧弹窗为参照）。

## [1.1.57] - 2026-07-15

### Changed
- **工具栏同步窗靠右**：弹窗模式下点击扩展图标打开的窗口，贴靠当前浏览器窗口右侧（多显示器按最后聚焦窗定位）。

## [1.1.56] - 2026-07-15

### Fixed
- **备份/快照列表语言串中文**：配置备份与书签快照不再永久写入当时翻译文案；显示时按当前界面语言解析（含旧数据「安装/更新时自动备份」「合并前」等）。

## [1.1.55] - 2026-07-15

### Fixed
- **界面语言覆盖串中文**：手动选英文等语言时，缺失文案不再回落到浏览器语言（常为中文），改为英文兜底；切换语言时清除「已切换为…」残留提示。

## [1.1.54] - 2026-07-15

### Changed
- **通用文案**：设置页外观 →「标签 / 菜单树」；打开方式 →「标签 / 弹窗」。

## [1.1.53] - 2026-07-15

### Added
- **通用 · 打开方式**：可选「独立弹窗」或「浏览器标签页」；作用于工具栏图标与设置入口。标签页模式下窗口大小选项禁用。
  - 扩展：`uiOpenMode`、`openSettingsWindow` / `openHomeWindow`。
  - **Mac 无需对齐**。

## [1.1.52] - 2026-07-15

### Fixed
- **默认窗口大小对图标/设置生效**：去掉 `action.default_popup`（WXT 会自动注入，需在 manifest hook 剥离），工具栏图标走 `action.onClicked` → 按偏好尺寸开独立同步窗；齿轮设置开独立设置窗。
  - **Mac 无需对齐**。

## [1.1.51] - 2026-07-15

### Fixed
- **工具栏图标 / 设置改为独立窗路径**（1.1.52 才真正去掉 default_popup）。

## [1.1.50] - 2026-07-15

### Fixed
- **设置窗口尺寸入口统一**：首次安装、后台「打开设置」、同步首页兜底、弹窗展开、选项页改尺寸等路径均走 `openSettingsWindow`（按所选尺寸打开/缩放独立窗）；选项页在 popup 内加载时也会应用首选尺寸。浏览器标签页打开设置时无法改窗尺寸（平台限制）。
- **通用外观即时生效**（延续 1.1.49）：本地 state 驱动导航；侧栏为左侧文字菜单。

## [1.1.49] - 2026-07-15

### Added
- **通用外观**：可在「标签 / 左侧菜单树」间切换设置页导航（侧栏参考沉浸式翻译式布局）；切换即时生效。
- **默认窗口大小**：弹窗展开独立窗口时可选 紧凑 / 舒适(推荐 760×720) / 宽屏(侧栏最佳) / 大屏。
  - 扩展：`uiPreferences`、`options.tsx` / `options.css`、`popup.tsx`、i18n。
  - **Mac 无需对齐**。

## [1.1.48] - 2026-07-15

### Added
- **智能整理（MVP→v3）**：选项新增主导航 **「整理」**；通用设置接入 OpenAI 兼容 / Anthropic / Gemini / Ollama 等 API。
  - **MVP**：本地域名聚类 +（可选）大模型 JSON 方案；差异预览勾选；应用前自动本地快照；只移动/建夹/重命名/归档，不删。
  - **v2**：重复链接提示并入待裁决；不确定队列筛选；每周减负建议（本地告警 + 通知）。
  - **v3**：对比紧凑（本地）与详细（AI）双方案；Ollama/本地规则离线可用；可配置 taxonomy。
  - 扩展：`aiOrganize*.ts`、`OrganizePanel.tsx`、`featureHandlers`、`background`、i18n。
  - **Mac 无需对齐**（整理/LLM 为扩展 Tools 类能力）。

## [1.1.47] - 2026-07-14

### Fixed
- **Chrome 包剔除 `browser_specific_settings`**：该字段仅 Firefox/AMO 需要；写入 Chrome ZIP 后，桌面端常忽略，手机端 Chromium（如 Kiwi）会报「安装包损坏 / 无法识别的字段」。现仅在 `browser === 'firefox'` 时写入。
  - 扩展：`wxt.config.ts`、`check-store-zip.mjs`。
  - **Mac 无需对齐**。

## [1.1.46] - 2026-07-14

### Fixed
- **智能合并：移动书签不再双端留空/双端重复；删除文件夹不再复活成空壳**（GitHub Issue #3）：三方合并不再仅按 URL 并集 + 同名文件夹递归，改为**路径索引**：
  - 识别单侧相对基准的 **URL 移动**，只保留一侧归属；
  - **文件夹路径**参与删除传播，避免已删文件夹被远端旧树灌回成空文件夹；
  - 仍无基准时回退纯并集；本地空/远小于云端时保留恢复剪枝豁免。
  - 扩展：`mergeBookmarks.ts`、`tests/mergeThreeWay.test.ts`。
  - **Mac 已对齐**：`BookmarkMerge.swift`。

## [1.1.44] - 2026-07-12

### Fixed
- **应用语言立即切换**：选项「通用 → 语言」后立刻加载语言包并刷新界面；弹窗等正确监听压缩后的 `options` 存储（此前误听顶层 `appLanguage`，几乎不生效）。
- **繁中同步文案占位符**：修复 `zh_TW` 中 `$1$` 被写成字面量 `\$`，导致「\$ 分鐘前已同步」而非具体分钟数。
- **应用语言覆盖彻底化**：选项/弹窗/工具/向导/后台通知统一走 `getMessage`，不再跟浏览器语言半切半不切。
  - **Mac 无需对齐**（语言覆盖为扩展 UI；Mac 用系统本地化）。

## [1.1.43] - 2026-07-12

### Added
- **快速开始导入配置**：向导内可从文件导入已有配置备份 JSON，跳过手工填 Token（扩展 + Mac 向导）。

### Fixed
- **同链接多文件夹**：合并/增量写入时，同一 URL 在多个文件夹各需一份时改为**克隆**，不再移动导致「计划 N、M 个未写入」与本地/云端条数差（如 583 vs 585）。
  - 扩展：`bookmarkTreeSync.ts`；Mac 写回 Safari 为整树替换，本问题主要在浏览器扩展增量路径。

### Improved
- **快速开始连通性结果**：成功/失败改为醒目横幅（连接可用 / 不可用），避免被忽略。

## [1.1.42] - 2026-07-11

### Added
- **同步 HTML 备份**：上传/合并成功后，在主同步文件旁额外写入 Netscape 格式 `.html`（如 `BookmarkSync.html`），便于在任意浏览器手工导入；设置中可关，**默认开启**。失败不影响 JSON 主同步。
  - 扩展：`htmlRemoteBackup.ts`、`background.ts`、高级同步开关、i18n。
  - **Mac 已对齐**：`SettingsStore` / `RemoteSyncService` / `MacFeatureViews`。

## [1.1.41] - 2026-07-11

### Added
- **卫生扫描可发现**：首次向导可勾选「每周书签卫生扫描」（默认开、可关）；健康卡展示近期扫描摘要（重复组 / 失效链接）。
- **Profiles 顶栏切换**：设置页标题栏可一键切换已保存的工作/个人等配置档。
  - 扩展：`SetupWizard.tsx`、`SyncHealthCard.tsx`、`ProfileSwitcher.tsx`、`options.tsx`、i18n。
  - **Mac 无需对齐**（Profiles / 工具调度为扩展独有）。

## [1.1.40] - 2026-07-11

### Added
- **会话快捷入口**：同步首页可一键「保存窗口 / 恢复最近」标签页会话，无需进入工具页。
- **差异 CTA 强化**：数量不一致时主按钮为「立即对齐」（合并），次要为「查看明细」。
  - 扩展：`SyncHomePanel.tsx`、`sync-home.css`、i18n。
  - **Mac 无需对齐**（标签页会话为扩展独有；Mac 差异查看器仍待做）。

## [1.1.39] - 2026-07-11

### Added
- **同步健康一屏**：首页展示绿/黄/红健康状态（成功、失败、待同步、数量不一致、久未成功）；失败可一键重试，不一致/过期可一键合并；失败反馈保留日志与快照入口。
  - 扩展：`syncHealthSummary.ts`、`SyncHealthCard.tsx`、`SyncHomePanel.tsx`、i18n。
  - **Mac 尚未对齐**。

## [1.1.38] - 2026-07-11

### Changed
- **排版与层级打磨**：说明文案统一 ≥12px；tertiary 对比加深；删除 10px 硬编码；引入 4px 间距网格；首页减少边框、强化主操作、弱化危险区与微标签。
  - 扩展：`extensionTheme.css`、`sync-home.css`、`popup.css`、`options.css`。
  - **Mac 无需对齐**（扩展 UI）。

## [1.1.37] - 2026-07-11

### Changed
- **图标视觉升级**：重绘扩展与 macOS 主图标——多层蓝渐变、高光与暗角、书签层次阴影、云同步符号加粗，小尺寸（16px）仍清晰可辨。
  - 扩展：`src/assets/icon.svg`、`icon.png`、`scripts/generate-extension-icons.mjs`。
  - Mac：`macos/BookmarkSyncApp/Resources/AppIconSource.png`（与扩展同源矢量导出）。

## [1.1.36] - 2026-07-11

### Improved
- **上传/下载响应加速**：手动上传、下载改为「立即响应 + 后台执行」；计数写入不再阻塞等待远端拉取；下载不再强制等待本地快照；合并基准与日志/通知改为后台写入。
  - 扩展：`background.ts`、`syncOrchestrator.ts`、`SyncHomePanel.tsx`、`syncCounts.ts`、i18n。
  - **Mac 尚未对齐**。

## [1.1.35] - 2026-07-11

### Improved
- **条数差异明细**：「差异 N」场景下列出完整链接 URL；每份副本显示书签标题 + 文件夹路径（含书签栏/其他书签等根目录）；高亮标出本地/云端多出的副本。
  - 扩展：`bookmarkDiff.ts`、`BookmarkDiffDialog.tsx`、`sync-home.css`、i18n。
  - **Mac 尚未对齐**。

## [1.1.34] - 2026-07-11

### Added
- **差异明细与处理**：当出现「差异 N」（尤其 URL 相同但条数不同）时，「查看差异」会列出具体链接及两端每一份副本的文件夹路径；弹窗内可直接「合并同步 / 上传对齐本地 / 下载对齐云端」。
  - 扩展：`bookmarkDiff.ts`、`BookmarkDiffDialog.tsx`、`SyncHomePanel.tsx`、`sync-home.css`、i18n。
  - **Mac 尚未对齐**（差异查看器仍为扩展独有，见 `MAC_EXTENSION_PARITY.md`）。

## [1.1.33] - 2026-07-11

### Changed
- **颜色与搭配优化**：页面底改为冷灰蓝以抬升白卡片层次；边框/阴影略加强；强调色与分段选中态统一 Logo 蓝；语义色（成功/危险/警告）加深以保证对比；深色模式卡片与背景分层更清晰。
  - 扩展：`extensionTheme.css`、`popup.css`。
  - **Mac 无需对齐**（扩展 UI 配色）。

## [1.1.32] - 2026-07-11

### Changed
- **字体与字号体验优化**：正文提升至 14px，说明/标签不低于 12px；收紧字距更适合中英混排；系统字体栈补齐 Windows 雅黑；次要文字对比度略加强；表单输入保持 ≥14px。
  - 扩展：`extensionTheme.css`、`options.css`、`popup.css`、`tools.css`。
  - **Mac 无需对齐**（扩展 UI 排版）。

## [1.1.31] - 2026-07-11

### Changed
- **选项卡图标**：连接/策略/数据/工具/通用改用 Lucide 语义图标（云配置、滑杆、数据库、扳手、设置）；图标字形 16px、触控底 24px。
  - 扩展：`options.tsx`、`options.css`。
  - **Mac 无需对齐**（扩展 UI）。

## [1.1.30] - 2026-07-11

### Fixed
- **设置页与主页窗口宽度不一致**：Popup 内嵌设置曾固定为 400px，现与主页同宽铺满（540px）；嵌入模式去掉多余边距限制。
  - 扩展：`options.css`、`options.tsx`、`popup.css`。
  - **Mac 无需对齐**（扩展 Popup UI）。

## [1.1.29] - 2026-07-11

### Changed
- **界面图标与配色美化**：同步流程卡、上传/下载按钮、差异提示、成功反馈、选项卡与标题图标统一为 Logo 蓝软底圆角徽章；页头 Logo 增加淡蓝光晕。
  - 扩展：`extensionTheme.css`、`sync-home.css`、`options.css`、`popup.css`。
  - **Mac 无需对齐**（扩展 UI 样式）。

## [1.1.28] - 2026-07-10

### Fixed
- **合并数字口径自洽**：日志与差异弹窗同时展示「书签条数」（本地/云端/合并后）与「去重 URL」（共同/仅本地/仅远程），避免「共同 581、仅本地/仅远程 0」看起来与 583/584 矛盾；差异空态文案带入具体数字。
  - 扩展：`mergeConflictStats.ts`、`bookmarkDiff.ts`、`BookmarkDiffDialog.tsx`、i18n。
  - **Mac 部分对齐**：若 Mac 有合并摘要文案，需同步占位符顺序；本轮仅扩展。

## [1.1.27] - 2026-07-10

### Changed
- **「合并同步」主卡片深度微调**：比 Logo 实心蓝略浅（约 78–88% accent 混白），白字图标，避免过淡。
  - 扩展：`sync-home.css`。
  - **Mac 无需对齐**（扩展 UI 样式）。

## [1.1.26] - 2026-07-10

### Changed
- **「合并同步」主卡片更淡**：由实心蓝改为浅蓝底 + 蓝色文字/图标，边框与阴影更轻，仍属 Logo 蓝色系。
  - 扩展：`sync-home.css`。
  - **Mac 无需对齐**（扩展 UI 样式）。

## [1.1.25] - 2026-07-10

### Changed
- **同步成功提示自动消失**：首页成功反馈约 4.5 秒后自动关闭；错误提示仍需手动关闭以便查看日志/快照。
  - 扩展：`SyncHomePanel.tsx`。
  - **Mac 无需对齐**（扩展 UI）。

## [1.1.24] - 2026-07-10

### Changed
- **全界面品牌色统一为 Logo 蓝**：将紫/青绿装饰色、页面背景紫晕、本地/云端计数与流程图标、差异横幅与差异弹窗、工具健康数字等对齐 `--ms-accent`（`#0071e3`）；`--ms-purple`/`--ms-teal` 别名改为蓝色。错误/危险仍用红，语义成功按钮仍用绿。
  - 扩展：`extensionTheme.css`、`sync-home.css`、`tools.css`、`BookmarkDiffDialog.tsx`。
  - **Mac 无需对齐**（扩展 UI 样式）。

## [1.1.23] - 2026-07-10

### Changed
- **同步成功反馈条配色**：由翠绿改为与主题图标/强调色 `--ms-accent` 同一蓝色系（浅蓝底 + 蓝色勾选图标）。
  - 扩展：`sync-home.css`。
  - **Mac 无需对齐**（扩展 UI 样式）。

## [1.1.22] - 2026-07-10

### Fixed
- **「查看差异」无反应**：首页误发未注册的 `previewMergeDiff` 消息；改为既有后台 `previewMerge`，并在无有效预览时给出错误反馈。
  - 扩展：`SyncHomePanel.tsx`。
  - **Mac 无需对齐**（扩展消息名修复）。

## [1.1.21] - 2026-07-10

### Changed
- **首页「合并同步」主按钮配色**：去掉紫→蓝渐变，改为与主题图标/强调色 `--ms-accent` 同一蓝色系的浅纵渐变与光晕，观感更自然。
  - 扩展：`sync-home.css`。
  - **Mac 无需对齐**（扩展 UI 样式）。

## [1.1.20] - 2026-07-10

### Fixed
- **消息通道提前关闭**：后台 `onMessage` 对同步/校验/快照等异步分支补全 `return true` 与错误回复；未知消息改为 `return false`；避免 `createSnapshot`/`restoreSnapshot`/`deleteSnapshot` 被重复处理，消除 Chrome「message channel closed before a response was received」控制台警告。
  - 扩展：`background.ts`。
  - **Mac 无需对齐**（浏览器扩展消息通道问题）。

## [1.1.19] - 2026-07-10

### Added
- **Google Drive / OneDrive（Access Token）**：连接页可配置 Access Token 与文件名并测试连通；同步后端写入应用数据目录 / Graph；自动同步与通知按目标独立开关。
  - 扩展：`googleDriveBackend`/`oneDriveBackend`、`verifySyncConfig`、options/popup 表单、权限请求、i18n。
  - **Mac 未对齐**：仍为即将支持提示；需后续移植 Access Token 流程。

### Changed
- **策略页文案**：同步策略标签改为「策略」；专家区标题改为「高级设置」（`optionsTabSync` / `syncExpertSettingsTitle`）。

## [1.1.18] - 2026-07-10

### Added
- **界面语言完整 12 语种**：语言选择器列出 zh_CN / zh_TW / en / ja / ko / de / fr / es / it / pt / ru / ar（`appLanguage_*` 键）；ja/ko/de/fr/es/it/pt/ru/ar 与 zh_TW 语言包补全为真实译文（非英文拷贝）。
  - 扩展：`scripts/build-locale-translations.mjs`、`scripts/i18n-overrides/`、各 `_locales/*/messages.json`。
  - **Mac 部分对齐**：`LanguageSettingsRow` 提供相同语言代码；运行时仍为中英双语（zh*→中文，其余→英文），完整 Mac 多语言待后续。

## [1.1.17] - 2026-07-10

### Changed
- **同步 UX 澄清**：主页标签改为「同步」、原同步标签改为「自动与安全」；主操作文案改为「合并同步」；连接目标选择区分可用 / 即将支持；设置向导可测连通或合并一次后完成；专家选项与备份策略折叠；操作反馈更清晰。
  - 扩展：`options.tsx`、`SyncHomePanel`/`SetupWizard`/`ManualSyncTargetPicker`、CSS、12 语言 i18n。
  - **Mac 部分对齐**：同步标签文案、即将支持目标在选择器中禁用；未重写向导。

## [1.1.16] - 2026-07-10

### Added
- **同步目标扩展**：新增 Gitee、GitLab 完整同步；Google Drive / OneDrive 出现在下拉中并标注「即将支持」（不可验证/同步）。
  - 扩展：syncProvider、giteeBackend/gitlabBackend、连接面板、i18n、校验与远程快照；主页已去掉手动目标选择器（流程条仍显示当前目标）。
  - **Mac 已对齐**：SyncProvider 枚举、连接表单、RemoteSyncService 上传/下载/校验；云盘为即将支持提示。远程快照归档与 iCloud 配置快照中的 Gitee/GitLab 字段为部分对齐。

## [1.1.15] - 2026-07-10

### Changed
- **问题反馈去掉邮件入口**：帮助页与 Mac 仅保留 GitHub Issue。

## [1.1.14] - 2026-07-10

### Changed
- **同步目标改为下拉选择**：主页、连接页、首次向导与 Mac 同步页由分段/芯片改为 `<select>` / 菜单式 Picker，便于后续扩展更多目标；选项仍来自 `ALL_SYNC_PROVIDERS`。
  - 扩展：`ManualSyncTargetPicker.tsx`、`options.tsx`、`SetupWizard.tsx`、`SyncHomePanel.tsx`。
  - **Mac 已对齐**：`SyncTargetPanel`、设置向导改用 `.pickerStyle(.menu)`。

## [1.1.13] - 2026-07-10

### Changed
- **防误删阈值可配置**：默认仍为 30%，可在「高级同步」改为 1–90%；合并/下载按该比例判断是否中止。
  - 扩展：`syncMassDeleteThreshold`、`mergeGuard.ts`、`options.tsx`、12 语言 i18n。
  - **Mac 已对齐**：`SettingsStore`/`MergeGuard`/`MacFeatureViews`、iCloud 快照字段。

## [1.1.12] - 2026-07-10

### Added
- **通用设置**：语言、主题、本机名称集中到「通用」标签；本机名称写入同步日志、最近同步状态与远程 JSON `deviceName`（默认如 `Chrome@Windows` / `Safari@Mac`）。
  - 扩展：`uiPreferences.ts`、`options` General 标签、主题 CSS、`syncLogger`/`syncStatus`/`SyncDataInfo`。
  - **Mac 已对齐**：通用区主题/本机名称、`SyncDataInfo.deviceName`、同步日志展示设备名、`preferredColorScheme`。

## [1.1.11] - 2026-07-10

### Added
- **防误删保护（默认开启）**：合并或下载将删除超过约 30% 书签时自动中止；可在「高级同步」关闭。与「删除保护」（阻止下载覆盖）并存。
  - 扩展：`mergeGuard.ts`（保留比例 70%）、`syncOrchestrator.ts`、`options.tsx`、`optionsDefaults`/`setting`、en/zh_CN i18n。
  - **Mac 已对齐**：`MergeGuard.swift`、`SettingsStore`/`SettingsCloudStore`、`RemoteSyncService`/`AutoSyncService`/`BookmarkSyncApp`、`MacFeatureViews`。

### Fixed
- **合并前后计数不一致**：差异预览与正式合并共用三方基准与 `computeMergeConflictStats`；弹窗显示与首页一致的本地/云端条数；「合并后」与日志同口径（节点数）；顶栏/日志成功时显示实际写入数而非计划数；URL 相同但条数不一时不再误报「完全一致」。

## [1.1.10] - 2026-07-07

### Fixed
- **合并/下载在本地远少于云端时只上传或显示成功 0 条**：三方合并在本地为空或远小于云端时不再把云端书签当作「本地已删」而剪枝清空；增量写入支持无系统根文件夹包裹的远端树；远端计数为 0 时不再用上次成功同步数回填 UI；合并计划为空时禁止上传以免覆盖云端；下载计划有书签但本地写入 0 时记为失败；删除保护在云端多于本地时仍允许下载恢复。
  - 扩展：`mergeBookmarks.ts`、`bookmarkTreeSync.ts`、`syncCounts.ts`、`syncSafety.ts`、`syncGuards.ts`、`background.ts`、`SyncHomePanel.tsx`、en/zh_CN i18n。
  - **Mac 已对齐**：`BookmarkMerge.swift`（同等删除剪枝跳过规则）。

### Changed
- **备份策略文案简化**：缩短标签与频率选项，去掉每项下拉框下的重复说明；快照区说明一并收紧。12 语言 i18n + Mac `BackupPolicyPanel`。

## [1.1.9] - 2026-07-07

### Fixed
- **同步失败只显示「错误」、无具体原因**：手动同步失败时后台改为抛出/回传真实错误信息；HTTP 错误（WebDAV/Gitea 等）格式化更清晰。
  - 扩展：`syncManualResult.ts`、`background.ts`、`formatError.ts`、`SyncHomePanel.tsx`、`syncSafety.ts`。
- **合并同步误报「本地写入不完整」**：`isMergeLocalApplyComplete` 认可唯一 URL 数达标；Mac 同版发布。

### Added
- **备份策略细化（4 项独立配置 + 每周）**：配置备份、本地快照（自动）、远程归档（自动）、手动同步备份可分别设为每次/每天/每周/仅手动；默认远程归档每周、手动同步每天最多一次；仅改备份策略不再触发配置自动备份。
  - 扩展：`backupPolicy.ts`、`options.tsx`、`optionsDefaults.ts`、`background.ts`、12 语言 i18n。
  - **Mac 已对齐**：`BackupPolicy.swift`、`SettingsStore`、`SyncSafety`、`RemoteSyncService`、`MacFeatureViews.swift`、`BookmarkSyncApp.swift`。

## [1.1.8] - 2026-07-07

### Fixed
- **WebDAV 下载/自动同步报 `this.request(..).text is not a function`**：`WebdavBackend.get()` / `getFileContent()` 在 `async request()` 返回的 Promise 上直接调用 `.text()`，上传（PUT）不受影响。现已先 `await` 响应再读正文。
  - 扩展：`webdavBackend.ts`；新增 `tests/webdavBackend.test.ts`。

### Added
- **可配置备份策略（默认每天一次）**：配置备份与自动同步前的本地快照/远程归档支持「每次 / 每天最多一次 / 仅手动」；手动同步始终备份。设置 → 数据 → 备份策略。
  - 扩展：`backupPolicy.ts`、`optionsDefaults.ts`、`background.ts`、`options.tsx`、12 语言 i18n。
  - **Mac 已对齐**：`BackupPolicy.swift`、`SettingsStore`、`SyncSafety`、`RemoteSyncService`、`AutoSyncService`、`MacFeatureViews`。

### Changed
- 配置自动备份默认从「每次改设置」改为「每天最多一次」；自动同步快照/远程归档同理，减轻 5 分钟智能同步下的备份频率。


## [1.1.7] - 2026-07-04

### Fixed
- **合并同步：本地写入不完整时不再先上传远程**：此前合并 apply 失败或部分跳过时仍会把合并结果推到远端，下一轮三方合并可能误删远程书签。现在先以 `isMergeLocalApplyComplete` 校验本地 apply，**仅完整时才上传**；不完整则记失败日志并保留远端不变。
  - 扩展：`background.ts`（`mergeSyncBookmarks` 上传顺序）。
- **删除保护使用实时本地计数**：`syncGuards` 删除保护改读 `countLocalBookmarksLive()`，storage 缓存失败时回退 `readStoredLocalBookmarkCount()`，避免误拦或误放下载。
  - 扩展：`syncGuards.ts`。
- **变更触发同步失败时保留待同步标记**：`runChangeAutoSyncForProvider` 仅成功时 `clearPendingChangeSync()`，失败则重排 `scheduleAutoUpload()`，避免改动丢失。
  - 扩展：`background.ts`。
- **周期自动同步与手动同步互斥**：`runPeriodicAutoSync` 检查 `isSyncOperationRunning()` 并包在 `withSyncOperationLock` 内，避免与变更/手动同步并发；周期 download 仅在成功时清 badge/刷新计数。

### Changed
- **Popup / 设置页 UI 美化与窄屏布局**：
  - Popup 同步流程条改为纵向堆叠（`ms-sync-flow--popup`），隐藏连接器；双端同步警告、目标 chips 使用 compact 样式。
  - 设置按钮改为仅图标（`aria-label` + `title`）。
  - `SyncStatusBar`、diff 横幅、快照筛选操作行、工具列表项在窄屏下换行/纵向排列。
  - 扩展：`SyncHomePanel.tsx`、`popup.css`、`popup.tsx`、`extensionTheme.css`、`sync-home.css`、`options.css`、`tools.css`。

### Added
- **合并大规模删除防护**、**书签快照按日保留 + 分页**、**远程快照子目录迁移**、**工具/数据标签职责分离**、**同步流程条中间目标节点**、**多语言补全**（自 1.1.6 Unreleased 并入本版发布）。

## [1.1.6] - 2026-06-30

### Changed
- **智能模式默认「书签一改就同步」，不再等周期间隔**：此前变更触发同步把**周期间隔（默认 5 分钟）当成两次变更同步的最小间隔**，导致改完书签后 5 分钟内的后续改动都被推迟——表现为「改了要等几分钟才上传」。现在把三件事彻底解耦:
  - **去抖窗口（3s）**:合并连续编辑/拖拽整理/批量导入为一次同步,天然防风暴（批量导入只在结束后 3s 同步一次）。
  - **变更触发最小间隔**:从「周期分钟数」改为固定 `AUTO_SYNC_CHANGE_MIN_INTERVAL_MS = 3s`（≈去抖）,本机一改 → 约 3s 后立即合并同步。
  - **周期间隔（用户设的 5 分钟）**:只负责定时拉取**其他设备**的远端改动 + 失败自愈,不再影响本机改动的同步速度。
  - **同步进行中又有新改动不丢失**:此前 `runChangeAutoSync` 在已有同步运行时直接 `return`（丢弃该次触发）。现在改为**重排快速去抖、稍后重试**,保证最后一次改动一定被同步,且绝不并发两个同步。
  - 变更触发仍走 **merge**（拉+合+传）,既实时又不会覆盖其他设备刚改的远端;局域网下通常仍在 3s 内完成。
  - 扩展:`autoSync.ts`（新增 `AUTO_SYNC_CHANGE_MIN_INTERVAL_MS`）、`background.ts`（`runChangeAutoSyncForProvider` 用新常量、忙时重排不丢失）、i18n `autoSyncIntervalHintAuto` 文案改为「本机改动数秒内同步;此间隔只控拉取远端的频率」（12 语言）、`tests/autoSyncMode.test.ts`（解耦回归用例）。
  - **Mac 已对齐**:`AutoSyncService.changeSyncMinInterval = 3s`、`canRunChangeSync` 不再乘以周期分钟数、忙/节流时重排去抖而非丢弃（另有 15s 轮询定时器兜底）。

### Added
- **「未写入本浏览器」的链接现在能看到具体原因**：合并同步时被浏览器拒绝创建的书签（日志里的「N 个未写入」），此前只把错误打到 Service Worker 控制台，用户无从知晓为何本地永远比远端少。现在增量写入会**采集失败条目（标题/URL/归类原因）**，按原因聚合后写进同步日志（如「未写入本浏览器的原因：不支持的链接协议 ×180、FTP 链接 ×12」），完整明细（最多 50 条样本）存入 `storage.local` 的 `syncApplyFailureSamples` 供深入排查。原因归类含：FTP 链接、非 http(s) 协议、链接过长、父文件夹缺失、无效链接、其他。
  - 扩展：`bookmarkTreeSync.ts`（`classifyApplyFailure`/`summarizeApplyFailures`/采集失败样本，`applyBookmarkTreeIncremental` 返回 `failureSamples`）、`background.ts`（聚合写日志 + 存诊断）、i18n `applyFailReason*`（12 语言）、新增 `tests/applyFailureDiagnostics.test.ts`。
  - **背景**：本地 388 / 远程 580 长期不一致，正是这 ~192 条链接浏览器拒绝写入所致；它们会一直显示「仅远程」。先暴露原因，再决定是否从云端清理。

### Changed
- **智能合并改为三方合并：删除终于生效，不再被「复活」**：此前合并同步用的是 local∪remote **纯并集**，永远不会删除——删掉一条本地书签后，约 3 秒自动同步触发 merge，远端那条还在，于是被并回本地、看似「自动恢复」。现在引入**上次同步基准快照**做三方合并：
  - **删除传播（双向）**：某条 URL 在基准里有、但现在本地没了（本机删除）或远端没了（其他设备删除）→ 判定为删除，从合并结果剔除并同步到各端，不再复活。
  - **新增仍照常**：基准里没有、本地或远端新出现的 URL 视为新增，正常合并。
  - **首次安全**：无基准时（首次同步或老用户升级）退回并集行为；每次成功的合并/上传/下载后写入新基准（本地≡远端的状态）。清空远端后基准置空；快照恢复后基准置空（恢复是有意的整树替换，下次合并按并集，避免把「恢复掉的条目」当删除传播）。
  - 升级后**首次**合并会先把现状（含你之前被复活的那条）确立为基准；**再删一次**即可永久生效。
  - 扩展：`mergeBookmarks.ts`（`mergeBookmarkTrees` 增加 `baseRoots` + 删除剪枝）、`syncOrchestrator.ts`（`buildMergePlan`/`runMergeSync` 透传基准并回传 `newBaseRoots`）、`mergeConflictStats.ts`、`background.ts`（`lastSyncedBaseRoots` 读写：合并/上传/下载/清空远端/恢复各节点维护基准）、新增 `tests/mergeThreeWay.test.ts`。
  - **Mac 已对齐**：`BookmarkMerge.merge(...baseRoots:)` 同等剪枝、新增 `SyncBaseStore`（UserDefaults `lastSyncedBaseRoots`），`AutoSyncService`/`RemoteSyncService`/`BookmarkSyncApp` 的合并/上传/下载/清空远端/快照恢复同步维护基准。

### Fixed
- **合并成功后 popup 仍显示「本地 580 · 云端 579 · Δ1」**：同步日志与合并结果已正确报告 580/580，但 popup 打开时会 `refreshCounts` 重新拉远端并用 `countUniqueBookmarkUrls`（按 URL 去重）计数，而本地与合并计划使用 `countCreatableBookmarkUrls`（按可写入的书签条目数）。当同一 URL 出现在多个文件夹时两者差 1。现远端刷新计数与本地统一为 `countCreatableBookmarkUrls`。
  - 扩展：`syncCounts.ts`、新增 `tests/syncCounts.test.ts`。
- **加强「父文件夹缺失」修复（192 条仍写不进本地）**：上一轮已做静态 id 重定向 + 同根合并，但若扩展未重载、或系统根在 `getTree` 里存在却**拒绝 `bookmarks.create`**（典型：桌面 Chrome 的移动书签根 id `'3'`），仍会 192 次 `Can't find parent`。现增加三层兜底：
  - **`resolveWritableSystemFolderIds`**：用 `bookmarks.get` 实测每个系统根 id 是否真实可寻址，不可寻址则重定向到第一个可写文件夹（不再只比对 getTree 子节点列表）。
  - **修复 `verifyParentFolderId`**：`bookmarks.get` 返回的是数组，旧代码当成单节点导致校验恒失败。
  - **`createBookmarkEntry` 父缺失回退**：若 trusted 父 id 创建仍抛 parent 错误，取消信任并回退到书签栏/已验证文件夹，避免对同一死 id 空转 5 次。
  - 合并 apply 改用 `buildVerifiedBookmarkCreateContext`；新增单元/集成回归（缺 Mobile 根、Mobile 根拒绝 create）。
- **根治「仅远程 192 条 · 父文件夹缺失」永远写不进本地**：诊断显示这 192 条全部因「父文件夹缺失」失败——它们属于某个**本机不存在的系统根**（典型：远端带「移动设备书签 / Mobile bookmarks」根，而本机这台桌面 Chrome 没有该文件夹，其默认 id `'3'` 不存在）。旧逻辑把这个**猜测的、根本不存在的** id 预先列入「可信父」，`bookmarks.create` 一律抛 `Can't find parent`，且每次重试同一个死 id → 永远失败、永远「仅远程」。现在：
  - **存在性重定向**：`systemFolderIdsFromRootChildren` 解析后，任何不在真实根节点中的系统文件夹 id 一律重定向到确实存在的文件夹（优先「其他书签」，其次书签栏），书签从此有处可落。
  - **同根合并**：当多个 desired 根（如 Mobile 根与 Other 根）重定向到同一真实文件夹时，`applyBookmarkTreeIncremental` 先按真实系统文件夹 id **合并各根的子节点再处理一次**，避免第二个根的对账删除清掉第一个根刚写入的书签（防止反复增删/重复）。
  - 扩展：`bookmarkTreeWriter.ts`（`systemFolderIdsFromRootChildren` 重定向）、`bookmarkTreeSync.ts`（`groupDesiredBySystemFolder` + 按真实文件夹合并 apply/匹配）、新增集成回归用例（移除本机 Mobile 根后，远端移动书签仍被写入且二次同步幂等无重复）。
  - **Mac 无需此修复**：macOS 走 Safari plist 整树写入，不存在「挂载到不存在的固定根 id」的问题。
- **合并同步误报「本地写入不完整 391/580」**：当浏览器拒绝写入的链接（如 bookmarklet、`javascript:` 等，日志里的 190 条）已在 apply 阶段跳过时，成功判定应把「已写入 + 已跳过」一并计入。此前只比较 `appliedCount >= plannedCount`，导致 391+190≈580 仍报失败并提示重试。现在用 `isMergeLocalApplyComplete(applied + skipped >= planned)` 判定。
- **Gitea「测试连通性通过但上传 403」**：连通性测试此前只做 GET（读文件），读-only Token 也能通过；实际上传 PUT 需要写权限。现在测试会检查仓库 API 返回的 `permissions.push`，无写权限时直接提示「Token 仅有读权限」；上传 403 时也抛出相同说明。
  - 扩展：`syncOrchestrator.ts`（`isMergeLocalApplyComplete`）、`background.ts`、`verifySyncConfig.ts`、`giteaBackend.ts`、i18n `verifyGiteaNoWriteAccess`。
- **修复「改书签约 3 秒仍不同步」(MV3 SW 重启丢 timer)**：书签变更的 3s 去抖此前只靠内存 `setTimeout` + 短 `alarm`;Service Worker 常在 3s 内被回收,timer 丢失,而 Chrome 对打包扩展的 `alarm` 又有 ~1 分钟下限,导致变更触发同步**静默永不执行**。现在把「待同步截止时间」写入 `storage.local`(`pendingChangeSyncAt`),SW 每次唤醒时检查:已过期则**立即补跑**,未过期则重挂剩余毫秒计时器;同时修复 `suppressAutoSync`/手动同步占用锁时**丢弃变更**的问题(改为重排去抖),变更合并期间设置 `curOperType=SYNC` 避免本地写入触发的事件风暴,并写入 `syncDiagPhase`(`auto:scheduled`/`auto:changeSync`/`auto:skip:*`)便于排查。
  - 扩展:`autoSync.ts`（`PENDING_CHANGE_SYNC_AT_KEY`、`changeSyncDelayMs`）、`background.ts`（`flushPendingChangeSync`/`armChangeDebounceTimer`/持久化去抖）。
- **修复「离开界面后彻底不自动同步」的根因（MV3 alarm 反模式）**：`setupAutoSync` 此前在 Service Worker **每次被唤醒**（开 popup、书签事件、收消息等）时都先 `clear` 再 `create` 周期 alarm。由于 SW 被频繁唤醒（往往短于同步间隔），5 分钟的周期 alarm 的倒计时**每次都被重置、永远到不了期** → 定时/智能同步实际上从不触发。同时它还会清掉刚为「书签变更」排好的 debounce alarm，可能吞掉那一次变更触发的同步。
  - 现在 `setupAutoSync` **幂等**：先 `alarms.get` 检查，已存在且周期一致的 alarm **原样保留**（倒计时不被重置），仅在缺失或间隔变化时才重建；只清理「非当前提供方/已关闭」的过期周期 alarm；**不再清理 debounce alarm**。配置变更时仍会按需重建。
  - 扩展：`background.ts`（`setupAutoSync` 重写为幂等 + `ALL_PERIODIC_ALARMS`）。
  - **Mac 无需此修复**：macOS 是常驻应用，用 `Timer` 而非 alarm，不存在「被反复重置」问题。
- **变更触发同步 3s 内完成（绕过 Chrome alarm 的 ~30s 下限）**：书签变更的 3s 防抖此前仅靠 `alarms.create({when})` 实现，而 Chrome 对打包扩展的 alarm 有 **~30s 最小延迟**，导致「改完书签要等 ~30s 才同步」。现在改为**真实 `setTimeout(3s)` 作为主路径**（书签事件刚把 SW 唤醒、此刻 SW 必然存活，3s 计时器可靠触发），alarm 仅作为「SW 在 3s 内被回收」的兜底；计时器先触发时会清掉兜底 alarm。局域网下变更→同步可稳定落在 3s 内。
  - 扩展：`background.ts`（`scheduleAutoUpload` 改为 `setTimeout` 主 + alarm 兜底，`changeDebounceTimer`）。
- **旧的纯变更模式归一为 `auto`，让升级用户也获得定时兜底**：存量配置里若是 `onChange`/`onChangeMerge`（旧默认，无周期 alarm，拉不到其他设备改动、失败不自愈），现在读取时统一归一为 `auto`；显式的 `periodicUpload`/`periodicDownload`/`periodicMergeSync`/`readOnlyMirror`（单向/镜像意图）原样保留。
  - 扩展：`autoSync.ts`（新增 `normalizeAutoSyncMode`）、`setting.ts`（`autoSyncFor` 应用归一）、`tests/autoSyncMode.test.ts`（归一用例）。
  - **Mac 已对齐**：`AutoSyncMode.normalized` + `SettingsStore.autoSyncSettings(for:)` 应用归一。

### Changed
- **同步策略合并为单一「智能同步（`auto`）」并设为默认**：此前自动同步有 6 种模式（变更上传/变更合并/定时上传/定时下载/定时合并/只读镜像），用户需在 6 选 1 中纠结，且最常用的「变更时合并」与「定时合并」是割裂的两种。现在新增统一的 `auto` 模式并设为所有提供方的默认：**本机书签一变更就防抖后合并同步（实时上传本机改动），同时挂定时 alarm 周期性合并兜底（拉取其他设备的远端改动 + 失败自愈）**。一种策略同时覆盖「实时」与「定时」，开箱即用、双向最终一致。
  - **修复多设备数据不一致根因**：旧的纯变更触发模式（`onChange`/`onChangeMerge`）只在**本机**书签变更时触发、不挂定时 alarm，导致其他设备改了远端、而本机没动书签时**永远不会拉取**——长期本地/云端不一致。`auto` 的定时合并兜底解决此问题。
  - **修复「离开界面后不自动同步」残留**：变更触发若失败/超时无重试兜底；`auto` 的定时合并会周期性自愈。
  - **UI 简化**：设置页同步方式下拉由 6 项精简为「智能同步（推荐）/ 只读镜像」两档（开关本身表达「关闭」）；已保存旧模式的用户仍会看到该旧模式可选项、行为继续兼容，切换后即升级为新值。
  - 扩展：`autoSync.ts`（新增 `auto` 类型、`isChangeAutoSyncMode`/`isPeriodicAutoSyncMode` 含 `auto`、新增 `isMergeAutoSyncMode`、描述 key）、`background.ts`（两个 runner 加 `auto`→合并分支；`setupAutoSync` 因 `auto` 同属两类自动既记指纹又建 alarm）、`optionsDefaults.ts`/`setting.ts`/`useOptionsAutoSave.ts`（默认值 `auto`）、`options.tsx`（下拉简化 + 旧值归一）、i18n `autoSyncAuto`/`autoSyncDescAuto`/`autoSyncIntervalHintAuto`（12 语言）、新增 `tests/autoSyncMode.test.ts`。
  - **Mac 已对齐**：`SettingsStore.AutoSyncMode` 新增 `.auto`（`usesChangeMonitor`+`usesPeriodicTimer` 均含）、默认值改 `.auto`；`AutoSyncService` 的 `checkBookmarkChange`/`runPeriodicSync` 对 `.auto` 走合并；`MacFeatureViews` 模式选择器简化为 `selectableCases`（`.auto`/`.readOnlyMirror`）+ 旧值兼容。

### Fixed
- **删除保护静默跳过下载、用户无感知**：`readOnlyMirror`/`periodicDownload` 在「开启删除保护且本地已有书签」时直接静默 `return/continue`，既不提示也不刷新——表现为「只读镜像同步没反应、远端新增永远拉不下来」。现在跳过时**保留待同步角标并写入同步日志**（`syncSkippedDeleteProtection`），用户能在同步日志看到原因与处理建议。
  - 扩展：`background.ts`（`noteDownloadSkippedByDeleteProtection`，变更与定时两路下载跳过均记录）、i18n `syncSkippedDeleteProtection`（12 语言）。
  - **Mac 无需对齐**：Mac 端 `performDownload` 经 `assertDownloadAllowed` 抛异常并记 `.failure` 日志，本就不静默。

## [1.1.5] - 2026-06-29

### Changed
- **Windows 开发环境 Node.js**：本机已通过 winget 安装 Node.js LTS（v24）；新增 `scripts/ensure-node.ps1` 与 `scripts/test.ps1`，在 PATH 未含 `node`/`npm` 时自动定位 `Program Files\nodejs` 等常见安装路径；`npm run test:win` 与 `git-sync.ps1` 均会先调用该脚本。`npm run test` 已验证 **66/66** 通过。
- **自动同步只对当前选中的一种同步方式生效**：此前各提供方（GitHub/Gitea/WebDAV/S3）默认都开着自动同步，只要配置了凭证，后台会对所有已配置提供方分别建立监听/定时器并同步。现在自动同步**只针对当前 `syncProvider`（用户选定的那一种）**运行，其余提供方即使已配置且开了自动同步也不会触发。与设置页「自动同步只显示当前提供方配置」的现状保持一致。
  - 扩展：`setting.ts`（`hasAnyAutoSyncEnabled` 仅看当前提供方）、`background.ts`（`setupAutoSync`/`runChangeAutoSync`/`runPeriodicAutoSync` 不再遍历 `ALL_SYNC_PROVIDERS`，并忽略非当前提供方的过期 alarm）。
  - **Mac 已对齐**：`AutoSyncService`（`applySettings`/`checkBookmarkChange`/`runPeriodicSync` 仅对 `settings.syncProvider` 生效，忽略过期定时器）。

### Changed
- **大幅加快同步速度（减少网络与本地读取往返）**：合并同步的关键路径此前包含多次冗余开销，现已削减：
  - **本地读取 3 次 `getTree` → 1 次**：`applyBookmarkTreeIncremental` 用同一次 `getTree` 结果同时完成「系统文件夹定位 / preHeal / 匹配检查」，仅当 preHeal 真正改动过树时才重新读取（新增 `systemFolderIdsFromRootChildren`、`buildBookmarkCreateContextFromRootChildren`）。
  - **Gitea 上传省去一次「取 sha」GET**：合并开始时的 `get()` 会缓存文件 blob sha，`update()` 直接复用，PUT 成功后用响应里的新 sha 刷新缓存；sha 失效（409/422/404）时自动回退重取并重试，绝不会因缓存陈旧写坏远端。
  - **合并成功后不再额外打 2 次远端 GET 刷新计数**：合并刚上传完，本地/远端数量已知（本地=已写入数、远端=已上传数），直接写入存储，去掉内部与 `finishSyncMessage` 各一次 `refreshSyncCounts` 的远端请求。
  - 综合效果：**稳定态（无变化）合并 ≈ 2 次 Gitea 往返 + 1 次本地 `getTree`**，局域网下通常 1s 内完成；首次清理 191 条无效链接那种大改动属一次性。实际耗时仍受局域网 Gitea 延迟下限约束。
  - 扩展：`bookmarkTreeWriter.ts`、`bookmarkTreeSync.ts`、`giteaBackend.ts`、`background.ts`、新增 `getTree` 单次读取回归测试。
  - **Mac 待对齐（可选优化）**：`RemoteSyncService` 的 Gitea 上传可同样缓存 sha；本地写入读取优化为扩展独有。

- **同步自动过滤无法存储的链接（一次到位）**：`buildMergePlan` 现在在合并阶段就把 `javascript:`/`chrome://`/`data:` 等浏览器无法保存的链接从**本地写入树**与**上传内容**中一并剔除。效果：本地写入不再产生「被浏览器拒绝」的失败、合并干净地报成功（附「已过滤 N 个无效链接」说明），且**再同步一次后云端文件也会收敛为干净的可同步集合**，本地与云端的可同步书签数自然一致。
  - 扩展：`syncOrchestrator.ts`（`merged` 树预先 `sanitizeBookmarkTreeForCreate`、`omittedUncreatableCount` 基于过滤前后差值）、新增回归测试。
- **帮助页新增「哪些书签无法同步」说明**：列出 bookmarklet、浏览器内部页、`data:`/`mailto:` 等非网页协议、畸形链接四类，并说明同步会自动过滤、被过滤数量会记入日志。
  - 扩展：`options.tsx`（帮助页新区块）、i18n `helpUnsyncable*`（12 语言，非英语为英文回退）。
- **修复 i18n 文件损坏**：此前批量脚本用 `$1` 字符串替换误把整块内容嵌入，导致 10 个语言的 `syncUncreatableInCloud`/`syncLocalApplyGap`/`logMergePartial` 等键 JSON 损坏；已用函数替换重建为有效英文回退，并补回 zh_CN 丢失的 `logOperationAutoDownload` 键。12 语言全部校验通过。

### Fixed
- **合并日志仍显示「582 成功」与 190 条被拒矛盾**：冲突统计现仅计可创建 URL（不再出现「仅远程 191 条」误导）；上传 payload 会剔除 `javascript:`/`chrome://` 等无效链接（下次远端计数与本地对齐）；有浏览器拒绝写入时改为**部分完成**（`logMergePartial`），不再标「成功 + 同步仍已完成」。
  - 扩展：`mergeConflictStats.ts`、`syncOrchestrator.ts`（`sanitize` 上传）、`background.ts`、i18n `logMergePartial`/`syncUncreatableOmittedFromUpload`（12 语言）。

- **合并显示「成功」但本地/云端永远不一致（391 vs 582 根因）**：合并计划用原始 URL 计数（582），但 Chrome 无法创建约 191 个无效/被拦截链接（`javascript:`、`chrome://` 等）；`scopedTreeMatches` 用「可创建子集」比对后误判为已匹配，跳过本地写入，却仍把上传当成功并乐观写入计数。现在：① 本地/云端计数统一为**可创建**书签数；② `applyLocalRoots` 写入后**实测**本地数量，不再假定计划数；③ 本地未写满则标为失败并提示；④ 合并完成后刷新真实计数；⑤ 云端含不可创建链接时给出说明。
  - 扩展：`bookmarkTreeWriter.ts`（`countCreatableBookmarkUrls`）、`syncCounts.ts`、`syncOrchestrator.ts`、`background.ts`、i18n `syncUncreatableInCloud`/`syncLocalApplyGap`（12 语言）。
  - **Mac 待对齐**：Swift 端计数与成功判定需同样区分可创建 URL。

- **同步耗时过长 / 离开界面后自动同步跑不完（preHeal 冗余 IO 根因）**：合并前的一次性重复项自愈 `preHeal`（`healLiveDuplicateSiblingsRecursive`）即使在**没有任何重复**时，也会对树中**每个文件夹**无条件执行一次 `browser.bookmarks.getChildren`，且其返回值丢失了 `children`，导致递归时**每个子文件夹又被额外 `getChildren` 一次**。582 条书签、上百文件夹 ⇒ 数百次串行 API 调用，preHeal 阶段就要耗费可观时间。同步整体过重时，MV3 Service Worker 在 popup 关闭后会被浏览器回收，后台自动同步在完成前被中断——这正是「离开扩展界面后不自动同步」的主因。现在 `healLiveDuplicateSiblingsAtLevel` **仅在本层确实发生了去重改动时才重新拉取子节点**，否则直接复用 `getTree` 已带的 `children`，无重复树的 preHeal 几乎零额外 IO，同步显著加快、后台自动同步更可能在被回收前完成。
  - 扩展：`bookmarkTreeSync.ts`（`healLiveDuplicateSiblingsAtLevel` 增加 `mutated` 判定，未改动则复用既有 `children`）。
  - **Mac 无需对齐**：此自愈逻辑针对浏览器原生同步产生的重复文件夹，为扩展独有；Safari plist 写入路径无同类机制。

- **`Can't find bookmark for id.` 导致合并同步失败（真正根因）**：本地写入阶段，删除多余书签/文件夹时直接 `browser.bookmarks.get()/remove()/removeTree()`，但目标 id 可能在本轮中已被「父文件夹 removeTree」或「重复项自愈」提前删除而失效。这三处删除调用**未加 try/catch**，一旦命中失效 id 就抛 `Can't find bookmark for id.` 并中断整个合并 → 上传不执行、同步失败。现在统一用 `removeStaleNode` 包裹：失效 id 视为「已删除」并跳过，绝不再因单个失效节点中断同步。
  - 扩展：`bookmarkTreeSync.ts`（`removeStaleNode` + `MISSING_NODE_ERROR` 容错、scoped 删除加 try/catch）、新增集成测试「重复自愈留下失效 id 时不抛错」。
  - **Mac 待对齐**：核对 Swift 端写入删除是否也需容忍失效节点。

- **合并同步长期停在 `merge:localApply`（本地写入极慢）**：增量写入 `syncFolderLevel` 在**每个文件夹层级**都重复执行整棵子树的重复项自愈（`healLiveDuplicateSiblingsRecursive`），582 条书签 + 深层文件夹会触发**数千次**串行 `browser.bookmarks` API 调用，表现为一直停在「正在同步 · merge:localApply」。现在改为：**仅在合并开始前做一次 preHeal**，去掉每层 start/end 的冗余自愈；写入过程每 20 次操作更新阶段（`merge:localApply:40` 等），便于确认在前进而非卡死。
  - 扩展：`bookmarkTreeSync.ts`（移除 per-level 冗余 heal、新增 `onProgress`）、`background.ts`（写入进度写入 `syncDiagPhase`）。
  - **Mac 待对齐**：Swift 端增量写入若存在同类 per-level 重复自愈，需同样优化。

- **合并同步因个别书签被浏览器拒绝而每次失败（根因）**：本地增量写入时，`applyIncremental` 只要遇到 `result.failed > 0` 就抛 `bookmarkCreatePartialFailure`，导致 `runMergeSync` 直接失败、**上传根本不执行**。只要云端书签里含浏览器拒绝创建的 URL（`javascript:`、`chrome://`、`place:`、畸形/超长链接等），同步就**每次必然失败**——连接测试只做 GET 故能通过。现在本地写入**容忍**这些被拒节点：跳过它们、继续完成合并与上传，并在同步日志/通知里如实标注「跳过 N 条」。
  - 同时新增**同步阶段实时诊断**：后台在 `merge:start/fetchRemote/plan/localApply/localApplied/upload/finalize/done` 等关键步骤写入 `storage.local.syncDiagPhase`；popup「正在同步」提示会**实时显示当前阶段**（经 storage 监听更新），超时提示也会附上最后阶段，能直接看出卡在拉取、本地写入还是上传。`runMergeSync` 新增 `onPhase` 回调以区分「计算方案 / 本地写入 / 写入完成」。
  - 扩展：`background.ts`（`applyIncremental` 不再因部分失败抛错、`lastLocalApplyFailures` 计数、`setSyncDiag` 阶段写入、合并日志追加 `syncLocalApplyPartial`）、`SyncHomePanel.tsx`（超时提示附带阶段）、i18n `syncLocalApplyPartial`（12 语言）。
  - **Mac 待对齐**：核对 Swift 端合并写入是否也会因个别书签失败而整体中断，如是需同样改为容忍。

- **Gitea 合并同步 90s 超时（连接测试通过但同步失败）**：`runMergeSync` 曾用 `Promise.all` 同时等待「本地书签合并」与「远端快照归档」（`pushRemoteSnapshot` 含多次 Gitea PUT/DELETE）。连接测试只做 GET，合并却要写快照 + 上传，内网 Gitea 写入慢时总耗时超过 90s 锁超时。现在快照归档改为**后台异步**（不阻塞合并），合并锁上限单独放宽至 **180s**（上传/下载仍为 90s）。
  - 扩展：`syncOrchestrator.ts`（`parallelArchive` fire-and-forget）、`syncOperationLock.ts`（`MERGE_SYNC_MAX_MS`）、`background.ts`（merge 用 180s 锁）、`SyncHomePanel.tsx`（客户端看门狗 200s）、新增集成测试「不等待 parallelArchive」。
  - **Mac 待对齐**：`RemoteSyncService` 合并前远端归档若同样阻塞主路径，需改为异步（后续核对 Swift 合并流程）。

- **同步后一直提示「正在同步中」无法再同步（死锁）**：后台用内存锁 `withSyncOperationLock` 串行化同步，靠 `work()` 完成后的 `finally` 释放。若某次同步的网络请求在 TCP 层被静默丢包/卡住而永不返回（常见于内网 Gitea 经防火墙），`finally` 永不执行，`running` 永久卡在 `true`，之后每次点同步都被 `isSyncOperationRunning()` 直接挡回「正在同步中」。现在给锁加**硬超时（90s）**：无论 `work()` 是否返回，超时即强制释放锁并抛 `SyncOperationTimeoutError`，调用方收到友好的「同步超时」提示而非死锁。
  - 扩展：`syncOperationLock.ts`（`withSyncOperationLock` 加 `maxMs` 竞速 + `SyncOperationTimeoutError`）、`background.ts`（`finishSyncMessage` 将超时错误映射为 `syncTimeoutHint`）、`SyncHomePanel.tsx`（客户端看门狗提到 110s，置于后台超时之上以便真实错误先返回）、新增 `tests/syncOperationLock.test.ts` 超时释放用例。
  - **Mac 不适用**：死锁源于 MV3 后台 Service Worker 的内存锁，macOS 原生应用无此结构（属平台独有）。

- **同步「一直转圈、几分钟不结束」**：MV3 Service Worker 可能在同步进行中被浏览器回收，导致 popup/设置页的 `sendMessage` 响应丢失、`await` 永不返回、spinner 永久转圈（从未报错）。现在为每次同步/上传/下载/差异预览加**客户端看门狗超时**（同步 90s、预览 45s），超时即停掉 spinner 并提示「同步超时，去同步日志查看结果」；后台若稍后完成，计数仍会经 storage 监听自动刷新。
  - 同时收紧网络层超时：三个远端后端（GitHub/Gitea/WebDAV）的 ky `timeout` 由 **60s 降到 20s**（保留 `retry: 1`），内网/不可达时快速失败，不再串成好几分钟。
  - 扩展：`SyncHomePanel.tsx`（`sendMessageWithTimeout` 看门狗 + `syncTimeoutHint` 提示，popup 与设置页共用）、`giteaBackend.ts`/`githubHttp.ts`/`webdavBackend.ts`（timeout 20s）、i18n `syncTimeoutHint`（12 语言）。
  - **Mac 已对齐（网络超时）**：`RemoteSyncService` 的 `giteaRequest`/`githubRequest`/`webdavRequest` 设 `request.timeoutInterval = 20`。看门狗为 MV3 消息机制特有，macOS 原生应用无此问题（属平台独有，无需对齐）。

### Changed
- **点击图标改为弹出轻量浮窗**：此前工具栏图标的 `default_popup` 指向完整设置页 `options.html`，把六个标签（首页/连接/自动同步/数据/工具/帮助）和自动保存长表单挤进 popup，失焦即关闭、编辑易被打断。现在新增独立轻量入口 `popup.html`，只承载同步首页（计数、同步/上传/下载、查看差异、切换目标），并在顶部提供「设置」按钮通过 `openOptionsPage` 打开完整设置页。`options.html` 仍作为独立设置标签页保留。
  - 扩展：`src/entrypoints/popup/{index.html,popup.tsx,popup.css}`（复用 `SyncHomePanel`/`SyncStatusBar` + react-hook-form 表单骨架与 `useOptionsAutoSave` 持久化）、`wxt.config.ts`（`action.default_popup` 改为 `popup.html`）。popup chunk 仅约 18KB。
  - **Mac 不适用**：popup 为浏览器工具栏图标特性，macOS 应用使用菜单栏窗口，无对应概念（属平台独有，无需对齐）。

### Added
- **差异查看器**：当本地与云端书签数量不一致时，同步首页出现醒目提示横幅，可一键「查看差异」；数量一致时也提供轻量入口（可发现「数量相同但内容不同」的情况）。差异弹窗按双栏布局展示「仅本地有 / 仅远端有」的具体书签，含字母色块头像、标题、域名、所在文件夹路径，支持搜索过滤、点击在新标签页打开，并可直接「合并同步」消除差异。
  - 扩展：`bookmarkDiff.ts`（`computeMergePreview` 增加 `localOnlyItems/remoteOnlyItems` 结构化项与路径、截断标志）、`BookmarkDiffDialog.tsx`、`SyncHomePanel.tsx`、`sync-home.css`、i18n `diffViewer*`。复用既有 `previewMerge` 后台消息，差异计算沿用 scope + exclude 过滤口径。
  - **Mac 待对齐**：macOS 应用尚未提供等价的差异查看 UI；底层 scope/计数逻辑已对齐（见 1.1.4），仅缺可视化弹窗，后续在同步页补充。

## [1.1.4] — 2026-06-28

### Fixed
- **本地与云端数量长期不一致**：云端计数此前统计远端文件里的**全部**书签，而本地计数会按「同步范围」和「排除文件夹」过滤，导致只要设置了范围或排除规则，两侧数字就永远对不上。现在云端计数同样应用相同的 scope + exclude 过滤，口径一致。
  - 扩展：`syncCounts.ts`（`fetchRemoteScopedBookmarkCount` 解析远端后走 `prepareBookmarksForSync`）。
  - **Mac 已对齐**：`RemoteSyncService.fetchRemoteBookmarkCount` 改用 `SyncCounts.countScopedBookmarkUrls`。
- 说明：扩展图标「!」与数量漂移的根因若来自**浏览器自带书签同步与本扩展同时开启**，无法仅靠扩展消除——两者会互相覆盖书签。必须二选一（见双重同步提醒）。

## [1.1.3] — 2026-06-27

### Fixed
- **重复文件夹自愈（加强）**：商店版 v1.1.2 未包含上一版修复；本版在合并/下载写入前**先**递归折叠浏览器里同层同名文件夹，合并逻辑也会合并多个同名本地/远程文件夹的子项，不再丢失内容。
  - 扩展：`bookmarkTreeSync.ts`（`healLiveDuplicateSiblingsRecursive`）、`mergeBookmarks.ts`（同名文件夹分组合并 + `collapseDuplicateSiblingNodesInRoots`）。
  - **Mac 已对齐**：`SafariBookmarkStore.collapseDuplicateSiblings`（v1.1.2 起已有）。

### Added
- **双重同步冲突提醒**：在首次引导（SetupWizard）、主页（SyncHomePanel）、设置→同步高级里提示用户「浏览器自带书签同步」与本扩展只能保留一套，否则会产生重复文件夹。
  - 扩展：`DualSyncWarningBanner.tsx` + i18n `dualSyncWarning*`；主页提示可「知道了」永久关闭。
  - **Mac 已对齐**：同步页顶部 `StatusBanner(.warning)` 提示关闭 iCloud Safari 书签同步（`L10n.dualSyncWarning`）。

### Fixed
- **自动同步在 MV3 下不可靠**：书签变更触发的防抖从 `setTimeout` 改为 `chrome.alarms`（Service Worker 休眠后仍会执行）；间隔节流到期后自动补调度。
- **自动同步开关检测**：`hasAnyAutoSyncEnabled` 按当前手动同步目标（如 Gitea）判断，避免误跳过。
- 设置页补充间隔说明：「书签变更时」模式下的间隔仅为节流；真正定时同步需选「定时合并同步」等模式。
- 扩展图标叹号悬停提示：本地书签已变更、等待自动同步。

## [Unreleased]

## [1.1.78] - 2026-07-22

### Changed
- **整理 / AI**：去掉「仅本地规则」选项与「关闭（仅本地规则）」服务商；有模型则走 AI，未配置时仍自动回退本地引擎。

## [1.1.77] - 2026-07-22

### Added
- **兼容 OpenCode**：新增 OpenCode Zen / Go 预设（https://opencode.ai/zen/v1）；支持导入本机 opencode.json 自动填充服务商、Base URL 与模型。

## [1.1.76] - 2026-07-22

### Changed
- **AI 模型设置**：扩充中国常用（DeepSeek / 通义 / 智谱 / Kimi / 硅基流动 / 豆包等）与通用（OpenAI / Claude / Gemini / OpenRouter / Groq 等）预设；支持自定义 OpenAI 兼容网关与任意模型名；切换服务商自动填入 Base URL 与推荐模型。

## [1.1.75] - 2026-07-16

### Changed
- **文件夹对照表**：方案预览先展示「旧文件夹 → 新文件夹」一一对照，可改新夹名、逐条/全部采纳；未采纳行不进入应用范围。

## [1.1.74] - 2026-07-16

### Changed
- **方案预览可读性**：每条显示「原文件夹 → 新文件夹」；顶部汇总文件夹数前后对比与移动/归档/保留/待定数；明确归档不等于删除。

## [1.1.73] - 2026-07-16

### Fixed
- **智能整理无反应**：未配置 API 时误走云端权限校验导致失败且 UI 未提示；现默认本地规则即可生成方案，并正确展示后台错误。


Chrome Web Store resubmission after **Code Readability** rejection (obfuscated JS in store ZIP).

### Fixed
- Chrome / Web Store builds use **minification only** (`WXT_SKIP_OBFUSCATION=1`); `javascript-obfuscator` is no longer applied to packages submitted to Chrome.
- `scripts/check-store-zip.mjs` fails the build if `_0x…` obfuscator identifiers remain in the Chrome bundle.
- **`docs/PRIVACY.md`** — English/Chinese aligned with v1.1.2 (S3, E2E, tabs/windows/webNavigation, tab sessions, broken-link check).

## [1.1.1] — 2026-06-20

Chrome Web Store release following **1.1.0**.

### Added
- Header version badge on options / popup UI.
- Incremental bookmark sync (no full clear-and-rewrite on merge/download).
- Remote snapshots stored under `BookmarkSync/_snapshots/` (not repo root).
- Configurable remote snapshot retention (max count, max age, scheduled cleanup).

### Improved
- Sync UI no longer blocks the whole panel while syncing; other tabs stay usable.
- Sync mutex prevents parallel merge/upload/download races.
- Local/remote counts align after merge; URL normalization unified.
- 自动同步：各提供方独立注册周期 alarm；变更模式支持间隔设置与节流；S3 配置变更会触发 alarm 重建。
- 书签数量：本地/远端统一按同步范围（scope）统计，手动同步后两侧计数一致。
- 配置备份说明缩短为两行以内。
- **Mac 应用**：与扩展对齐（`SyncCounts.swift`、`AutoSyncService`、设置 UI、远程快照子目录与保留策略）。

### Fixed
- Double-click sync could inflate bookmark counts and freeze the UI.
- 合并后本地/远端书签计数不一致（按唯一 URL 计数）。

## [1.1.0] — 2026-06-19

### Added

- **Tools hub** — Health overview, duplicate bookmark detection & cleanup, broken-link checker, empty-folder cleanup, organize by domain, HTML/JSON import & export
- **Remote snapshot center** — List remote snapshots, preview diff, restore from snapshot (GitHub / Gitea / WebDAV / S3)
- **Merge preview** — See local-only / remote-only items before merge sync
- **Version history** — Browse Git commits (GitHub / Gitea) or remote snapshot history with diff preview
- **Config backup** — Export/import settings profiles; local config backup list
- **S3-compatible storage** — Full UI for endpoint, bucket, keys, auto-sync, and notifications
- **Advanced sync** — Delete protection, read-only mirror mode, sync scope, folder exclude patterns, E2E encryption UI & remote re-encrypt
- **Scheduled tool tasks** — Optional periodic duplicate / link checks (Tools)
- **Tab sessions 2.0** — Save, restore, and sync named tab sessions
- **Production build hardening** — Minification, no source maps, optional JS obfuscation for release ZIPs
- **Chrome Web Store publish scripts** — `npm run publish:chrome`, local OAuth token flow

### Improved

- Tools panel reorganized into Health, Backup, Governance, Session, Platform groups
- Duplicate detection 2.0 — URL normalization (tracking params, www)
- Link checker 2.0 — Strictness levels, inconclusive handling, batch remove
- i18n — Extended `en` / `zh_CN` strings for all new tools
- macOS app parity (separate deliverable) — Tools tab, S3/E2E, merge preview, version history

### Fixed

- Sync guards — Delete protection blocks destructive download when local bookmarks exist
- Read-only mode blocks remote uploads consistently
