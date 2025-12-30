---
description: Project-wide rules for commits, file organization, and AI assistant behavior
---

# Project Rules

This document defines project-wide rules that the AI assistant must follow.

---

## 📝 Commit Rules

### Commit Message Format

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Types

| Type       | Description                                  |
| ---------- | -------------------------------------------- |
| `feat`     | A new feature or content                     |
| `fix`      | A bug fix or correction                      |
| `docs`     | Documentation changes                        |
| `style`    | Formatting, no code change                   |
| `refactor` | Code restructuring without changing behavior |
| `test`     | Adding or updating tests/quizzes             |
| `chore`    | Maintenance tasks                            |

### Scopes

| Scope            | Description                          |
| ---------------- | ------------------------------------ |
| `vocabulary`     | Vocabulary quiz system               |
| `workplace`      | Workplace English learning materials |
| `workplace-quiz` | Workplace English quiz system        |
| `config`         | Configuration and workflow files     |

### Examples

```
feat(vocabulary): add quiz-002 with 25 questions
fix(vocabulary): correct answer for Q14 in quiz-001
docs(workplace): update meetings.md with new patterns
test(workplace-quiz): complete interviews quiz with 87% score
refactor(config): restructure workplace-question folders
chore: update README with new project structure
```

### When to Commit

1. After creating a new quiz
2. After grading a quiz and updating progress/mistakes
3. After adding new vocabulary words
4. After restructuring files or folders
5. After updating documentation

---

## 📂 File Organization Rules

### Naming Conventions

| Item          | Convention               | Example        |
| ------------- | ------------------------ | -------------- |
| Quiz files    | `quiz-XXX.md` (3 digits) | `quiz-001.md`  |
| Mixed quizzes | `mixed-XXX.md`           | `mixed-001.md` |
| Topic folders | lowercase with hyphens   | `code-review/` |

### File Locations

| Content            | Location                      |
| ------------------ | ----------------------------- |
| Vocabulary words   | `vocabulary/words.md`         |
| Vocabulary quizzes | `vocabulary/quizzes/`         |
| Workplace quizzes  | `workplace-question/[topic]/` |
| Mixed quizzes      | `workplace-question/mixed/`   |
| Workflows          | `.agent/workflows/`           |

---

## 🤖 AI Assistant Behavior

### Language Rules

| Context                           | Language             |
| --------------------------------- | -------------------- |
| Commit messages                   | English              |
| Quiz questions                    | English (全英文題目) |
| Explanations to user              | Chinese (中文說明)   |
| File content (learning materials) | Mixed (中英對照)     |

### After Grading a Quiz

1. Display results to user
2. Update the quiz file with answer record
3. Update `progress.md`
4. Update `mistakes.md`
5. Commit changes with appropriate message

### After Adding New Words

1. Update `vocabulary/words.md`
2. Update word count in summary section
3. Commit changes

---

## 📊 Progress Tracking Rules

### Status Indicators

| Symbol | Meaning                      |
| ------ | ---------------------------- |
| ⬜     | Not started / Not tested     |
| 🟡     | In progress (accuracy < 85%) |
| 🟢     | Mastered (accuracy ≥ 85%)    |
| ✅     | Tested                       |
| ❌     | Wrong answer                 |

### Priority Levels (Vocabulary)

| Level | Description     | Quiz Priority                       |
| ----- | --------------- | ----------------------------------- |
| 5     | Core vocabulary | Highest - must appear in every quiz |
| 4     | Important       | High - frequent appearance          |
| 3     | Useful          | Medium                              |
| 2     | Supplementary   | Low                                 |
| 1     | Extra           | Occasional                          |
