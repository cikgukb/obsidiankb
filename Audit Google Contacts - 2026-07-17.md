---
title: Audit Google Contacts
date: 2026-07-17
tags:
  - google-contacts
  - audit
  - email
  - phone
  - marketing
status: completed
consent_status: unknown
---

# Audit Google Contacts — 17 Julai 2026

## Ringkasan

| Metrik | Jumlah |
|---|---:|
| Kontak sumber | 7,311 |
| Rekod email sah sebelum deduplikasi | 260 |
| **Email unik dengan nama** | **250** |
| Rekod email pendua digabungkan | 10 |
| Kontak tanpa kombinasi nama + email sah | 7,064 |
| Rekod bersih dengan nombor utama | 236 |
| Rekod dengan nombor mobile tambahan | 34 |
| Isu normalisasi telefon | 22 |

## Struktur senarai bersih

- `Name`
- `Email`
- `Labels`
- `Phone Number`
- `Mobile Phone 2`
- `Mobile Phone 3`

Setiap email hanya muncul sekali. `Phone Number` ialah nombor utama pertama yang sah. Nombor tambahan dimasukkan dalam sel tersendiri dan hanya diterima sebagai mobile berdasarkan pola Malaysia atau label mobile untuk nombor antarabangsa.

## Fail

- [[Attachments/Google_Contacts_Name_Email_Audit_2026-07-17.xlsx|Buka workbook audit]]
- [[Attachments/Google_Contacts_Name_Email_Unique_2026-07-17.csv|Buka CSV nama + email unik]]
- [[Attachments/Google_Contacts_Original_2026-07-17.csv|Buka eksport Google Contacts asal]]

## Pemeriksaan

- Jumlah eksport sepadan dengan paparan Google Contacts: **7,311**.
- Tiada email pendua dalam CSV bersih.
- Semua baris CSV mempunyai nama dan email sah.
- Semua telefon dalam CSV menggunakan format E.164.
- Nombor Malaysia dalam lajur mobile tambahan mesti bermula dengan `+601`.
- 22 nombor yang rosak atau mempunyai kod negara tidak jelas diasingkan dalam sheet **Phone Issues**.

> [!warning] Persetujuan pemasaran
> Status consent tidak tersedia dalam Google Contacts dan dianggap **Unknown**. CSV ini lulus audit teknikal tetapi bukan bukti bahawa penerima telah memberi persetujuan untuk menerima promosi.

## Keselamatan

- Data diproses secara lokal.
- Tiada kontak Google diubah atau dipadam.
- Tiada email atau mesej blasting dihantar.

