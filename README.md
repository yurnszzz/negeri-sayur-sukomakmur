![Negeri Sayur Sukomakmur — catatan perjalanan, HTML dan CSS](docs/media/readme-header.svg)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css&logoColor=white)
[![Lisensi source code MIT](https://img.shields.io/badge/License-MIT-24513F?style=flat)](LICENSE)

# Negeri Sayur Sukomakmur

Website satu halaman tentang Negeri Sayur Sukomakmur di Dusun Nampan, Desa Sukomakmur, Kecamatan Kajoran, Kabupaten Magelang. Tampilannya mengambil bentuk jurnal perjalanan: warna kertas hangat, hijau hutan, foto berbingkai, dan formulir seperti kartu pos.

Mini project individu **Study Club Frontend Basic KSM Veterantech UPNVJ 2026**, dibuat oleh **Hasan Shofiyyur Rahman**. Proyek ini merupakan latihan frontend, bukan situs resmi pengelola wisata.

[Repository GitHub](https://github.com/yurnszzz/negeri-sayur-sukomakmur)

## Preview

![Preview halaman utama Negeri Sayur Sukomakmur](docs/media/preview-hero.png)

[Halaman penuh desktop](docs/media/preview-desktop.png) · [Halaman penuh ponsel](docs/media/preview-mobile.png) · [Menu ponsel terbuka](docs/media/preview-mobile-menu.png)

Screenshot diambil dari implementasi di Chrome pada 18 Oktober 2026. Header SVG di awal README merupakan ilustrasi dokumentasi beranimasi.

## Cara membuka

1. Unduh atau clone repository ini.
2. Buka `index.html` langsung di browser, atau pilih **Open with Live Server** pada file tersebut di VS Code.

Tidak diperlukan instalasi dependency, build, atau server aplikasi. Seluruh stylesheet, logo, dan foto memakai file lokal. Tautan ke Google Maps, media sosial, dan referensi memerlukan koneksi internet saat dibuka.

## Fitur dan teknologi

Website memakai **HTML5 dan satu file CSS native**, tanpa JavaScript, framework, atau backend. Georgia dan Arial menggunakan font sistem.

- Header desktop ringkas dengan tautan langsung; ponsel memakai menu **Menu/Tutup** melalui `details` dan `summary` native.
- Navbar sticky dengan animasi mengambang saat scroll pada browser yang mendukung CSS scroll timeline. Browser lain dan mode reduced motion memakai versi sticky tanpa animasi.
- Hero dengan foto lanskap utuh, cerita perjalanan, daftar aktivitas, dan tabel informasi kunjungan.
- Tiga rekomendasi wisata dalam bingkai besar berjajar di desktop/tablet dan satu kolom di ponsel.
- Form kartu pos dengan validasi bawaan browser, kredit foto buka/tutup, skip link, dan fokus keyboard yang terlihat.

Flexbox menyusun navigasi dan kelompok tombol. Grid mengatur hero, cerita, serta rekomendasi. Media query menyesuaikan layout pada layar kecil. Penjelasan kode dan bahan presentasi tersedia di [catatan belajar](docs/LEARNING-NOTES.md).

Menu ponsel tetap terbuka setelah memilih tujuan; tekan **Tutup** untuk menutupnya. Penanda navigasi mengikuti tujuan anchor yang dipilih.

## Mencoba formulir

Form adalah **demo validasi HTML**. Coba kirim dalam keadaan kosong, gunakan email yang tidak valid, lalu isi dengan data contoh yang valid.

Form menggunakan `method="get"` dan `action="#kontak"`. Setelah valid, browser membuka kembali halaman dengan isian sebagai parameter URL. Form belum mengirim pesan, menyimpan data pada aplikasi, atau membuat reservasi. Gunakan data contoh. Tautan **Kirim email** terpisah membuka aplikasi email.

## Struktur proyek

```text
negeri-sayur-sukomakmur/
├── index.html
├── assets/
│   ├── css/style.css
│   └── images/
│       ├── brand/
│       ├── destination/
│       └── recommendations/
├── docs/
│   ├── ASSETS.md
│   ├── LEARNING-NOTES.md
│   └── media/
│       ├── readme-header.svg
│       ├── preview-hero.png
│       ├── preview-desktop.png
│       ├── preview-mobile.png
│       └── preview-mobile-menu.png
├── README.md
├── LICENSE
└── .gitignore
```

Sumber utama yang diedit adalah `index.html` dan `assets/css/style.css`. Berkas pengumpulan dibuat sebagai salinan lokal dari sumber beserta seluruh gambar; folder `submission/` tidak dilacak Git.

## Pemeriksaan

Implementasi diperiksa di **Chrome**, melalui file lokal dengan JavaScript dinonaktifkan, pada lebar **1440, 1366, 768, 390, dan 320 px**. Pemeriksaan mencakup gambar lokal, overflow, navigasi anchor, menu ponsel, keyboard, simulasi sentuhan, validasi form, navbar saat scroll, dan reduced motion.

Hasil pemeriksaan: halaman sumber **35/35**, HTML ekspor **37/37**, navbar **84/84**, serta pemeriksaan tambahan proporsi dan menu **66/66** lolos. Cakupan tiap rangkaian tersedia di [catatan pemeriksaan](docs/LEARNING-NOTES.md#pemeriksaan). Safari, Firefox, perangkat fisik, pembaca layar, dan zoom browser 200% belum diuji.

## Foto dan informasi wisata

Dua varian logo asli dan enam foto disimpan secara lokal. Foto utama serta foto berkabut memberikan konteks kawasan Sumbing/Magelang; keduanya tidak diklaim sebagai foto lokasi persis Negeri Sayur Sukomakmur. Foto jalur pengunjung terverifikasi sebagai Negeri Sayur Sukomakmur. Tiga foto lainnya menampilkan Nepal van Java, Ketep Pass, dan Punthuk Setumbu.

Kredit pembuat, sumber, lisensi, dan panduan penggantian foto tersedia di footer serta [dokumentasi aset](docs/ASSETS.md).

Informasi kunjungan bersifat pengantar. Fasilitas dapat berubah; kondisi terkini perlu dikonfirmasi sebelum berangkat. Referensi informasi dicantumkan pada halaman website.

## Pembuat dan lisensi

**Hasan Shofiyyur Rahman** — [Portofolio](https://portofolio-hasan-shofiyyur-rahman.vercel.app/) · [Instagram](https://www.instagram.com/yurnsz/) · [Email](mailto:hasanshofiyyur@gmail.com).

Kode dan dokumentasi buatan proyek menggunakan [MIT License](LICENSE), © 2026 Hasan Shofiyyur Rahman. Hak logo tetap milik pembuatnya. Foto mengikuti lisensi masing-masing, termasuk Pexels dan Creative Commons; lisensi MIT kode tidak menggantikan ketentuan tersebut. Lihat [kredit aset](docs/ASSETS.md) sebelum menggunakan ulang gambar.
