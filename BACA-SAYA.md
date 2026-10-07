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

## Simpanan
Kemajuan disimpan dalam pelayar setiap peranti. Gunakan **Tetapan → Sandaran simpanan → Eksport** untuk menyalin kemajuan, dan **Import** untuk memulihkannya di peranti lain.
