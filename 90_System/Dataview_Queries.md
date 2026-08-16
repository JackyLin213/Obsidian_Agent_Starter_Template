# Dataview 常用查詢語法庫 (Dataview Query Library)

本文件整理了 Obsidian Vault 中最常用的 Dataview 與 DataviewJS 查詢語法，供使用者與 Agent 在建立 MOC 或總覽儀表板時快速引用。

---

## 1. Inbox 待處理清單
列出 `00_Inbox` 中尚未歸檔或狀態為 `inbox` 的筆記：

```dataview
TABLE type AS "類型", created AS "建立時間", file.folder AS "所在目錄"
FROM "00_Inbox" OR #inbox
WHERE status = "inbox"
SORT file.ctime DESC
```

---

## 2. 最近提煉的永久/原子筆記 (Permanent Notes)
列出最近 15 篇建立或修改的原子概念卡片：

```dataview
TABLE tags AS "主題標籤", up AS "上層 MOC", file.mtime AS "最後更新"
FROM "30_Resources/02_Permanent"
WHERE type = "permanent"
SORT file.mtime DESC
LIMIT 15
```

---

## 3. 文獻筆記與剪藏摘要 (Literature Notes)
依據作者與主題列出文獻筆記：

```dataview
TABLE author AS "作者", tags AS "標籤", status AS "狀態", file.mtime AS "更新時間"
FROM "30_Resources/01_Literature"
WHERE type = "literature"
SORT file.mtime DESC
```

---

## 4. 主題地圖（MOC）總覽
列出 Vault 中所有的 MOC 地圖：

```dataview
TABLE file.mtime AS "更新時間", tags AS "標籤"
FROM "30_Resources/03_MOCs"
WHERE type = "moc"
SORT file.name ASC
```

---

## 5. 活躍專案進度追蹤 (Active Projects)
列出進行中的專案與截止日：

```dataview
TASK
FROM "10_Projects"
WHERE !completed
GROUP BY file.link
```

---

## 6. 孤立筆記排查 (Orphan Notes - 無出鏈或無入鏈)
```dataview
TABLE file.folder AS "目錄", file.cday AS "建立日期"
FROM "30_Resources/02_Permanent"
WHERE length(file.inlinks) = 0 AND length(file.outlinks) = 0
```
