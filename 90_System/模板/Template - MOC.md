---
title: "MOC - {{topic}}"
type: moc
status: active
tags:
  - moc
  - index
created: {{date}} {{time}}
updated: {{date}} {{time}}
aliases:
  - "{{topic}} MOC"
up: "[[00_Index]]"
---

# MOC - {{topic}}

> [!INFO] 🗺️ 主題地圖導覽
> 本地圖彙整與「{{topic}}」相關的所有原子概念卡片、文獻摘要與實踐專案，構成結構化的知識樞紐。

```toc
minLevel: 2
maxLevel: 4
```

---

## 🏛️ 核心架構與概念體系 (Core Mental Models)
- [[核心概念 1]]：簡短說明
- [[核心概念 2]]：簡短說明

## 🛠️ 方法論與實踐工具 (Methodologies & Tools)
- [[實踐方法 1]]
- [[工具與技術 1]]

## 📚 相關文獻與研究來源 (Literature Notes)
- [[文獻筆記 1]]
- [[文獻筆記 2]]

---

## 📊 動態筆記清單 (Dataview Query)

### 本主題下的原子筆記 (Permanent Notes)
```dataview
TABLE file.mtime AS "最後更新", tags AS "標籤"
FROM "30_Resources/02_Permanent"
WHERE contains(tags, "{{topic_tag}}") OR up = this.file.link
SORT file.mtime DESC
```

### 本主題下的文獻筆記 (Literature Notes)
```dataview
TABLE author AS "作者", status AS "狀態", file.mtime AS "更新時間"
FROM "30_Resources/01_Literature"
WHERE contains(tags, "{{topic_tag}}") OR up = this.file.link
SORT file.mtime DESC
```
