# Remote & Async Communication — 遠端與非同步溝通英文大全

## Core Vocabulary

| 單字/片語 | 中文意思  | 常見搭配                               |
| --------- | --------- | -------------------------------------- |
| async     | 非同步    | async update, async decision           |
| timezone  | 時區      | timezone overlap, UTC                  |
| bandwidth | 心力/時間 | I don't have the bandwidth             |
| sync      | 同步      | sync meeting, quick sync               |
| thread    | 討論串    | keep the thread, summarize the thread  |
| recording | 錄影      | meeting recording, watch the recording |
| summary   | 摘要      | TL;DR, executive summary               |
| follow-up | 跟進      | actionable follow-up                   |
| etiquette | 禮儀      | meeting etiquette, mute/unmute         |
| overlap   | 重疊時間  | timezone overlap                       |

---

## Useful Patterns

### 發起非同步請求

- Sharing context below; please comment by [date/timezone].
- Proposing Option A/B; vote with 👍/👎 by [deadline].
- I'll leave this in the doc for async review.

### 安排跨時區

- Could we meet during the [X–Y] UTC overlap?
- I can do early morning my time or late afternoon yours.
- What's a time that works across timezones?

### 釐清與確認

- To confirm, you're suggesting that … correct?
- Noted. I'll update the doc and circle back.
- Just to make sure I understood correctly...

### 線上會議

- Let's keep mics muted unless speaking.
- I'll share my screen; please let me know if it's visible.
- I'll record this for those who can't attend.

---

## Context Examples

### Slack/Teams 簡訊

- "Quick async update: deployment succeeded; details in the doc." 簡短非同步更新：部署成功，細節見文件。

### PR/Doc 留言

- "Left some comments inline; overall looks good." 已在內文留言，整體不錯。

### 跨時區協作

- "I'll leave notes so you can pick this up in your morning." 我會留筆記，方便你早上銜接。

---

## Dialogue Examples — 實際對話範例

### 🌐 跨時區協作銜接

**情境**：美國和亞太團隊的工作交接

**US Engineer (EOD)**: I'll leave notes in the shared doc so APAC can pick up the investigation in the morning.

**APAC Engineer (morning)**: Thanks for the detailed notes! I see you narrowed it down to the payment gateway.

**US Engineer**: I suspect it's related to the timeout configuration. Check the logs around 14:30 UTC.

**APAC Engineer**: Found it! I'll post an update by our EOD so you can review when your day starts.

---

### 📝 非同步決策制定

**情境**：團隊需要在分散時區中做出技術決策

**Tech Lead**: Sharing context below on database migration options. Please comment by Thursday 5 PM UTC.

**Backend Engineer**: Option A looks simpler. Zero downtime and easy rollback. 👍

**DevOps Engineer**: I prefer Option B. More upfront work but better long-term performance.

**Tech Lead**: Thanks everyone. Option A wins 2-1. I'll start the implementation plan.

---

### 🎥 虛擬會議協調

**情境**：組織跨地區的重要會議

**Project Manager**: We need to sync all stakeholders. What's everyone's availability?

**EU Team Lead**: I can do Tuesday 8-10 AM UTC.

**US West Coast**: Tuesday 8 AM UTC is 1 AM for me. Could we do Wednesday 4-6 PM UTC?

**PM**: Wednesday 4-6 PM UTC it is. I'll send calendar invites with pre-read materials.

---

### 💬 即時訊息協作

**情境**：Slack 上的快速問題解決

**Developer**: Quick question - has anyone seen this error in the auth service? [screenshot]

**Senior Engineer**: That's usually a Redis connection issue. Check if the cluster is healthy.

**Developer**: Good catch! Pool is at 98% utilization. Restarted. Error rate dropped to zero.

---

### 🚀 緊急事件遠端協調

**情境**：緊急系統問題需要遠端團隊即時協調

**Incident Manager**: All hands - we have a Sev-1. Payment processing is down.

**DBA (remotely)**: I can see a long-running query blocking transactions. Killing it now... Done.

**On-call Engineer**: Confirmed - error rate is back to baseline.

**IM**: Great work. Let's schedule a postmortem for tomorrow.

---

## Mini Drills

1. **精簡訊息練習**：把 3 句話濃縮成 1 句 TL;DR
2. **時區排程**：給三個可行時段（含 UTC）
3. **寫一段交接訊息**：現狀、待處理、注意事項

---

## Quick Reference — 中英雙語卡

| English                                          | 中文                                  |
| ------------------------------------------------ | ------------------------------------- |
| Sharing context below; please comment by [date]. | 下方提供背景，請在[日期]前回覆。      |
| Vote with 👍/👎 by [deadline].                   | 請在[截至時間]前以 👍/👎 投票。       |
| Could we meet during the [X–Y] UTC overlap?      | 我們可否在 UTC [X–Y] 的重疊時段見面？ |
| Noted—I'll update the doc and circle back.       | 收到—我會更新文件再回覆。             |
| Let's keep mics muted unless speaking.           | 除非發言，請保持靜音。                |
| I'll leave notes for async handoff.              | 我會留筆記方便非同步交接。            |
