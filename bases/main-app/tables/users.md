---
tags:
  - table
  - has-formula
  - field-type/multipleRecordLinks
base: "[[bases/main-app/index|Main App]]"
table_id: tbl1r15vHh4nW3Xjo
---

# Users

> Kullanıcı hesapları ve profilleri.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tbl1r15vHh4nW3Xjo` |
| Base | [[bases/main-app/index|Main App]] |
| Views | 4 |

## 📊 Fields

### Identity

| Field | Type | Description |
|-------|------|-------------|
| Email | [[reference/field-types#singleLineText\|singleLineText]] | Primary identifier |
| Name | [[reference/field-types#singleLineText\|singleLineText]] | Display name |
| Notes | [[reference/field-types#multilineText\|multilineText]] | Notlar |
| Magic link | [[reference/field-types#url\|url]] | Auth link |

### Status

| Field | Type | Description |
|-------|------|-------------|
| Assignee | [[reference/field-types#singleCollaborator\|singleCollaborator]] | Atanan kişi |
| Status | [[reference/field-types#singleSelect\|singleSelect]] | [[reference/status-workflows#Standard 3-State\|Todo/Progress/Done]] |

### Course Links

| Field | Type | Links To |
|-------|------|----------|
| Courses | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/courses\|Courses]] |
| Course_enrollment | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/course-enrollment\|Course_enrollment]] |
| Lessen | [[reference/field-types#lookup\|lookup]] | From Courses |
| Startdate | [[reference/field-types#lookup\|lookup]] | From Course_enrollment |
| Closedate | [[reference/field-types#lookup\|lookup]] | From Course_enrollment |
| Teacher | [[reference/field-types#lookup\|lookup]] | From Course_enrollment |
| Current Lesson Week | [[reference/field-types#formula\|formula]] | [[#Formula: Current Week]] |

### Progress & Tests

| Field | Type | Links To |
|-------|------|----------|
| Progress | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/task-progress\|Task Progress]] |
| Questions Progress | [[reference/field-types#singleLineText\|singleLineText]] | - |
| WRITING_TESTS 2 | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/writing-tests\|WRITING_TESTS]] |
| AUDIO_TESTS | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/audio-tests\|AUDIO_TESTS]] |
| MTP_TESTS | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/mtp-tests\|MTP_TESTS]] |
| Aantal Writing tests | [[reference/field-types#count\|count]] | Writing test sayısı |
| Aantal Audio tests | [[reference/field-types#count\|count]] | Audio test sayısı |

### Organization

| Field | Type | Links To |
|-------|------|----------|
| Clients | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/clients\|Clients]] |
| Chats | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/chats\|Chats]] |
| User Groups | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/user-groups\|User Groups]] |
| Certificates | [[reference/field-types#multipleAttachments\|multipleAttachments]] | Sertifikalar |

## 📐 Formulas

### Formula: Current Week

```
(DATETIME_DIFF({Startdate}, TODAY(), 'weeks')) + 1
```

Başlangıçtan bu yana kaçıncı hafta.

## 👁️ Views

| View | Purpose |
|------|--------|
| Grid view | Default |
| All current A1 Part 1 | A1 Part 1 öğrencileri |
| Current A1 part 1 Jamila | Jamila'ın öğrencileri |
| Current A1 part 1 Anne E. | Anne E.'ın öğrencileri |

## 🔗 Relationships

```
┌───────────┐
│  Clients  │
└─────┬─────┘
      │
      ▼
┌─────────────────────────────────┐
│              USERS               │ ◄── You are here
└┬──────┬──────┬──────┬──────┬──────┬┘
 │      │      │      │      │      │
 ▼      ▼      ▼      ▼      ▼      ▼
Courses Chats Writing Audio MTP  Groups
              Tests  Tests Tests
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/courses|Courses]]
- [[bases/main-app/tables/chats|Chats]]
- [[bases/main-app/tables/writing-tests|WRITING_TESTS]]