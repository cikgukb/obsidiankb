# MCP Blasting Wabot dan Kirim.Email

Tarikh dibina: 16 Julai 2026

## Tujuan

MCP tempatan ini menyediakan alat selamat untuk menyediakan dan menjalankan kerja blasting melalui Wabot dan KIRIM.EMAIL. Ia didaftarkan dalam Codex sebagai `wabot_kirimemail`.

Lokasi projek:

`C:\Users\user\Documents\Codex\2026-07-16\tol\outputs\wabot-kirimemail-mcp`

## Keupayaan

### Wabot

- semak instance dan nombor WhatsApp;
- bersihkan, nyahpendua dan preview senarai penerima;
- blast teks secara bersiri dengan sela masa;
- hantar media;
- batalkan mesej dalam queue.

### KIRIM.EMAIL

- lihat list, subscriber dan broadcast;
- preview subjek, kandungan dan jadual;
- cipta atau jadualkan broadcast kepada satu list.

## Kunci keselamatan

Penghantaran sebenar memerlukan ketiga-tiga syarat serentak:

1. `BLASTING_ENABLED=true` dalam fail `.env`;
2. arahan MCP menggunakan `execute=true`;
3. kod pengesahan sepadan dengan `BLAST_CONFIRMATION_CODE`.

Konfigurasi asal ialah `BLASTING_ENABLED=false`. Token API tidak boleh disimpan dalam Obsidian.

## Persediaan sekali sahaja

Isi fail `.env` projek dengan Wabot access token, Wabot instance ID, username KIRIM.EMAIL dan API token KIRIM.EMAIL. Selepas itu buka semula Codex supaya konfigurasi dibaca.

## Aliran kerja disyorkan

1. Panggil `system_health`.
2. Semak sambungan/list.
3. Buat preview dan bersihkan penerima.
4. Semak izin, opt-out, kandungan, pautan dan masa.
5. Minta pengesahan manusia.
6. Barulah aktifkan penghantaran dan gunakan kod pengesahan.
7. Pantau queue/report selepas penghantaran.

## Arahan contoh kepada Codex

> Gunakan MCP wabot_kirimemail. Semak kesihatan dan preview senarai ini sahaja. Jangan hantar.

> Sediakan preview broadcast KIRIM.EMAIL untuk list yang saya pilih. Jangan execute sehingga saya sahkan.

## Catatan berkaitan

- [[📲 Sistem Wabot]]
- [[📧 Sistem Kirim.Email]]
