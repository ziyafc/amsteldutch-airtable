---
tags:
  - table
  - junction-table
  - has-formula
base: "[[bases/main-app/index|Main App]]"
table_id: tbl8XWGbHeT6JoVIM
---

# Course_enrollment

> Junction table: Users ↔ Courses.

## 📋 Table Info

| Property | Value |
|----------|-------|
| Table ID | `tbl8XWGbHeT6JoVIM` |
| Base | [[bases/main-app/index|Main App]] |
| Type | Junction Table |

## 📊 Fields

| Field | Type | Description |
|-------|------|-------------|
| Name | [[reference/field-types#formula\|formula]] | User + Course combined |
| User | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/users\|Users]] |
| Course | [[reference/field-types#multipleRecordLinks\|multipleRecordLinks]] | → [[bases/main-app/tables/courses\|Courses]] |
| Startdate | [[reference/field-types#date\|date]] | Başlangıç |
| Closedate | [[reference/field-types#date\|date]] | Bitiş |
| Email (from User) | [[reference/field-types#lookup\|lookup]] | User email |
| Teacher | [[reference/field-types#singleSelect\|singleSelect]] | [[#Teachers]] |

### Teachers

| Option |
|--------|
| Jamila |
| Anne E |
| Annemijn |
| Anne V |
| Elsa |
| Roxane |
| Ella |
| Wesley |
| Catalina |
| Luis |
| Kelly |

## 📐 Formulas

### Formula: Name

```
{User} & " " & {Course}
```

## 📌 Related

- [[bases/main-app/index|← Back to Main App]]
- [[bases/main-app/tables/users|Users]]
- [[bases/main-app/tables/courses|Courses]]
- [[reference/patterns#User-Course Enrollment Pattern|Enrollment Pattern]]