<div align="center">

# EQBrain 2027

**以 AFFiNE 為基礎重構的 AI 任務協作系統**

</div>

> 本檔為中文版 README。**上半部「EQBrain 2027」為本專案的功能與定位說明**；**下半部為原 AFFiNE 專案 README 的中文翻譯**（本專案以 [AFFiNE](https://github.com/toeverything/AFFiNE) 為基礎 fork 改造）。原文見 [`README.md`](./README.md)。

---

## 一、EQBrain 2027 是什麼（功能與定位）

EQBrain 是一套以 **AI 素養（AI Fluency）** 為核心的**任務編組協作系統**：把工作拆進「任務編組」，讓 AI 同事能和人一起處理票務，並以風險分級與授權把關，確保 AI 能幫上忙又不失控。**EQBrain 2027 版以 AFFiNE 為基礎重構**，取其區塊編輯器、白板、本機優先與即時協作能力，疊上 EQBrain 既有的編組、權限、AI 執行、知識庫與稽核。

### 核心功能

- **任務編組與權限**：工作以「任務編組」組織；角色含成員、主管、組長、團隊管理員。權限一律在伺服器端強制（不信任瀏覽器），成員只看得到所屬編組、主管綜覽、非成員擋下。
- **票務（Notion 式）**：票的內容採 Notion 式區塊編輯器（標題、清單、待辦、引用、程式碼等），支援**多人即時協作**（看得到誰在編輯、即時同步游標與內容）、草稿自動存、按「完成」才重判風險與授權。
- **風險分級與授權**：每張票依風險分級（L1／L2／L3），重大（紅線）動作需人類核准；內容變更會重新判定風險、必要時作廢原授權，全程寫入稽核。
- **AI 執行**：可把票指派給編組的 AI 同事執行，結果回寫並自動交付驗收；AI 僅能存取所屬編組範圍。
- **知識庫（RAG）**：以本機嵌入建立編組知識庫，供 AI 回答時有所本；跨編組、跨租戶皆不可讀。
- **多租戶隔離**：以資料列安全（RLS）隔離各租戶資料。

### 定位

EQBrain 2027 的目標，是在 AFFiNE 這套成熟的「文件／白板／資料表超融合」工作空間之上，長出企業級的**任務編組、權限治理、AI 代理執行與稽核**，成為團隊與 AI 共同工作的作業系統。

> 功能內容由 EQBrain 幕僚長（Max）依現行產品設計整理；細節以產品設計文件與實作為準。

---

## 二、原 AFFiNE README（中文翻譯）

> 以下為 [AFFiNE](https://affine.pro) 原始 README 的中文翻譯，內容著作權屬 AFFiNE／toeverything。保留原文連結與出處；翻譯僅供本專案團隊閱讀參考。

<div align="center">

# [AFFiNE.Pro](https://affine.pro)
### 寫作、繪圖、規劃，一次到位

</div>

> 一套**注重隱私、本機優先、開源、開箱即用**的 Notion 與 Miro 替代方案。為天馬行空的創作者打造的超融合平台。

連結：[首頁](https://affine.pro) ｜ [Discord](https://affine.pro/redirect/discord) ｜ [線上體驗](https://app.affine.pro) ｜ [部落格](https://affine.pro/blog/) ｜ [文件](https://docs.affine.pro/)

> 文件、畫布與表格在 AFFiNE 裡被「超融合」在一起——正如 affine 這個字（əˈfʌɪn，近似「a-fine」）。

### 開始使用並持續關注

為我們按星（Star），就能在第一時間收到 GitHub 上所有的發行通知。

### 什麼是 AFFiNE

[AFFiNE](https://affine.pro) 是一套開源、全合一的工作空間，也是組裝你的知識庫所需各種「積木」的作業系統——維基、知識管理、簡報、數位資產等皆涵蓋。它是比 Notion 與 Miro 更好的替代方案。

### 功能特色

**真正能容納任何形式積木的畫布；文件與白板已完全融合。**

- 許多編輯器都自稱是生產力畫布，但 AFFiNE 是少數能讓你把任何積木放上無邊際畫布的產品——富文本、便利貼、內嵌網頁、多視圖資料庫、連結頁面、形狀，甚至投影片，應有盡有。

**隨時可上工的多模態 AI 夥伴**

- 寫一份專業工作報告？把大綱變成好看的簡報？把文章整理成結構化心智圖？整理工作計畫與待辦？或……用一句提示直接畫出並產生原型 App 與網頁？[AFFiNE AI](https://affine.pro/ai) 把你的創意推到想像力的邊界，就像 [Canvas AI](https://affine.pro/blog/best-canvas-ai) 能為腦力激盪生成心智圖。

**本機優先，且即時協作**

- 我們信奉「本機優先」：不論雲端如何，你的資料永遠存在你自己的磁碟、由你擁有。此外 AFFiNE 支援網頁與跨平台用戶端的即時同步與協作。

**自架，並打造你自己的 AFFiNE**

- 你可以自由管理、自架、fork 並打造屬於自己的 AFFiNE。外掛社群與第三方積木即將推出，更多進展見 [BlockSuite](https://blocksuite.io)。自架方式見 [如何自架 AFFiNE](https://docs.affine.pro/self-host-affine)。

### 致謝

「我們塑造工具，然後工具塑造我們。」一路上有許多先行者啟發我們，例如：

- Quip 與 Notion 的「萬物皆積木」概念
- Trello 的看板（Kanban）
- Airtable 與 Miro 的免程式可程式化資料表
- Miro 與 Whimsical 的無邊際視覺白板
- Remote 與 Capacities 的物件式標籤系統

這些 App 的原子化「積木」有很大重疊，但它們既非開源、也沒有像 VSCode 那樣可供貢獻者客製的外掛系統。我們想做出一個涵蓋所有我們喜愛功能、並更進一步的產品。感謝你的關注，更多細節見 https://affine.pro/ 。

### 貢獻

歡迎各類貢獻——臭蟲回報、功能建議、問題討論、社群參與。詳見原專案 [docs/types-of-contributions.md](https://github.com/toeverything/AFFiNE/blob/canary/docs/types-of-contributions.md) 與 [CONTRIBUTING.md](https://github.com/toeverything/AFFiNE/blob/canary/docs/CONTRIBUTING.md)。

> 注意：向原 AFFiNE 貢獻程式前需簽署其 [貢獻者授權協議（CLA）](https://cla-assistant.io/toeverything/AFFiNE)。

### 範本與部落格

AFFiNE 提供團隊預製的[範本](https://affine.pro/templates)（願景板、一頁式、課程計畫、數位手帳、ADHD 計畫表、閱讀紀錄、康乃爾筆記等），以及介紹用法與技巧的[部落格](https://affine.pro/blog/)。完整清單見原連結。

### 生態系

- [@affine/component](https://github.com/toeverything/AFFiNE/tree/canary/packages/frontend/component)：AFFiNE 元件資源。
- [@toeverything/theme](https://github.com/toeverything/AFFiNE/tree/canary/packages/common/theme)：AFFiNE 佈景主題。

### 上游專案（致謝）

AFFiNE 得以實現，仰賴眾多開源專案：

- [BlockSuite](https://github.com/toeverything/BlockSuite)——AFFiNE 背後的開源協作編輯器專案。
- [y-octo](https://github.com/y-crdt/y-octo)——原生、高效能、執行緒安全的 YJS CRDT 實作，是 AFFiNE 用戶端／伺服器達成「本機優先」的核心引擎。
- [OctoBase](https://github.com/toeverything/OctoBase)——AFFiNE 背後的開源資料庫，本機優先又可協作；以 Rust 寫成的輕量、可擴充資料引擎。
- 以及 [yjs](https://github.com/yjs/yjs)、[Electron](https://github.com/electron/electron)、[React](https://github.com/facebook/react)、[napi-rs](https://github.com/napi-rs/napi-rs)、[Jotai](https://github.com/pmndrs/jotai)、[async-call-rpc](https://github.com/Jack-Works/async-call-rpc)、[Vite](https://github.com/vitejs/vite) 等上游相依套件。

感謝社群提供如此強大又簡潔的函式庫，讓我們能更專注於產品邏輯的實作。

### 貢獻者

感謝所有曾為 AFFiNE 貢獻的人。相關專案、文件、工具或範本，歡迎提交 PR 到 [awesome-affine](https://github.com/toeverything/awesome-affine)。

### 自架（Self-Host）

可用 Docker 部署你自己、功能完整且不受限的 AFFiNE 版本。團隊持續更新至最新版，自架說明見[文件](https://docs.affine.pro/self-host-affine)；亦提供一鍵部署到 Render 與 Sealos 的途徑。

### 建置（Building）

- **Codespaces**：在 GitHub repo 主頁點綠色「Code」鈕、選「Create codespace on master」，會開啟已 clone、建置好的 Codespace。
- **本機**：從原始碼建置見 [BUILDING.md](https://github.com/toeverything/AFFiNE/blob/canary/docs/BUILDING.md)。

### 授權（License）

- **AFFiNE 社群版（CE）**：目前可用版本，依 **MIT** 授權、可免費自架。
- **AFFiNE 企業版（EE）**：尚未發行，將有更進階與面向企業的功能（如重新品牌化、SSO、進階管理與稽核等），詳見 https://affine.pro/pricing 。

詳見原專案 [LICENSE](https://github.com/toeverything/AFFiNE/blob/canary/LICENSE)。

---

*本中文 README 由 EQBrain 團隊整理：上半部為 EQBrain 2027 功能說明，下半部為 AFFiNE 原 README 之翻譯摘要（著作權屬 AFFiNE／toeverything）。如有出入，以原文 [README.md](./README.md) 與 https://affine.pro 為準。*
