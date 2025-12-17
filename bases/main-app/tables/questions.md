---
tags:
  - table
  - has-formula
base: "[[bases/main-app/index|Main App]]"
table_id: tblwPF7NZ0y6Tjb9U
---

# Questions

> Quiz soruları.

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Number | formula | Task + Question combined |
| Task | multipleRecordLinks | → [[bases/main-app/tables/tasks\|Tasks]] |
| Question | singleLineText | Soru metni |
| Extra information | multilineText | İpucu/bağlam |
| Correct Answer | singleLineText | Doğru cevap |

## 📐 Formulas

### Formula: Number
```
{Task} & " " & {Question}
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/tasks|Tasks]]