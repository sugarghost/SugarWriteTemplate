---
status: active
start_date: <% tp.date.now("YYYY-MM-DD") %>
end_date: 
tags: [project]
---
# <% tp.file.title %>

## 🎯 프로젝트 목표 (Goals)
- **궁극적인 목표 (Ultimate Goal):** - **성공 기준 (Success Criteria):** (이것이 완료되면 '성공'이라고 말할 수 있다)

---
## ⏳ 타임라인 및 마일스톤 (Timeline & Milestones)
- **마감일:**
- **주요 일정:**
    - [ ] 마일스톤 1
    - [ ] 마일스톤 2

---
## 🗂️ 핵심 리소스 및 링크 (Key Resources & Links)
%% 이 프로젝트의 MOC(Map of Content) 역할을 하는 섹션. 관련 노트들을 연결한다. %%
- 

---
## ✅ 주요 할 일 (Main Tasks)
```dataview
TASK
FROM outgoing([[#]])
WHERE !completed
GROUP BY file.link
```