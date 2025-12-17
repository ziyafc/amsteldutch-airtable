---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblBfmTN20XWC4sU3
---

# Chats

> Sohbet/destek sistemi.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblBfmTN20XWC4sU3` |
| Base | [[bases/main-app/index|Main App]] |

## 📊 Fields

### Core

| Field | Type | Description |
|-------|------|-------------|
| Subject | [[reference/field-types#singleLineText\|singleLineText]] | Konu |
| Status | [[reference/field-types#singleSelect\|singleSelect]] | [[#Chat Status\|Durum]] |
| Score | [[reference/field-types#rating\|rating]] | 1-10 puan |
| Personal Advise | [[reference/field-types#singleLineText\|singleLineText]] | Kişisel tavsiye |
| Created Time | [[reference/field-types#createdTime\|createdTime]] | Oluşturulma |
| Attachments | [[reference/field-types#multipleAttachments\|multipleAttachments]] | Ekler |

### Links

| Field | Type | Links To |
|-------|------|----------|
| Users | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/users\|Users]] |
| Messages | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/messages\|Messages]] |
| WRITING_TESTS | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/writing-tests\|WRITING_TESTS]] |
| AUDIO_TESTS | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/audio-tests\|AUDIO_TESTS]] |
| Teacher | [[reference/field-types#lookup\|lookup]] | From Users |

### Chat Status

Bkz: [[reference/status-workflows#Chat/Support Workflow]]

| Option | Color | Meaning |
|--------|-------|--------|
| Submitted | 🟠 Orange | Yeni |
| Processing Internally | 🔵 Cyan | İşleniyor |
| Responded | 🟢 Green | Yanıtlandı |
| Archived | 🟣 Purple | Arşivlendi |

## 🔗 Relationships

```
┌─────────┐
│  Users  │
└────┬────┘
     │
     ▼
┌─────────┐
│  CHATS  │ ◄── You are here
└────┬────┘
     │
     ├───────────────┐
     ▼         ▼         ▼
┌────────┐┌────────┐┌────────┐
│Messages││WRITING ││ AUDIO  │
└────────┘│ TESTS  ││ TESTS  │
         └────────┘└────────┘
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/messages|Messages]]
- [[bases/main-app/tables/users|Users]]
- [[reference/patterns#Chat/Messaging Pattern|Chat Pattern]]