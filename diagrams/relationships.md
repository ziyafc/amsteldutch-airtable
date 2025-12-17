---
tags:
  - diagram
---

# Cross-Base Relationships

> Base'ler arası yapısal karşılaştırma.

## 🔄 Table Equivalents

| Concept | Expat Student | Main App | Dev/Staging |
|---------|--------------|----------|-------------|
| Users | [[bases/expat-student/tables/students\|Students]] | [[bases/main-app/tables/users\|Users]] | [[bases/dev-staging/tables/users\|Users]] |
| Courses | [[bases/expat-student/tables/courses\|Courses]] | [[bases/main-app/tables/courses\|Courses]] | [[bases/dev-staging/tables/courses\|Courses]] |
| Enrollment | [[bases/expat-student/tables/enrollments\|Enrollments]] | [[bases/main-app/tables/course-enrollment\|Course_enrollment]] | - |
| Progress | - | [[bases/main-app/tables/task-progress\|Task Progress]] | [[bases/dev-staging/tables/progress\|Progress]] |
| Content | - | [[bases/main-app/tables/lessons\|Lessons]] + [[bases/main-app/tables/tasks\|Tasks]] | [[bases/dev-staging/tables/lessons\|Lessons]] |
| Assessment | [[bases/expat-student/tables/assessments\|Assessments]] | [[bases/main-app/tables/writing-tests\|WRITING]] + [[bases/main-app/tables/audio-tests\|AUDIO]] | - |

## 📊 Shared Patterns

### 1. User-Course Junction

Her LMS base'inde var:

```
Users ◄───► Junction Table ◄───► Courses
              │
              ├─ Start/End dates
              ├─ Progress %
              └─ Status
```

**Implementations:**
- [[bases/expat-student/tables/enrollments|Expat: Enrollments]]
- [[bases/main-app/tables/course-enrollment|Main: Course_enrollment]]

### 2. Content Hierarchy

```
Courses
   └── Lessons/Modules
         └── Tasks/Activities
               └── Questions
```

**Depth by base:**
| Base | Depth | Levels |
|------|-------|--------|
| Expat | 2 | Courses → Assessments |
| Main | 4 | Courses → Lessons → Tasks → Questions |
| Dev | 2 | Courses → Lessons |

### 3. Progress Tracking

```
User + Content Item = Progress Record
```

**Implementations:**
- [[bases/main-app/tables/task-progress|Main: Task Progress]] (granular)
- [[bases/dev-staging/tables/progress|Dev: Progress]] (simple)
- [[bases/expat-student/tables/enrollments|Expat: Enrollments]] (embedded)

## 🤖 AI Usage

| Base | AI Field | Purpose |
|------|----------|--------|
| [[bases/expat-student/tables/courses\|Expat: Courses]] | Course Summary | Marketing text |
| [[bases/expat-student/tables/courses\|Expat: Courses]] | Suggested Improvement | Analytics |
| [[bases/main-app/tables/writing-tests\|Main: WRITING_TESTS]] | AI assist | Dutch correction |

## 📌 Navigation Map

```
                     README
                        │
        ┌───────────────┼───────────────┐
        │               │               │
        ▼               ▼               ▼
    bases/          reference/      diagrams/
        │               │               │
   ┌────┼────┐    ┌────┼────┐    ┌───┴───┐
   │    │    │    │    │    │    │       │
   ▼    ▼    ▼    ▼    ▼    ▼    ▼       ▼
amstel expat main dev  types status overview relationships
   │    │    │    │    api-ids patterns
   │    │    │    │
   ▼    ▼    ▼    ▼
tables/ tables/ tables/ tables/
```

## 📌 Related

- [[diagrams/overview|Architecture Overview]]
- [[reference/patterns|Common Patterns]]
- [[reference/api-ids|API IDs]]