---
tags:
  - table
  - has-ai
  - field-type/aiText
base: "[[bases/main-app/index|Main App]]"
table_id: tblyBQSYVCDJTb6Ij
---

# WRITING_TESTS

> Yazılı testler - 🤖 AI-powered Dutch correction.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tblyBQSYVCDJTb6Ij` |
| Base | [[bases/main-app/index|Main App]] |
| AI Fields | ✅ AI assist |

## 📊 Fields

### Input

| Field | Type | Description |
|-------|------|-------------|
| Input | [[reference/field-types#multilineText\|multilineText]] | Öğrenci yazısı |
| Exercise | [[reference/field-types#singleLineText\|singleLineText]] | Egzersiz ID |
| lesson_Id | [[reference/field-types#singleLineText\|singleLineText]] | Ders ID |

### AI Processing

| Field | Type | Description |
|-------|------|-------------|
| AI assist | [[reference/field-types#aiText\|aiText]] | 🤖 [[#AI: Dutch Correction]] |

### Links

| Field | Type | Links To |
|-------|------|----------|
| User | [[reference/field-types#singleLineText\|singleLineText]] | Legacy |
| User_ | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/users\|Users]] |
| Chats | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | [[bases/main-app/tables/chats\|Chats]] |
| Course_enrollment | [[reference/field-types#lookup\|lookup]] | From User_ |

### Metadata

| Field | Type |
|-------|------|
| Created By | createdBy |

## 🤖 AI: Dutch Correction

**Field:** `AI assist`

**Prompt:**
```
Please provide the correct dutch way in spelling and writing 
of this value in this field. "{Input}" 

Firstly provide the old version, then the corrected version, 
then point out positive feedback, provide overview of errors.

Keep in mind level of the student is in the course name: {Course_enrollment}

Refer to the student as 'you'. 
Please reply in english except for explicit dutch words and texts.

Only correct students to use u to refer to a person when the 
sentence contains meneer or mevrouw, otherwise the student 
can choose to refer to a person using je or u.

Use the term feedback instead of positive feedback.
```

**Referenced Fields:**
- Input (student's text)
- Course_enrollment (student level context)

**Output Structure:**
1. Old version
2. Corrected version
3. Feedback (positive points)
4. Error overview

## 🔄 Workflow

```
┌───────────────┐
│ Student Input │  Öğrenci yazısını girer
└───────┬───────┘
        │
        ▼
┌───────────────┐
│   AI assist   │  Otomatik düzeltme + feedback
└───────┬───────┘
        │
        ▼
┌───────────────┐
│    Chats      │  Öğretmen ile tartışma
└───────────────┘
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/users|Users]]
- [[bases/main-app/tables/chats|Chats]]
- [[reference/patterns#AI Feedback Pattern|AI Pattern]]
- [[reference/field-types#aiText|aiText Field Type]]