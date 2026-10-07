# LO:TONG: a little school story (versi PWA)

Folder ini membolehkan LO:TONG **dipasang** pada telefon, tablet atau Chromebook seperti aplikasi, dan **dimainkan tanpa internet**.

## Kandungan
| Fail | Kegunaan |
|---|---|
| `index.html` | Game LO:TONG |
| `manifest.webmanifest` | Maklumat aplikasi (nama, ikon, mod skrin penuh landskap) |
| `sw.js` | Service worker untuk main tanpa internet |
| `icon-*.png`, `apple-touch-icon.png` | Ikon aplikasi |

## Hos di GitHub Pages
1. Cipta repositori baharu di GitHub, contohnya `lotong`.
2. Muat naik **semua fail dalam folder ini** ke repositori itu (bukan folder itu sendiri). Pastikan `index.html` berada di akar repositori.
3. Pergi ke **Settings → Pages**. Di bawah *Build and deployment*, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, kemudian **Save**.
4. Tunggu 1 hingga 2 minit. Game boleh dibuka di `https://NAMA-PENGGUNA.github.io/lotong/`.

## Pasang pada peranti
- **Android / Chromebook (Chrome):** buka pautan di atas, tunggu sehingga halaman dimuatkan sepenuhnya, kemudian tekan butang **📲 Pasang Game** di muka depan. Butang ini juga boleh didapati melalui menu Chrome → *Pasang aplikasi*.
- **iPhone / iPad (Safari):** tekan butang **Kongsi**, kemudian **Tambah ke Skrin Utama**.

## Main tanpa internet
Buka game **sekali dengan internet** selepas dipasang, supaya Three.js dan fon disimpan dalam peranti. Selepas itu, game boleh dimainkan walaupun tanpa internet.

## Mengemas kini game
Apabila `index.html` diganti dengan versi baharu, tukar juga `VERSI` di baris atas `sw.js` (contohnya `lotong-v2`). Peranti akan memuat turun versi baharu apabila dibuka dengan internet.

## Jika aplikasi Android tidak terbuka atau pegun
1. Buang aplikasi LO:TONG lama dari skrin utama (tekan lama ikon → *Nyahpasang* / *Buang*).
2. Buka pautan GitHub Pages dalam Chrome dan tunggu muka depan dimuatkan. Muat semula halaman sekali.
3. Pasang semula melalui butang **📲 Pasang Game** atau menu Chrome → *Pasang aplikasi*.
4. Jika game masih tidak bermula selepas 15 saat, skrin akan menunjukkan butang **Baiki & muat semula**. Butang ini membersihkan salinan lama dan memuat turun semula game.

## Papan Anugerah Mingguan (dikongsi seluruh sekolah)
Tanpa langkah ini, Papan Anugerah hanya menunjukkan profil dalam peranti yang sama. Supaya semua murid melihat papan yang sama:

1. Buka [Google Sheets](https://sheets.google.com) dan cipta helaian baharu, contohnya **LO:TONG Papan Anugerah**.
2. Pilih menu **Sambungan → Apps Script**. Padam kod sedia ada, kemudian tampal semua kandungan fail `papan-anugerah.gs`. Tekan **Simpan**.
3. Tekan **Gunakan (Deploy) → Penggunaan baharu**. Pilih jenis **Aplikasi web**:
   - *Laksanakan sebagai:* **Saya**
   - *Siapa yang mempunyai akses:* **Sesiapa sahaja (Anyone)**
4. Tekan **Gunakan**, benarkan akses akaun Google, dan salin **URL aplikasi web** (berakhir dengan `/exec`).
5. Buka `index.html`, cari baris `const PAPAN_URL = '...';` dan tampal URL itu di antara tanda petikan. (URL Apps Script cikgu sudah dimasukkan dalam versi ini.)
6. Muat naik `index.html` yang dikemas kini ke GitHub, dan tukar `VERSI` dalam `sw.js`.

**Mengurus papan:** markah murid muncul dalam helaian **Pemain**. Untuk menyorok nama yang tidak sesuai, taip `ya` dalam lajur **sorok**. Murid juga boleh menyorok nama sendiri melalui **Tetapan → Nama di Papan Anugerah**.

**Nota:** markah dihantar oleh peranti murid, jadi papan ini sesuai untuk motivasi, bukan untuk penilaian rasmi. Gunakan nama panggilan sahaja, bukan nama penuh.

## Main Bersama (Geng)
- Tekan **🤝** dalam permainan (atau **Main Bersama** di muka depan). Seorang murid tekan **Buka Geng** dan mendapat **Kod Geng** (contoh `LTG-4821`); kawan tekan **Sertai** dan masukkan 4 nombor itu. Sehingga 4 orang dalam satu geng.
- Ketua geng memilih aktiviti: **Gotong-royong kutip sampah** atau **Cari kad huruf bersama**. Semua ahli mendapat ganjaran apabila selesai.
- Hanya emoji dan ayat sedia boleh dihantar; tiada chat bebas.
- Perlu internet, dan hanya berfungsi dari GitHub Pages (bukan pautan claude.ai). Jika rangkaian sekolah menyekat sambungan, cuba hotspot telefon.

## Simpanan
Kemajuan disimpan dalam pelayar setiap peranti. Gunakan **Tetapan → Sandaran simpanan → Eksport** untuk menyalin kemajuan, dan **Import** untuk memulihkannya di peranti lain.
