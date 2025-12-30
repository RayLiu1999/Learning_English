# Project Management — 專案管理與跨部協作英文大全

## Core Vocabulary

| 單字/片語     | 中文意思     | 常見搭配                                  |
| ------------- | ------------ | ----------------------------------------- |
| milestone     | 里程碑       | hit/meet a milestone                      |
| dependency    | 依賴項       | manage dependencies, unblock a dependency |
| blocker       | 阻礙         | remove a blocker, blocked by              |
| deliverable   | 交付物       | final deliverables, sign-off              |
| scope         | 範圍         | scope creep, out of scope                 |
| risk          | 風險         | identify/mitigate risks, risk register    |
| timeline      | 時程         | project timeline, revised timeline        |
| owner         | 負責人       | DRI (Directly Responsible Individual)     |
| stakeholder   | 利害關係人   | key stakeholders, stakeholder map         |
| retrospective | 事後檢討     | project retro                             |
| escalation    | 升級處理     | escalate to                               |
| ETA           | 預計完成時間 | share an ETA                              |

---

## Useful Patterns

### 狀態更新

- We're on track for [milestone] by [date].
- We're slightly behind due to [reason], new ETA is [date].
- Status is [green/yellow/red] due to [reason].

### 風險與阻礙

- A current risk is [risk]; mitigation plan is [plan].
- We're blocked by [dependency]; request support from [team].
- Risk mitigation: we'll [action] and monitor [metrics].

### 對齊與決策

- To align on scope, here's the proposal and trade-offs.
- Decision needed on [topic] by [date] to avoid delays.
- Options are A, B, C; I recommend B because [reason].

### 交付與驗收

- Here are the deliverables for your review and sign-off.
- Let's schedule a handoff and walkthrough.

---

## Context Examples

### Sprint 站會

- "Yesterday I finalized the API spec, today I'll implement endpoints, no blockers." 昨天完成 API 規格，今天實作端點，無阻礙。

### 依賴協調

- "Could data team prioritize the schema change this week?" 資料團隊可否本週優先處理資料表調整？

### 風險緩解

- "To reduce launch risk, we'll roll out in phases and monitor metrics." 為降低上線風險，我們將分階段釋出並監控指標。

### 變更請求

- "This change is out of scope; proposing a follow-up phase." 此變更不在範圍，建議下一階段處理。

---

## Dialogue Examples — 實際對話範例

### 📊 里程碑檢視會議

**情境**：每週專案狀態檢討會議

**Project Manager**: Let's review the Q4 release status. Overall we're in yellow status due to the data migration dependency. New ETA is November 18th.

**Stakeholder**: What's the impact on the marketing launch campaign?

**PM**: Marketing can proceed with the original date. Core features will be ready, but advanced analytics will be in the follow-up release.

**Stakeholder**: Options to accelerate?

**PM**: We could de-scope the custom export feature. That reduces launch risk significantly.

---

### 🚨 風險緩解策略討論

**情境**：識別到重大風險時的應對會議

**Engineering Lead**: This release touches core payment logic, so there's inherent risk. I recommend we feature-flag the new logic and roll out gradually.

**PM**: Timeline for the gradual rollout?

**Eng Lead**: One week between each phase. If metrics degrade, rollback is instant.

**PM**: What metrics should we monitor?

**Eng Lead**: Payment success rate, latency, and error rates.

---

### 📅 依賴項協調會議

**情境**：解決跨團隊依賴和阻礙

**PM**: We're blocked by the authentication service upgrade. Data team, what's your timeline?

**Data Team Lead**: We're running behind due to the compliance audit. Realistically, we need two more weeks.

**PM**: Backend team, can you adapt?

**Backend Lead**: We can. Could data team prioritize the schema changes over performance optimizations?

**Data Team Lead**: Yes, we can deliver schema changes by November 30th.

---

### 🔄 敏捷 Sprint 規劃

**情境**：Sprint 計劃會議討論任務優先級

**Scrum Master**: For Sprint 12, we have 40 story points of capacity. What are the priorities?

**Product Owner**: User profile overhaul is highest—21 points. Then API rate limiting at 13 points.

**Developer**: The profile overhaul is large. Should we break it down?

**Scrum Master**: Good idea. Let's also reserve 6 points for bug fixes and tech debt.

---

### 📈 進度報告與狀態同步

**情境**：向高層報告專案整體進度

**VP Engineering**: How's the mobile app rewrite progressing?

**PM**: We're 60% complete and on track for January launch. Core functionality is done.

**VP**: Any risks?

**PM**: Two medium risks: app store review could add 2 weeks, and we're waiting on final designs.

**VP**: Mitigation strategies?

**PM**: We'll submit early for parallel review, and we're using wireframes while design finalizes.

---

### 🎯 範圍變更討論

**情境**：客戶要求新功能或變更

**Client**: We need to add real-time notifications. Can we add it to the current release?

**PM**: This would delay launch by a month and increase costs by 25%. I recommend we deliver notifications as a phase 2 enhancement.

**Client**: Timeline for phase 2?

**PM**: If we start planning next month, we could deliver by March.

---

## Mini Drills

1. **60 秒週報**：用「進度-風險/阻礙-下一步」三段式
2. **風險描述演練**：用一句話說清風險、影響、緩解
3. **準備狀態更新**：Green/Yellow/Red + 原因 + 行動

---

## Quick Reference — 中英雙語卡

| English                                   | 中文                               |
| ----------------------------------------- | ---------------------------------- |
| We're on track for [milestone] by [date]. | 我們有望在[日期]達成[里程碑]。     |
| New ETA is [date] due to [reason].        | 因[原因]新的預計完成時間為[日期]。 |
| We're blocked by [dependency].            | 我們被[依賴項]卡住。               |
| Decision needed on [topic] by [date].     | [主題]需在[日期]前做決定。         |
| Here are the deliverables for sign-off.   | 這是待你核可的交付物。             |
| This is out of scope; proposing phase 2.  | 這超出範圍，建議在第二階段處理。   |
