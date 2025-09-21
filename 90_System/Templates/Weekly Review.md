---
tags:
  - weekly-review
week_key: <% tp.date.now("YYYY-[W]WW") %>
week_start_date: <% tp.date.weekday("YYYY-MM-DD", 0) %>
week_end_date: <% tp.date.weekday("YYYY-MM-DD", 6) %>
created: <% tp.file.creation_date("YYYY-MM-DD HH:mm") %>
---
# <% tp.date.now("YYYY-[W]WW") %> 주간 회고 및 계획

> [!summary] 지난 한 주 요약
> 주요 성과/이슈 한 줄 요약을 적어주세요.

---
## 📊 Weekly Dashboard

### 📝 이번 주에 생성된 노트
```dataview
TABLE WITHOUT ID
  file.link as "파일",
  file.cday as "생성일"
FROM -"90_System" AND -"05_Periodic"
WHERE file.cday >= date(this.week_start_date) AND file.cday <= date(this.week_end_date)
SORT file.cday ASC
```
---

### ✅ 이번 주에 완료한 일들
```dataview
TASK
FROM #daily
WHERE completed AND (
  (completion >= date(this.week_start_date) AND completion <= date(this.week_end_date))
  OR (
    date(file.day) >= date(this.week_start_date) AND date(file.day) <= date(this.week_end_date)
  )
)
GROUP BY file.link
```
---

### 💡 이번 주에 배운 것들 (TIL)
```dataview
TABLE L.text AS "TIL"
FROM #daily
WHERE week_key = this.file.name
FLATTEN file.lists AS L
WHERE contains(lower(meta(L.section).subpath), "til") AND L.text != ""
SORT file.day ASC
```
---

## 🤔 Weekly Reflection

### 🚀 이번 주 성과 (Wins & Achievements)

### 🌱 성찰 및 교훈 (Reflection & Lessons)

### 🎯 다음 주 목표 (Goals for Next Week)
