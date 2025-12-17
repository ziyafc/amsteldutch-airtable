# 1. Giriş - Temel Kavramlar

Önce bazı temel kavramları öğrenelim. Bunları anlamadan devam etmek zor olur.

---

## 📦 Veritabanı Nedir?

Veritabanı, **bilgileri düzenli şekilde sakladığımız bir yerdir**.

### Günlük Hayattan Örnek

Telefonundaki **Rehber** uygulamasını düşün:
- Her kişinin adı var
- Her kişinin telefon numarası var
- Her kişinin email adresi var
- Belki fotoğrafı var

İşte rehber uygulaması aslında küçük bir veritabanı. Bilgileri düzenli tutuyor ve istediğinde kolayca bulmanı sağlıyor.

### Bizim Sistemimiz

Biz de aynı mantıkla:
- Öğrencilerin bilgilerini tutuyoruz
- Kursların bilgilerini tutuyoruz
- Derslerin bilgilerini tutuyoruz
- Ve bunların hepsini birbirine bağlıyoruz

---

## 📋 Tablo Nedir?

Tablo, **aynı türden bilgileri sakladığımız bir listedir**.

### Excel Biliyor musun?

Eğer Excel kullandıysan, tablo tam olarak Excel sayfası gibi:
- **Satırlar** = Her bir kayıt (mesela her bir öğrenci)
- **Sütunlar** = Bilgi türleri (mesela ad, email, telefon)

### Örnek: Öğrenci Tablosu

| Ad | Email | Telefon | Kursu |
|----|-------|---------|-------|
| Ahmet Yılmaz | ahmet@email.com | 555-1234 | A1 |
| Ayşe Kaya | ayse@email.com | 555-5678 | A2 |
| Mehmet Demir | mehmet@email.com | 555-9012 | A1 |

Gördüğün gibi:
- Her **satır** bir öğrenci
- Her **sütun** bir bilgi türü (buna "alan" veya "field" diyoruz)

---

## 🔗 Tablolar Arası Bağlantı Nedir?

Bu en önemli kavram. Tablolar birbirine **bağlanabiliyor**.

### Neden Bağlantı Lazım?

Düşün ki sadece 1 tablomuz var ve her şeyi oraya yazıyoruz:

| Öğrenci | Email | Kurs Adı | Kurs Seviyesi | Öğretmen | Öğretmen Email |
|---------|-------|----------|---------------|----------|----------------|
| Ahmet | ahmet@email.com | Hollandaca A1 | Başlangıç | Jamila | jamila@okul.com |
| Ayşe | ayse@email.com | Hollandaca A1 | Başlangıç | Jamila | jamila@okul.com |
| Mehmet | mehmet@email.com | Hollandaca A2 | Orta | Anne | anne@okul.com |

**Sorunlar:**
1. "Jamila" ve "jamila@okul.com" tekrar tekrar yazılmış
2. Jamila'nın emaili değişirse her yerde tek tek değiştirmemiz lazım
3. Tablo çok karmaşık oluyor

### Çözüm: Ayrı Tablolar + Bağlantı

**Öğrenciler Tablosu:**
| Ad | Email | Kursu |
|----|-------|-------|
| Ahmet | ahmet@email.com | → A1 Kursu |
| Ayşe | ayse@email.com | → A1 Kursu |
| Mehmet | mehmet@email.com | → A2 Kursu |

**Kurslar Tablosu:**
| Kurs Adı | Seviye | Öğretmen |
|----------|--------|----------|
| A1 Kursu | Başlangıç | → Jamila |
| A2 Kursu | Orta | → Anne |

**Öğretmenler Tablosu:**
| Ad | Email |
|----|-------|
| Jamila | jamila@okul.com |
| Anne | anne@okul.com |

Şimdi:
- Her bilgi **bir kere** yazılıyor
- Jamila'nın emaili değişirse **sadece 1 yerde** değiştiriyoruz
- Her tablo **kendi işine** bakıyor

"→" işareti **bağlantıyı** gösteriyor. Ahmet'in "Kursu" alanı, Kurslar tablosundaki "A1 Kursu"na bağlı.

---

## 🏢 Bizim Sistemimizde Kaç Veritabanı Var?

4 tane ayrı veritabanımız var:

| # | Veritabanı | Ne İçin? | Kaç Tablo? |
|---|------------|----------|------------|
| 1 | **Ana Sistem** | Gerçekten kullandığımız sistem | 20 tablo |
| 2 | Expat Student | Farklı bir proje denemesi | 6 tablo |
| 3 | Amstel Dutch | Çok basit bir takip sistemi | 1 tablo |
| 4 | Test Ortamı | Denemeleri yaptığımız yer | 5 tablo |

**En önemlisi "Ana Sistem"** - öğrencilerin ve öğretmenlerin gerçekten kullandığı sistem bu.

---

## 💡 Şimdiye Kadar Ne Öğrendik?

✅ **Veritabanı** = Bilgileri düzenli sakladığımız yer  
✅ **Tablo** = Aynı türden bilgilerin listesi (Excel sayfası gibi)  
✅ **Satır** = Tek bir kayıt (mesela bir öğrenci)  
✅ **Sütun/Alan** = Bir bilgi türü (mesela email)  
✅ **Bağlantı** = Bir tablodaki kayıt, başka tablodaki kayıtla ilişkilendirilebilir

---

## ➡️ Sonraki Adım

Şimdi asıl sistemi inceleyelim:

**[[bases/main-app/ACIKLAMA|2. Ana Sistem →]]**
