---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblBBkQKTtgV7zX8q
---

# Activities

> Grup aktiviteleri ve etkinlikler.

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | singleLineText | Aktivite adı |
| Datum en tijd | dateTime | Tarih ve saat |
| Notes | multilineText | Notlar |
| Attachments | multipleAttachments | Ekler |
| Location | singleLineText | Lokasyon |
| Group Specific Activity | multipleRecordLinks | → [[bases/main-app/tables/user-groups\|User Groups]] |
| Users (from Group...) | lookup | Kullanıcılar |
| More info link | url | Detay linki |

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/user-groups|User Groups]]