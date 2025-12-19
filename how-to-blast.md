# How to Do Email Blasting using Thunderbird

## Tools yang Dibutuhkan

1. **Mozilla Thunderbird** (gratis)
2. **Mail Merge Add-on** untuk Thunderbird
3. File **CSV** berisi daftar penerima
4. Template email **HTML** (seperti yang ada di repository ini)

---

## Install Mail Merge Add-on

1. Buka Mozilla Thunderbird
2. Masuk ke menu **Add-ons and Themes**
3. Cari **Mail Merge**
4. Install add-on tersebut
5. Restart Thunderbird

---

## Menyiapkan Data Penerima (CSV)

Buat file CSV sederhana, contoh: `contacts.csv`

```csv
email,name,company
john@example.com,John Doe,Example Inc
jane@example.com,Jane Smith,Sample Ltd
```

Nama kolom ini nantinya akan digunakan untuk personalisasi email.

---

## Menyiapkan Email Template

1. Buka salah satu file template HTML
2. Salin seluruh isi HTML
3. Buka **Write / Tulis Email Baru** di Thunderbird
4. Paste HTML ke body email
5. Sesuaikan konten jika diperlukan

### Contoh Personalisasi

Gunakan format variabel dari Mail Merge:

```
{{name}}
{{company}}
```

Contoh penggunaan di email:

```
Halo {{name}},

Terima kasih telah menjadi bagian dari {{company}}.
```

---

## Melakukan Email Blasting

1. Setelah email siap, **jangan langsung kirim**
2. Klik menu **Mail Merge** di bagian kanan atas
3. Atur konfigurasi:

   * Source: **CSV**
   * Attachments: Kosongkan
   * Deliver Mode: **Send Later** (Lebih baik untuk "Send Later" untuk mencegah bug
   * Klik "Send" kemudian "Start"
4. Kemudian untuk mengirim, ke Local Folder > Outbox (Klik kanan) > Send Unsent Messagess


---
