---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblfGcMDhdUQux6KH
---

# Task Progress

> Kullanıcı görev ilerlemesi.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblfGcMDhdUQux6KH` |
| Base | [[bases/main-app/index|Main App]] |

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Notes | multilineText | Notlar |
| Finished | checkbox | Tamamlandı mı |
| Finished time | lastModifiedTime | Tamamlanma zamanı |
| Users | multipleRecordLinks | → [[bases/main-app/tables/users\|Users]] |
| Task | multipleRecordLinks | → [[bases/main-app/tables/tasks\|Tasks]] |
| Name (from Lessons) | lookup | Ders adı |
| Les notitie | lookup | Ders notu |
| Clients (from Users) | lookup | Müşteri |

## 🔄 Workflow

```
┌────────┐     ┌────────┐     ┌───────────────┐
│  User  │ + │  Task  │  =  │ TASK PROGRESS │
└────────┘     └────────┘     └───────────────┘
                                  │
                          ┌───────┴───────┐
                          │ Finished      │
                          │ Finished time │
                          │ Notes         │
                          └───────────────┘
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/users|Users]]
- [[bases/main-app/tables/tasks|Tasks]]
- [[reference/patterns#Progress Tracking Pattern|Progress Pattern]]