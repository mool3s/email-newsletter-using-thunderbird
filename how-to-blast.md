# 🇮🇩 Cara Email Blasting dengan Thunderbird

Panduan singkat menggunakan Mozilla Thunderbird + Mail Merge untuk kirim massal dengan personalisasi.

## Alat yang Dibutuhkan
1. Mozilla Thunderbird (gratis) – [unduh di sini][thunderbird]
2. Add-on Mail Merge untuk Thunderbird
3. File CSV berisi penerima
4. Template email HTML (tersedia di repo ini)

---

## Install Mail Merge
1. Buka Thunderbird → **Add-ons and Themes**
2. Cari **Mail Merge**
3. Install, lalu restart Thunderbird

---

## Siapkan Data Penerima (CSV)
Buat file, misal `contacts.csv`:

```csv
email,name,company
john@example.com,John Doe,Example Inc
jane@example.com,Jane Smith,Sample Ltd
```

Kolom ini dipakai untuk personalisasi di template.

---

## Siapkan Email Template
1. Buka salah satu file HTML template
2. Salin seluruh isi HTML
3. Di Thunderbird, **Write / Tulis Email Baru** → paste ke body
4. Sesuaikan konten jika perlu

### Contoh Personalisasi
Gunakan placeholder Mail Merge:

```
{{name}}
{{company}}
```

Contoh di email:

```
Halo {{name}},

Terima kasih telah menjadi bagian dari {{company}}.
```

---

## Kirim Email Blasting
1. Setelah email siap, **jangan langsung kirim**.
2. Klik **Mail Merge** (kanan atas).
3. Setel konfigurasi:
   - Source: **CSV**
   - Attachments: kosong
   - Deliver Mode: **Send Later** (lebih aman)
   - Klik **Send** lalu **Start**
4. Untuk benar-benar mengirim: Local Folders → Outbox (klik kanan) → **Send Unsent Messages**

---

# 🇬🇧 How to Do Email Blasting with Thunderbird

Quick guide for Mozilla Thunderbird + Mail Merge to send personalized bulk emails.

## Required Tools
1. Mozilla Thunderbird (free) – [download here][thunderbird]
2. Mail Merge add-on for Thunderbird
3. CSV file with recipients
4. HTML email template (from this repo)

---

## Install Mail Merge
1. Open Thunderbird → **Add-ons and Themes**
2. Search **Mail Merge**
3. Install, then restart Thunderbird

---

## Prepare Recipient Data (CSV)
Create a file, e.g. `contacts.csv`:

```csv
email,name,company
john@example.com,John Doe,Example Inc
jane@example.com,Jane Smith,Sample Ltd
```

These columns become personalization placeholders in the template.

---

## Prepare the Email Template
1. Open any HTML template file
2. Copy all HTML content
3. In Thunderbird, **Write New Email** → paste into the body
4. Adjust content as needed

### Personalization Example
Use Mail Merge placeholders:

```
{{name}}
{{company}}
```

Example in the email:

```
Hi {{name}},

Thanks for being part of {{company}}.
```

---

## Send the Blast
1. When ready, **do not send directly**.
2. Click **Mail Merge** (top right).
3. Configure:
   - Source: **CSV**
   - Attachments: none
   - Deliver Mode: **Send Later** (safer)
   - Click **Send** then **Start**
4. To dispatch: Local Folders → Outbox (right-click) → **Send Unsent Messages**

---

[thunderbird]: https://www.thunderbird.net/
