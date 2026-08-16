---
title: "MOC - 個人知識管理與第二大腦 (PKM)"
type: moc
status: active
tags:
  - moc
  - index
  - productivity/pkm
created: "2026-08-16 13:29:00"
updated: "2026-08-16 13:29:00"
aliases:
  - "PKM MOC"
  - "第二大腦主題地圖"
up: "[[30_Resources/03_MOCs/00_Index]]"
---

# MOC - 個人知識管理與第二大腦 (PKM)

> [!INFO] 🗺️ 主題地圖導覽
> 本主題地圖匯聚個人知識管理（Personal Knowledge Management）、卡片盒筆記法（Zettelkasten）、PARA 架構與現代知識工程實踐，作為第二大腦知識體系的頂層導航樞紐。

---

## 🏛️ 核心架構與方法論 (Core Methodologies)
- [[PARA 方法論在知識管理中的核心邏輯]]：以行動性（Actionability）為核心的四層動態分類法。
- [[卡片盒筆記法的原子性原則 (Atomicity Principle)]]：網狀卡片盒知識庫的自洽與單一概念基石。
- [[漸進式總結法 (Progressive Summarization)]]：低認知負擔的多層次知識壓縮機制。

---

## 📚 相關文獻與精華閱讀 (Literature Notes)
- [[@TiagoForte_2022_打造第二大腦核心精華]]：CODE 模型與第二大腦實踐總覽。

---

## 📊 動態關聯清單 (Dataview Query)

### 本主題下的原子筆記 (Permanent Notes)
```dataview
TABLE file.mtime AS "最後更新", tags AS "標籤"
FROM "30_Resources/02_Permanent"
WHERE contains(tags, "productivity/pkm") OR up = this.file.link
SORT file.mtime DESC
```

### 本主題下的文獻筆記 (Literature Notes)
```dataview
TABLE author AS "作者", status AS "狀態", file.mtime AS "更新時間"
FROM "30_Resources/01_Literature"
WHERE contains(tags, "productivity/pkm") OR up = this.file.link
SORT file.mtime DESC
```
