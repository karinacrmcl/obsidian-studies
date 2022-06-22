---
tags: utility
aliases: notes
---

# 📒Notebook

### 🌱Seedling
```dataview
TABLE priority FROM "Notes" AND #note 
WHERE status = "seedling"
SORT file.mtime DESC
```
### 🌿Fern
```dataview
TABLE priority FROM "Notes" AND #note 
WHERE status = "fern"
SORT file.mtime DESC
```

### 🎋Incubator
```dataview
TABLE priority FROM "Notes" AND #note 
WHERE status = "incubator"
SORT file.mtime DESC
```

### 🌲Evergreen

```dataview
TABLE priority FROM "Notes" AND #note 
WHERE status = "evergreen"
SORT file.mtime DESC
```

## Metadata
- Releated: [[01 Home]]