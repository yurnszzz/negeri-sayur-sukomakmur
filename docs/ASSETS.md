# Panduan aset

Dua logo asli Hasan Shofiyyur Rahman dan **enam foto lokal sudah dipasang**. Izin terbaru pengguna untuk mencari keenam foto menggantikan ketentuan placeholder dalam brief awal. Tidak ada lagi gambar placeholder pada halaman.

Foto utama dan kebun berkabut menunjukkan konteks kawasan Sumbing/Magelang; sumbernya tidak memastikan desa persis. Foto jalur pengunjung terverifikasi sebagai Negeri Sayur Sukomakmur. Ketiga foto rekomendasi sesuai dengan destinasi masing-masing. Caption dan kredit halaman mempertahankan pembedaan ini.

## Daftar tujuh ID aset

Path dihitung dari root proyek. BRAND-01 mencakup dua varian logo yang sama. Dimensi adalah ukuran berkas lokal; rasio tampilan diatur melalui CSS.

| ID | Fungsi dan berkas lokal | Dimensi intrinsik | Tampilan | Status dan sumber |
| --- | --- | --- | --- | --- |
| BRAND-01 | Header: `assets/images/brand/logo-horizontal.svg`; footer/favicon: `assets/images/brand/logo-simbol.svg` | 1835 × 390; 672 × 672 | Proporsi asli, `object-fit: contain` | Terpasang; SVG asli Hasan Shofiyyur Rahman, tanpa perubahan isi. |
| DEST-01 | Hero: `assets/images/destination/sukomakmur-hero.jpg` | 1600 × 1067 px | Rasio asli 1600:1067, tampil utuh | Terpasang; Tri Martono AS, Pexels License. Konteks kawasan Sumbing. |
| DEST-02 | Foto cerita pendamping: `assets/images/destination/sukomakmur-terasering.jpg` | 1200 × 800 px | 4:3, `cover` | Terpasang; Cekrek Moment, Pexels License. Konteks Magelang. |
| DEST-03 | Foto cerita utama: `assets/images/destination/sukomakmur-jalur-tani.jpg` | 720 × 571 px | 4:3, `cover` | Terpasang; Deprilsalucky, CC BY-SA 4.0. Lokasi Sukomakmur terverifikasi. |
| REC-01 | Nepal van Java: `assets/images/recommendations/nepal-van-java.jpg` | 720 × 900 px | Bingkai besar 4:3, `object-position: 50% 55%` | Terpasang; Deprilsalucky, CC BY-SA 4.0. |
| REC-02 | Ketep Pass: `assets/images/recommendations/ketep-pass.jpg` | 653 × 490 px | Bingkai besar 4:3, `cover` | Terpasang; Ng Min Shen, CC BY-SA 3.0. Pemandangan dari Ketep Pass. |
| REC-03 | Punthuk Setumbu: `assets/images/recommendations/punthuk-setumbu.jpg` | 1280 × 853 px | Bingkai besar 4:3, `cover` | Terpasang; Ridwan Adhitama, CC BY-SA 4.0. |

Foto utama didahulukan pemuatannya; lima foto lainnya memakai `loading="lazy"`. Delapan elemen gambar menghitung dua logo serta enam foto. Semua menggunakan path lokal dan dapat tampil tanpa internet.

## Sumber dan atribusi

### BRAND-01 — logo pengguna

Pembuat: **Hasan Shofiyyur Rahman**. Sumber asli disimpan sebagai [logo horizontal](../logo-horizontal.svg) dan [logo simbol](../logo-simbol.svg). Salinan pada folder brand identik dengan sumber. Alt header: “Negeri Sayur Sukomakmur”; alt footer: “Simbol Negeri Sayur Sukomakmur”. Logo tidak dipotong, direntangkan, atau diubah bentuknya. Izin penggunaannya berasal dari pengguna untuk proyek ini; hak logo tidak otomatis menjadi MIT.

### DEST-01 — lanskap lereng Sumbing

Foto: [Scenic Terraced Fields at Mount Sumbing](https://www.pexels.com/photo/scenic-terraced-fields-at-mount-sumbing-39985609/), oleh **Tri Martono AS**. Lisensi: [Pexels License](https://www.pexels.com/license/). Berkas lokal merupakan ukuran 1600 × 1067 dari foto sumber 5616 × 3744.

- Alt: “Barisan tanaman dan kebun berterasering dengan Gunung Sumbing di latar belakang”.
- Caption: “Lanskap pertanian di lereng Sumbing, Magelang”.
- Batas identifikasi: konteks kawasan; lokasi persis Negeri Sayur Sukomakmur tidak dipastikan oleh sumber.
- Tampilan sejak revisi 18 Oktober 2026: rasio asli 1600:1067, tanpa crop. CSS `height: auto`, `aspect-ratio: auto`, dan `object-fit: contain` menjaga seluruh tanaman, langit, dan gunung tetap terlihat. Bingkai sekitar 683 px pada viewport desktop 1440 px; ukurannya mengikuti ruang layar.

### DEST-02 — kebun berkabut

Foto: [Foggy Terraced Fields in Magelang, Indonesia](https://www.pexels.com/photo/foggy-terraced-fields-in-magelang-indonesia-36228487/), oleh **Cekrek Moment**. Lisensi: [Pexels License](https://www.pexels.com/license/). Berkas lokal merupakan ukuran 1200 × 800 dari foto sumber 5184 × 3456.

- Alt: “Kebun berterasering dan pepohonan di Magelang dengan kabut menyelimuti lereng”.
- Caption: “Kebun berterasering di Magelang, berselimut kabut”.
- Batas identifikasi: sumber menyebut Magelang, bukan kepastian desa Sukomakmur.
- Crop tampilan: 4:3; digunakan lebih kecil sebagai foto pendamping cerita.

### DEST-03 — lokasi Negeri Sayur Sukomakmur

Foto: [Negeri Sayur Sukomakmur, Kajoran](https://commons.wikimedia.org/wiki/File:Negeri_Sayur_Sukomakmur,_Kajoran.jpg), oleh **Deprilsalucky**, 10 Maret 2024. Lisensi: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Foto sumber berukuran 720 × 571, sama dengan berkas lokal.

- Alt: “Jalur pengunjung di antara kebun Negeri Sayur Sukomakmur, dengan gazebo dan Gunung Sumbing di belakangnya”.
- Caption: “Jalur pengunjung Negeri Sayur Sukomakmur”.
- Sumber secara eksplisit mengidentifikasi Negeri Sayur Sukomakmur di Nampan, Kajoran.
- Crop tampilan: 4:3; digunakan sebagai foto utama dalam cerita.

### REC-01 — Nepal van Java

Foto: [Nepal van java2](https://commons.wikimedia.org/wiki/File:Nepal_van_java2.jpg), oleh **Deprilsalucky**. Lisensi: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Berkas lokal 720 × 900, sama dengan sumber.

- Alt: “Rumah berwarna-warni Nepal van Java di lereng Gunung Sumbing, dikelilingi lahan pertanian dan awan”.
- Nama destinasi tampil pada heading tautan “Nepal van Java”.
- Foto sumber berbentuk portrait. Bingkai 4:3 memakai posisi 50% 55% agar permukiman terlihat. Tiga rekomendasi kini berupa foto besar sejajar di desktop/tablet dan satu kolom pada ponsel maksimal 650 px.

### REC-02 — Ketep Pass

Foto: [Ketep Pass5](https://commons.wikimedia.org/wiki/File:Ketep_Pass5.jpg), oleh **Ng Min Shen** (akun Wikimedia Ronaldoowen). Lisensi: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). Berkas lokal 653 × 490, sama dengan sumber.

- Alt: “Lembah hijau di antara Gunung Merapi dan Merbabu dilihat dari Ketep Pass”.
- Nama destinasi tampil pada heading tautan “Ketep Pass”.
- Foto menunjukkan pemandangan dari Ketep Pass, bukan bangunan fasilitasnya. Crop tampilan 4:3.

### REC-03 — Punthuk Setumbu

Foto: [Sunrise di punthuk setumbu](https://commons.wikimedia.org/wiki/File:Sunrise_di_punthuk_setumbu.jpg), oleh **Ridwan Adhitama** (akun Wikimedia Ridwanad). Lisensi: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Berkas lokal adalah thumbnail Wikimedia 1280 × 853 dari sumber 3000 × 2000.

- Alt: “Cahaya matahari terbit di balik Gunung Merapi dan Merbabu dari Punthuk Setumbu”.
- Nama destinasi tampil pada heading tautan “Punthuk Setumbu”.
- Crop tampilan 4:3, mempertahankan panorama gunung dan cahaya pagi.

## Perubahan ukuran dan tampilan

Berkas foto diunduh dari sumber atau layanan ukuran gambar sumbernya, tanpa retouch, pewarnaan ulang, maupun penyuntingan isi. DEST-01, DEST-02, dan REC-03 memakai versi yang diperkecil. Hero DEST-01 ditampilkan utuh mengikuti rasio berkasnya. Pada lima foto lainnya, CSS `object-fit: cover` memotong bagian tepi secara visual agar foto mengisi bingkai 4:3; berkas lokal tidak dipotong ulang. Perubahan ukuran dan crop tampilan diungkapkan pada kredit halaman.

Kredit lengkap tersedia dalam `details#kredit-foto` pada footer, termasuk judul, pembuat, sumber, dan tautan lisensi. Foto CC BY-SA beserta versi tampilan adaptasinya tetap mengikuti lisensi CC BY-SA masing-masing. Penggunaan foto tidak berarti fotografer mendukung atau berafiliasi dengan proyek.

## Mengganti foto kemudian

1. Pilih foto yang sesuai lokasi dan memiliki izin atau lisensi penggunaan yang jelas. Catat sumber serta pembuatnya.
2. Simpan dalam folder tujuan. Gunakan format gambar sebenarnya; jangan hanya mengubah ekstensi.
3. Cari komentar `ASSET DEST-01` atau ID terkait pada `index.html`, lalu perbarui `src`, dimensi intrinsik, alt, dan caption.
4. Perbarui kredit footer serta dokumen ini. Jika sumber hanya membuktikan kawasan sekitar, pertahankan batas identifikasi tersebut.
5. Periksa crop desktop/ponsel dan proporsi logo. Perbarui screenshot README bila tampilan berubah.
6. Ekspor ulang `submission/` dari sumber utama sesuai [README](../README.md#menyiapkan-paket-pengumpulan); jangan mengedit salinan secara terpisah.

## Dokumentasi dan status pemeriksaan

[Preview hero](media/preview-hero.png), [desktop penuh](media/preview-desktop.png), [ponsel penuh](media/preview-mobile.png), dan [menu ponsel terbuka](media/preview-mobile-menu.png) menampilkan implementasi 18 Oktober 2026 dengan enam foto. [Pembuka sebelum penyempurnaan proporsi](media/preview-before-proportion.png) serta [layout awal](media/preview-before-layout.jpg) disimpan sebagai pembanding.

`docs/media/readme-header.svg` adalah ilustrasi dokumentasi buatan proyek, bukan logo atau foto destinasi. Teksnya terlihat pada frame statis; animasi garis jurnal berhenti saat reduced motion aktif.

Pada 18 Oktober 2026, sumber dan paket pengumpulan diperiksa di Chrome pada lebar 1440, 768, 390, dan 320 px dengan JavaScript dinonaktifkan: sumber lolos 35/35 dan ekspor 37/37 pemeriksaan. Seluruh delapan gambar termuat. Pemeriksaan tambahan pada 1440, 1366, 768, 390, dan 320 px memastikan rasio asli hero, bingkai penuh pada viewport desktop, serta tiga kolom rekomendasi di desktop/tablet dan satu kolom pada ponsel. Crop dan screenshot ditinjau. Angka tersebut berasal dari Chrome Windows, bukan pengujian perangkat fisik atau browser lain.

[Lisensi MIT](../LICENSE) berlaku pada kode serta dokumentasi asli proyek; tidak menggantikan hak logo, lisensi foto, atau lisensi skill. Lihat [lisensi pihak ketiga](THIRD-PARTY-LICENSES.md) dan [catatan pemeriksaan](DESIGN-REVIEW.md).
