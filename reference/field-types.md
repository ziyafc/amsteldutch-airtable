---
tags:
  - reference
---

# Field Types

> Airtable'da kullanılan tüm field type'ları.

## 📝 Text Fields

### singleLineText

Tek satırlık text. İsimler, ID'ler, kısa notlar için.

**Kullanıldığı yerler:**
- [[bases/amstel-dutch/tables/product-launches|Product Launches]] - Product Name
- [[bases/expat-student/tables/students|Students]] - First Name, Last Name
- [[bases/main-app/tables/users|Users]] - Email, Name

### multilineText

Çok satırlık text. Notlar, açıklamalar için.

### richText

Formatlanmış text. Bold, italic, listeler destekler.

---

## 🔢 Number Fields

### number

Sayısal değer. Precision ayarlanabilir.

**Options:**
- `precision`: 0-8 arası decimal

### currency

Para birimi formatında sayı.

### percent

Yüzde formatında sayı.

### rating

1-10 arası yıldız rating.

---

## 📅 Date Fields

### date

Sadece tarih.

**Kullanıldığı yerler:**
- [[bases/amstel-dutch/tables/product-launches|Product Launches]] - Launch date
- [[bases/expat-student/tables/students|Students]] - Date of Birth
- [[bases/expat-student/tables/enrollments|Enrollments]] - Enrollment Date

### dateTime

Tarih + saat.

### createdTime

Otomatik: Kayıt oluşturulma zamanı.

### lastModifiedTime

Otomatik: Son değişiklik zamanı. Specific field'lara bağlanabilir.

---

## ✅ Selection Fields

### singleSelect

Tek seçim dropdown.

**Kullanıldığı yerler:**
- [[bases/amstel-dutch/tables/product-launches|Product Launches]] - Status
- [[bases/expat-student/tables/courses|Courses]] - Course Level
- [[bases/expat-student/tables/enrollments|Enrollments]] - Completion Status

**Color Options:**
- `red`, `redLight2`
- `yellow`, `yellowLight2`
- `green`, `greenLight2`
- `blue`, `blueLight2`
- `cyan`, `cyanLight2`
- `teal`, `tealLight2`
- `orange`, `orangeLight2`
- `pink`, `pinkLight2`
- `purple`, `purpleLight2`
- `gray`, `grayLight2`

### multiSelect

Çoklu seçim.

### checkbox

Boolean değer.

**Options:**
- `icon`: check, star, heart, thumbsUp, flag
- `color`: greenBright, yellowBright, etc.

---

## 🔗 Link Fields

### multipleRecordLinks

Tablolar arası ilişki. One-to-many veya many-to-many.

**Options:**
- `linkedTableId`: Hedef tablo ID
- `inverseLinkFieldId`: Karşı taraftaki field
- `prefersSingleRecordLink`: true ise tek link tercih eder

**Kullanıldığı yerler:**
- [[bases/expat-student/tables/enrollments|Enrollments]] - Student, Course
- [[bases/main-app/tables/users|Users]] - Courses, Chats, Tests

### lookup

Linked record'dan değer çekme.

**Options:**
- `recordLinkFieldId`: Hangi link field'dan
- `fieldIdInLinkedTable`: Hangi field'ı çek

### rollup

Linked record'lardan aggregate değer.

**Functions:**
- COUNT, SUM, AVG, MIN, MAX
- ARRAYUNIQUE, ARRAYJOIN
- CONCATENATE

### count

Linked record sayısı. Rollup'un basit hali.

---

## 📐 Computed Fields

### formula

Hesaplanmış değer.

**Örnek formulas:**

```
// String birleştirme
{First Name} & ' ' & {Last Name}

// Tarih farkı
DATETIME_DIFF(TODAY(), {Date}, 'days')

// Koşullu
IF({Status} = 'Completed', TRUE(), FALSE())
```

**Kullanıldığı yerler:**
- [[bases/expat-student/tables/students|Students]] - Full Name, Age
- [[bases/expat-student/tables/enrollments|Enrollments]] - Progress %, Days Since
- [[bases/main-app/tables/users|Users]] - Current Lesson Week

### autoNumber

Otomatik artan sayı. Primary key olarak kullanılabilir.

---

## 🤖 AI Fields

### aiText

AI-generated text. Prompt + referenced fields tanımlanır.

**Kullanıldığı yerler:**
- [[bases/expat-student/tables/courses|Courses]] - Course Summary, Suggested Improvement
- [[bases/main-app/tables/writing-tests|WRITING_TESTS]] - AI assist (Dutch correction)

---

## 👥 People Fields

### singleCollaborator

Tek Airtable kullanıcısı.

### createdBy

Otomatik: Kayıt oluşturan.

### lastModifiedBy

Otomatik: Son düzenleyen.

---

## 📎 Attachment Fields

### multipleAttachments

Dosya ekleri. Görseller, PDF'ler, videolar.

**Options:**
- `isReversed`: Display sırası

---

## 🔗 Other Fields

### url

URL linki.

### email

E-posta adresi.

### phone

Telefon numarası.

### barcode

Barkod/QR code.

---

## 📌 Related

- [[reference/patterns|Common Patterns]]
- [[reference/api-ids|API IDs]]