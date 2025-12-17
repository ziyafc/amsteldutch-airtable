---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblx0byituDy8t15y
---

# AUDIO_TESTS

> Sesli/konuşma testleri.

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | singleLineText | Test adı |
| Status | singleSelect | Todo/In progress/Done |
| T1 | multipleAttachments | Öğretmen ses 1 |
| S1 | multipleAttachments | Öğrenci ses 1 |
| A1 | url | Audio URL |
| Lesson | singleLineText | Ders |
| lesson_Id | singleLineText | Ders ID |
| User_ | singleLineText | Legacy |
| User | multipleRecordLinks | → [[bases/main-app/tables/users\|Users]] |
| Chats | multipleRecordLinks | → [[bases/main-app/tables/chats\|Chats]] |

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/users|Users]]
- [[bases/main-app/tables/chats|Chats]]