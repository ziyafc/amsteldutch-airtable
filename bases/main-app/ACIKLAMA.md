# Ana Uygulama - Detaylı Açıklama

> Hollandaca öğrenme platformunun ana veritabanı.

## 🎯 Bu Veritabanı Ne Yapıyor?

Bu, **Hollandaca dil kursu** yönetim sistemi. İçinde:

- 👥 **Öğrenciler** - Kim katılıyor?
- 📖 **Kurslar** - Hangi seviyeler var? (A1, A2, B1...)
- 📚 **Dersler** - Her kursta neler öğretiliyor?
- ✅ **Ödevler** - Öğrenciler ne yapmalı?
- 📝 **Testler** - Yazma, konuşma, çoktan seçmeli
- 💬 **Sohbetler** - Öğretmen-öğrenci iletişimi

---

## 🗺️ Genel Yapı

Sistemi bir **ağaç** gibi düşün:

```
🏢 MÜŞTERİLER (Kurumlar)
    │
    └── 👥 ÖĞRENCİLER
            │
            ├── 📖 KURSLAR (A1, A2, B1...)
            │       │
            │       └── 📚 DERSLER (Hafta 1, Hafta 2...)
            │               │
            │               └── ✅ ÖDEVLER (Görevler)
            │                       │
            │                       └── ❓ SORULAR
            │
            ├── 📊 İLERLEME (Hangi ödevleri yaptı?)
            │
            ├── 📝 TESTLER (Yazma, Ses, Çoktan Seçmeli)
            │
            └── 💬 SOHBETLER (Öğretmenle iletişim)
```

---

## 📊 Tablolar ve Ne İşe Yararlar

### 👥 İnsan Tabloları

| Tablo | Ne Tutuyor? | Örnek |
|-------|-------------|-------|
| [[bases/main-app/tables/users\|Users (Öğrenciler)]] | Tüm öğrenci bilgileri | Ad, email, hangi kursta, ilerlemesi |
| [[bases/main-app/tables/clients\|Clients (Müşteriler)]] | Kurumsal müşteriler | Şirket X, Şirket Y |
| [[bases/main-app/tables/user-groups\|User Groups (Gruplar)]] | Öğrenci grupları | "Salı sabah grubu" |

**Örnek Senaryo:** Şirket X (müşteri) 10 çalışanını (öğrenci) Hollandaca kursuna gönderiyor.

---

### 📚 İçerik Tabloları

| Tablo | Ne Tutuyor? | Örnek |
|-------|-------------|-------|
| [[bases/main-app/tables/courses\|Courses (Kurslar)]] | Kurs seviyeleri | A1 Part 1, A1 Part 2, A2 |
| [[bases/main-app/tables/lessons\|Lessons (Dersler)]] | Her kurstaki dersler | Hafta 1: Tanışma, Hafta 2: Alışveriş |
| [[bases/main-app/tables/tasks\|Tasks (Ödevler)]] | Her dersteki görevler | "Kendinizi tanıtın" ödevi |
| [[bases/main-app/tables/questions\|Questions (Sorular)]] | Quiz soruları | "'Hoe heet je?' ne demek?" |

**Nasıl Bağlı?**
```
A1 Part 1 Kursu
    ├── Ders 1: Tanışma
    │       ├── Ödev: Kendinizi tanıtın (yazılı)
    │       ├── Ödev: Sayıları öğrenin (quiz)
    │       └── Ödev: Telaffuz (sesli)
    ├── Ders 2: Alışveriş
    │       ├── ...
```

---

### 📝 Test Tabloları

Öğrenciler 3 tür test yapabiliyor:

| Tablo | Test Türü | Nasıl Çalışıyor? |
|-------|----------|----------------|
| [[bases/main-app/tables/writing-tests\|WRITING_TESTS]] | ✉️ Yazma | Öğrenci yazar → **AI otomatik düzeltir** → Öğretmen kontrol eder |
| [[bases/main-app/tables/audio-tests\|AUDIO_TESTS]] | 🎙️ Konuşma | Öğrenci ses kaydeder → Öğretmen dinler ve puan verir |
| [[bases/main-app/tables/mtp-tests\|MTP_TESTS]] | ✅ Çoktan Seçmeli | Öğrenci cevaplar → Otomatik puanlama |

**🤖 AI Nasıl Çalışıyor? (Yazma Testlerinde)**

Öğrenci Hollandaca bir şey yazdığında:
1. Yapay zeka yazıyı analiz ediyor
2. Hataları buluyor
3. Doğru versiyonunu gösteriyor
4. Olumlu geri bildirim veriyor
5. Hataların listesini çıkarıyor

Örnek:
```
Öğrenci yazdı: "Ik ben gaan naar de winkel"
AI düzeltmesi: "Ik ga naar de winkel"
Açıklama: "'ben gaan' yerine 'ga' kullanılır çünkü..."
```

---

### 💬 İletişim Tabloları

| Tablo | Ne Tutuyor? | Örnek |
|-------|-------------|-------|
| [[bases/main-app/tables/chats\|Chats (Sohbetler)]] | Öğretmen-öğrenci sohbet konuları | "Ders 3 hakkında soru" |
| [[bases/main-app/tables/messages\|Messages (Mesajlar)]] | Sohbet içindeki mesajlar | Tek tek mesajlar |

**Sohbet Durumları:**
1. 🟠 **Gönderildi** - Öğrenci yazdı
2. 🔵 **İşleniyor** - Öğretmen bakıyor
3. 🟢 **Yanıtlandı** - Öğretmen cevapladı
4. 🟣 **Arşivlendi** - Konu kapandı

---

### 📊 Takip Tabloları

| Tablo | Ne Tutuyor? | Örnek |
|-------|-------------|-------|
| [[bases/main-app/tables/task-progress\|Task Progress (İlerleme)]] | Kim hangi ödevi yaptı? | Ahmet + Ödev 3 = Tamamlandı ✅ |
| [[bases/main-app/tables/course-enrollment\|Course_enrollment (Kayıtlar)]] | Kim hangi kursa kayıtlı? | Ahmet + A1 Part 1 = 15 Ocak'ta başladı |
| [[bases/main-app/tables/events\|Events (Etkinlikler)]] | Canlı dersler ne zaman? | "A1 Grup dersi - Salı 14:00" |

---

## 🔄 Tipik Bir Akış

Bir öğrencinin sistemi nasıl kullandığını görelim:

```
1️⃣ Ahmet sisteme kayıt oluyor
   → Users tablosuna ekleniyor
   → Course_enrollment ile A1 kursuna bağlanıyor

2️⃣ Ahmet derslerini görüyor
   → Kursu üzerinden Lessons'a erişiyor
   → Her dersin Tasks'ını görüyor

3️⃣ Ahmet bir yazı ödevi yapıyor
   → WRITING_TESTS'e kaydediliyor
   → AI otomatik geri bildirim veriyor
   → Öğretmen kontrol edip puan veriyor

4️⃣ Ahmet'in sorusu var
   → Chats'te yeni sohbet açıyor
   → Messages'a mesajı yazıyor
   → Öğretmen yanıtlıyor

5️⃣ Öğretmen ilerlemeyi takip ediyor
   → Task Progress'ten kimin ne yaptığını görüyor
```

---

## 👩‍🏫 Öğretmenler

Sistemde 11 öğretmen tanımlı:
- Jamila, Anne E, Annemijn, Anne V, Elsa
- Roxane, Ella, Wesley, Catalina, Luis, Kelly

Her öğrenci bir öğretmene atanabiliyor.

---

## 📌 İlgili Sayfalar

- [[GIRIS|← Giriş sayfasına dön]]
- [[bases/main-app/index|Teknik detaylar (geliştiriciler için)]]