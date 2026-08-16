# 常用 Dataview 查詢代碼庫 (Dataview Queries Library)

本文件整理了知識庫中常用的 Dataview 與 DataviewJS 查詢語法，可直接複製至 MOC 或 Dashboard 中使用。

---

## 1. 收集箱待處理清單 (Inbox Triage)
列出 `00_Inbox` 中尚未清洗提煉的草稿筆記：

```dataview
TABLE file.ctime AS "建立時間", tags AS "標籤"
FROM "00_Inbox"
WHERE status = "inbox" OR status = "draft"
SORT file.ctime DESC
```

---

## 2. 進行中的專案 (Active Projects)
列出目前正在進行中的專案與其截止日期：

```dataview
TABLE deadline AS "截止日", file.mtime AS "最後更新"
FROM "10_Projects"
WHERE status = "active"
SORT deadline ASC
```

---

## 3. 領域主題卡片索引 (Permanent Notes by Domain)
以特定領域標籤查詢所有長青原子筆記：

```dataview
TABLE aliases AS "別名", up AS "所屬 MOC", file.mtime AS "修改時間"
FROM "30_Resources/02_Permanent"
WHERE contains(file.tags, "Tech")
SORT file.mtime DESC
```

---

## 4. 近期新增的文獻筆記 (Recent Literature Notes)
追蹤最近閱讀或剪藏整理的文獻筆記：

```dataview
TABLE author AS "作者", file.ctime AS "建立時間", sources AS "來源"
FROM "30_Resources/01_Literature"
SORT file.ctime DESC
LIMIT 10
```

---

## 5. 主題地圖 (MOCs) 清單
列出知識庫中現有的所有知識地圖：

```dataview
TABLE file.mtime AS "最後維護時間", tags AS "標籤"
FROM "30_Resources/03_MOCs"
SORT file.name ASC
```

---

## 6. 最近 7 天的每日覆盤 (Recent Daily Notes)
```dataview
TABLE file.day AS "日期"
FROM "20_Areas/日誌"
SORT file.name DESC
LIMIT 7
```
