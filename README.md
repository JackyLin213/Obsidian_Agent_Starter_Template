# Obsidian AI 知識庫啟動模板 (Obsidian Agent Starter Template)

歡迎使用結合 **PARA 方法論**、**Zettelkasten 卡片盒筆記法** 與 **AI Agent 協同架構** 的現代化 Obsidian 知識庫！

本專案專為搭配 **Antigravity** 或其他本地/雲端 AI Agent 設計，提供自動化的資料清洗、靈感提煉、原子化筆記重構與主題地圖（MOC）管理能力。

---

## 🌟 核心特色

- 🏛️ **PARA × Zettelkasten 完美融合**：以 PARA 管理行動專案與生活領域，以卡片盒體系沉澱高價值、長青的原子化知識。
- 🤖 **AI Agent 專屬架構 (`AGENTS.md`)**：內建完整 Agent 執行規範，支援直接透過自然語言對話驅動 AI 整理 Inbox、清洗剪藏與提煉概念。
- ⚛️ **兩階段蒸餾法 (Two-Stage Distillation)**：文獻筆記（完整出處與上下文）與永久原子筆記（單一概念、高度複用）分層管理。
- 🗺️ **MOC 主題地圖與動態 Dataview**：兼具人工結構化導航與自動化查詢索引。
- 🏷️ **嚴謹的 Frontmatter 元數據標準**：統一欄位定義，避免標籤污染與斷鏈。

---

## 📁 目錄結構說明

```
.
├── 00_Inbox/                  # [收集箱] 靈感、隨手問題、待清洗剪藏的暫存入口
│   └── Clippings/             # [剪藏暫存] 網頁剪藏預設存入區（自動納管）
├── 10_Projects/               # [專案] 具明確目標與截止日的短期任務（YYYY-專案名稱.md）
├── 20_Areas/                  # [領域] 長期維護的責任範疇（健康、財務、技術研發等）
│   ├── 日誌/                  # [全域日誌] 每日覆盤與工作生活記錄（YYYY-MM-DD.md）
│   └── <責任領域名稱>/         # 特定領域管理目標與專業日誌
├── 30_Resources/              # [知識庫核心 - Zettelkasten 沉澱區]
│   ├── 01_Literature/         # 文獻筆記：網頁剪藏、論文摘要、閱讀記錄（@作者_標題.md）
│   ├── 02_Permanent/          # 原子永久筆記：高度提煉的單一概念卡片（至多 3 階子資料夾）
│   └── 03_MOCs/               # 主題地圖 (Maps of Content)：領域知識樞紐（MOC - 主題.md）
├── 40_Archives/               # [歸檔] 歷史封存檔案
│   ├── Projects/              # 已結案封存的歷史專案
│   └── Inbox_History/         # 已提煉完成之 Inbox 歷史原始檔（Inbox Zero 封存）
└── 90_System/                 # [系統設定] 模板庫、附件與 Dataview 語法參考
    ├── Attachments/           # 附件集中存放區（圖片、PDF、音訊等）
    ├── Dataview_Queries.md    # 常用 Dataview 查詢代碼庫
    └── Templates/             # 標準 Markdown 模板庫
```

---

## 🚀 如何與 AI Agent 協同工作？

當你透過 **Antigravity** 連接到此專案時，Agent 會自動讀取根目錄的 `AGENTS.md` 規範。你可以直接在對話中使用以下常見場景：

### 1. 整理收集箱 (Triage Inbox)
> **你對 Agent 說**：「請幫我整理 `00_Inbox` 裡面的所有筆記。」  
> **Agent 會做的事**：自動判斷內容類型，清洗雜訊，生成文獻筆記並提煉 3~5 張原子概念卡片存入 `30_Resources`，依 **Inbox Zero** 原則將原始檔無損歸檔至 `40_Archives/Inbox_History/`，最後更新相關 MOC。

### 2. 處理網頁剪藏 (Process Web Clipper)
> **你對 Agent 說**：「我剪藏了一篇關於《分散式系統一致性演算法》的文章，請幫我清洗並做成原子筆記。」  
> **Agent 會做的事**：移除廣告與雜訊，產生 `@作者_文章標題.md` 文獻筆記，並萃取如 `Paxos 演算法核心機制.md`、`Raft 與 Paxos 的異同.md` 等原子卡片。

### 3. 記錄隨手靈感與每日日誌
> **你對 Agent 說**：「幫我記錄今天的每日日誌：今天完成了核心架構重構，開了 2 場技術評審...」  
> **Agent 會做的事**：套用標準日誌模板，快速寫入 `20_Areas/日誌/YYYY-MM-DD.md`。

### 4. 專案結案與歸檔 (Archive Project)
> **你對 Agent 說**：「我的 2026-Q4 資料庫遷移專案已經完成了，請幫我結案。」  
> **Agent 會做的事**：檢查任務完成度，將狀態更新為 `completed`，萃取專案沉澱的方法論為永久卡片，並將檔案移至 `40_Archives/Projects/`。

### 5. 建立與維護主題地圖 (Generate MOC)
> **你對 Agent 說**：「請為我建立一份關於『人工智慧與大型語言模型』的 MOC。」  
> **Agent 會做的事**：自動掃描 Vault 中相關的概念卡片與文獻，在 `30_Resources/03_MOCs/` 建立結構化主題地圖與 Dataview 查詢。

---

## 🛠️ 推薦安裝的 Obsidian 外掛

為了獲得最佳體驗，建議在 Obsidian 中啟用以下社群外掛（Community Plugins）：

1. **Dataview**：強大的資料庫查詢與動態列表功能。
2. **Templater** 或 **Templates (內建)**：快速插入 `90_System/Templates/` 下的標準範本。
3. **Omnisearch** 或 **Smart Connections**：強化語意搜尋與 AI 關聯能力。
4. **Linter**：自動在存檔時排版 Markdown 與規範 Frontmatter。

---

詳細的 Agent 工作流程與規範請參閱 [AGENTS.md](AGENTS.md) 或 `[[AGENTS]]`。
