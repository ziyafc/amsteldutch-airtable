# Expat Student Course Management

**Base ID:** `appAe8WSfkPmp8P8I`  
**Permission Level:** Create

## Overview

Comprehensive student enrollment and course management system for expat education programs.

---

## Tables

### 1. Courses

**Table ID:** `tbllHRWQNJvVjdsbW`

| Field Name | Type | Description |
|------------|------|-------------|
| Course Name | `singleLineText` | Course title |
| Course Level | `singleSelect` | Beginner, Intermediate, Advanced |
| Course Photo | `multipleAttachments` | Visual assets |
| Total Enrollments | `count` | Auto-calculated from Enrollments |
| Enrollments | `multipleRecordLinks` | → Enrollments table |
| Course Summary | `aiText` | AI-generated course summary |
| Suggested Improvement | `aiText` | AI-generated improvement suggestions |
| Students | `multipleRecordLinks` | → Students table |
| lessons | `singleLineText` | Lesson info |
| Assessments | `multipleRecordLinks` | → Assessments table |

---

### 2. Students

**Table ID:** `tblqLbVNQQbE05gU4`

| Field Name | Type | Description |
|------------|------|-------------|
| Student ID | `singleLineText` | Unique identifier |
| First Name | `singleLineText` | - |
| Last Name | `singleLineText` | - |
| Date of Birth | `date` | - |
| Email Address | `singleLineText` | - |
| Phone Number | `singleLineText` | - |
| Profile Photo | `multipleAttachments` | - |
| Nationality | `singleLineText` | - |
| Enrollment Date | `date` | - |
| Courses Enrolled | `multipleRecordLinks` | → Courses |
| Enrollment Records | `multipleRecordLinks` | → Enrollments |
| Full Name | `formula` | `{First Name} & ' ' & {Last Name}` |
| Age | `formula` | `DATETIME_DIFF(TODAY(), {Date of Birth}, 'years')` |
| Total Courses Enrolled | `count` | - |
| Current Progress | `rollup` | From Enrollment Records |
| Assessments | `multipleRecordLinks` | → Assessments |

---

### 3. Enrollments

**Table ID:** `tbl3LE5BoyxQ60WkA`

| Field Name | Type | Description |
|------------|------|-------------|
| Enrollment ID | `singleLineText` | - |
| Student | `multipleRecordLinks` | → Students |
| Course | `multipleRecordLinks` | → Courses |
| Enrollment Date | `date` | - |
| Progress | `number` | 0-100 |
| Completion Status | `singleSelect` | Not Started, In Progress, Completed |
| Schedule | `multipleRecordLinks` | → Schedules |
| Student Name | `lookup` | From Student |
| Course Name | `lookup` | From Course |
| Progress Percentage | `formula` | `{Progress} * 100` |
| Days Since Enrollment | `formula` | `DATETIME_DIFF(TODAY(), {Enrollment Date}, 'days')` |
| Is Completed | `formula` | Boolean based on status |

---

### 4. Schedules

**Table ID:** `tbl1ADP4zZllvOkBj`

| Field Name | Type | Description |
|------------|------|-------------|
| Start Time | `singleLineText` | - |
| Instructor | `multipleRecordLinks` | → Instructors |
| Session Date | `date` | - |
| Course | `singleLineText` | - |
| End Time | `singleLineText` | - |
| Location | `singleLineText` | - |
| Session Type | `singleSelect` | Lecture, Workshop, Seminar |
| Course Name | `lookup` | - |
| Instructor Name | `lookup` | From Instructor |
| Session Duration | `formula` | Minutes between start/end |
| Number of Enrollments | `count` | - |
| Enrollments | `multipleRecordLinks` | → Enrollments |
| Session Status | `formula` | Completed/Upcoming based on date |

---

### 5. Instructors

**Table ID:** `tblber3wEWGjCNdU6`

| Field Name | Type | Description |
|------------|------|-------------|
| Instructor Name | `singleLineText` | - |
| Photo | `multipleAttachments` | - |
| Qualifications | `multilineText` | - |
| Email | `singleLineText` | - |
| Phone Number | `singleLineText` | - |
| Assigned Courses | `singleLineText` | - |
| Total Courses Assigned | `count` | - |
| Average Course Level | `rollup` | - |
| Upcoming Sessions | `rollup` | Session dates |
| Schedules | `multipleRecordLinks` | → Schedules |
| Contact Info | `formula` | Email / Phone combined |

---

### 6. Assessments

**Table ID:** `tbloZt35vRi7Q5ZUu`

| Field Name | Type | Description |
|------------|------|-------------|
| Assessment ID | `singleLineText` | - |
| Student | `multipleRecordLinks` | → Students |
| Course | `multipleRecordLinks` | → Courses |
| Assessment Date | `date` | - |
| Score | `number` | Decimal precision: 2 |
| Feedback | `multilineText` | - |
| Assessment Type | `singleSelect` | Written Exam, Oral Exam, Project, Participation |
| Completion Status | `checkbox` | - |

---

## Entity Relationships

```
Students ←→ Courses (many-to-many via Enrollments)
    ↓
Enrollments → Schedules
    ↓
Instructors → Schedules
    ↓
Students ←→ Assessments ←→ Courses
```

---

## Key Features

- **AI-Powered Fields:** Course summaries and improvement suggestions auto-generated
- **Progress Tracking:** Automatic calculation of enrollment duration and completion
- **Multi-level Relationships:** Students → Courses → Assessments → Instructors