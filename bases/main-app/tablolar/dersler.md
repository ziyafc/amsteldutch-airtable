# 📚 Dersler Tablosu (Lessons)

## Bu Tablo Ne İçin?

Bu tabloda **her kurstaki dersler** tutuluyor. Mesela A1 kursunun 1. dersi, 2. dersi gibi.

---

## 📝 Bu Tabloda Neler Var?

### Ders İçeriği

| Alan | Açıklama | Örnek |
|------|---------|-------|
| **Name** | Dersin İngilizce adı | "Introduction" |
| **Naam** | Dersin Hollandaca adı | "Kennismaking" |
| **Notes** | İngilizce açıklama | "Bu derste tanışma kalıpları öğrenilir" |
| **Notitie** | Hollandaca açıklama | "In deze les leer je..." |
| **Video** | Ders videosu | (dosya olarak yüklü) |

> 💡 Neden hem İngilizce hem Hollandaca var? Çünkü öğrenciler başlangıçta Hollandaca bilmiyor, İngilizce açıklamaları okuyor. İlerledikçe Hollandaca versiyona geçiyorlar.

### Egzersiz Linkleri

Her ders için farklı türde egzersizler var:

| Alan | Ne İçin? |
|------|--------|
| **writing_url** | Yazma egzersizi sayfasına link |
| **speaking_url** | Konuşma egzersizi sayfasına link |
| **reading_url** | Okuma egzersizi sayfasına link |
| **dialogue_url** | Diyalog egzersizi sayfasına link |

### Ses Dosyaları

Öğrencilerin dinlemesi ve tekrar etmesi için ses dosyaları:

| Alan | Ne İçin? |
|------|--------|
| **Speak_Audio_url_1** | 1. ses dosyası linki |
| **Speak_Audio_Text_1** | 1. seste ne söyleniyor (metin) |
| **Speak_Audio_url_2** | 2. ses dosyası linki |
| **Speak_Audio_Text_2** | 2. seste ne söyleniyor |
| **Speak_Audio_url_3** | 3. ses dosyası linki |
| **Speak_Audio_Text_3** | 3. seste ne söyleniyor |

### Durum Bilgileri

| Alan | Açıklama |
|------|--------|
| **Status** | Dersin durumu (Yapılacak / Devam / Tamamlandı) |
| **Creator** | Dersi kim oluşturdu? |
| **Lesson_Id** | Otomatik verilen numara |

### Bağlantılar

| Alan | Ne Gösterir? |
|------|-------------|
| **Course** | Bu ders hangi kursa ait? |
| **Task** | Bu derste hangi ödevler var? |

---

## 🔗 Ders Yapısı

```
A1 Part 1 Kursu
    │
    └── Ders 1: Tanışma (Kennismaking)
            │
            ├── Video: Tanışma videosu
            │
            ├── Egzersizler:
            │       ├── Yazma egzersizi
            │       ├── Konuşma egzersizi
            │       └── Diyalog egzersizi
            │
            ├── Ses dosyaları:
            │       ├── "Hoe heet je?" (Adın ne?)
            │       ├── "Ik heet..." (Benim adım...)
            │       └── "Aangenaam" (Memnun oldum)
            │
            └── Ödevler:
                    ├── Ödev 1: Kendinizi tanıtın
                    └── Ödev 2: Sayılar quiz'i
```

---

## 📌 İlgili Sayfalar

- [[bases/main-app/ACIKLAMA|← Ana Sistem'e dön]]
- [[bases/main-app/tablolar/kurslar|Kurslar tablosu]]
- [[bases/main-app/tablolar/odevler|Ödevler tablosu]]