# Incident Management — 事故處理英文大全

## Core Vocabulary
- severity 嚴重度：sev-1/2/3, P0/P1
- impact 影響：blast radius, affected users
- detection 偵測：alerts, monitoring
- mitigation 緩解：workaround, throttle, failover, rollback
- timeline 時序：incident timeline, TTD/MTTR
- communication 溝通：status update, stakeholder brief, status page
- root cause 根因：RCA, contributing factors
- action items 行動項：corrective actions, follow-ups
- runbook 操作手冊：SOP, playbook

## Useful Patterns
- 初次公告（內部）：
  - We're investigating a sev-1 impacting [service]; symptoms: […]. Next update at [time].
- 狀態頁更新（對外）：
  - Identified the issue; implementing mitigation. Next update in 30 minutes.
- 交接/輪班：
  - Handover: current state, active mitigations, owners per stream.
- 回復與收尾：
  - Service has recovered; we're monitoring for 1 hour before closure.
- 事後檢討（Postmortem）骨架：
  - Summary, Impact, Timeline, Root Cause, What Went Well, What Went Wrong, Action Items, Preventive Measures.

## Context Examples
- Slack 戰情室：
  - "Requesting DB on-call to check replication lag; web errors at 8% 5xx."
- 客戶信（Sev-1）：
  - "We apologize for the disruption between 09:10–09:55 UTC; root cause was a config regression. We're adding a safeguard and improving tests."
- 管理層簡報：
  - "Impact limited to APAC; MTTR 42m; no data loss; actions on slide 5."

## Dialogue Examples — 實際對話範例

### 🚨 事故戰情室對話
**情境**：緊急事故處理中的團隊協調

**Incident Commander**: We've got a Sev-1 affecting 20% of users. Payment processing is down. Current status?

**Engineer (Mike)**: Database connections are maxed out. I'm checking for a connection leak in the payment service.

**SRE (Lisa)**: I see a spike starting 10 minutes ago. Could be related to the deployment at 2:15.

**IC**: Let's roll back that deployment first to mitigate. How long to roll back?

**DevOps (Sam)**: 5 minutes to rollback, assuming no DB schema changes. Checking now... we're clear.

**IC**: Execute the rollback. I'll update the status page that we've identified the issue and are applying a fix.

### 📞 客戶溝通
**情境**：向客戶說明服務中斷情況

**Support Lead**: We're getting calls about checkout failures. What should I tell customers?

**IC**: We've identified the issue and are applying a fix. ETR is 15 minutes. Tell them to retry after 2:45 PM.

**Support Lead**: Got it. Should I proactively reach out to enterprise customers?

**IC**: Yes, and offer to extend their trial period by one day for the inconvenience.

**Support Lead**: I'll draft the communication now and send it out.

### 📈 事後檢討會議
**情境**：事故後的團隊檢討和改進討論

**Facilitator**: Let's walk through the timeline. What went well?

**Engineer**: Detection was fast—alerts fired within 2 minutes of the issue starting.

**SRE**: Communication was clear. Everyone knew their role and responsibilities.

**Facilitator**: What could we improve?

**DevOps**: We need better rollback automation. Manual steps took too long and increased MTTR.

**Manager**: Agreed. Let's prioritize automated rollbacks for next sprint.

**Engineer**: Also, we should add connection pool monitoring to catch this sooner.

### 🔄 事故狀態更新
**情境**：向管理層和利害關係人報告進展

**IC**: Update for leadership: We've mitigated the payment issue by rolling back. Error rate dropped from 15% to 0.2%.

**VP Engineering**: What's the root cause?

**IC**: Connection pool exhaustion due to a configuration change. We're analyzing why the change passed testing.

**VP Engineering**: Customer impact?

**IC**: Approximately 500 customers experienced checkout failures. Customer success is reaching out with credits.

**VP Engineering**: Timeline for permanent fix?

**IC**: Full analysis tomorrow, fix deployment by end of week.

### 📊 事故指標討論
**情境**：檢討事故響應指標和改進目標

**SRE Manager**: Let's review our SLIs for this incident. MTTD was 2 minutes, MTTR was 18 minutes.

**Engineer**: MTTD was good, but MTTR could be better. The rollback process took 12 minutes.

**DevOps Lead**: We can automate that. Target should be 5-minute rollbacks.

**SRE Manager**: What about customer communication?

**Support Manager**: First customer notification went out 8 minutes after detection. We can improve that to 5 minutes.

**SRE Manager**: Let's set those as our targets for next quarter.

### 📝 Postmortem 撰寫
**情境**：團隊協作撰寫事故報告

**Tech Writer**: I'm drafting the postmortem. Can someone explain the technical root cause?

**Senior Engineer**: The connection pool size was reduced from 100 to 20 in the config change, but we didn't update the load test parameters.

**Tech Writer**: Why didn't the staging tests catch this?

**QA Lead**: Staging only has 10% of production traffic. The issue only manifests at full load.

**Tech Writer**: What's the action item?

**Senior Engineer**: Update load testing to use production-scale traffic patterns.

### 🛠️ 預防措施討論
**情境**：制定防止類似事故再次發生的策略

**Engineering Manager**: How do we prevent this type of issue in the future?

**SRE**: We need connection pool monitoring with alerts before we hit 80% utilization.

**DevOps**: Also, configuration changes should require performance review, not just functional review.

**QA**: We can add synthetic transactions that simulate peak load continuously.

**Engineering Manager**: Timeline for implementing these?

**SRE**: Monitoring can be done this week. Load testing improvements need 3 weeks.

**Engineering Manager**: Let's track these in our reliability backlog.

## Mini Drills
- 寫 4 句狀態頁更新（Investigating/Identified/Monitoring/Resolved）。
- 用 5 句話寫 Postmortem 摘要（含影響與兩項行動）。

## Quick Reference — 中英雙語卡
- We're investigating a sev-1 incident. 我們正在調查一個最嚴重等級事件。
- Issue identified; applying mitigation. 問題已找出；正在緩解。
- Service has recovered; we're monitoring. 服務已恢復；持續監控中。
- We'll publish the RCA by [date]. 我們會在[日期]發布根因分析。
- Action items are tracked in the ticket. 行動項已建立工單追蹤。
