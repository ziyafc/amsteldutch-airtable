# ✅ Ödevler Tablosu (Tasks)

## Bu Tablo Ne İçin?

Bu tabloda **öğrencilerin yapması gereken görevler** tutuluyor. Her ders birkaç ödev içerir.

---

## 📝 Bu Tabloda Neler Var?

### Ödev İçeriği

| Alan | Açıklama | Örnek |
|------|---------|-------|
| **Name** | Ödevin adı/açıklaması | "Kendinizi tanıtın" |
| **Introduction** | Ödeve giriş | "Bu ödevde Hollandaca kendinizi tanıtacaksınız" |
| **Notes** | Ekstra notlar | "En az 5 cümle yazın" |
| **Module_icon** | Ödevin ikonu | (öğrenci arayüzünde görünür) |
| **Video** | Açıklama videosu | |
| **Bijlage** | Ek dosyalar | PDF, resim vs. |

### Ödev Türleri

Farklı türde ödevler olabilir:

| Alan | Ne Demek? |
|------|----------|
| **Module_Dialoog** | Diyalog ödevi |
| **Module_Speaking** | Konuşma ödevi |
| **Module_Conversation** | Sohbet ödevi |

### Durum ve Kontrol

| Alan | Açıklama |
|------|--------|
| **Status** | Yapılacak / Devam ediyor / Tamamlandı |
| **Teacher Check** | Öğretmen kontrolü gerekiyor mu? ✅/❌ |
| **ID** | Otomatik ödev numarası |

### Linkler

| Alan | Ne İçin? |
|------|--------|
| **Test Url** | Online test sayfası linki |
| **Flashcard url** | Kelime kartları sayfası linki |

### Bağlantılar

| Alan | Ne Gösterir? |
|------|-------------|
| **Lesson** | Bu ödev hangi derse ait? |
| **Progress** | Kim bu ödevi yaptı? |
| **Questions** | Bu ödevde hangi sorular var? |

---

## 🔗 Ödev Yapısı

```
Ders 1: Tanışma
    │
    ├── Ödev 1: Kendinizi Tanıtın
    │       │
    │       ├── Tür: Yazma ödevi
    │       ├── Öğretmen kontrolü: Evet
    │       └── Durum: Aktif
    │
    ├── Ödev 2: Sayılar Quiz'i
    │       │
    │       ├── Tür: Çoktan seçmeli
    │       ├── 10 soru içeriyor
    │       └── Otomatik puanlama
    │
    └── Ödev 3: Diyalog Uygulaması
            │
            ├── Tür: Konuşma ödevi
            └── Ses kaydı gerekiyor
```

---

## 🎯 Öğretmen Kontrolü

Bazı ödevlerde "Teacher Check" işaretli:
- Öğrenci ödevi yapar
- Sistem otomatik kaydeder
- **Öğretmen kontrol edip onaylar**
- Onaydan sonra "İlerleme" tablosuna işlenir

---

## 📌 İlgili Sayfalar

- [[bases/main-app/ACIKLAMA|← Ana Sistem'e dön]]
- [[bases/main-app/tablolar/dersler|Dersler tablosu]]
- [[bases/main-app/tablolar/ilerleme|İlerleme tablosu]]
- [[bases/main-app/tablolar/sorular|Sorular tablosu]]