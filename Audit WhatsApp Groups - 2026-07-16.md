---
title: Audit WhatsApp Groups
date: 2026-07-16
tags:
  - whatsapp
  - audit
  - group
  - wabot
status: completed-with-unverified-records
---

# Audit WhatsApp Groups — 16 Julai 2026

## Ringkasan

| Kategori | Jumlah |
|---|---:|
| Grup aktif diaudit | 117 |
| Rekod Archived dikenal pasti | 144 |
| **Only admin can send** | **28** |
| **5 ahli atau kurang** | **7** |
| **Grup aktif melebihi 20 ahli** | **81** |
| Rekod dengan sekurang-kurangnya satu medan `Unable to verify` | 126 |

> [!warning] Rekod belum dapat disahkan
> Sebahagian sejarah Archived lama gagal dimuatkan secara stabil oleh WhatsApp Web. Rekod tersebut dikekalkan dalam Audit Log sebagai `Unable to verify` dan tidak dianggap memenuhi mana-mana kategori tanpa bukti.

## Grup dengan 5 ahli atau kurang

| Group Name | Folder | Ahli | Send Permission |
|---|---|---:|---|
| Kb X Kalodata | Active | 2 | All members |
| Bank rakyat Hackhaton | Active | 3 | All members |
| iwstay group | Active | 3 | All members |
| Family mama apak | Active | 4 | All members |
| Familyku Syurgaku | Active | 4 | All members |
| BMC Apps | Active | 4 | All members |
| Tuisyen ai batch 1 | Active | 4 | All members |

## Hasil audit

- 28 grup disahkan sebagai `Admins only`.
- 81 grup aktif mempunyai lebih daripada 20 ahli.
- Grup yang mempunyai tepat 5 ahli turut termasuk dalam kriteria kumpulan kecil.
- Semua rekod lengkap berada dalam fail Excel di bawah.

## Fail audit

- [[Attachments/WhatsApp_Group_Audit_2026-07-16.xlsx|Buka fail Excel audit WhatsApp]]

## Kaedah dan keselamatan

- Audit dibuat terus melalui WhatsApp Web.
- WA Gear tidak digunakan.
- Permission disemak melalui **Group Permissions** atau notis WhatsApp yang tersedia.
- Bilangan ahli disemak melalui **Group Info**.
- Tiada mesej dihantar.
- Tiada tetapan atau keahlian grup diubah.

