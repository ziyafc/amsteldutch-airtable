---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblmSLMsyy2GxPVO7
---

# Courses

> Kurs kataloğu.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblmSLMsyy2GxPVO7` |
| Base | [[bases/main-app/index|Main App]] |

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | [[reference/field-types#singleLineText\|singleLineText]] | Kurs adı |
| Notes | [[reference/field-types#multilineText\|multilineText]] | Notlar |
| Teacher | [[reference/field-types#singleCollaborator\|singleCollaborator]] | Eğitmen |
| Status | [[reference/field-types#singleSelect\|singleSelect]] | [[reference/status-workflows#Online/Offline Toggle\|Online/Offline]] |
| Linked Users | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/users\|Users]] |
| Lessons | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/lessons\|Lessons]] |
| Course_enrollment | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/course-enrollment\|Course_enrollment]] |
| Events | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/events\|Events]] |

## 🔗 Relationships

| Linked To | Relationship |
|-----------|-------------|
| [[bases/main-app/tables/users\|Users]] | Many-to-many |
| [[bases/main-app/tables/lessons\|Lessons]] | One-to-many |
| [[bases/main-app/tables/course-enrollment\|Course_enrollment]] | One-to-many |
| [[bases/main-app/tables/events\|Events]] | One-to-many |

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/lessons|Lessons]]
- [[reference/patterns#Hierarchical Content Pattern|Content Pattern]]