---
tags:
  - table
base: "[[bases/main-app/index|Main App]]"
table_id: tblBH8VGXZ4wGKXpH
---

# Lessons

> Ders modülleri - çoklu dil desteği ile.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblBH8VGXZ4wGKXpH` |
| Base | [[bases/main-app/index|Main App]] |

## 📊 Fields

### Content

| Field | Type | Description |
|-------|------|-------------|
| Name | [[reference/field-types#singleLineText\|singleLineText]] | English name |
| Naam | [[reference/field-types#singleLineText\|singleLineText]] | Dutch name |
| Notes | [[reference/field-types#multilineText\|multilineText]] | English notes |
| Notitie | [[reference/field-types#multilineText\|multilineText]] | Dutch notes |
| Video | [[reference/field-types#multipleAttachments\|multipleAttachments]] | Lesson video |

### Metadata

| Field | Type | Description |
|-------|------|-------------|
| Creator | [[reference/field-types#singleCollaborator\|singleCollaborator]] | Oluşturan |
| Status | [[reference/field-types#singleSelect\|singleSelect]] | [[reference/status-workflows#Standard 3-State\|Todo/Progress/Done]] |
| Module ID | [[reference/field-types#autoNumber\|autoNumber]] | Auto ID |
| Lesson_Id | [[reference/field-types#autoNumber\|autoNumber]] | Auto ID |

### Exercise URLs

| Field | Type | Description |
|-------|------|-------------|
| writing_url | [[reference/field-types#url\|url]] | Yazı egzersizi |
| speaking_url | [[reference/field-types#url\|url]] | Konuşma egzersizi |
| reading_url | [[reference/field-types#url\|url]] | Okuma egzersizi |
| dialogue_url | [[reference/field-types#url\|url]] | Diyalog egzersizi |

### Audio Files (Google Drive)

| Field | Type |
|-------|------|
| Speak_Audio_url_1_GoogleDrive | url |
| Speak_Audio_url_2_GoogleDrive | url |
| Speak_Audio_url_3_GoogleDrive | url |
| Speak_Audio_Text_1 | multilineText |
| Speak_Audio_Text_2 | multilineText |
| Speak_Audio_Text_3 | multilineText |

### Links

| Field | Type | Links To |
|-------|------|----------|
| Course | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/courses\|Courses]] |
| Task | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/tasks\|Tasks]] |

## 🔗 Relationships

```
┌─────────┐
│ Courses │
└────┬────┘
     │ 1:N
     ▼
┌───────────┐
│  LESSONS  │ ◄── You are here
└────┬──────┘
     │ 1:N
     ▼
┌─────────┐
│  Tasks  │
└─────────┘
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/courses|Courses]]
- [[bases/main-app/tables/tasks|Tasks]]
- [[reference/patterns#Hierarchical Content Pattern|Content Pattern]]