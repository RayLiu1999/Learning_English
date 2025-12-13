# Code Review — 程式碼審查英文大全

## Core Vocabulary
- LGTM/Request changes 看起來可/請修改
- nit 小問題/風格：nitpick
- blocking 阻擋合併：blocking comment
- suggestion 建議：apply suggestion
- readability 可讀性：self-documenting, naming
- maintainability 可維護性：coupling, cohesion
- performance 效能：time/space complexity, hot path
- security 安全：injection, XSS, SSRF, sanitize/validate
- testing 測試：edge case, negative case, flaky
- docs 文件：inline docs, README, ADR

## Useful Patterns
- 提問：
  - Could you clarify how this handles [edge case]?
  - What's the trade-off of choosing [approach A] over [B]?
- 建議：
  - Consider extracting this into a helper to reduce duplication.
  - Suggest renaming to [betterName] for clarity.
- 阻擋：
  - This can cause a race condition; please guard with a lock or make it idempotent.
  - Missing input validation; this is blocking.
- 作者回覆：
  - Thanks—addressed in 4c2d1f; added tests for empty payload.
  - I kept the current approach due to [constraint]; added a comment and TODO.

## Context Examples
- Reviewer：
  - "Mind adding a unit test for zero-length input?"
  - "This loop is O(n^2); could we pre-index by id?"
- Author：oi
  - "Refactored per feedback; PTAL."
  - "Split into two commits: behavior change and refactor."

## Dialogue Examples — 實際對話範例

### 💬 程式碼審查討論
**情境**：在GitHub PR中進行代碼審查

**Senior Developer (Alex)**: Thanks for the PR! Overall structure looks good. I have a few questions about the error handling approach.

**Junior Developer (Sam)**: Sure! I was wondering about that too. Should I be using custom exceptions here?

**Alex**: For this case, I think the standard ValidationError would be sufficient. Also, line 45 - could we extract this logic into a helper method?

**Sam**: Good point. The method is getting long. I'll refactor it into smaller functions.

**Alex**: Perfect. One more thing - could you add unit tests for the edge cases we discussed?

**Sam**: Absolutely. I'll add tests for empty input and invalid date formats.

### 🔍 設計模式討論
**情境**：討論代碼架構和設計選擇

**Tech Lead**: I noticed you're using a singleton pattern here. What's the reasoning?

**Developer**: I wanted to ensure we only have one instance of the cache manager across the application.

**Tech Lead**: I see the intent, but singletons can make testing difficult. Have you considered dependency injection?

**Developer**: I haven't tried that approach yet. Could you show me how that would work?

**Tech Lead**: Sure, I'll add some inline comments with an example. It'll make the code more testable and flexible.

**Developer**: That sounds better. I'll refactor it and update the tests accordingly.

### 🐛 程式碼品質改進
**情境**：討論代碼質量和最佳實踐

**Code Reviewer**: The functionality works well, but I see some opportunities for improvement.

**Author**: I'm open to feedback. What did you notice?

**Code Reviewer**: The variable names could be more descriptive. For example, 'data' doesn't tell us much about what it contains.

**Author**: You're right. I should rename it to something like 'userProfileData'. Any other suggestions?

**Code Reviewer**: Yes, and consider breaking this 50-line function into smaller, focused functions. It'll be easier to test and maintain.

**Author**: Makes sense. I'll split it into validation, processing, and formatting functions.

### 🚀 效能最佳化討論
**情境**：檢討程式碼效能和改進建議

**Performance Engineer**: I ran some benchmarks on your code. The algorithm works correctly, but we might hit scaling issues.

**Developer**: What's the main bottleneck?

**Performance Engineer**: The nested loops in the data processing section. With large datasets, it's O(n²) complexity.

**Developer**: Could we optimize it to O(n log n) by using a different data structure?

**Performance Engineer**: Exactly! A hash map would reduce lookups from linear to constant time.

**Developer**: I'll implement that change and add performance tests to catch regressions.

### 📋 審查清單檢查
**情境**：確保代碼符合團隊標準

**Team Lead**: Let's go through our review checklist. Does this code follow our naming conventions?

**Reviewer**: Yes, all functions and variables use camelCase as specified in our style guide.

**Team Lead**: How about error handling and logging?

**Reviewer**: Good coverage. All exceptions are properly caught and logged with appropriate levels.

**Team Lead**: Security considerations?

**Reviewer**: Input validation is present, and no sensitive data is logged. Looks secure.

**Team Lead**: Documentation?

**Reviewer**: All public methods have JSDoc comments. The README is updated with the new API endpoints.

### 🎯 架構決策討論
**情境**：評估大型功能的架構選擇

**Senior Architect**: This is a significant change to our data layer. Let's discuss the architectural implications.

**Feature Developer**: I chose this approach because it simplifies the API interface and reduces database calls.

**Architect**: I appreciate the performance consideration. How does this affect our existing caching strategy?

**Developer**: I think we'll need to update the cache invalidation logic. Currently, it assumes single-table updates.

**Architect**: That's a good point. Could you document the cache implications and create tickets for the necessary updates?

**Developer**: Sure. I'll also add integration tests to verify the caching behavior works correctly.

### 🔄 重構建議與討論
**情境**：建議重構現有代碼以提高可維護性

**Staff Engineer**: The feature works well, but I think we can improve the long-term maintainability.

**Developer**: What specific areas concern you?

**Staff Engineer**: The business logic is mixed with data access code. Consider implementing the repository pattern.

**Developer**: That would separate concerns better. Should I do that refactoring in this PR or create a follow-up?

**Staff Engineer**: Let's keep this PR focused on the feature. Create a tech debt ticket for the refactoring.

**Developer**: Good approach. I'll add TODO comments noting the areas that need refactoring and link to the ticket.

## Mini Drills
- 把模糊評論（如：不太好）改成具體可行的審查意見。
- 為一段易錯邏輯設計 2 個邊界測試案例。

## Quick Reference — 中英雙語卡
- Could you clarify this part? 這段可以再說明一下嗎？
- Suggest extracting into a helper. 建議抽成共用函式。
- This is blocking due to [reason]. 因為[原因]，這是阻擋項。
- PTAL. 請過目。
- Addressed in the latest commit. 已在最新提交修正。
