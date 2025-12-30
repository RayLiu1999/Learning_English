# Software Engineering — 軟體工程日常英文大全

## Core Vocabulary

| 單字/片語           | 中文意思           | 常見搭配                                   |
| ------------------- | ------------------ | ------------------------------------------ |
| code review         | 程式碼審查         | request a review, review comments          |
| pull request (PR)   | 合併請求           | open/merge/close a PR                      |
| merge/rebase/squash | 合併/重整/壓縮提交 | merge conflicts, rebase onto main          |
| CI/CD               | 持續整合/部署      | pipeline, build, deploy                    |
| tests               | 測試               | unit/integration/e2e, flaky test, coverage |
| feature flag        | 功能開關           | roll out/roll back, canary, blue-green     |
| release             | 發佈               | release notes, hotfix, semantic versioning |
| API contract        | API 契約           | backward compatibility, deprecation        |
| tech debt           | 技術債             | pay down tech debt, refactor               |
| performance         | 效能               | regression, throughput, latency            |
| concurrency         | 併發               | race condition, deadlock, idempotent       |
| observability       | 可觀測性           | logs, metrics, traces                      |
| reliability         | 可靠度             | SLO/SLI/SLA, error budget                  |
| on-call             | 值班               | pager, rotation, handover                  |
| incident            | 事故               | mitigation, RCA, postmortem, rollback      |
| security            | 安全               | sanitize, validate input, least privilege  |
| scalability         | 可擴展性           | horizontal/vertical scaling, sharding      |

---

## Useful Patterns

### 站會更新（Yesterday/Today/Blockers）

- Yesterday I [completed X]. Today I'll [work on Y]. Blocked by [Z].
- No blockers on my side. I'll sync with [person] after standup.

### PR 描述（背景/變更/風險/測試/回滾）

- **Context**: …
- **Changes**: …
- **Risks**: …
- **Tests**: …
- **Rollback plan**: …

### 程式碼審查評論

- **Suggestion**: Consider … to improve readability.
- **Question**: What's the rationale behind …?
- **Blocking**: This can break [case]; propose [fix].
- **Nit**: Minor style issue, not blocking.

### 架構討論與取捨

- Trade-off between [simplicity] and [scalability]; I propose … because …
- Given [constraint], I recommend [approach].

### 估時與風險

- Estimate is [X days] given [scope/dependencies]; risks include …
- I'll need to spike this before giving a firm estimate.

### 事故溝通

- We're investigating a spike in errors; mitigated by rolling back to v1.2.
- Next update in 30 minutes.

### 交接與文件

- Handover: current status, known issues, runbooks, next steps.

---

## Context Examples

### PR 描述模板

- "Context: Users report timeouts on search. Changes: add caching layer with 5-min TTL. Risks: stale data. Tests: unit + load tests. Rollback: disable via feature flag."

### 審查評論

- "Nit: rename var to isAuthorized for clarity."
- "Could we add a test for empty payload?"

### Commit 訊息（Conventional Commits）

- "feat(search): add Redis cache to reduce latency"
- "fix(api): handle null user in auth middleware"

### 釋出公告（內部）

- "v2.3.0 includes rate limiting, expect slight 429 increase during ramp-up."

### Slack 事故更新

- "Mitigated by scaling read replicas; error rate down from 12%→0.5%."

---

## Dialogue Examples — 實際對話範例

### 🏃‍♂️ 站會對話

**情境**：敏捷開發團隊的每日同步會議

**Scrum Master**: Good morning team. Let's start with Alice.

**Alice (Backend Developer)**: Yesterday I finished the user authentication API. Today I'm working on the frontend integration. No blockers, but I'll need to sync with David on the token format.

**David (Frontend Developer)**: I can walk you through that after standup. The spec is in the PR description, but happy to clarify.

**Tom (QA Engineer)**: I'm writing integration tests for the payment flow. I'll need the staging environment updated with Alice's auth changes.

**Alice**: I'll deploy to staging right after this meeting.

---

### 🔍 PR 審查對話

**情境**：程式碼審查中的技術討論

**Author (Sarah)**: @reviewers, this PR adds caching for the search endpoint. PTAL when you have a chance.

**Reviewer (Mike)**: Looks good overall! Two questions: what's the cache TTL strategy, and have we considered the memory impact?

**Author**: Good catch—TTL is 5 minutes for search results, and I added memory monitoring. Updated the PR description with the metrics.

**Reviewer**: Perfect. LGTM after you add a unit test for the cache miss scenario.

**Author**: Will do. Should I also add a test for TTL expiration?

**Reviewer**: Yes, that would be comprehensive. Also consider testing concurrent cache writes.

---

### 🏗️ 架構討論

**情境**：技術選型會議討論系統設計

**Tech Lead (James)**: For the notification service, we're considering a queue-based approach vs real-time WebSockets.

**Engineer 1 (Alex)**: WebSockets give better UX, but queues are more reliable for high volume.

**Engineer 2 (Maya)**: What's our expected message volume?

**Tech Lead**: Peak is around 10K messages per minute. Given that, I'm leaning toward the queue with WebSocket updates for active users only.

**Engineer 1**: That hybrid approach makes sense. We could fall back to polling for inactive sessions.

**Engineer 2**: How do we handle connection failures with WebSockets?

**Tech Lead**: Good point. We'd need exponential backoff and circuit breakers.

---

### 🚨 生產事故處理

**情境**：緊急修復生產問題的快速協調

**On-call Engineer (Lisa)**: We have elevated 5xx errors on the checkout service. Started 5 minutes ago.

**Site Reliability Engineer (Dan)**: I see the spike. Database connections are maxed out. Could be a connection leak.

**Tech Lead**: Let's roll back the 2 PM deployment first to mitigate. How long to rollback?

**DevOps Engineer (Sam)**: 3 minutes if no DB schema changes. Checking now... no schema changes, we're good to rollback.

**Tech Lead**: Execute the rollback. Lisa, update the incident channel with status.

**Lisa**: Rollback in progress. I'll monitor error rates and update in 5 minutes.

---

## Mini Drills

1. **寫一段 5 行 PR 描述**（含風險與回滾）
2. **把一段模糊回饋改寫為可執行建議**（含理由）
3. **30 秒站會更新**（含阻礙與請求支援）
4. **寫 2 條 commit 訊息**（feat/fix 各一）

---

## Quick Reference — 中英雙語卡

| English                         | 中文                   |
| ------------------------------- | ---------------------- |
| Requesting a review on this PR. | 請幫忙審這個 PR。      |
| Context: … Changes: …           | 背景：… 變更：…        |
| Any blockers on your side?      | 你那邊有阻礙嗎？       |
| Rolling back via feature flag.  | 透過功能旗標回滾。     |
| Mitigated; monitoring errors.   | 已緩解；持續監控錯誤。 |
| LGTM, ship it!                  | 我看沒問題，上線吧！   |
| Could you add a test for this?  | 可以加個測試嗎？       |
| What's the rollback plan?       | 回滾計畫是什麼？       |
