# 📚 職場英文測驗系統

這個目錄包含職場英文各主題的測驗與學習追蹤。

## 📂 目錄結構

```
workplace-question/
├── README.md                    # 本說明文件
├── progress.md                  # 學習進度追蹤
├── mistakes.md                  # 錯誤片語/句型追蹤
├── meetings/                    # 會議主題
│   ├── quiz-001.md
│   └── ...
├── emails/                      # 電子郵件主題
│   └── ...
├── ... (其他主題資料夾)
└── mixed/                       # 混合測驗
    └── ...
```

---

## 🎯 測驗類型

### 類型 A：主題測驗

- 每個主題資料夾內的 `quiz-XXX.md`
- 每份約 30 題，涵蓋該主題的單字、片語、文法
- 適合深入學習特定情境

### 類型 B：混合測驗

- 在 `mixed/` 目錄內
- 每份約 20-25 題，跨多個主題
- 優先出錯誤率高的項目
- 適合綜合複習

---

## 🚀 使用流程

### Step 1: 選擇測驗

告訴 AI 你想做的測驗：

- 「我想做 meetings 測驗」→ 做 `meetings/quiz-001.md`
- 「產生混合測驗」→ AI 產生新的跨主題測驗

### Step 2: 作答並提交

做完後把答案貼給 AI：

```
meetings/quiz-001 答案：
1: B
2: C
3: B
...
```

### Step 3: 獲得批改結果

AI 會：

1. ✅ 批改答案，計算成績
2. 📊 更新 `progress.md` 學習進度
3. ❌ 更新 `mistakes.md` 錯誤追蹤
4. 📝 在測驗檔案中加入作答紀錄

---

## 📋 19 個主題清單

| 編號 | 主題       | 資料夾                    |
| ---- | ---------- | ------------------------- |
| 1    | 會議       | `meetings/`               |
| 2    | 電子郵件   | `emails/`                 |
| 3    | 簡報       | `presentations/`          |
| 4    | 電話與視訊 | `phone-video-calls/`      |
| 5    | 遠端溝通   | `remote-communication/`   |
| 6    | 面試       | `interviews/`             |
| 7    | 績效回饋   | `performance-feedback/`   |
| 8    | 談判協商   | `negotiations/`           |
| 9    | 團隊合作   | `team-collaboration/`     |
| 10   | 客訴客服   | `customer-support/`       |
| 11   | 銷售會議   | `sales-client-meetings/`  |
| 12   | 小寒暄文化 | `small-talk-and-culture/` |
| 13   | 專案管理   | `project-management/`     |
| 14   | 時間管理   | `time-management/`        |
| 15   | 報告撰寫   | `reports-writing/`        |
| 16   | 訂單合約   | `orders-and-contracts/`   |
| 17   | 軟體工程   | `software-engineering/`   |
| 18   | 程式碼審查 | `code-review/`            |
| 19   | 事故管理   | `incident-management/`    |

---

## 📊 追蹤項目

### progress.md 追蹤

- 各主題測驗次數與正確率
- 各題型（單字/片語/文法）表現
- 整體學習進度

### mistakes.md 追蹤

- 錯誤的單字/片語/句型
- 錯誤次數與正確率
- 常見混淆組合
- 記憶技巧
