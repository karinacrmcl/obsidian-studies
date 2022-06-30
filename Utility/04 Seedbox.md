---
tags: utility
---

# 📥Seedbox

## ⚪Backlog
```dataview
TABLE type, priority FROM "Notes" AND #seedbox 
WHERE status = "backlog"
SORT file.mtime DESC
```
## 🟠Inprogress

```dataview
TABLE type,priority FROM "Notes" AND #seedbox 
WHERE status = "inprogress"
SORT file.mtime DESC
```
## 🟢Completed
```dataview
TABLE type, priority FROM "Notes" AND #seedbox 
WHERE status = "completed"
SORT file.mtime DESC
```

## Metadata
- Related: [[01 Home]]
