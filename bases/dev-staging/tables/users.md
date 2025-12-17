---
tags:
  - table
base: "[[bases/dev-staging/index|Dev/Staging]]"
table_id: tbl1r15vHh4nW3Xjo
---

# Users (Dev)

> Kullanıcılar - sadeleştirilmiş versiyon.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tbl1r15vHh4nW3Xjo` |
| Base | [[bases/dev-staging/index|Dev/Staging]] |

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | [[reference/field-types#singleLineText\|singleLineText]] | Ad |
| Email | [[reference/field-types#singleLineText\|singleLineText]] | E-posta |
| Notes | [[reference/field-types#multilineText\|multilineText]] | Notlar |
| Assignee | [[reference/field-types#singleCollaborator\|singleCollaborator]] | Atanan |
| Status | [[reference/field-types#singleSelect\|singleSelect]] | [[reference/status-workflows#Standard 3-State\|Todo/Progress/Done]] |
| Courses | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/dev-staging/tables/courses\|Courses]] |
| Progress | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/dev-staging/tables/progress\|Progress]] |
| Lessen | [[reference/field-types#lookup\|lookup]] | From Courses |

## 📌 Related

- [[bases/dev-staging/index|← Back to Dev/Staging]]
- [[bases/main-app/tables/users|Main App: Users]] - Full version