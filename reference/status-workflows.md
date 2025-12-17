---
tags:
  - reference
---

# Status Workflows

> Projelerde kullanılan standart durum akışları.

## 🟢 Standard 3-State

En yaygın workflow. Çoğu tabloda kullanılır.

```
┌──────────┐     ┌─────────────┐     ┌────────┐
│   Todo   │ ──► │ In Progress │ ──► │  Done  │
│  🔴 Red   │     │  🟡 Yellow  │     │🟢 Green│
└──────────┘     └─────────────┘     └────────┘
```

**Kullanıldığı tablolar:**
- [[bases/main-app/tables/users|Users]]
- [[bases/main-app/tables/lessons|Lessons]]
- [[bases/main-app/tables/tasks|Tasks]]
- [[bases/dev-staging/tables/users|Dev: Users]]

---

## 📦 Product Launch Workflow

4-state workflow with risk tracking.

```
┌─────────────┐     ┌──────────┐     ┌──────────┐     ┌───────────┐
│ Not started │ ──► │ At risk  │ ──► │ On track │ ──► │ Completed │
│   🔴 Red     │     │🟡 Yellow │     │🟠 Orange │     │  🟢 Green │
└─────────────┘     └──────────┘     └──────────┘     └───────────┘
```

**Kullanıldığı tablolar:**
- [[bases/amstel-dutch/tables/product-launches|Product Launches]]

---

## 📩 Chat/Support Workflow

4-state support ticket workflow.

```
┌───────────┐     ┌────────────────────┐     ┌───────────┐     ┌──────────┐
│ Submitted │ ──► │Processing Internally│ ──► │ Responded │ ──► │ Archived │
│ 🟠 Orange │     │      🔵 Cyan       │     │ 🟢 Green  │     │ 🟣 Purple│
└───────────┘     └────────────────────┘     └───────────┘     └──────────┘
```

**Kullanıldığı tablolar:**
- [[bases/main-app/tables/chats|Chats]]

---

## 🟢 Online/Offline Toggle

Basit 2-state toggle.

```
┌──────────┐          ┌──────────┐
│  Online  │ ◄──────► │ Offline  │
│ 🟢 Green │          │ 🟡 Yellow│
└──────────┘          └──────────┘
```

**Kullanıldığı tablolar:**
- [[bases/main-app/tables/courses|Courses]]
- [[bases/main-app/tables/events|Events]]

---

## 📖 Enrollment Status

3-state progress workflow.

```
┌─────────────┐     ┌─────────────┐     ┌────────────┐
│ Not Started │ ──► │ In Progress │ ──► │  Completed │
│   🔵 Blue   │     │   🔵 Cyan   │     │  🔵 Teal  │
└─────────────┘     └─────────────┘     └────────────┘
```

**Kullanıldığı tablolar:**
- [[bases/expat-student/tables/enrollments|Enrollments]]

---

## 📌 Related

- [[reference/field-types#singleSelect|singleSelect Field Type]]
- [[reference/patterns|Common Patterns]]