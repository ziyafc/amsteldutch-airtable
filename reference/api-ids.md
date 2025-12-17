---
tags:
  - reference
  - api
---

# API IDs

> Tüm Base ve Table ID'leri API kullanımı için.

## 💾 Base IDs

| Base | ID | Link |
|------|-------|------|
| Amstel Dutch | `app8UfvWnkJWFKUpt` | [[bases/amstel-dutch/index]] |
| Expat Student | `appAe8WSfkPmp8P8I` | [[bases/expat-student/index]] |
| Main App | `apptQsmAbTKpeV2z0` | [[bases/main-app/index]] |
| Dev/Staging | `appg5FhzhGeUrEjve` | [[bases/dev-staging/index]] |

```javascript
const BASES = {
  AMSTEL_DUTCH: 'app8UfvWnkJWFKUpt',
  EXPAT_STUDENT: 'appAe8WSfkPmp8P8I',
  MAIN_APP: 'apptQsmAbTKpeV2z0',
  DEV_STAGING: 'appg5FhzhGeUrEjve'
};
```

---

## 🗂️ Amstel Dutch Tables

| Table | ID |
|-------|----|
| [[bases/amstel-dutch/tables/product-launches\|Product Launches]] | `tblnUG1lqNMIlLzdJ` |

---

## 🗂️ Expat Student Tables

| Table | ID |
|-------|----|
| [[bases/expat-student/tables/courses\|Courses]] | `tbllHRWQNJvVjdsbW` |
| [[bases/expat-student/tables/students\|Students]] | `tblqLbVNQQbE05gU4` |
| [[bases/expat-student/tables/enrollments\|Enrollments]] | `tbl3LE5BoyxQ60WkA` |
| [[bases/expat-student/tables/schedules\|Schedules]] | `tbl1ADP4zZllvOkBj` |
| [[bases/expat-student/tables/instructors\|Instructors]] | `tblber3wEWGjCNdU6` |
| [[bases/expat-student/tables/assessments\|Assessments]] | `tbloZt35vRi7Q5ZUu` |

---

## 🗂️ Main App Tables

### Core

| Table | ID |
|-------|----|
| [[bases/main-app/tables/users\|Users]] | `tbl1r15vHh4nW3Xjo` |
| [[bases/main-app/tables/clients\|Clients]] | `tbloGxTg8v8s6OsZx` |
| [[bases/main-app/tables/courses\|Courses]] | `tblmSLMsyy2GxPVO7` |
| [[bases/main-app/tables/lessons\|Lessons]] | `tblBH8VGXZ4wGKXpH` |

### Content

| Table | ID |
|-------|----|
| [[bases/main-app/tables/tasks\|Tasks]] | `tblSyEAVZAYExNBSu` |
| [[bases/main-app/tables/task-progress\|Task Progress]] | `tblfGcMDhdUQux6KH` |
| [[bases/main-app/tables/questions\|Questions]] | `tblwPF7NZ0y6Tjb9U` |

### Tests

| Table | ID |
|-------|----|
| [[bases/main-app/tables/writing-tests\|WRITING_TESTS]] | `tblyBQSYVCDJTb6Ij` |
| [[bases/main-app/tables/audio-tests\|AUDIO_TESTS]] | `tblx0byituDy8t15y` |
| [[bases/main-app/tables/mtp-tests\|MTP_TESTS]] | `tbls2Ha3PO9QFoukW` |

### Communication

| Table | ID |
|-------|----|
| [[bases/main-app/tables/chats\|Chats]] | `tblBfmTN20XWC4sU3` |
| [[bases/main-app/tables/messages\|Messages]] | `tblzuVXq93AxyJvne` |

### Organization

| Table | ID |
|-------|----|
| [[bases/main-app/tables/user-groups\|User Groups]] | `tbliF0jhuw7jXkOi6` |
| [[bases/main-app/tables/activities\|Activities]] | `tblBBkQKTtgV7zX8q` |
| [[bases/main-app/tables/events\|Events]] | `tblhnBw7Q8sR3RRB1` |
| [[bases/main-app/tables/course-enrollment\|Course_enrollment]] | `tbl8XWGbHeT6JoVIM` |

```javascript
const MAIN_APP_TABLES = {
  USERS: 'tbl1r15vHh4nW3Xjo',
  CLIENTS: 'tbloGxTg8v8s6OsZx',
  COURSES: 'tblmSLMsyy2GxPVO7',
  LESSONS: 'tblBH8VGXZ4wGKXpH',
  TASKS: 'tblSyEAVZAYExNBSu',
  TASK_PROGRESS: 'tblfGcMDhdUQux6KH',
  QUESTIONS: 'tblwPF7NZ0y6Tjb9U',
  WRITING_TESTS: 'tblyBQSYVCDJTb6Ij',
  AUDIO_TESTS: 'tblx0byituDy8t15y',
  MTP_TESTS: 'tbls2Ha3PO9QFoukW',
  CHATS: 'tblBfmTN20XWC4sU3',
  MESSAGES: 'tblzuVXq93AxyJvne',
  USER_GROUPS: 'tbliF0jhuw7jXkOi6',
  ACTIVITIES: 'tblBBkQKTtgV7zX8q',
  EVENTS: 'tblhnBw7Q8sR3RRB1',
  COURSE_ENROLLMENT: 'tbl8XWGbHeT6JoVIM'
};
```

---

## 🗂️ Dev/Staging Tables

| Table | ID |
|-------|----|
| [[bases/dev-staging/tables/users\|Users]] | `tbl1r15vHh4nW3Xjo` |
| [[bases/dev-staging/tables/courses\|Courses]] | `tblmSLMsyy2GxPVO7` |
| [[bases/dev-staging/tables/clients\|Clients]] | `tbloGxTg8v8s6OsZx` |
| [[bases/dev-staging/tables/progress\|Progress]] | `tblfGcMDhdUQux6KH` |
| [[bases/dev-staging/tables/lessons\|Lessons]] | `tblBH8VGXZ4wGKXpH` |

---

## 📌 Related

- [[reference/field-types|Field Types]]
- [[diagrams/overview|Architecture Overview]]