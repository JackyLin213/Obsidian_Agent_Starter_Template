# Obsidian AI 知識庫啟動模板 (Obsidian Agent Starter Template)

歡迎使用結合 **PARA 方法論**、**Zettelkasten 卡片盒筆記法** 與 **AI Agent 協同架構** 的現代化 Obsidian 知識庫！

本專案專為搭配 **Antigravity** 或其他本地/雲端 AI Agent 設計，提供自動化的資料清洗、靈感提煉、原子化筆記重構與主題地圖（MOC）管理能力。

---

## 🌟 核心特色

- 🏛️ **PARA × Zettelkasten 完美融合**：以 PARA 管理行動專案與生活領域，以卡片盒體系沉澱高價值、長青的原子化知識。
- 🤖 **AI Agent 專屬架構 (`AGENTS.md`)**：內建完整 Agent 執行規範，支援直接透過自然語言或指令驅動 AI 整理 Inbox、清洗剪藏與提煉概念。
- ⚛️ **兩階段蒸餾法 (Two-Stage Distillation)**：文獻筆記（完整出處與上下文）與永久原子筆記（單一概念、高度複用）分層管理。
- 🗺️ **MOC 主題地圖與動態 Dataview**：兼具人工結構化導航與自動化查詢索引。
- 🏷️ **嚴謹的 Frontmatter 元數據標準**：統一欄位定義，避免標籤污染與斷鏈。

---

## 📁 目錄結構說明

```
.
├── 00_Inbox/                  # [收集箱] 靈感、隨手問題、待清洗剪藏的暫存入口
├── 10_Projects/               # [專案] 具明確目標與截止日的短期任務
├── 20_Areas/                  # [領域] 長期維護的責任範疇（健康、財務、技術研發等）
├── 30_Resources/              # [知識庫核心 - Zettelkasten 沉澱區]
│   ├── 01_Literature/         # 文獻筆記：網頁剪藏、論文摘要、閱讀記錄
│   ├── 02_Permanent/          # 原子筆記：單一概念卡片（Evergreen Notes）
│   └── 03_MOCs/               # 主題地圖 (Maps of Content)：領域知識樞紐
├── 40_Archives/               # [歸檔] 已完成專案與歷史封存檔案
└── 90_System/                 # [系統設定] 模板庫與 Dataview 語法參考
    ├── 模板/                   # 標準 Markdown 模板
    └── Dataview_Queries.md    # 常用 Dataview 查詢代碼庫
```

---

## 🚀 如何與 AI Agent 協同工作？

當你透過 **Antigravity** 連接到此專案時，Agent 會自動讀取根目錄的 `AGENT.md` 規範。你可以直接在對話中使用以下常見場景：

### 1. 整理收集箱 (Triage Inbox)
> **你對 Agent 說**：「請幫我整理 `00_Inbox` 裡面的所有筆記。」  
> **Agent 會做的事**：自動判斷內容類型，清洗雜訊，生成文獻筆記並提煉 3~5 張原子概念卡片存入 `30_Resources`，最後更新相關的 MOC。

### 2. 處理網頁剪藏 (Process Web Clipper)
> **你對 Agent 說**：「我剪藏了一篇關於《分散式系統一致性演算法》的文章，請幫我清洗並做成原子筆記。」  
> **Agent 會做的事**：移除廣告與雜訊，產生 `@作者_文章標題.md` 文獻筆記，並萃取如 `Paxos 演算法核心機制.md`、`Raft 與 Paxos 的異同.md` 等原子卡片。

### 3. 記錄隨手靈感與零碎問題
> **你對 Agent 說**：「我剛才在思考如何優化微服務間的快取失效問題，有幾個想法...」  
> **Agent 會做的事**：剖析問題痛點、補齊架構上下文、產出清晰可執行的行動清單（Next Actions）或提煉為問題卡片。

### 4. 建立與維護主題地圖 (Generate MOC)
> **你對 Agent 說**：「請為我建立一份關於『人工智慧與大型語言模型』的 MOC。」  
> **Agent 會做的事**：自動掃描 Vault 中相關的概念卡片與文獻，在 `30_Resources/03_MOCs/` 建立結構化主題地圖與 Dataview 查詢。

---

## 🛠️ 推薦安裝的 Obsidian 外掛

為了獲得最佳體驗，建議在 Obsidian 中啟用以下社群外掛（Community Plugins）：

1. **Dataview**：強大的資料庫查詢與動態列表功能。
2. **Templater** 或 **Templates (內建)**：快速插入 `90_System/模板/` 下的標準範本。
3. **Omnisearch** 或 **Smart Connections**：強化語意搜尋與 AI 關聯能力。
4. **Linter**：自動在存檔時排版 Markdown 與規範 Frontmatter。

---

詳細的 Agent 工作流程與規範請參閱 [AGENTS.md](file:///AGENTS.md)。
