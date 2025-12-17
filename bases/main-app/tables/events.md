---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblhnBw7Q8sR3RRB1
---

# Events

> Zamanlanmış etkinlikler/dersler.

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | singleLineText | Etkinlik adı |
| Date | dateTime | Başlangıç |
| Endtime | dateTime | Bitiş |
| Location | singleLineText | Lokasyon |
| Course | multipleRecordLinks | → [[bases/main-app/tables/courses\|Courses]] |
| Open Lesson | url | Ders linki |
| Status | singleSelect | [[reference/status-workflows#Online/Offline Toggle\|Online/Offline]] |
| Email (from Linked Users) | lookup | Katılımcı emailleri |
| Online Meeting url | url | Video call linki |
| Attachment | multipleAttachments | Ekler |

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/courses|Courses]]