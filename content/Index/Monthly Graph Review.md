---
title: "Monthly Graph Review"
type: index
tags: [type/index]
---

> Run this review once a month. It takes 20–30 minutes and keeps the graph alive and useful.

---

## Step 1 — Orphan check (5 min)
Open graph view → filter panel → enable "Orphans". For every isolated node:
- [ ] Add at least one outgoing link to a related concept or theme
- [ ] Add a link to the relevant MOC

---

## Step 2 — Draft note sweep (5 min)
Open [[Dashboard]] and check the "Concepts still in draft" table.
For each draft note:
- [ ] Fill in the "My thinking" section with at least one sentence
- [ ] Change `status/draft` to `status/complete` in the YAML

---

## Step 3 — Theme review (5 min)
Open each Theme note and ask:
- [ ] Has a new book or concept been added that belongs under this theme?
- [ ] Are there points of tension or agreement that should be noted?
- [ ] Is there a new synthesis forming across books?

Update the "My synthesis" section if yes.

---

## Step 4 — New connections (10 min)
Open graph view and look at the layout with fresh eyes.
- [ ] Are there two concept nodes sitting near each other with no link between them? Should there be one?
- [ ] Are there People notes that should link to more concepts?
- [ ] Are there Quote notes with only one concept link? Can you add another?

---

## Step 5 — Prepare for next book (5 min)
- [ ] Have you decided which book to add next?
- [ ] Create a stub Book note in `Books/` with just the title and author
- [ ] Add any Themes from that book that don't exist yet as stub Theme notes

---

## Graph health metrics
Run these Dataview queries and note the numbers each month to track growth:

**Total notes:**
```dataview
TABLE length(rows) AS "Count"
FROM ""
GROUP BY type
```

**Most connected concepts (proxy: notes with most outgoing links):**
```dataview
TABLE length(file.outlinks) AS "Outgoing links"
FROM "Concepts"
SORT length(file.outlinks) DESC
LIMIT 5
```

**Least connected notes (candidates for enrichment):**
```dataview
TABLE length(file.outlinks) AS "Outgoing links"
FROM ""
WHERE length(file.outlinks) < 2
SORT length(file.outlinks) ASC
LIMIT 10
```
