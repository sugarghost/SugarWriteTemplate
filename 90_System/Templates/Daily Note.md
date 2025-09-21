---
tags:
  - daily
day_of_week: <% tp.date.now("dddd") %>
week_key: <% tp.date.now("YYYY-[W]WW", 0, tp.file.title, "YYYY-MM-DD") %>
created: <% tp.file.creation_date("YYYY-MM-DD HH:mm") %>
---
# <% tp.file.title %>

> [!quote]
> Today's Highlight: 

---
### 🧭 Navigation
- **Weekly:** [[<% tp.date.now("YYYY-[W]WW", 0, tp.file.title, "YYYY-MM-DD") %>]]
- **Monthly:** [[<% tp.date.now("YYYY-MM", 0, tp.file.title, "YYYY-MM-DD") %>]]

---
### ✅ Tasks & Events
%% 그날의 할 일이나 있었던 이벤트를 기록합니다. Tasks 플러그인과 연동됩니다. %%
- [ ] 

---
### 📓 Journal
%% 자유로운 생각, 감정, 업무 회고 등 인간으로서의 성찰을 기록합니다. %%
- 

---
### 💡 TIL (Today I Learned)
%% 개발자로서 배운 점, 깨달은 점을 기록합니다. 주간 회고 때 자동으로 수집됩니다. %%
- 

---
### 🔗 Links
%% 오늘 생성했거나 작업한 주요 노트를 연결하여 하루의 작업을 요약합니다. %%
- 

---
