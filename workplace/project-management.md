# Project Management — 專案管理與跨部協作英文大全

#### Dialogue Examples — 實際對話範例

### 📊 里程碑檢視會議
**情境**：每週專案狀態檢討會議

**Project Manager**: Let's review the Q4 release status. Overall we're in yellow status due to the data migration dependency. New ETA is November 18th.

**Stakeholder**: What's the impact on the marketing launch campaign?

**PM**: Marketing can proceed with the original November 15th date. We'll have core features ready, but advanced analytics will be in the follow-up release.

**Engineering Lead**: The database migration is more complex than anticipated. We discovered legacy data that needs cleanup.

**Stakeholder**: Options to accelerate?

**PM**: We could de-scope the custom export feature and deliver it in December. That reduces launch risk significantly.

**Stakeholder**: I'm comfortable with that approach. Let's proceed with the revised scope.

### 🚨 風險緩解策略討論
**情境**：識別到重大風險時的應對會議

**Engineering Lead**: I want to discuss the rollout strategy. This release touches core payment logic, so there's inherent risk.

**PM**: What's your recommendation for risk mitigation?

**Eng Lead**: We can feature-flag the new logic and roll out gradually. Start with 5% of traffic, then 25%, then full rollout.

**PM**: Timeline for the gradual rollout?

**Eng Lead**: One week between each phase, assuming no issues. If metrics degrade, rollback is instant.

**PM**: That sounds prudent. What metrics should we monitor?

**Eng Lead**: Payment success rate, latency, and error rates. We'll set up alerts for any degradation beyond baseline.

**PM**: Perfect. Let's document the guardrails and assign owners for each metric.

### 📅 依賴項協調會議
**情境**：解決跨團隊依賴和阻礙

**PM**: We're blocked by the authentication service upgrade. Data team, what's your current timeline?

**Data Team Lead**: We're running behind due to the compliance audit. Realistically, we need two more weeks.

**PM**: That pushes our integration testing to December. Frontend team, how does this affect your work?

**Frontend Lead**: We can mock the new auth endpoints and continue development. Integration testing delay isn't critical for us.

**PM**: Backend team impact?

**Backend Lead**: We can adapt our timeline. Could data team prioritize the schema changes over the performance optimizations?

**Data Team Lead**: Yes, schema changes are less complex. We can deliver those by November 30th.

**PM**: Great. I'll update the project timeline and communicate the changes to stakeholders.

### 🔄 敏捷Sprint規劃
**情境**：Sprint計劃會議討論任務優先級和估算

**Scrum Master**: For Sprint 12, we have 40 story points of capacity. Product owner, what are the priorities?

**Product Owner**: User profile overhaul is highest priority—that's 21 points. Then the API rate limiting feature at 13 points.

**Developer**: The profile overhaul is large. Should we break it down further?

**PO**: Good idea. Profile editing could be 8 points, settings migration 8 points, and UI updates 5 points.

**Scrum Master**: That's more manageable. With rate limiting at 13 points, we're at 34 total. We have 6 points remaining.

**Tech Lead**: Let's reserve those 6 points for bug fixes and tech debt. We had several production issues last sprint.

**Scrum Master**: Agreed. Final sprint commitment: profile editing, settings migration, UI updates, API rate limiting, plus 6 points for maintenance.

### 📈 進度報告與狀態同步
**情境**：向高層報告專案整體進度

**VP Engineering**: How's the mobile app rewrite progressing? Board wants an update for next week.

**PM**: We're 60% complete and on track for January launch. Core functionality is done, working on polish and edge cases.

**VP**: Any risks to the timeline?

**PM**: Two medium risks: app store review process could add 2 weeks, and we're waiting on final designs for the onboarding flow.

**VP**: Mitigation strategies?

**PM**: We'll submit to app stores early for parallel review, and we're using wireframes to start development while design finalizes.

**VP**: Budget status?

**PM**: 55% of budget used with 60% completion, so we're slightly under budget. No concerns there.

**VP**: User feedback from beta testing?

**PM**: Very positive. 4.6/5 rating with users particularly praising the improved performance and intuitive navigation.

### 🎯 範圍變更討論
**情境**：客戶或利害關係人要求新功能或變更

**Client**: We need to add real-time notifications to the dashboard. Our users are requesting this urgently.

**PM**: I understand the business need. This would be a significant scope change requiring 3-4 weeks of additional development.

**Client**: Can we add it to the current release?

**PM**: Adding it now would delay the launch by a month and increase costs by 25%. I recommend we deliver the core dashboard first.

**Client**: What's the alternative?

**PM**: We could deliver notifications as a phase 2 enhancement. That way you get value from the main dashboard immediately.

**Client**: Timeline for phase 2?

**PM**: If we start phase 2 planning next month, we could deliver notifications by March.

**Client**: That works. Let's proceed with the original scope and plan phase 2 separately.

### 🛠️ 技術債務與維護
**情境**：平衡新功能開發與技術債務處理

**Engineering Manager**: Our tech debt backlog is growing. We need to allocate time for maintenance and refactoring.

**PM**: What's the impact of not addressing it?

**Eng Manager**: Development velocity is slowing, and we're seeing more production issues. Our error rate increased 15% this quarter.

**PM**: Proposed solution?

**Eng Manager**: Dedicate 20% of each sprint to tech debt. That's about 8 story points per sprint for maintenance work.

**PM**: How do we justify this to stakeholders who want new features?

**Eng Manager**: I can show the correlation between tech debt and slower delivery. Investing in maintenance actually accelerates future feature development.

**PM**: Can you quantify the impact?

**Eng Manager**: Based on past data, addressing tech debt should improve our velocity by 25% within two months.

**PM**: That's compelling. Let's present this to the product team and get buy-in for the 20% allocation.bulary
- milestone 里程碑：hit/meet a milestone
- dependency 依賴項：manage dependencies, unblock a dependency
- blocker 阻礙：remove a blocker, blocked by
- deliverable 交付物：final deliverables, sign-off
- scope 範圍：scope creep, out of scope
- risk 風險：identify/mitigate risks, risk register
- timeline 時程：project timeline, revised timeline
- owner 負責人：DRI (Directly Responsible Individual)
- stakeholder 利害關係人：key stakeholders, stakeholder map
- retrospective 事後檢討：project retro
- escalation 升級處理：escalate to
- ETA 預計完成時間：share an ETA

## Useful Patterns
- 狀態更新：
  - We’re on track for [milestone] by [date].
  - We’re slightly behind due to [reason], new ETA is [date].
- 風險與阻礙：
  - A current risk is [risk]; mitigation plan is [plan].
  - We’re blocked by [dependency]; request support from [team].
- 對齊與決策：
  - To align on scope, here’s the proposal and trade-offs.
  - Decision needed on [topic] by [date] to avoid delays.
- 交付與驗收：
  - Here are the deliverables for your review and sign-off.
  - Let’s schedule a handoff and walkthrough.

## Context Examples
- Sprint 站會：
  - “Yesterday I finalized the API spec, today I’ll implement endpoints, no blockers.” 昨天完成 API 規格，今天實作端點，無阻礙。
- 依賴協調：
  - “Could data team prioritize the schema change this week?” 資料團隊可否本週優先處理資料表調整？
- 風險緩解：
  - “To reduce launch risk, we’ll roll out in phases and monitor metrics.” 為降低上線風險，我們將分階段釋出並監控指標。
- 變更請求：
  - “This change is out of scope; proposing a follow-up phase.” 此變更不在範圍，建議下一階段處理。

## Dialogue Examples — 實際對話範例

### 里程碑檢視會
PM: Status is yellow—dependency on data migration. New ETA is the 18th.
Stakeholder: What’s the impact on launch?
PM: Low risk if we de-scope the custom export; I recommend we proceed.

### 風險緩解對話
Eng Lead: We can feature-flag and roll out gradually. If metrics degrade, rollback is instant.
PM: Great—let’s document guardrails and owners.

## Mini Drills
- 60 秒週報：用「進度-風險/阻礙-下一步」三段式。
- 風險描述演練：用一句話說清風險、影響、緩解。

## Quick Reference — 中英雙語卡
- We’re on track for [milestone] by [date]. 我們有望在[日期]達成[里程碑]。
- New ETA is [date] due to [reason]. 因[原因]新的預計完成時間為[日期]。
- We’re blocked by [dependency]. 我們被[依賴項]卡住。
- Decision needed on [topic] by [date]. [主題]需在[日期]前做決定。
- Here are the deliverables for sign-off. 這是待你核可的交付物。

---

## Engineering Add-on — 工程加值章節

### 工程化術語對照
- DRI/Owner → 值班/主責工程師（assignee, owner）
- Dependency → 服務/資料表/外部 API 依賴（service/schema/external API）
- Risk → 效能回歸/相容性破壞/可用性風險（performance regression, breaking change, availability)
- Deliverable → PR/可部署分支/文件與 Runbook

### 工程專用句型
- 發版時程：
  - We’ll cut a release branch on [date] and target GA on [date].
  - Rollout plan: canary 5% → 25% → 100% with metrics guardrails.
- 依賴管理：
  - This feature depends on schema v3; requesting migration by [date].
  - Please provide a stable API contract; we’ll version as /v2.
- 風險緩解：
  - Feature-flagged; can roll back without redeploy.
  - Added SLO alerts to catch latency regressions.

### 小範例（站會/週會）
- “API ready for QA; waiting on auth team for token introspection. ETA Friday.”
- “Risk: cache stampede under load; mitigation: request coalescing.”
