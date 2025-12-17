# 👥 Öğrenciler Tablosu (Users)

## Bu Tablo Ne İçin?

Bu tabloda **tüm öğrencilerin bilgileri** tutuluyor. Sisteme kayıt olan herkes burada.

---

## 📝 Bu Tabloda Neler Var?

### Kişisel Bilgiler

| Alan | Açıklama | Örnek |
|------|---------|-------|
| **Name** | Öğrencinin adı | Ahmet Yılmaz |
| **Email** | E-posta adresi | ahmet@email.com |
| **Notes** | Ekstra notlar | "Özel ders isteği var" |

### Giriş Bilgileri

| Alan | Açıklama |
|------|--------|
| **Magic link** | Öğrencinin sisteme giriş yapacağı özel link |

> 💡 **Magic link nedir?** Şifre yerine öğrenciye özel bir link gönderiyoruz. Bu linke tıklayarak sisteme girebiliyor. Şifre hatırlamaya gerek yok!

### Durum Bilgileri

| Alan | Açıklama | Değerler |
|------|---------|----------|
| **Status** | Öğrencinin durumu | Yapılacak / Devam ediyor / Tamamlandı |
| **Assignee** | Sorumlu kişi | Öğretmen adı |

### Kurs Bilgileri

| Alan | Açıklama |
|------|--------|
| **Courses** | Hangi kurslara kayıtlı? |
| **Course_enrollment** | Kayıt detayları (başlangıç/bitiş tarihi) |
| **Teacher** | Atanan öğretmen |
| **Startdate** | Kursa başlama tarihi |
| **Closedate** | Kurs bitiş tarihi |

### Test ve İlerleme

| Alan | Açıklama |
|------|--------|
| **Progress** | Tamamladığı ödevler |
| **WRITING_TESTS 2** | Gönderdiği yazı testleri |
| **AUDIO_TESTS** | Gönderdiği ses testleri |
| **MTP_TESTS** | Çözdüğü çoktan seçmeli testler |
| **Aantal Writing tests** | Kaç yazı testi yaptı? (otomatik sayılıyor) |
| **Aantal Audio tests** | Kaç ses testi yaptı? (otomatik sayılıyor) |

### Diğer Bağlantılar

| Alan | Açıklama |
|------|--------|
| **Clients** | Hangi şirket/kurum adına kayıtlı? |
| **Chats** | Öğretmenle yaptığı sohbetler |
| **User Groups** | Dahil olduğu gruplar |
| **Certificates** | Aldığı sertifikalar (dosya olarak) |

---

## 🔗 Bu Tablo Nelere Bağlı?

```
Öğrenci (Users)
    │
    ├── Hangi şirketten? → Clients tablosu
    │
    ├── Hangi kursta? → Courses tablosu
    │
    ├── Kayıt detayları? → Course_enrollment tablosu
    │
    ├── Hangi ödevleri yaptı? → Task Progress tablosu
    │
    ├── Hangi testleri gönderdi? → WRITING_TESTS, AUDIO_TESTS, MTP_TESTS
    │
    ├── Hangi sohbetleri açtı? → Chats tablosu
    │
    └── Hangi gruplarda? → User Groups tablosu
```

---

## 💡 Örnek Senaryo

**Ahmet Yılmaz** sisteme kayıt oldu:

1. Users tablosuna eklendi
2. ABC Şirketi adına geldiği için Clients ile bağlandı
3. A1 Part 1 kursuna kayıt yapıldı (Course_enrollment)
4. Jamila öğretmene atandı
5. 15 Ocak'ta başladı, 15 Nisan'da bitirecek
6. "Salı Sabah Grubu"na eklendi

Ahmet bir ödev yaptığında → Task Progress tablosuna kayıt düşer
Ahmet bir yazı gönderdiğinde → WRITING_TESTS tablosuna kayıt düşer
Ahmet soru sorduğunda → Chats tablosunda sohbet açılır

---

## 📌 İlgili Sayfalar

- [[bases/main-app/ACIKLAMA|← Ana Sistem'e dön]]
- [[bases/main-app/tablolar/kurslar|Kurslar tablosu]]
- [[bases/main-app/tablolar/yazi-testleri|Yazı Testleri tablosu]]