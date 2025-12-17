---
tags:
  - base
base_id: appg5FhzhGeUrEjve
permission: create
---

# Dev/Staging (Untitled Base)

> Geliştirme/test ortamı - Main App'in sadeleştirilmiş versiyonu.

## 📋 Base Info

| Property | Value |
|----------|-------|
| Base ID | `appg5FhzhGeUrEjve` |
| Permission | Create |
| Tables | 5 |

## 📑 Tables

- [[bases/dev-staging/tables/users|Users]] - Kullanıcılar
- [[bases/dev-staging/tables/courses|Courses]] - Kurslar
- [[bases/dev-staging/tables/clients|Clients]] - Müşteriler (bağımsız)
- [[bases/dev-staging/tables/progress|Progress]] - İlerleme
- [[bases/dev-staging/tables/lessons|Lessons]] - Dersler

## 🔗 Relationship Map

```
┌─────────┐     ┌─────────┐     ┌─────────┐
│  Users  │◄───►│ Courses │◄───►│ Lessons │
└────┬────┘     └─────────┘     └────┬────┘
     │                               │
     └───────────►┌──────────┐◄──────┘
                  │ Progress │
                  └──────────┘

┌─────────┐
│ Clients │ (standalone - bağlı değil)
└─────────┘
```

## ⚠️ Main App vs Dev/Staging

| Feature | Main App | Dev/Staging |
|---------|----------|-------------|
| Tables | 20 | 5 |
| AI Fields | ✅ | ❌ |
| Chat System | ✅ | ❌ |
| Tests | ✅ | ❌ |
| User Groups | ✅ | ❌ |
| Events | ✅ | ❌ |

## 📌 Related

- [[bases/main-app/index|Main App]] - Production version
- [[reference/api-ids#Dev/Staging Tables|API IDs]]