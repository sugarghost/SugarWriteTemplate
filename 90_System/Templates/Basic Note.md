---
tags: 
aliases: 
related: 
created: <% tp.file.creation_date("YYYY-MM-DD HH:mm") %>
---
# [<% tp.file.title %>]()

# 🗂️ 관련 노트 목록
```dataview
TABLE WITHOUT ID
  file.link as "파일 이름",
  file.cday as "생성일"
FROM ""
WHERE related AND related = this.file.link
SORT file.cday DESC
```