# Expat Student - Detaylı Açıklama

> Yabancı öğrenciler için kurs yönetim sistemi.

## 🎯 Bu Veritabanı Ne Yapıyor?

Bu, **yabancı öğrenciler için eğitim takip sistemi**. Ana uygulamaya benzer ama daha basit ve farklı özellikler içeriyor.

---

## 📊 6 Tablo Var

### 1️⃣ Students (Öğrenciler)

Her öğrencinin bilgileri:
- Ad, soyad
- Doğum tarihi
- Email, telefon
- Uyruk
- Profil fotoğrafı

**Özel:** Yaş otomatik hesaplanıyor (doğum tarihinden).

---

### 2️⃣ Courses (Kurslar)

Kurs seviyeleri:
- Beginner (Başlangıç)
- Intermediate (Orta)
- Advanced (İleri)

**🤖 AI Özelliği:** Her kurs için:
- **Kurs Özeti** - AI otomatik açıklama yazıyor
- **İyileştirme Önerileri** - AI kursu nasıl geliştirebileceğinizi söylüyor

---

### 3️⃣ Enrollments (Kayıtlar)

Öğrenci + Kurs eşleştirmesi:

```
Ahmet + A1 Kursu = Bir kayıt
```

Her kayıtta:
- Başlangıç tarihi
- İlerleme yüzdesi (%0-100)
- Durum (Başlamadı / Devam ediyor / Tamamlandı)

---

### 4️⃣ Instructors (Eğitmenler)

Eğitmen bilgileri:
- Ad
- Yetkinlikler
- İletişim bilgileri
- Atandığı kurslar

---

### 5️⃣ Schedules (Programlar)

Ders programları:
- Hangi gün, saat?
- Nerede? (Online/Yüz yüze)
- Hangi eğitmen?
- Ders tipi (Lecture, Workshop, Seminar)

---

### 6️⃣ Assessments (Değerlendirmeler)

Öğrenci değerlendirmeleri:
- Yazılı sınav
- Sözlü sınav
- Proje
- Katılım

Her değerlendirmede puan ve geri bildirim var.

---

## 🔗 Tablolar Nasıl Bağlı?

```
┌─────────────┐
│  Öğrenciler  │
└──────┬──────┘
       │
       │ öğrenci hangi kurslara kayıtlı?
       ▼
┌─────────────┐      ┌─────────────┐
│   Kayıtlar   │◄────►│   Kurslar    │
└──────┬──────┘      └──────┬──────┘
       │                     │
       │                     │ kursun programı ne?
       ▼                     ▼
┌─────────────┐      ┌─────────────┐
│Değerlendirme│      │  Programlar  │
└─────────────┘      └──────┬──────┘
                            │
                            │ kim ders veriyor?
                            ▼
                     ┌─────────────┐
                     │  Eğitmenler  │
                     └─────────────┘
```

---

## 🎯 Ana Uygulama ile Farkı

| Özellik | Ana Uygulama | Expat Student |
|---------|-------------|---------------|
| Tablo sayısı | 20 | 6 |
| Sohbet sistemi | ✅ Var | ❌ Yok |
| Yazı testleri | ✅ AI ile | ❌ Yok |
| Ses testleri | ✅ Var | ❌ Yok |
| Kurs özeti AI | ❌ Yok | ✅ Var |

---

## 📌 İlgili Sayfalar

- [[GIRIS|← Giriş sayfasına dön]]
- [[bases/expat-student/index|Teknik detaylar]]