---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblSyEAVZAYExNBSu
---

# Tasks

> Öğrenme aktiviteleri ve görevler.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblSyEAVZAYExNBSu` |
| Base | [[bases/main-app/index|Main App]] |

## 📊 Fields

### Content

| Field | Type | Description |
|-------|------|-------------|
| Name | [[reference/field-types#multilineText\|multilineText]] | Task description |
| Introduction | [[reference/field-types#multilineText\|multilineText]] | Giriş |
| Notes | [[reference/field-types#multilineText\|multilineText]] | Ek notlar |
| Module_icon | [[reference/field-types#multipleAttachments\|multipleAttachments]] | İkon |
| Video | [[reference/field-types#multipleAttachments\|multipleAttachments]] | Video |
| Bijlage | [[reference/field-types#multipleAttachments\|multipleAttachments]] | Ekler |

### Module Types

| Field | Type |
|-------|------|
| Module_Dialoog | singleLineText |
| Module_Speaking | singleLineText |
| Module_Conversation | singleLineText |

### Status

| Field | Type | Description |
|-------|------|-------------|
| Status | [[reference/field-types#singleSelect\|singleSelect]] | [[reference/status-workflows#Standard 3-State\|Todo/Progress/Done]] |
| Teacher Check | [[reference/field-types#checkbox\|checkbox]] | Öğretmen kontrolü |
| ID | [[reference/field-types#autoNumber\|autoNumber]] | Auto ID |

### URLs

| Field | Type |
|-------|------|
| Test Url | url |
| Flashcard url | url |

### Links

| Field | Type | Links To |
|-------|------|----------|
| Lesson | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/lessons\|Lessons]] |
| Progress | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/task-progress\|Task Progress]] |
| Questions | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/questions\|Questions]] |

### Lookups

| Field | Source |
|-------|--------|
| Module ID -> Lesson | Lessons.Module ID |
| Course (from Lesson) | Lessons.Course |

## 🔗 Relationships

```
┌──────────┐
│ Lessons  │
└────┬─────┘
     │ 1:N
     ▼
┌──────────┐
│  TASKS   │ ◄── You are here
└────┬─────┘
     │
     ├─────────┐
     ▼         ▼
┌────────┐ ┌───────────┐
│Progress│ │ Questions │
└────────┘ └───────────┘
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/lessons|Lessons]]
- [[bases/main-app/tables/task-progress|Task Progress]]
- [[bases/main-app/tables/questions|Questions]]