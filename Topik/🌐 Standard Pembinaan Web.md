---
tags: [standard, web, dna-cikgukb]
dicipta: 2026-07-13
status: aktif
---

# 🌐 Standard Pembinaan Web — DNA Cikgu KB

> [!important] Peraturan wajib
> Setiap web app yang dibina **MESTI** ada 3 perkara ni sebelum dianggap siap. Tiada pengecualian.

## ✅ Senarai semak wajib

### 1. Favicon
- Format: SVG (`assets/favicon.svg`) — ringan, tajam pada semua saiz
- Fallback: sediakan juga route `/favicon.ico` yang layan SVG yang sama
- Design: monogram ringkas atas warna jenama projek (cth: "CF" untuk ContentForge)
- Tag dalam `<head>`:
  ```html
  <link rel="icon" type="image/svg+xml" href="assets/favicon.svg">
  ```

### 2. Preview image (Open Graph) — untuk share link WhatsApp/FB/Telegram
- Saiz: **1200 × 630 px**, JPEG, bawah 300 KB (WhatsApp reject imej besar)
- Kandungan: nama app besar + tagline + "Dibuat oleh cikgukb.my"
- URL imej mesti **absolute** (penuh dengan https://), bukan relative
- Tag wajib dalam `<head>` **setiap halaman**:
  ```html
  <meta property="og:type" content="website">
  <meta property="og:title" content="NamaApp — Tagline">
  <meta property="og:description" content="Ayat ringkas jual app ni.">
  <meta property="og:url" content="https://domain-app/">
  <meta property="og:image" content="https://domain-app/assets/og-image.jpg">
  <meta property="og:image:width" content="1200">
  <meta property="og:image:height" content="630">
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:image" content="https://domain-app/assets/og-image.jpg">
  ```
- **Nota WhatsApp**: WhatsApp cache preview. Kalau dah pernah hantar link sebelum OG dipasang, tambah `?v=2` pada link untuk paksa preview baru.

### 3. Footer credit
- Setiap halaman mesti ada di footer:
  ```html
  <p>Dibuat oleh <a href="https://cikgukb.my" target="_blank" rel="noopener">cikgukb.my</a></p>
  ```
- Link mesti **boleh tekan** dan buka tab baru.

## 📌 Projek yang dah patuh standard ni
- **ContentForge** — https://contentforge-ai.kbcimb.workers.dev (2026-07-13)

## Rujukan
- Design system rasmi: [[🎨 Design System Cikgu KB]]
- Semak preview OG: https://www.opengraph.xyz atau hantar link kat WhatsApp diri sendiri
