# Cross-Base Relationships & Architecture

## Base Comparison

| Feature | Amstel Dutch | Expat Student | !!Base for App!! | Untitled |
|---------|--------------|---------------|------------------|----------|
| **Purpose** | Product launches | Course mgmt | Main app | Dev/staging |
| **Tables** | 1 | 6 | 20 | 5 |
| **AI Fields** | No | Yes (Course Summary) | Yes (Writing Feedback) | No |
| **Chat System** | No | No | Yes | No |
| **Test System** | No | Yes (Assessments) | Yes (Multi-modal) | No |
| **Progress Tracking** | No | Yes (Enrollment-based) | Yes (Task-based) | Yes (Basic) |

---

## Data Model Patterns

### User-Course Enrollment Pattern

Used in both Expat Student and Base for App:

```
Users <--[many-to-many]--> Courses
           |
           +-- via Junction Table (Enrollments / Course_enrollment)
                   |
                   +-- Start Date
                   +-- End Date  
                   +-- Progress %
                   +-- Status
```

### Hierarchical Content Pattern

```
Courses
   +-- Lessons/Modules
         +-- Tasks/Activities
               +-- Questions/Assessments
```

### Progress Tracking Pattern

```
User + Task/Lesson = Progress Record
   |
   +-- Completed (checkbox)
   +-- Completed At (timestamp)
   +-- Notes (feedback)
```

---

## Common Field Types Used

| Type | Usage |
|------|-------|
| `singleLineText` | Names, IDs, short text |
| `multilineText` | Notes, descriptions |
| `singleSelect` | Status fields (Todo/Progress/Done) |
| `multipleRecordLinks` | Table relationships |
| `lookup` | Derived values from linked records |
| `rollup` | Aggregations (counts, sums) |
| `formula` | Calculated fields |
| `checkbox` | Boolean flags (completed, verified) |
| `date` / `dateTime` | Scheduling, tracking |
| `autoNumber` | Sequential IDs |
| `aiText` | AI-generated content |
| `multipleAttachments` | Files, images, videos |

---

## Status Workflow Standards

Most tables use consistent status values:

```
+----------+     +-------------+     +--------+
|   Todo   | --> | In Progress | --> |  Done  |
|  (Red)   |     |  (Yellow)   |     |(Green) |
+----------+     +-------------+     +--------+
```

---

## API Usage Notes

### Base IDs

```javascript
const BASES = {
  AMSTEL_DUTCH: 'app8UfvWnkJWFKUpt',
  EXPAT_STUDENT: 'appAe8WSfkPmp8P8I',
  MAIN_APP: 'apptQsmAbTKpeV2z0',
  DEV_STAGING: 'appg5FhzhGeUrEjve'
};
```

### Key Table IDs (Main App)

```javascript
const TABLES = {
  USERS: 'tbl1r15vHh4nW3Xjo',
  COURSES: 'tblmSLMsyy2GxPVO7',
  LESSONS: 'tblBH8VGXZ4wGKXpH',
  TASKS: 'tblSyEAVZAYExNBSu',
  PROGRESS: 'tblfGcMDhdUQux6KH',
  WRITING_TESTS: 'tblyBQSYVCDJTb6Ij',
  AUDIO_TESTS: 'tblx0byituDy8t15y',
  CHATS: 'tblBfmTN20XWC4sU3',
  MESSAGES: 'tblzuVXq93AxyJvne',
  ENROLLMENT: 'tbl8XWGbHeT6JoVIM'
};
```

---

## Recommended Integrations

1. **User Authentication:** Magic link field in Users table
2. **Progress Sync:** Task Progress -> User.Progress relationship
3. **Communication:** Chats -> Messages -> Users flow
4. **Assessment:** WRITING_TESTS / AUDIO_TESTS -> AI feedback loop
5. **Scheduling:** Events -> Courses -> Users notification chain