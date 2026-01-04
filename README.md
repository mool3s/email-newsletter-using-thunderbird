# 🇮🇩 Email Newsletter dengan Thunderbird

Template HTML siap pakai untuk kampanye newsletter menggunakan Mozilla Thunderbird + add-on Mail Merge. Fokusnya ringan dan kompatibel dengan mayoritas email client.

## Mengapa Thunderbird?
- Gratis, open source, dan mendukung add-on Mail Merge untuk personalisasi massal.
- Sumber data fleksibel: CSV, Excel (.xlsx), JSON, atau Address Book.
- Alternatif yang lebih bebas lisensi dibandingkan Outlook (tidak butuh akun Microsoft atau Excel).

## Isi Template
| File | Keterangan |
|------|------------|
| template-1.html | Layout newsletter sederhana |
| template-2.html | Layout newsletter variasi 2 |
| template-3.html | Layout newsletter variasi 3 |
| template-with-content.html | Contoh lengkap dengan teks & gambar |

## Cara Cepat Pakai (ringkas)
1) Instal Thunderbird ([unduh di sini][thunderbird]) dan add-on Mail Merge.
2) Siapkan CSV penerima minimal dengan kolom `email` (opsional `name`, `company`, dll.).
3) Buka salah satu template HTML, salin seluruh isi, lalu paste ke body email baru di Thunderbird.
4) Personalisasi dengan placeholder Mail Merge, contoh `{{name}}` atau `{{company}}`.
5) Pilih menu Mail Merge → Source: CSV → Deliver Mode: Send Later → Start.
6) Kirim melalui Local Folders → Outbox → Send Unsent Messages.

Detail langkah lebih lengkap ada di how-to-blast.md.

## Personalisasi Contoh
```
Halo {{name}},

Terima kasih telah menjadi bagian dari {{company}}.
```

## Catatan Teknis
- HTML sederhana, CSS inline untuk kompatibilitas email client.
- Tidak ada JavaScript atau external assets berat.
- Siap dipakai untuk email blasting lintas tool yang mendukung HTML.

---

# 🇬🇧 Email Newsletter (English)

Ready-to-use HTML templates for Thunderbird + Mail Merge, kept light for broad email client compatibility.

## Why Thunderbird?
- Free, open source, and supports the Mail Merge add-on for personalized bulk sends.
- Flexible data sources: CSV, Excel (.xlsx), JSON, or Address Book.
- License-free alternative to Outlook (no Microsoft account or Excel dependency).

## Templates
| File | Description |
|------|-------------|
| template-1.html | Simple newsletter layout |
| template-2.html | Alternate layout 2 |
| template-3.html | Alternate layout 3 |
| template-with-content.html | Full example with text & images |

## Quick Start
1) Install Thunderbird ([download here][thunderbird]) and the Mail Merge add-on.
2) Prepare a CSV with `email` (and optional fields like `name`, `company`).
3) Open any HTML template, copy all content, and paste it into a new email body in Thunderbird.
4) Add placeholders such as `{{name}}` or `{{company}}` for personalization.
5) Open Mail Merge → Source: CSV → Deliver Mode: Send Later → Start.
6) Send via Local Folders → Outbox → Send Unsent Messages.

See how-to-blast.md for the detailed walkthrough.

## Personalization Example
```
Hi {{name}},

Thanks for being part of {{company}}.
```

## Technical Notes
- Lightweight HTML, inline CSS for maximum client compatibility.
- No JavaScript or heavy external assets.
- Safe to reuse in other email tools that accept HTML.

[thunderbird]: https://www.thunderbird.net/
