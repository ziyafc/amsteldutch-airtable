---
tags:
  - reference
---

# Common Patterns

> Tekrar eden veri modeli yapıları.

## 🔗 User-Course Enrollment Pattern

Many-to-many ilişki için junction table kullanımı.

```
┌─────────┐           ┌───────────────┐           ┌─────────┐
│  Users  │◄── 1:N ──►│  Enrollments  │◄── N:1 ──►│ Courses │
└─────────┘           └───────────────┘           └─────────┘
                              │
                      Extra fields:
                      - Start Date
                      - End Date
                      - Progress %
                      - Status
```

**Kullanıldığı yerler:**
- [[bases/expat-student/tables/enrollments|Expat: Enrollments]]
- [[bases/main-app/tables/course-enrollment|Main: Course_enrollment]]

**Avantajlar:**
- Her enrollment'a ek veri eklenebilir (tarih, progress)
- History tutulabilir
- Reporting kolay

---

## 📚 Hierarchical Content Pattern

Kurs > Ders > Görev > Soru hiyerarşisi.

```
┌─────────┐
│ Courses │  Level 1: Course catalog
└────┬────┘
     │ 1:N
     ▼
┌─────────┐
│ Lessons │  Level 2: Course modules
└────┬────┘
     │ 1:N
     ▼
┌─────────┐
│  Tasks  │  Level 3: Activities
└────┬────┘
     │ 1:N
     ▼
┌───────────┐
│ Questions │  Level 4: Quiz items
└───────────┘
```

**Kullanıldığı yerler:**
- [[bases/main-app/index|Main App]] - Full implementation
- [[bases/expat-student/index|Expat Student]] - Courses > Assessments

---

## 📊 Progress Tracking Pattern

User + Content = Progress kaydı.

```
┌────────┐     ┌─────────────┐     ┌─────────┐
│ Users  │────►│  Progress   │◄────│  Tasks  │
└────────┘     └─────────────┘     └─────────┘
                    │
            Fields:
            - Completed (checkbox)
            - Completed At (timestamp)
            - Notes (feedback)
```

**Kullanıldığı yerler:**
- [[bases/main-app/tables/task-progress|Main: Task Progress]]
- [[bases/dev-staging/tables/progress|Dev: Progress]]

---

## 💬 Chat/Messaging Pattern

Chat > Messages one-to-many.

```
┌──────────┐     ┌──────────┐
│  Chats   │────►│ Messages │
└────┬─────┘     └────┬─────┘
     │                 │
     │  Fields:        │  Fields:
     │  - Subject      │  - Message
     │  - Status       │  - Direction (In/Out)
     │  - Score        │  - Timestamp
     │  - Users        │  - Attachments
     │  - Tests ◄──────┘
     ▼
┌──────────────┐
│ WRITING_TESTS │
│ AUDIO_TESTS   │
└──────────────┘
```

**Kullanıldığı yerler:**
- [[bases/main-app/tables/chats|Main: Chats]]
- [[bases/main-app/tables/messages|Main: Messages]]

---

## 🤖 AI Feedback Pattern

User input -> AI processing -> Feedback.

```
┌────────────┐
│ User Input │  multilineText field
└──────┬─────┘
       │
       ▼
┌────────────┐
│ AI Field   │  aiText field with prompt
│ (assist)   │  References: Input + Context
└────────────┘
       │
       ▼
   Output:
   - Corrected version
   - Error analysis
   - Feedback
```

**Kullanıldığı yerler:**
- [[bases/main-app/tables/writing-tests|Main: WRITING_TESTS]] - Dutch correction
- [[bases/expat-student/tables/courses|Expat: Courses]] - Summary generation

---

## 📌 Related

- [[reference/field-types|Field Types]]
- [[reference/api-ids|API IDs]]
- [[diagrams/relationships|Cross-Base Relationships]]