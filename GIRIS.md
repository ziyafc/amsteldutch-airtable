# Amstel Dutch - Nasıl Çalışır?

> Bu doküman, teknik bilgi gerektirmeden sistemin nasıl çalıştığını anlatır.

## 🎯 Bu Sistem Ne İçin?

Bu sistem, **Hollandaca dil eğitimi** veren bir platformun veritabanıdır. 

Düşün ki bir dil okulu açtın:
- Öğrencilerin var
- Kursların var (A1, A2, B1 seviyeleri)
- Her kursta dersler var
- Her derste ödevler var
- Öğrenciler ödev yapıyor, sen kontrol ediyorsun

Tüm bunları Excel'de tutmak yerine, bu sistem her şeyi **organize ve bağlı** tutuyor.

---

## 📚 4 Farklı Veritabanı Var

Sistemde 4 ayrı "base" (veritabanı) var. Her biri farklı amaç için:

| Veritabanı | Ne İçin? | Detay |
|------------|---------|-------|
| [[bases/main-app/ACIKLAMA\|Ana Uygulama]] | Asıl çalışan sistem | 20 tablo, tüm özellikler |
| [[bases/expat-student/ACIKLAMA\|Expat Student]] | Farklı bir kurs yönetim sistemi | 6 tablo, AI özellikleri |
| [[bases/amstel-dutch/ACIKLAMA\|Amstel Dutch]] | Basit ürün takibi | 1 tablo, çok basit |
| [[bases/dev-staging/ACIKLAMA\|Test Ortamı]] | Geliştirme için | Ana sistemin küçük kopyası |

**En önemlisi [[bases/main-app/ACIKLAMA|Ana Uygulama]]** - asıl çalışan sistem bu.

---

## 🔗 Tablolar Nasıl Bağlı?

Excel'de her şey ayrı dosyalarda olur ve bağlantı kurmak zordur. Burada tablolar birbirine **bağlı**.

Örnek: Bir öğrenci düşün - Ahmet

```
Ahmet (Öğrenci)
    │
    ├── Hangi kursa kayıtlı? → A1 Part 1 kursu
    │       │
    │       └── Bu kursta hangi dersler var? → Ders 1, Ders 2, Ders 3...
    │               │
    │               └── Her derste hangi ödevler var? → Yazı ödevi, Konuşma ödevi...
    │
    ├── Hangi ödevleri tamamladı? → İlerleme tablosunda
    │
    ├── Yazdığı metinler? → Yazı Testleri tablosunda
    │
    └── Öğretmenle konuşmaları? → Sohbetler tablosunda
```

Böylece Ahmet'e tıkladığında, onunla ilgili **her şeyi** görebilirsin.

---

## 📖 Sonraki Adımlar

Her veritabanının detaylı açıklaması için:

1. **Önce [[bases/main-app/ACIKLAMA|Ana Uygulama]]'yı oku** - asıl sistem bu
2. Sonra merak edersen diğerlerine bak

---

## ❓ Sık Sorulan Sorular

### "Tablo" ne demek?
Excel'deki bir sayfa gibi düşün. Her tabloda satırlar (kayıtlar) ve sütunlar (alanlar) var.

### "Bağlantı" ne demek?
Bir tablodaki kayıt, başka tablodaki kayıtla ilişkilendirilebilir. Örneğin "öğrenci" tablosundaki Ahmet, "kurs" tablosundaki A1 kursuyla bağlı.

### "AI alanı" ne demek?
Bazı alanlarda yapay zeka otomatik içerik üretiyor. Örneğin öğrenci bir metin yazdığında, AI otomatik düzeltme ve geri bildirim veriyor.

### Neden 4 farklı veritabanı var?
- Ana sistem (çalışan)
- Test ortamı (denemeler için)
- Diğerleri farklı projeler veya eski versiyonlar