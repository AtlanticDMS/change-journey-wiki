---
title: "Knowledge Graph Dashboard"
type: index
tags: [type/index]
---

> This dashboard auto-updates as you add notes. All queries use Dataview — install it from Community Plugins before opening this note.

---

## 📚 All books in the vault

```dataview
TABLE author, year, status
FROM "Books"
WHERE type = "book"
SORT year DESC
```

---

## 💡 Concepts still in draft

```dataview
TABLE source_books
FROM "Concepts"
WHERE contains(tags, "status/draft")
SORT file.name ASC
```

---

## 🔁 Themes and how many books cover them

```dataview
TABLE length(books_covering_this) AS "Books covering this"
FROM "Themes"
SORT length(books_covering_this) DESC
```

---

## 👤 People referenced across the vault

```dataview
TABLE books_referenced_in, books_written
FROM "People"
SORT file.name ASC
```

---

## 💬 All quotes, sorted by book

```dataview
TABLE source_book, source_person
FROM "Quotes"
SORT source_book ASC
```

---

## ❗ Orphan concepts (no source book linked)

```dataview
LIST
FROM "Concepts"
WHERE !source_books
```

---

## 📝 Notes edited in the last 7 days

```dataview
TABLE file.mtime AS "Last edited", type
FROM "" 
WHERE file.mtime >= date(today) - dur(7 days)
SORT file.mtime DESC
```

---

## 🗺 All Maps of Content

```dataview
LIST
FROM "Index"
WHERE type = "index"
SORT file.name ASC
```
