---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblzuVXq93AxyJvne
---

# Messages

> Chat mesajları.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblzuVXq93AxyJvne` |
| Base | [[bases/main-app/index|Main App]] |

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Message | [[reference/field-types#singleLineText\|singleLineText]] | Mesaj içeriği |
| Chats | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/chats\|Chats]] |
| Direction | [[reference/field-types#singleSelect\|singleSelect]] | [[#Direction Options\|Yön]] |
| Attachment | [[reference/field-types#multipleAttachments\|multipleAttachments]] | Ekler |
| Timestamp | [[reference/field-types#createdTime\|createdTime]] | Zaman damgası |

### Direction Options

| Option | Meaning |
|--------|--------|
| Outbound | Öğretmenden öğrenciye |
| Inbound | Öğrenciden öğretmene |

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/chats|Chats]]