# Evaluasi desain

## Penyempurnaan proporsi — 18 Oktober 2026

Permintaan terbaru mempertahankan arah jurnal yang sudah disukai, tetapi mengoreksi skala pembuka, hubungan foto dengan catatan, penataan header, dan bentuk rekomendasi. Perubahan ini menggantikan keputusan rekomendasi ringkas pada evaluasi 17 Oktober di bawah.

| Before | After | Why |
| --- | --- | --- |
| H1 mencapai 96 px pada desktop | Maksimal 64 px, tetap berada di atas foto dan catatan | Judul tetap menjadi identitas halaman tanpa mendominasi seluruh layar. |
| Bingkai hero sekitar 835 px lebar; foto dipaksa 16:10 | Bingkai sekitar 683 px; gambar mengikuti rasio asli 1600:1067 tanpa crop | Lanskap tampil utuh dan bingkai beserta caption masuk dalam layar desktop 1366 × 768 maupun 1440 × 900. |
| Catatan sejajar dengan sisi bawah foto | Catatan selebar maksimal 23 rem disejajarkan ke tengah bingkai | Lokasi, pengantar, tombol, dan kalimat penutup terbaca sebagai satu kelompok pendamping foto. |
| Header desktop sekitar 80 px; Kontak memakai kotak garis | Header 60 px, logo 200 px, tautan 14 px dengan area tekan 44 px dan latar Kontak lembut | Header lebih hemat ruang; hover, fokus, dan tujuan anchor tetap terbaca. |
| Logo dan tautan desktop ditumpuk pada ponsel | Satu baris logo 170 px dan Menu/Tutup; daftar 2 × 2 dibuka melalui `details` | Ponsel memiliki struktur sendiri, dengan ruang lebih besar untuk isi halaman. |
| Urutan ponsel judul, catatan, foto | Judul, foto, catatan sesuai urutan HTML | Pengunjung melihat lanskap sebelum uraian dan tindakan. |
| Rekomendasi berupa tiga baris thumbnail | Tiga bingkai besar 4:3 berjajar di desktop/tablet; satu kolom pada lebar ≤650 px | Mengikuti pilihan terbaru pengguna; tiga destinasi memang merupakan pilihan setara. |
| Tautan kembali ke atas di footer | Footer berisi identitas, tautan pembuat, serta kredit | Mengikuti permintaan pengguna. Logo header tetap menjadi tautan ke awal halaman. |

Gaya kertas, hijau, Georgia/Arial, dua logo asli, foto cerita berbeda ukuran, tabel lapang, dan formulir kartu pos dipertahankan. Tidak ada JavaScript atau framework yang ditambahkan.

### Penilaian dan referensi navigasi

Penilaian visual dilakukan terpisah dari pemindaian mekanis. Sebelum perubahan, reviewer melihat judul yang terlalu besar, foto hampir memenuhi tinggi layar, dan catatan yang dimulai jauh di bawah tepi foto. Setelah perubahan, screenshot 1440, 768, dan 390 px (termasuk menu terbuka) menunjukkan enam permintaan pengguna terpenuhi tanpa masalah visual material. Tidak dibuat skor baru untuk menyatakan keberhasilan.

Header ponsel memakai disclosure native berdasarkan [MDN details](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/details). Prinsip tautan navigasi biasa, tanpa `role="menu"`, mengikuti [W3C disclosure navigation](https://www.w3.org/WAI/ARIA/apg/patterns/disclosure/examples/disclosure-navigation/); contoh W3C memakai JavaScript, sedangkan proyek memakai perilaku native HTML.

Menu tetap terbuka setelah tautan anchor dipilih dan ditutup melalui tombol Tutup. Ini perilaku yang sengaja dipertahankan sesuai `details`, tanpa menyembunyikan panel sambil membiarkan state terbuka. Panel berada di alur dokumen; CSS menambah `scroll-padding-top` menjadi 14 rem saat terbuka. Penanda tautan memakai `:target` dan `:has()`, sehingga menunjukkan tujuan anchor yang dipilih, bukan pelacakan scroll otomatis.

### Bukti revisi terbaru

- Halaman utama: **35/35** pemeriksaan umum lolos; paket pengumpulan: **37/37** lolos.
- Navbar: **84/84** lolos, mencakup scroll, posisi mengambang, anchor, keyboard, reduced motion, dan simulasi fallback sticky.
- Pemeriksaan khusus revisi: **66/66** lolos pada 1440 × 900, 1366 × 768, 768 × 1024, 390 × 844, dan 320 × 760. Meliputi rasio foto utuh, H1 maksimal 64 px, keselarasan catatan, susunan rekomendasi, footer, serta menu ponsel memakai keyboard, mouse, dan sentuhan simulasi.
- Menu tertutup setinggi 60 px. Pada 1440 px, foto selebar sekitar 683 px dan berakhir di y710; di layar 1366 × 768 berakhir di y707. Judul tujuan anchor tidak tertutup header saat menu terbuka.
- Semua pengujian fungsi menggunakan Chrome Windows dengan JavaScript halaman dinonaktifkan. Safari, Firefox, perangkat fisik, pembaca layar, dan zoom browser 200% belum diuji. Simulasi sentuhan bukan pengujian ponsel fisik.

Impeccable dengan scope layout memberi **satu warning** sebelum dan sesudah revisi: padding `.activity-section`. Ini false positive karena jarak horizontal diberikan oleh child `.container`; bagian aktivitas tidak diubah pada revisi ini.

Lint Taste terbaru menghasilkan **17 FAIL dan 4 WARN**; inspector browser **6 kategori FAIL dan 8 kategori WARN**. Temuan terkait bayangan/bingkai/gradient tombol mengikuti material jurnal yang diminta. Garis ikon Menu, pemisah, dan penanda anchor mempunyai fungsi. Temuan `focal-point` meminta judul atau foto diperbesar lagi, bertentangan dengan evaluasi terbaru pengguna; ukuran baru dipertahankan setelah pemeriksaan screenshot. Gerak/video tambahan tidak ditambahkan, sementara navbar tetap menjadi satu animasi utama. Peringatan lain menyangkut pilihan font/warna, teks kredit, pemisah kartu pos, dan scroll tabel ponsel yang disengaja. Tidak ada klaim seluruh aturan estetika alat telah lolos.

[Pembuka sebelum penyempurnaan](media/preview-before-proportion.png) · [Pembuka terbaru](media/preview-hero.png) · [Desktop penuh](media/preview-desktop.png) · [Ponsel penuh](media/preview-mobile.png) · [Menu ponsel terbuka](media/preview-mobile-menu.png).

## Riwayat evaluasi layout — 17 Oktober 2026

Bagian berikut menyimpan alasan dan hasil evaluasi terdahulu. Keputusan judul, hero, header, serta rekomendasi sudah diperbarui pada 18 Oktober di atas.

Target: `index.html`. Tujuan evaluasi adalah mengurangi pola template sambil mempertahankan warna kertas/hijau, Georgia/Arial, logo pengguna, konsep jurnal perjalanan, dan seluruh elemen tugas HTML/CSS.

Metode: dua penilaian independen. Agen `layout_review` menilai screenshot tanpa membaca hasil detektor; agen `layout_evidence` memeriksa Impeccable dan bukti browser. Hasil digabung setelah penilaian visual selesai. Ini adalah evaluasi untuk langsung diterapkan, bukan sertifikasi kualitas atau aksesibilitas.

## Masalah utama dan hasil perubahan

Masalah awal bukan kekurangan dekorasi. Hero dan hampir semua bagian menggunakan pembagian dua kolom dengan bobot serupa. Label kecil bernomor serta tiga kartu rekomendasi memperkuat pengulangan itu.

| Before | After | Why |
| --- | --- | --- |
| Judul dan tombol di kiri, foto di kanan | Judul membentang di atas; lanskap besar dengan catatan lebih sempit di tepinya | Tempat dan foto memimpin pembukaan, sementara ajakan menjadi catatan pendamping. |
| Judul/paragraf lalu dua foto setara | Teks bersanding dengan foto Sukomakmur yang dominan; foto kawasan berkabut lebih kecil | Ukuran foto menyatakan perannya: lokasi utama dan konteks sekitarnya. |
| Label `01`, `02`, dan seterusnya di setiap bagian | Heading langsung, tanpa nomor dekoratif | Bagian dikenali dari isinya, tanpa kerangka bab berulang. Urutan persiapan tetap memakai `ol` karena memang bermakna. |
| Kartu alamat besar di samping tabel sempit | Alamat ringkas di atas tabel selebar konten | Informasi praktis memperoleh ruang baca yang cukup. |
| Tiga kartu rekomendasi dengan foto besar yang sama | Tiga baris dengan foto kecil dan nama tempat | Penutup lebih ringkas, terutama di ponsel. |
| Catatan persiapan dan aktivitas hampir sama lebar | Daftar aktivitas utama dan kertas persiapan lebih sempit | Hierarki lebih jelas tanpa membuat semua bagian menjadi kartu. |

Urutan pembacaan: mengenali tempat, melihat lanskap, membaca kehidupan pertanian, memilih aktivitas, memeriksa informasi kunjungan, lalu menulis catatan atau membuka destinasi lain. Pada ponsel, judul, pengantar, dan tombol tetap mendahului foto hero. Susunan cerita mengikuti DOM; semua tautan dan form dapat digunakan tanpa script.

[Tampilan sebelum evaluasi layout](media/preview-before-layout.jpg) · [Hasil pembuka pada 17 Oktober](media/preview-before-proportion.png). Screenshot desktop dan ponsel pada README sudah mengikuti revisi 18 Oktober.

## Hasil review visual

Penilaian awal memberi nilai 25/32 untuk delapan heuristik yang relevan. Nilai ini adalah penilaian desain kualitatif, bukan angka yang diperoleh dari alat otomatis.

| Heuristik | Nilai awal / 4 | Dasar penilaian |
| --- | ---: | --- |
| Kejelasan status | 3 | Batas form latihan terlihat. |
| Kesesuaian dengan dunia nyata | 4 | Bahasa Indonesia, alamat, dan caption faktual. |
| Kontrol pengguna | 3 | Anchor, Maps, dan kembali ke atas tersedia. |
| Konsistensi | 4 | Warna, jenis huruf, serta pola tautan dan form konsisten. |
| Pencegahan kesalahan | 3 | `required`, tipe email, dan penjelasan demo. |
| Pengenalan tanpa menghafal | 3 | Nama bagian dan destinasi jelas. |
| Efisiensi aplikasi | Tidak dinilai | Website informasi sederhana tidak memerlukan shortcut aplikasi. |
| Estetika dan kesederhanaan | 2 | Pengulangan layout menjadi masalah utama. |
| Pemulihan kesalahan | 3 | Validasi form memakai perilaku native browser. |
| Bantuan khusus | Tidak dinilai | Penjelasan kontekstual sudah sesuai kebutuhan halaman. |

Review screenshot setelah revisi menyatakan ketiga masalah utama—hero generik, bagian berulang, dan rekomendasi setara—sudah ditangani. Tidak ditemukan cacat visual kritis pada 1440, 768, dan 390 px. Tinggi halaman 390 px turun dari sekitar 8.027 menjadi 6.594 px tanpa menghapus konten. Tidak dibuat nilai akhir baru hanya untuk menyatakan keberhasilan.

## Temuan alat dan interpretasinya

Impeccable awal: **12 temuan** (8 warning, 4 advisory). Setelah revisi: **5 warning**. Label bagian dan nomor dekoratif tidak lagi dilaporkan. Sisa temuan ditinjau satu per satu:

| Temuan akhir | Keputusan dan bukti |
| --- | --- |
| Dugaan kontras hover rendah | False positive penggabungan selector. Chrome mengonfirmasi teks tombol `#fffef9` di atas `#183d2e`, sekitar 11,9:1. |
| Dugaan aktivitas tanpa inset | False positive pada pembungkus. Child `.container` memberi jarak tepi 120 px di desktop 1440 px dan 16 px di ponsel. |
| Arial dianggap terlalu umum | Dipertahankan sesuai font sistem yang disepakati; website tetap dapat dibuka offline. |
| Latar warna kertas | Bagian identitas yang dipilih pengguna, bukan hasil pemilihan warna otomatis. |
| Judul serif miring | Kata Sukomakmur mempertahankan penekanan Georgia pada konsep jurnal. Aturan detektor sendiri mengakui konteks editorial sebagai pengecualian. |

Lint Taste akhir menandai **14 FAIL dan 5 WARN** terkait gradient tipis tombol, shadow, garis pemisah, dan bingkai. Itu adalah aturan estetika yang lebih ketat daripada brief. Material kertas, kontrol timbul, serta pemisah daftar dipertahankan dengan alasan visual; tidak ada klaim bahwa lint estetika sepenuhnya lolos. Pemeriksaan ini berbeda dari pemeriksaan fungsi browser.

Inspector Taste berbasis browser juga dijalankan: **6 kategori FAIL dan 9 kategori WARN**. Sebagian mengulang aturan material di atas. `few-pictures` hanya menghitung tiga foto besar karena thumbnail rekomendasi berada di bawah ambang ukuran alat; keenam JPG sebenarnya termuat. `still-page` dan `no-footage` meminta lebih banyak animasi/video daripada lingkup tugas. Peringatan lain mencakup pilihan font/warna yang dipertahankan, ukuran teks navigasi dan keterangan, panjang baris sumber, serta scroll horizontal tabel mobile yang disengaja dan diberi petunjuk. Screenshot pada ketiga lebar diperiksa langsung. Tidak ditemukan gambar rusak, overflow halaman, atau judul lebih dari dua baris pada ukuran inspector.

## Bukti teknis dan batasnya

- Chrome memeriksa halaman utama pada 1440, 768, 390, dan 320 px dengan JavaScript dinonaktifkan: **35/35 lolos**.
- Paket pengumpulan menjalani pemeriksaan yang sama, ditambah header dokumentasi: **37/37 lolos**.
- Pengujian khusus navbar: **84/84 lolos**, mencakup keadaan atas, tengah, mengambang, kembali ke atas, anchor, keyboard, reduced motion, dan simulasi fallback sticky.
- Semua delapan gambar lokal termuat; tidak ada request eksternal saat membuka halaman atau overflow horizontal seluruh halaman. Tabel mobile bergulir di dalam pembungkusnya.
- Kredit foto dapat dibuka dengan Enter dan ditutup dengan Space. Dua kegagalan pada pemeriksaan awal berasal dari pengiriman event keyboard alat uji yang belum menyertakan karakter Enter; setelah event diperbaiki, kontrol native lolos tanpa mengubah website.
- Screenshot diambil dari Chrome Windows. Safari, Firefox, perangkat fisik, dan pembaca layar belum diuji. Simulasi fallback bukan pengganti pengujian browser tersebut.

Tidak ada overlay detektor yang disajikan di browser pengguna. Bukti visual berasal dari screenshot Chrome dan laporan pengukuran; review tidak mengklaim overlay telah diinjeksikan. Alat browser memakai proses sementara, dan server inspector dihentikan setelah selesai. Berkas pemeriksaan sementara berada di `.tmp/` dan diabaikan Git.

Pertanyaan desain lanjutan tidak diperlukan pada evaluasi ini: pengguna sudah meminta implementasi dan menetapkan arah visual serta batas stack. Penjelasan kode untuk presentasi tersedia di [catatan belajar](LEARNING-NOTES.md).
