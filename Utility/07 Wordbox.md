---
tags: utility
aliases:
---

# 🗃️Wordbox
```dataview
TABLE W as Words
FROM "Notes"
where W != null 
SORT file.mtime DESC
```
## Word List:
```dataview
list from "Notes" and #word
```