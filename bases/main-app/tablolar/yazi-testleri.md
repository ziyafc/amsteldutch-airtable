# ✉️ Yazı Testleri Tablosu (WRITING_TESTS)

## Bu Tablo Ne İçin?

Bu tabloda **öğrencilerin gönderdiği yazılı metinler** tutuluyor. En önemli özellik: **Yapay zeka otomatik düzeltme yapıyor!**

---

## 🤖 Yapay Zeka Nasıl Çalışıyor?

Bu sistemin en güçlü özelliği bu!

### Adım Adım:

1. **Öğrenci yazıyor:**
   > "Ik ben gaan naar de winkel gisteren"

2. **Yapay zeka analiz ediyor:**
   - Gramer hatalarını buluyor
   - Kelime yanlışlıklarını buluyor
   - Cümle yapısını kontrol ediyor

3. **Yapay zeka geri bildirim veriyor:**
   > **Eski versiyon:** "Ik ben gaan naar de winkel gisteren"
   > 
   > **Düzeltilmiş versiyon:** "Ik ben gisteren naar de winkel gegaan"
   > 
   > **Geri bildirim:** Harika bir cümle kurmaya çalıştın! Kelime dağarcığın iyi.
   > 
   > **Hatalar:**
   > - "ben gaan" yerine "ben gegaan" kullanılır (geçmiş zaman)
   > - Zaman ifadesi (gisteren) cümle ortasına gelir

4. **Öğretmen kontrol eder:**
   - AI doğru mu baktı? 
   - Ekstra not ekler
   - Puan verir

---

## 📝 Bu Tabloda Neler Var?

### Öğrenci Girdisi

| Alan | Açıklama |
|------|--------|
| **Input** | Öğrencinin yazdığı metin |
| **Exercise** | Hangi egzersiz için yazdı? |
| **lesson_Id** | Hangi ders için? |

### Yapay Zeka Çıktısı

| Alan | Açıklama |
|------|--------|
| **AI assist** | Yapay zekanın otomatik üettiği geri bildirim |

### Bağlantılar

| Alan | Ne Gösterir? |
|------|-------------|
| **User_** | Bu yazıyı kim gönderdi? |
| **Chats** | Bu yazı hakkında sohbet var mı? |
| **Course_enrollment** | Öğrencinin kurs bilgisi |

---

## 🔄 Süreç Nasıl İşliyor?

```
Öğrenci                    Sistem                    Öğretmen
   │                         │                          │
   │  1. Metin yazar         │                          │
   │ ─────────────────────► │                          │
   │                         │                          │
   │                    2. AI analiz                    │
   │                       eder                         │
   │                         │                          │
   │  3. AI geri bildirimi   │                          │
   │ ◄───────────────────── │                          │
   │                         │                          │
   │                         │   4. Öğretmen kontrol    │
   │                         │ ────────────────────► │
   │                         │                          │
   │  5. Final geri bildirim │                          │
   │ ◄─────────────────────────────────────────────── │
```

---

## 🎯 AI'nın Dikkat Ettiği Şeyler

Yapay zeka şunlara bakıyor:

1. **Gramer hataları** - Fiil çekimleri, kelime sırası
2. **Yazım hataları** - Yanlış yazılmış kelimeler
3. **Öğrenci seviyesi** - A1 öğrencisine A1 seviyesinde geri bildirim verir
4. **Olumlu şeyler** - "Şunu iyi yapmışsın" der
5. **Hata açıklamaları** - Neden yanlış olduğunu açıklar

---

## 📌 İlgili Sayfalar

- [[bases/main-app/ACIKLAMA|← Ana Sistem'e dön]]
- [[bases/main-app/tablolar/ses-testleri|Ses Testleri]]
- [[bases/main-app/tablolar/sohbetler|Sohbetler]]