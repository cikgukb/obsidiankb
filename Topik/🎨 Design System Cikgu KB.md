---
tags: [design-system, brand, cikgukb]
dicipta: 2026-07-13
sumber: C:\Users\user\Downloads\Cikgu KB Design System.zip
---

# 🎨 Design System Cikgu KB

> [!quote] Konsep
> **"Hitam dan putih"** — identiti monokrom sepenuhnya, diilhamkan daripada watak **Cikgu Shaari** (P. Ramlee) dalam filem *Masam Masam Manis* (1965). Jenama poster-filem yang diterapkan pada dunia pendidikan: bermaruah, nostalgik, kontras tinggi — bukan klinikal.

## 🎨 Warna — TIADA warna jenama!
Drama datang dari **kontras** (dakwat atas kertas / putih atas hitam) dan **tekstur**, bukan warna.

| Token | Nilai | Guna |
|---|---|---|
| `--ink` (film-950) | `#0E0D0B` | Teks utama, permukaan hitam — "dakwat pencetak" hangat, bukan #000 |
| `--ink-soft` (film-700) | `#3A352B` | Teks sekunder |
| `--ink-muted` (film-500) | `#746E5C` | Kapsyen, metadata |
| `--paper` (film-050) | `#F6F1E5` | Latar halaman — macam stok filem lama |
| `--paper-raised` (film-000) | `#FBF8EE` | Kad, helaian |
| `--surface-invert` | `#0E0D0B` | "Kad malam" — scene terbalik putih atas hitam |
| `--line` | `#0E0D0B` | Garisan poster tebal hitam (default) |

Ramp penuh: `--film-000` → `--film-950`, semua warm-tinted (hue ≈ 42). Status pun monokrom — dibezakan dengan **berat**, bukan warna.

## ✍️ Tipografi — 4 suara, 4 tugas

| Font | Token | Tugas |
|---|---|---|
| **Bebas Neue** | `--font-marquee` | Jeritan — tajuk ALL CAPS, name badge, cop, nombor besar |
| **Playfair Display** | `--font-display` | Sentimen — tajuk editorial & pull-quote dialog filem (italic) |
| **Spectral** | `--font-body` | Bacaan — serif hangat untuk teks berjalan |
| **Courier Prime** | `--font-mono` | Cetakan halus — eyebrow, label, kredit, data "call sheet" |

## 📐 Ruang & bentuk
- Skala asas **4px**; container 1200px; ukuran bacaan ~760px
- **Bucu SEGI EMPAT** — radius default 0/2px. Bulat = pengecualian jarang, bukan peraturan (ini cetakan, bukan app-chrome)
- Border **keras dan hitam**: `--border` 1.5px hingga `--border-frame` 6px (bingkai filem berganda)

## 🌑 Bayang & kesan
- Tandatangan: **letterpress offset keras** — `--shadow-press: 4px 4px 0 ink`, *tenggelam bila ditekan*
- Tiada bayang berwarna, tiada glow lembut, tiada bounce
- Foto: WAJIB monokrom (`--filter-bw`), + grain filem (`--tex-grain`), halftone, vignette

## 🎬 Gerakan
- Easing rumah: `--ease-film` `cubic-bezier(.4,0,.2,1)`
- Entrance: **dissolve** (fade, 420ms). Hover: **invert/gelap** (bukan opacity-dim). Press: translate 2px + bayang hilang
- Hormati `prefers-reduced-motion`; tiada loop hiasan infinite

## ✒️ Suara & copy
- Bahasa Melayu hangat, bukan formal-rasmi. Guna "kita" dan "anda/awak"
- Frasa tandatangan: `TERBAIK!`, `TAYANGAN HEBAT`, `PENDAFTARAN DIBUKA`
- Eyebrow gaya **slugline skrip filem**: `EXT. SEKOLAH — PAGI`
- Metadata gaya tiket wayang: `No. 012`, `08:00 PG`, `BILIK 12`
- **TIADA EMOJI** dalam design — personaliti datang dari taip, grain & cop

## 🧩 Komponen (dalam zip: `components/`)
- **Actions**: Button (CTA "tiket" letterpress), IconButton
- **Forms**: Input, Select, Checkbox, Switch (semua bucu keras, isi dakwat pejal)
- **Display**: Card, Badge, **Stamp** ("TERBAIK" cop getah), Tag, Rating, Portrait
- **Brand**: **NameBadge** (pengganti logo!), Marquee, Ticket, FilmDivider, QuoteCard
- **Feedback**: Dialog, Toast, Tooltip

> [!note] Logo
> Tiada logo dicipta — tanda jenama ialah nama **CIKGU KB** dalam taip marquee, atau komponen `NameBadge` (rekaan semula lencana baju).

## 📁 Lokasi fail
- Zip asal: `C:\Users\user\Downloads\Cikgu KB Design System.zip`
- Ekstrak: `tokens/` (colors, typography, spacing, effects) · `components/` · `guidelines/` · `ui_kits/` (website + app pelajar) · `templates/` (poster kelas 1080×1350, slide deck 16:9) · `assets/photos/` (gambar fist & terbaik, versi B&W)
- Ikon: **Lucide** (monoline nipis, `currentColor`) — pengganti sementara, utamakan tanda tipografik (`◆`, `×`, `★`)

## Berkaitan
- Standard wajib setiap web: [[🌐 Standard Pembinaan Web]]

> [!warning] Nota penting
> Design system ini (hitam-putih filem) **berbeza** dari sistem "Arkitek" yang diguna dalam projek ContentForge (krem + biru #2B50C8). Dua identiti berasingan — pilih ikut projek: jenama peribadi Cikgu KB → sistem ini; app/tool lain → bebas.
