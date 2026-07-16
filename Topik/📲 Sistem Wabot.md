# Sistem Wabot — Peta Fungsi & Panduan Operasi

> [!info] Status nota
> Audit awal dibuat pada **16 Julai 2026** melalui akaun Wabot sebenar dan dokumentasi rasmi Fames Automate. Nota ini membezakan fungsi yang kelihatan dalam akaun semasa, fungsi yang terkunci mengikut pelan/izin, dan fungsi yang masih dibangunkan.

## Ringkasan satu ayat

Wabot ialah pusat operasi WhatsApp untuk mengurus akaun/nombor, audiens, fail, chatbot, broadcast, autoresponder, automasi, integrasi dan API dari satu dashboard.

## Keadaan akaun semasa

- Pelan: **Wabot Basic**.
- Satu akaun WhatsApp bernama **Cikgukb** sedang disambungkan.
- Dashboard memaparkan kuota mesej, penggunaan storan, baki kredit AI, aktiviti mesej, kadar kejayaan broadcast, pertumbuhan subscriber dan aktiviti terkini.
- Modul AI Chatbot dan AI Token Usage kelihatan tetapi akses konfigurasi AI disekat oleh pelan/izin semasa.
- Analytics penuh dan Automation V4 masih belum tersedia kepada pengguna biasa pada paparan semasa.

> [!warning] Perkara penting
> Akaun ini menggunakan sambungan **WhatsApp Unofficial API**. Ia fleksibel, tetapi risiko sekatan nombor lebih tinggi berbanding WhatsApp Official API. Elakkan kadar hantaran agresif, senarai tanpa izin dan kandungan berulang yang mencetuskan laporan spam.

## Peta navigasi

### General

#### Dashboard

Fungsi ringkasan operasi:

- penggunaan mesej dan storan;
- baki kredit AI;
- mesej bulan semasa dan jumlah sepanjang hayat;
- kadar kejayaan broadcast;
- bilangan chatbot aktif;
- jumlah dan pertumbuhan subscriber;
- aktiviti mesej mengikut sumber: API, autoresponder, broadcast dan chatbot;
- status akaun WhatsApp;
- aktiviti terkini.

#### Accounts

Pusat pengurusan sambungan WhatsApp:

- lihat status nombor/instance;
- cari dan tapis akaun;
- buka tetapan akaun;
- sambung, sambung semula, tukar atau buang nombor mengikut izin/pelan;
- pantau aktiviti dan jumlah penggunaan.

Amalan operasi: jika bot atau broadcast tidak bergerak, semak **Accounts** dahulu untuk memastikan status masih *Connected*.

#### Audience Hub

Pusat data audiens yang menggabungkan beberapa bahagian:

- **People** — subscriber yang pernah berinteraksi dengan bot dan contact yang disimpan;
- **Follow-Up Center** — mesej follow-up yang dijadualkan serta keputusan follow-up;
- **Subscriber Analytics** — pemerolehan, engagement dan re-engagement, dengan julat 7/30/90 hari atau semua;
- **Broadcast Lists** — senarai nombor yang dimuat naik untuk kempen, termasuk kiraan validasi;
- **Groups** — kumpulan WhatsApp yang disertai oleh nombor tersebut, bersama peserta dan peranan jika data tersedia.

People menyediakan carian, penapis, alat dan susunan data. Broadcast Lists ialah objek berasingan daripada subscriber bot.

#### Templates

Mengurus templat mesej untuk broadcast:

- **Pre-Approved** — templat yang diluluskan Meta untuk Official API;
- **Sequences** — susunan mesej berturutan;
- tapis mengikut akaun;
- sync templat daripada akaun WABA.

Pada akaun semasa tiada templat pre-approved yang diselaraskan.

#### File Manager

Repositori media untuk kegunaan chatbot, broadcast dan autoresponder:

- upload fail;
- cipta folder;
- cari dan tapis mengikut jenis;
- guna semula imej, video, audio atau dokumen;
- hasilkan pautan fail untuk digunakan dalam prompt/aliran tertentu.

Had fail bergantung pada pelan. Paparan autoresponder menyatakan media sehingga 10 MB, tetapi had sebenar akaun/pelan perlu dipatuhi.

#### Integrations

Integrasi yang kelihatan dalam dashboard:

- **Google OAuth** — asas sambungan Google tanpa service account;
- **Google Spreadsheets** — tambah atau kemas kini baris;
- **Telegram Notification** — notifikasi peristiwa ke chat/group ID;
- **WooCommerce** — AI boleh mencipta pesanan, memetakan produk dan menyimpan bukti bayaran;
- **WordPress Plugin** — sync contact, notifikasi dan data pengguna;
- **FunnelKit Connector** — automasi sales funnel dan customer journey;
- **Pabbly Connect** dan **Make** — sambungan aliran kerja dengan aplikasi lain;
- **KlikSini Connector** — pendekkan pautan dan jejak klik.

### Core

#### Chatbots

Wabot mempunyai dua konsep utama:

1. **Keyword chatbot** — padankan kata kunci dengan respons yang ditetapkan.
2. **AI chatbot** — respons generatif, training data, follow-up dan alat tambahan; memerlukan pelan/izin yang sesuai.

Paparan konfigurasi akaun semasa menunjukkan mod **Keyword**. Bahagian yang kelihatan ialah:

- Chatbot Settings;
- Chatbot Items;
- Custom Tools;
- jumlah subscriber yang berkaitan;
- kawalan menjalankan chatbot.

Pada pelan semasa, halaman konfigurasi AI mengembalikan `Permission denied: whatsapp_chatbot_ai`. Oleh itu fungsi AI belum boleh diaudit sepenuhnya dari akaun ini.

#### Broadcast

Aliran mencipta broadcast:

1. Beri nama kempen.
2. Pilih jenis akaun: **Unofficial API** atau **Official API**.
3. Pilih akaun penghantar.
4. Pilih audiens:
   - Contact Groups/Broadcast Lists; atau
   - Segmented Subscriber.
5. Pilih kumpulan untuk dimasukkan.
6. Pilih kumpulan pengecualian jika perlu.
7. Teruskan kepada kandungan, masa penghantaran dan semakan akhir.
8. Selepas berjalan, buka report untuk melihat jumlah dihantar/berjaya/gagal.

> [!danger] Sebelum menghantar
> Pastikan senarai mempunyai izin, buang nombor tidak sah/opt-out, gunakan pengecualian, uji pada senarai kecil, semak media dan pautan, serta elakkan blast besar secara tiba-tiba.

#### Automation

Konsep automasi yang dipaparkan:

- webhook trigger daripada sistem luar;
- label trigger apabila label berubah;
- follow-up berjadual;
- log respons/execution;
- tindakan hantar mesej;
- hantar templat Meta yang diluluskan;
- urus label;
- hantar notifikasi Telegram.

**Status semasa:** Automation V4 masih dalam pembangunan. Dashboard menyatakan automasi sedia ada boleh terus dijalankan melalui V3.

#### Autoresponder

Default Reply dicetuskan apabila tiada kata kunci sepadan dan tiada tetapan chatbot yang sepadan.

Pilihan konfigurasi yang tersedia:

- Enable/Disable;
- sasaran All, Individual atau Group;
- Text & Media;
- pilih media daripada File Manager atau upload;
- teks/caption;
- Normal Mode atau AI Reply Mode;
- tempoh jeda sebelum boleh dicetuskan semula;
- senarai nombor yang dikecualikan;
- Lead Management:
  - forward ke nombor/kumpulan WhatsApp;
  - forward data ke webhook;
  - tambah ke contact group;
  - buang daripada contact group.

Pada akaun semasa, autoresponder belum ditetapkan.

#### Queue Message

Paparan semua mesej yang menunggu untuk dihantar:

- cari penerima;
- tapis status dan tarikh;
- semak mesej tertangguh/gagal;
- padam semua mesej (tindakan berisiko dan tidak patut dibuat tanpa semakan).

#### REST API

API menyokong:

- OAuth 2.0 bearer token;
- client name, redirect URI, scopes dan audiences;
- confidential client dengan client secret sekali paparan;
- OAuth clients dan authorized grants;
- pemilihan instance untuk contoh API;
- endpoint mencipta instance, mendapatkan QR dan menyemak status sambungan;
- contoh request, respons berjaya, errors dan cURL.

Legacy team access token masih disokong untuk integrasi lama. Rahsia API, access token dan client secret tidak boleh disimpan dalam nota Obsidian biasa.

#### Tools — Captions

Perpustakaan caption yang boleh dicari dan digunakan semula. Butang **New Caption** mencipta caption baharu untuk kandungan kempen.

### Support & Team

#### Settings

Tab yang tersedia:

- **Profile** — nama, username, e-mel tetap, telefon dan gambar profil;
- **Preferences** — bahasa paparan dan zon masa; zon masa penting untuk jadual mesej;
- **Security** — tukar kata laluan;
- **Notifications** — notifikasi e-mel/Telegram untuk disconnect, status broadcast, ralat AI, kegagalan penghantaran dan amaran kredit AI;
- **Purchase History** — pembelian dan potongan kredit AI;
- **Activity Log** — audit perubahan mengikut modul, ahli pasukan dan masa.

#### Team

Menu pasukan membezakan ruang kerja/team. Activity Log berguna untuk mengesan siapa membuat perubahan, terutama apabila ramai ahli mengurus broadcast atau akaun.

## Aliran kerja disyorkan

### A. Onboarding nombor baharu

1. Sambung nombor di **Accounts** dan imbas QR.
2. Pastikan status Connected.
3. Tetapkan bahasa dan zon masa.
4. Upload media lazim ke File Manager.
5. Susun contact/broadcast lists dan label.
6. Cipta keyword chatbot atau autoresponder asas.
7. Uji mesej pada nombor sendiri.
8. Baru hidupkan broadcast/automasi secara berperingkat.

### B. Broadcast selamat

1. Bersihkan dan sahkan senarai.
2. Asingkan audiens mengikut konteks/izin.
3. Sediakan pengecualian dan opt-out.
4. Cipta caption dan media yang sesuai.
5. Hantar ujian kecil.
6. Jadualkan mengikut zon masa Malaysia.
7. Pantau Queue dan report.
8. Hentikan/ubah strategi jika kadar gagal, block atau laporan spam meningkat.

### C. Respons automatik

1. Tentukan kata kunci dan intent utama.
2. Cipta jawapan keyword yang spesifik.
3. Tetapkan Default Reply untuk pertanyaan yang tidak sepadan.
4. Guna cooldown supaya pelanggan tidak menerima jawapan berulang.
5. Forward lead bernilai tinggi kepada manusia/webhook.
6. Semak Activity Log dan Follow-Up Center secara berkala.

## Batasan dan perkara belum disahkan

- AI Chatbot tidak dapat diuji penuh kerana pelan/izin semasa.
- Automation V4 belum tersedia; operasi automasi lama bergantung pada V3.
- Analytics penuh masih ditanda *under development* untuk pengguna biasa.
- Groups kosong pada instance semasa, jadi pengurusan peserta/peranan belum dapat diuji.
- Templat Official API belum diselaraskan pada akaun semasa.
- Menghantar mesej sebenar, mengubah tetapan, reconnect nombor dan mencipta token tidak dilakukan semasa audit ini.

## Checklist rutin

### Harian

- [ ] Semak status **Connected**.
- [ ] Semak Queue Message dan kegagalan penghantaran.
- [ ] Semak baki mesej, storan dan kredit AI.
- [ ] Semak notifikasi serta aktiviti luar biasa.

### Sebelum broadcast

- [ ] Izin penerima disahkan.
- [ ] Senarai telah dibersihkan dan diuji.
- [ ] Pengecualian/opt-out dimasukkan.
- [ ] Nama kempen jelas.
- [ ] Kandungan, media dan pautan diuji.
- [ ] Waktu penghantaran sesuai.
- [ ] Pelan pemantauan report tersedia.

### Mingguan

- [ ] Semak pertumbuhan dan engagement subscriber.
- [ ] Semak Follow-Up Center.
- [ ] Semak Activity Log.
- [ ] Buang fail tidak diperlukan jika storan meningkat.
- [ ] Audit chatbot/autoresponder yang sudah lapuk.

## Rujukan rasmi

- [Wabot](https://wabot.my/)
- [Dashboard Wabot](https://app.wabot.io/dashboard)
- [Dokumentasi Wabot](https://docs.fatomate.com/categories/wabot-my)
- [Panduan sambungan WhatsApp](https://docs.fatomate.com/articles/wabot-connection-guide-to-whatsapp)

## Catatan berkaitan

- [[📧 Sistem Kirim.Email]]

