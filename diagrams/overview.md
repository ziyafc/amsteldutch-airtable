---
tags:
  - diagram
---

# Architecture Overview

> Tüm Airtable workspace'inin genel görünümü.

## 🗺️ Base Landscape

```
┌───────────────────────────────────────────────────────┐
│                    AIRTABLE WORKSPACE                      │
└───────────────────────────────────────────────────────┘
        │                    │                    │
        ▼                    ▼                    ▼
┌─────────────┐  ┌─────────────────┐  ┌─────────────┐
│ Amstel Dutch│  │  Expat Student  │  │  MAIN APP   │
│  (simple)   │  │  (education)    │  │ (full LMS)  │
└─────────────┘  └─────────────────┘  └──────┬──────┘
     │                   │                     │
     │                   │                     │ clone
     ▼                   ▼                     ▼
┌─────────────┐  ┌─────────────────┐  ┌─────────────┐
│  1 table    │  │    6 tables     │  │ Dev/Staging │
│  No links   │  │  AI + Relations │  │  (5 tables) │
└─────────────┘  └─────────────────┘  └─────────────┘
```

## 📊 Complexity Levels

| Level | Base | Tables | Features |
|-------|------|--------|----------|
| 🟢 Simple | [[bases/amstel-dutch/index\|Amstel Dutch]] | 1 | Status tracking |
| 🟡 Medium | [[bases/expat-student/index\|Expat Student]] | 6 | Relations, AI, Formulas |
| 🔴 Complex | [[bases/main-app/index\|Main App]] | 20 | Full LMS, Chat, Tests |
| ⚪ Dev | [[bases/dev-staging/index\|Dev/Staging]] | 5 | Simplified clone |

## 🏷️ Feature Matrix

| Feature | Amstel | Expat | Main | Dev |
|---------|--------|-------|------|-----|
| [[reference/field-types#multipleRecordLinks\|Relations]] | ❌ | ✅ | ✅ | ✅ |
| [[reference/field-types#formula\|Formulas]] | ❌ | ✅ | ✅ | ❌ |
| [[reference/field-types#aiText\|AI Fields]] | ❌ | ✅ | ✅ | ❌ |
| [[reference/patterns#Chat/Messaging Pattern\|Chat]] | ❌ | ❌ | ✅ | ❌ |
| [[reference/patterns#Progress Tracking Pattern\|Progress]] | ❌ | ✅ | ✅ | ✅ |
| Multi-modal Tests | ❌ | ❌ | ✅ | ❌ |

## 🔗 Cross-Base Patterns

Her base benzer patternler kullanır:

### [[reference/patterns#User-Course Enrollment Pattern|Enrollment Pattern]]
- [[bases/expat-student/tables/enrollments|Expat: Enrollments]]
- [[bases/main-app/tables/course-enrollment|Main: Course_enrollment]]

### [[reference/patterns#Hierarchical Content Pattern|Content Hierarchy]]
- [[bases/main-app/index|Main App]]: Courses → Lessons → Tasks → Questions
- [[bases/expat-student/index|Expat]]: Courses → Assessments

### [[reference/patterns#Progress Tracking Pattern|Progress Tracking]]
- [[bases/main-app/tables/task-progress|Main: Task Progress]]
- [[bases/dev-staging/tables/progress|Dev: Progress]]

## 📌 Quick Navigation

### By Purpose
- **Learning**: [[bases/main-app/index|Main App]], [[bases/expat-student/index|Expat Student]]
- **Tracking**: [[bases/amstel-dutch/index|Amstel Dutch]]
- **Development**: [[bases/dev-staging/index|Dev/Staging]]

### By Complexity
- **Beginner-friendly**: [[bases/amstel-dutch/index|Amstel Dutch]]
- **Full-featured**: [[bases/main-app/index|Main App]]

## 📌 Related

- [[diagrams/relationships|Cross-Base Relationships]]
- [[reference/api-ids|API IDs]]
- [[reference/patterns|Common Patterns]]