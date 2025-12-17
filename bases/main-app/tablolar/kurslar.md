# 📖 Kurslar Tablosu (Courses)

## Bu Tablo Ne İçin?

Bu tabloda **tüm kurs seviyeleri** tutuluyor. Örneğin A1 Part 1, A1 Part 2, A2 gibi.

---

## 📝 Bu Tabloda Neler Var?

| Alan | Açıklama | Örnek |
|------|---------|-------|
| **Name** | Kursun adı | "A1 Part 1" |
| **Notes** | Kurs hakkında notlar | "Başlangıç seviyesi, 12 hafta" |
| **Teacher** | Kurstan sorumlu öğretmen | Jamila |
| **Status** | Kursun durumu | Online / Offline |

### Bağlı Bilgiler

| Alan | Ne Gösterir? |
|------|-------------|
| **Linked Users** | Bu kursa kayıtlı öğrenciler |
| **Lessons** | Bu kurstaki dersler |
| **Course_enrollment** | Kayıt detayları |
| **Events** | Bu kursun canlı dersleri |

---

## 🔗 Kurs Yapısı

```
A1 Part 1 Kursu
    │
    ├── Hangi öğrenciler var? → Ahmet, Ayşe, Mehmet...
    │
    ├── Hangi dersler var? → Ders 1, Ders 2, Ders 3...
    │
    └── Ne zaman canlı ders var? → Her Salı 14:00
```

---

## 🟢 Kurs Durumları

| Durum | Anlamı |
|-------|--------|
| 🟢 **Online** | Kurs aktif, öğrenciler erişebilir |
| 🟡 **Offline** | Kurs pasif, kimse erişemez |

---

## 💡 Örnek

**A1 Part 1** kursu:
- 15 öğrenci kayıtlı
- 12 ders içeriyor
- Jamila öğretiyor
- Her Salı ve Perşembe 10:00'da canlı ders
- Durum: Online (aktif)

---

## 📌 İlgili Sayfalar

- [[bases/main-app/ACIKLAMA|← Ana Sistem'e dön]]
- [[bases/main-app/tablolar/dersler|Dersler tablosu]]
- [[bases/main-app/tablolar/ogrenciler|Öğrenciler tablosu]]