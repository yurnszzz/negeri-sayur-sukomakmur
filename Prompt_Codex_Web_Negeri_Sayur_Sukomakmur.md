### 1. Tujuan dan sumber tugas

Buat website berbahasa Indonesia yang memperkenalkan SATU destinasi utama: Negeri Sayur Sukomakmur, Dusun Nampan, Desa Sukomakmur, Kecamatan Kajoran, Kabupaten Magelang, Jawa Tengah. Angkat karakter kebun sayur berterasering dan lanskap lereng Gunung Sumbing.

Baca dahulu:

1. instruksi_mini_project_frontend.md sebagai ketentuan tugas;
2. scfe_basic_p1_p4.md sebagai acuan tingkat materi;
3. AGENTS.md yang berlaku dan struktur repository yang sudah ada;
4. README.md dan LICENSE dari repository contoh https://github.com/yurnszzz/heart-disease-prediction sebagai acuan penyajian dokumentasi GitHub.

Repository contoh dipakai untuk mempelajari pola dokumentasi: header beranimasi, badge, deskripsi, tabel penjelasan, struktur proyek, cara menjalankan, referensi, dan lisensi MIT. Sesuaikan isinya dengan proyek wisata individu ini. Kerjakan website pada repository task yang sedang aktif; jangan mengubah repository contoh.

Jika berkas tugas belum tersedia, cari berdasarkan nama di repository. Jika tetap tidak ditemukan, sampaikan keterbatasannya dan gunakan ketentuan lengkap dalam prompt ini; jangan mengaku sudah membaca berkas yang tidak ada.

Website berupa satu halaman dengan tautan antarbagian. Negeri Sayur Sukomakmur menjadi fokus cerita, foto, aktivitas, dan informasi. Rekomendasi destinasi lain cukup menjadi bagian ringkas menjelang akhir.

Identitas pembuat:

- Nama: Hasan Shofiyyur Rahman
- Email: hasanshofiyyur@gmail.com
- Media sosial: https://www.instagram.com/yurnsz/
- Portofolio opsional: https://portofolio-hasan-shofiyyur-rahman.vercel.app/

Gunakan nama tersebut untuk footer dan penamaan paket source code tugas. Jika URL portofolio belum diberikan, lewati tautannya dan catat di dokumentasi. Pertahankan tautan media sosial untuk memenuhi ketentuan tugas. Jangan mengarang kontak pengelola wisata atau menyatakan website ini sebagai situs resmi pengelola.

### 2. Stack dan cara menulis kode

Gunakan HTML5 dan CSS native yang ditulis sendiri. Seluruh halaman harus berjalan tanpa JavaScript. Tidak menggunakan framework, pustaka UI, Tailwind, Bootstrap, React, Vue, TypeScript, Sass, backend, database, atau build step untuk website.

Node/Python boleh digunakan sebagai alat pemasangan skill, preview, atau pemeriksaan saat pengembangan. Website akhirnya tetap berupa file HTML, CSS, dan aset lokal yang dapat dibuka langsung atau melalui Live Server.

Ikuti cara penyusunan dari materi:

- HTML menjadi struktur konten; CSS eksternal mengatur tampilannya.
- Gunakan header, nav, main, section, dan footer sesuai makna.
- Gunakan Flexbox untuk navbar dan kelompok elemen kecil; Grid untuk susunan area utama atau foto.
- Gunakan box model, gap, satuan px/rem/%, selector class, grouping, pseudo-class, dan position sesuai kebutuhan.
- Alur dokumen mengikuti urutan baca halaman dari atas ke bawah. Tulis konten langsung dalam HTML.
- Gunakan nama class yang jelas dan konsisten, indentasi dua spasi, serta komentar pendek pada bagian utama.
- Pakai beberapa class yang bisa digunakan ulang, seperti container, button, dan photo-print. Hindari banyak wrapper, selector terlalu panjang, penumpukan override, atau sistem komponen yang berlebihan.
- Custom properties untuk beberapa warna dan jarak boleh dipakai agar konsisten.

Skeuomorphism dan responsivitas boleh memakai tambahan CSS kecil seperti box-shadow, border-radius, linear-gradient yang sangat halus, object-fit, transform, transition, dan media query. Jelaskan tambahan yang memang digunakan dalam README, karena detail tersebut belum seluruhnya dijelaskan dalam materi. Perbaiki kesalahan sintaks bila ada pada contoh materi; ikuti konsep belajarnya.

### 3. Taste Skill dan UI UX Pro Max

Saya mengizinkan pemasangan kedua skill berikut secara lokal pada proyek untuk membantu keputusan desain:

- Taste Skill: https://github.com/Leonxlnx/taste-skill
- UI UX Pro Max: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill

Periksa dahulu apakah keduanya sudah ada. Jika belum, gunakan installer resmi yang sesuai dengan environment. Perintah yang dapat dicoba dari root proyek:

    npx --yes skills add https://github.com/Leonxlnx/taste-skill --skill design-taste-frontend --agent codex --copy --yes
    npx --yes ui-ux-pro-max-cli init --ai codex

Periksa hasil pemasangan dan baca SKILL.md yang benar-benar tersedia, beserta referensi yang relevan. Gunakan lokasi file hasil installer; jangan menganggap pemasangan berhasil hanya karena perintah dijalankan. Pertahankan berkas skill yang diperlukan agar dapat ikut dalam perubahan repository.

Jika koneksi atau kemampuan environment menghalangi pemasangan, laporkan singkat dan lanjutkan pekerjaan berdasarkan brief desain lengkap di bawah. Jangan mengklaim skill telah terpasang atau pemeriksaannya telah dijalankan bila belum dilakukan.

Gunakan Taste Skill untuk keputusan komposisi, tipografi, perencanaan penempatan foto, dan peninjauan visual. Gunakan UI UX Pro Max untuk keterbacaan, navigasi, formulir, aksesibilitas, dan responsivitas.

Ketentuan tugas, stack native, kesederhanaan kode, dan gaya pilihan saya harus didahulukan. Secara khusus:

- Bayangan dan gradient material yang halus diperbolehkan karena saya meminta skeuomorphism; larangan shadow/gradient dari Taste Skill tidak berlaku untuk kebutuhan ini.
- Animasi kompleks, widget interaktif dengan script, dan persyaratan motion dari skill tidak perlu diterapkan.
- Seluruh logo dan foto akan saya sediakan. Lewati langkah skill yang mencari, mengunduh, atau menghasilkan foto/logo; buat placeholder dan arahan aset sesuai bagian 6.
- Saran Tailwind, React, GSAP, atau stack lain diterjemahkan menjadi HTML/CSS sederhana jika relevan, bukan diinstal sebagai bagian website.
- Bagian tabel, form, serta beberapa gambar rekomendasi tetap wajib walaupun pola visual suatu skill menyarankan hal berbeda.

### 4. Arah visual

Konsep: “Catatan perjalanan ke Negeri Sayur Sukomakmur”.

Gabungkan skeuomorphism modern yang halus dengan jurnal perjalanan. Hasilnya terasa seperti membuka catatan kunjungan yang rapi, dengan foto cetak dan bahan kertas, sambil tetap nyaman digunakan sebagai website masa kini.

Arah warna: putih kertas sedikit hangat, hijau hutan sebagai warna utama, hijau sage untuk permukaan pendukung, dan teks gelap yang jelas. Contoh awal: #F5F4EE, #24513F, #D9E3CF, #202A22. Sesuaikan proporsi warna dengan tema kebun. Siapkan ruang foto yang tetap rapi saat placeholder diganti aset asli. Hindari warna kusam yang membuat teks sulit dibaca.

Gunakan paling banyak dua keluarga font: serif yang berkarakter untuk judul dan sans-serif yang bersih untuk isi. Fraunces dan DM Sans dapat dipertimbangkan; selalu sediakan fallback Georgia/Arial atau font sistem agar halaman tetap terbaca saat font eksternal tidak termuat.

Terapkan kesan fisik secara terarah:

- Foto utama atau foto pendukung dibingkai seperti foto cetak dengan pinggiran kertas dan bayangan jatuh tipis.
- Tombol terasa sedikit terangkat, dengan kondisi hover, focus, dan active yang jelas.
- Field form terasa seperti area tulis yang sedikit masuk ke permukaan.
- Satu detail selotip kertas atau catatan kecil boleh digunakan jika memperkuat konsep.
- Cahaya, bayangan, radius, dan bahan permukaan konsisten. Foto tetap dominan.
- Bila ada rotasi foto, gunakan sangat kecil dan sederhanakan pada layar sempit. Teks isi tetap tegak.

Hindari tampilan template yang tidak berhubungan dengan destinasi: gradient besar dekoratif, glassmorphism, emoji sebagai ikon, deretan kartu ikon yang berulang untuk semua section, efek timbul pada setiap elemen, terlalu banyak stiker/stempel, animasi terus-menerus, angka statistik, rating, testimoni, maupun logo mitra yang dibuat-buat.

Buat setiap bagian sesuai jenis isinya: cerita berupa paragraf, aktivitas berupa daftar, data berupa tabel, galeri berupa foto, dan kontak berupa formulir. Bangun karakter desain dari foto terasering, judul, serta detail jurnal yang dipakai secara terbatas.

### 5. Susunan halaman dan elemen wajib

A. Header dan navigasi

- Sediakan tempat logo berbentuk gambar yang akan saya berikan, dengan placeholder lokal berlabel “Logo”. Teks nama website seperti “Catatan Sukomakmur” boleh menjadi pendamping.
- Logo menggunakan object-fit: contain dan tidak dipotong atau ditarik. Jangan membuat logo pengganti atau mengambil logo pihak lain.
- Navbar kompak dengan permukaan solid seperti bilah kertas tebal, sedikit radius dan bayangan. Boleh sticky jika nyaman di semua ukuran.
- Tautan ke Cerita, Aktivitas, Info Kunjungan, dan Kontak.
- Pada mobile, susun ulang atau bungkus menu dengan Flexbox. Menu tetap terlihat dan dapat digunakan tanpa hamburger berbasis JavaScript.
- Header sticky tidak boleh menutupi tujuan tautan internal.

B. Hero

- Hanya satu h1 utama: “Negeri Sayur Sukomakmur”.
- Sediakan slot foto utama yang besar dan jelas, lokasi singkat, serta satu kalimat pengantar yang konkret. Saat ini gunakan placeholder aset DEST-01; foto aslinya akan saya berikan.
- Pada desktop, berikan porsi visual lebih besar kepada foto dan susun judul dengan komposisi yang seimbang. Pada mobile, urutkan judul, pengantar, tombol, lalu foto.
- CTA utama “Rencanakan Kunjungan” menuju bagian informasi. Tautan pendamping “Lihat Lokasi” membuka Google Maps.
- Jangan menambahkan kolom pencarian destinasi, login, atau pilihan paket pada website satu destinasi ini.

C. Cerita dan foto

- Dua paragraf pendek tentang terasering kebun sayur, lanskap Sumbing, dan kehidupan pertanian warga.
- Sediakan dua slot foto pendukung dengan placeholder DEST-02 dan DEST-03 serta caption singkat yang menjelaskan kebutuhan foto.
- Gunakan figure dan figcaption bila sesuai. Saat foto asli dipasang, caption dan alt harus sesuai isi fotonya.

D. Aktivitas dan persiapan

- Gunakan unordered list untuk aktivitas, misalnya menikmati panorama, berfoto dari jalur pengunjung, dan mengenal suasana pertanian warga dengan menghormati aktivitas mereka.
- Jangan menjanjikan pengalaman berbayar atau memanen bersama petani tanpa informasi yang mendukungnya.
- Gunakan ordered list untuk urutan persiapan kunjungan, seperti memeriksa informasi pengelola, menyiapkan perlengkapan, lalu mengikuti jalur pengunjung.
- Bedakan saran persiapan dari jadwal operasional resmi. Jangan menyuruh pengunjung memasuki lahan pertanian tanpa izin.

E. Informasi kunjungan

- Tampilkan tabel HTML yang benar dengan caption, thead, tbody, th, dan td. Gunakan scope pada header jika sesuai.
- Pilihan utama adalah tabel fasilitas dengan kolom “Fasilitas”, “Kegunaan”, dan “Catatan”. Isikan hanya fasilitas yang didukung sumber, misalnya area parkir, warung warga, atau tempat istirahat.
- Jika menyertakan harga atau jam buka, verifikasi pada sumber terbaru dan jelaskan tanggal/sumber datanya. Bila informasinya berbeda atau tidak dapat diverifikasi, cukup tampilkan keterangan untuk konfirmasi kepada pengelola; tabel fasilitas sudah memenuhi tugas.
- Jangan mengarang tarif, jam buka, nomor telepon, ketinggian, jarak, atau status “buka sekarang”.
- Sertakan lokasi dan tautan Google Maps yang menuju pencarian Negeri Sayur Sukomakmur di Nampan, Kajoran, Magelang. Tidak perlu membuat peta interaktif.

F. Form kontak sederhana

- Nama, email, dan pesan; semua memiliki label yang terlihat, id/for yang sesuai, name, dan required.
- Gunakan type="email" untuk validasi bawaan browser, serta textarea untuk pesan.
- Buat sebagai demo formulir menggunakan method="get" dan action="#kontak". Pengujian dilakukan dengan data contoh.
- Gunakan tombol submit yang jelas, misalnya “Coba Formulir”, dan catatan terlihat: “Form latihan; pesan belum dikirim.”
- Setelah input valid, browser hanya kembali ke halaman/bagian kontak dengan parameter URL. Jangan menampilkan klaim pesan terkirim, data tersimpan, atau reservasi berhasil.
- Sediakan tautan terpisah “Kirim email” dengan mailto:[EMAIL_PEMBUAT].
- Tampilkan form dalam komposisi seperti lembar kartu pos yang tetap lapang dan mudah diisi.

G. Rekomendasi wisata lain

- Tampilkan tiga slot gambar dan nama destinasi lain di Magelang: Nepal van Java, Ketep Pass, dan Punthuk Setumbu. Gunakan placeholder REC-01 sampai REC-03 sampai saya memberikan foto.
- Cukup satu baris ringkas pada desktop dan susunan vertikal pada mobile. Porsi bagian ini tidak mengalahkan destinasi utama.
- Hubungkan nama/gambarnya ke halaman informasi yang benar. Tidak perlu membuat halaman detail tambahan atau sistem katalog.

H. Footer

- Nama pembuat, tautan portofolio jika diberikan, media sosial yang diberikan, tautan email, dan tautan kembali ke atas.
- Beri identitas proyek secara ringkas, misalnya “Mini Project Frontend Basic — KSM Veterantech 2026”.
- Tambahkan kredit foto secara wajar bila diperlukan.

Semua jenis materi berikut harus muncul dengan penggunaan yang masuk akal: semantic HTML, Flexbox/Grid, heading dan paragraf, ordered/unordered list, table, gambar sebagai media, link internal, link eksternal, email link, dan form. Gunakan tingkat heading sesuai hierarki; tidak perlu memaksakan h1 sampai h6. Gambar sudah memenuhi unsur media, sehingga video/audio tidak wajib ditambahkan.

### 6. Logo, foto, dan penandaan aset

Logo website dan seluruh foto website akan SAYA sediakan. Tugasmu sekarang adalah membangun layout lengkap beserta placeholder yang mudah diganti. Jangan mencari, mengunduh, mengambil dari repo contoh, atau menghasilkan logo/foto final. Jangan menunda pengerjaan sambil menunggu aset.

Buat placeholder SVG lokal sederhana berupa bidang warna dan label pendek. Tidak perlu gambar pemandangan tiruan. Placeholder digunakan sebagai img yang benar-benar memiliki file, sehingga tidak ada ikon gambar rusak atau src yang menunjuk file yang belum ada. Isi placeholder harus jelas berstatus sementara.

Gunakan pemetaan berikut sebagai acuan. Berkas “saat ini” adalah SVG placeholder; nama “aset akhir” menjadi nama file yang perlu saya sediakan.

| ID       | Posisi                      | File placeholder saat ini                           | Nama aset akhir                                      | Rasio dan arahan                                                                            |
| -------- | --------------------------- | --------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| BRAND-01 | Logo header                 | assets/images/brand/logo-website.svg                | assets/images/brand/logo-website.png                 | PNG transparan sekitar 512px atau SVG asli dari saya; pertahankan proporsi logo.            |
| DEST-01  | Foto utama hero             | assets/images/destination/sukomakmur-hero.svg       | assets/images/destination/sukomakmur-hero.webp       | Landscape 16:10, saran 2400×1500px; panorama kebun terasering dengan Sumbing bila terlihat. |
| DEST-02  | Foto cerita pertama         | assets/images/destination/sukomakmur-terasering.svg | assets/images/destination/sukomakmur-terasering.webp | Landscape 4:3, saran 1600×1200px; detail susunan kebun sayur.                               |
| DEST-03  | Foto cerita kedua           | assets/images/destination/sukomakmur-jalur-tani.svg | assets/images/destination/sukomakmur-jalur-tani.webp | Landscape 4:3, saran 1600×1200px; jalur tani atau suasana pertanian warga.                  |
| REC-01   | Rekomendasi Nepal van Java  | assets/images/recommendations/nepal-van-java.svg    | assets/images/recommendations/nepal-van-java.webp    | Landscape 4:3, saran 1200×900px; foto Nepal van Java yang sesuai namanya.                   |
| REC-02   | Rekomendasi Ketep Pass      | assets/images/recommendations/ketep-pass.svg        | assets/images/recommendations/ketep-pass.webp        | Landscape 4:3, saran 1200×900px; foto Ketep Pass.                                           |
| REC-03   | Rekomendasi Punthuk Setumbu | assets/images/recommendations/punthuk-setumbu.svg   | assets/images/recommendations/punthuk-setumbu.webp   | Landscape 4:3, saran 1200×900px; foto Punthuk Setumbu.                                      |

Tulis detail tersebut di docs/ASSETS.md. Resolusi di atas adalah saran, bukan syarat mutlak. Jika saya memberi JPG, PNG, WebP, atau SVG logo dengan format berbeda, sesuaikan ekstensi dan src dengan file sebenarnya; jangan sekadar mengganti ekstensi file.

Pada setiap slot di HTML, tambahkan komentar singkat yang berisi ID aset, lokasi file akhir, serta arahan crop. Contoh: “ASSET DEST-01 — ganti src dengan assets/images/destination/sukomakmur-hero.webp setelah file diberikan; pertahankan panorama terasering.”

Tampilan placeholder cukup menampilkan label seperti “DEST-01 · Foto utama”. Instruksi panjang dan nama path cukup berada di komentar serta docs/ASSETS.md. Jangan menutup judul, tombol, atau isi halaman dengan catatan teknis.

Di docs/ASSETS.md sertakan:

- tabel ID, fungsi, path placeholder, path final, rasio, saran resolusi, alt/caption yang perlu disesuaikan, dan status “menunggu aset pengguna”;
- langkah mengganti file dan src, termasuk bila ekstensi berbeda;
- arahan object-fit: cover untuk foto dan contain untuk logo;
- kolom sumber/kredit/status penggunaan yang nanti saya isi;
- checklist mengganti semua placeholder dan memperbarui preview README.

Saat memakai placeholder, alt harus menyebut bahwa itu placeholder, tanpa mengklaim sebagai foto asli. Setelah foto dipasang, ubah alt menjadi deskripsi foto. Hapus penanda visual sementara dan placeholder yang sudah tidak dipakai, kemudian periksa kembali layout.

### 7. Konten dan sumber informasi

Tulis teks asli yang ringkas, informatif, dan berbahasa Indonesia. Referensi digunakan untuk mengecek fakta; tidak untuk mengambil aset atau menyalin desain/paragraf.

Lokasi utama: Dusun Nampan, Desa Sukomakmur, Kecamatan Kajoran, Kabupaten Magelang, Jawa Tengah. Hindari tarif, jam buka, ketinggian, jarak, dan klaim layanan yang tidak dapat diverifikasi. Tabel fasilitas cukup untuk memenuhi ketentuan tabel.

Referensi awal untuk diperiksa:

- Profil desa hasil KKN, untuk konteks lokasi; jangan menyatakannya sebagai portal resmi pemerintah: https://desa-sukomakmur.vercel.app/
- PPID Kabupaten Magelang, konteks pertanian Sukomakmur: https://ppid.magelangkab.go.id/berita/harga-loncang-stabil-petani-sukomakmur-tetap-untung-di-musim-kemarau
- Radar Jogja, 10 Maret 2024, informasi lokasi dan keterangan pengelola; data operasionalnya bersifat historis: https://radarjogja.jawapos.com/amp/jawa-tengah/2403100014/pesona-negeri-sayur-sukomakmur-magelang-jalur-pertanian-yang-diminati-wisatawan-tawarkan-lanskap-alam-hingga-gagahnya-gunung-sumbing
- Koran Jakarta, 4 Januari 2025, informasi fasilitas yang perlu diperiksa kondisinya: https://koran-jakarta.com/2025-01-04/keelokan-terasering-pertanian-sayur-desa-sukomakmur-di-punggung-sumbing-yang-menyejukkan-hati/amp
- Referensi rekomendasi wisata: gunakan halaman masing-masing destinasi pada https://visitjawatengah.jatengprov.go.id/ dan periksa tautan yang akan dipasang.

### 8. Responsivitas dan kenyamanan

- Susun layout sederhana dengan lebar konten maksimum dan padding yang nyaman.
- Ubah dua kolom menjadi satu pada layar sempit dengan media query seperlunya.
- Ukuran teks isi sekitar 16px atau lebih, line-height yang nyaman, serta kontras teks dan latar yang jelas.
- Tautan dan tombol mudah ditekan, dengan target sentuh sekitar 44px pada kontrol utama.
- Sediakan focus keyboard yang terlihat. Jangan hanya mengandalkan hover.
- Gunakan alt sesuai status placeholder atau foto asli, serta ukuran/rasio gambar yang stabil. Gambar hero segera dimuat; gambar di bawah boleh loading="lazy".
- Jaga agar halaman tidak melebar ke samping. Jika tabel perlu digulir, batasi scroll pada pembungkus tabelnya.
- Gunakan efek gerak pendek hanya untuk umpan balik tombol/foto. Hormati prefers-reduced-motion bila menggunakan transition atau smooth scroll.
- Semua informasi utama tetap terlihat tanpa animasi, JavaScript, atau efek hover.

### 9. Struktur proyek dan paket pengumpulan

Gunakan struktur proyek statis yang rapi berdasarkan tanggung jawab, dengan jumlah file yang tetap wajar untuk frontend basic. Struktur profesional di sini berarti pemisahan konten halaman, stylesheet, aset, dan dokumentasi yang jelas.

| Path                                        | Tanggung jawab                                                              |
| ------------------------------------------- | --------------------------------------------------------------------------- |
| index.html                                  | Satu halaman utama website dan sumber HTML yang dipelihara.                 |
| assets/css/style.css                        | Seluruh CSS website, dibagi komentar bagian secara rapi dalam satu file.    |
| assets/images/brand/                        | Placeholder logo, lalu logo yang saya berikan.                              |
| assets/images/destination/                  | Placeholder tiga foto destinasi utama, lalu foto dari saya.                 |
| assets/images/recommendations/              | Placeholder foto rekomendasi, lalu foto dari saya.                          |
| README.md                                   | Pengantar repository, preview, ringkasan fitur, dan cara menjalankan.       |
| docs/ASSETS.md                              | Daftar kebutuhan logo/foto dan panduan penggantiannya.                      |
| docs/LEARNING-NOTES.md                      | Penjelasan kode, pemetaan materi, dan tambahan CSS yang digunakan.          |
| docs/media/readme-header.svg                | Header dokumentasi dengan animasi ringan, dibuat dalam kode SVG.            |
| docs/media/                                 | Screenshot atau rekaman preview yang benar-benar tersedia.                  |
| LICENSE                                     | Teks MIT standar lengkap untuk source code proyek.                          |
| .gitignore                                  | Mengabaikan cache, file sementara, dependency alat, dan hasil ekspor.       |
| submission/                                 | Hasil ekspor pengumpulan tugas; dibuat dari sumber utama dan diabaikan Git. |
| .agents/skills/ atau lokasi hasil installer | Berkas skill yang diperlukan, terpisah dari source website.                 |

Jangan menambahkan folder components, services, routes, store, src, dist, atau file konfigurasi jika tidak diperlukan oleh proyek satu halaman ini. Jangan memecah CSS menjadi banyak file hanya untuk terlihat profesional.

Gunakan path relatif dari dokumen, misalnya assets/css/style.css. Hindari path yang diawali /assets karena website mungkin dibuka pada subpath repository GitHub Pages. Penulisan nama file dan src harus sama persis, termasuk huruf besar/kecil.

Sediakan hasil ekspor tugas pada submission/:

- Source Code_Hasan Shofiyyur Rahman.html
- Source Code_Hasan Shofiyyur Rahman.css
- assets/images/ yang digunakan oleh HTML tersebut

Ekspor disalin secara mekanis dari index.html dan assets/css/style.css setelah keduanya final. Ubah href stylesheet di HTML ekspor ke nama CSS tugas dalam folder yang sama, serta pastikan seluruh path gambar valid dari lokasi ekspor. Salin aset yang diperlukan tanpa membawa seluruh dokumentasi atau skill.

index.html dan assets/css/style.css tetap menjadi sumber yang diedit. submission/ adalah hasil ekspor; jangan mengembangkan dua versi kode secara terpisah. Setiap perubahan sumber atau pemasangan foto harus diikuti ekspor ulang sebelum pengumpulan. Dokumentasikan langkahnya secara sederhana; tidak perlu menambah build system atau bahasa pemrograman ke source website untuk langkah salin ini.

Dengan demikian repository mempunyai entry point standar untuk preview/GitHub, sementara file yang dikumpulkan tetap mengikuti “Source Code_Nama Mentee.html/css”.

### 10. Dokumentasi GitHub, animasi README, dan MIT

Susun README berbahasa Indonesia dengan pola penyajian yang terinspirasi repository contoh:

1. Header visual beranimasi ringan dengan nama proyek, warna yang selaras dengan website, dan deskripsi singkat.
2. Badge secukupnya: HTML5, CSS3, MIT. Jangan membuat badge status deployment atau hasil pengujian yang belum nyata.
3. Deskripsi proyek, konteks tugas individu, dan status pengerjaan aset.
4. Preview website bila screenshot sudah dibuat, dengan keterangan bila masih memakai placeholder.
5. Ringkasan fitur dan stack.
6. Struktur proyek serta fungsi folder/file.
7. Cara membuka index.html langsung, dengan Live Server, dan secara opsional dengan server lokal yang sudah tersedia.
8. Tautan relatif ke docs/ASSETS.md dan docs/LEARNING-NOTES.md.
9. Cara menyiapkan paket pengumpulan serta ringkasan langkah Git/GitHub.
10. Pembuat, portofolio/media sosial bila tersedia, referensi, dan tautan LICENSE.

Buat animasi header README sebagai SVG lokal di docs/media/readme-header.svg, dengan animasi CSS/SVG sederhana dan tanpa JavaScript. Teks utama harus tetap terbaca pada frame statis; berikan fallback/dukungan reduced motion bila memungkinkan. Boleh memakai gerakan tipis pada garis lanskap atau aksen jurnal. Header ini adalah ilustrasi dokumentasi dan tidak menggantikan logo website dari saya.

Animasi README tidak harus mengikuti semua gaya dekorasi repository contoh. Buat identitas yang sesuai proyek wisata ini. Hindari ketergantungan wajib pada layanan banner/typing eksternal. Badge eksternal sederhana boleh digunakan dengan alt yang jelas; jangan menambah banyak widget.

Jika browser tersedia, simpan screenshot desktop/mobile yang benar-benar diambil dari implementasi ke docs/media/. GIF walkthrough boleh ditambahkan bila dapat dibuat dari rekaman website yang nyata, tetapi header SVG lokal sudah memenuhi kebutuhan animasi README. Jangan membuat gambar palsu sebagai bukti hasil. Bila screenshot belum bisa dibuat, tulis status teks dan jangan memasang tautan gambar ke file yang belum ada.

docs/LEARNING-NOTES.md cukup memuat:

- alur struktur HTML dan fungsi tiap section;
- peran Flexbox dan Grid;
- pemetaan persyaratan tugas ke elemen serta lokasi file yang digunakan;
- teknik tambahan CSS di luar materi dan alasannya;
- batas fungsi form demo;
- hasil pemeriksaan yang benar-benar dijalankan dan status skill.

Tambahkan LICENSE berisi teks MIT standar lengkap, tahun 2026, dan [NAMA_MENTEE] sebagai pemegang hak cipta source code. Jangan membawa nama tim/pembuat dari repository contoh. Jelaskan singkat bahwa logo, foto pengguna, dan aset pihak ketiga mengikuti ketentuan masing-masing; jangan otomatis mengubahnya menjadi MIT. Lisensi bawaan skill tetap dipertahankan.

Siapkan repository agar siap dipush: .gitignore yang relevan, file sumber dan dokumentasi yang rapi, serta petunjuk git status/add/commit/push yang sesuai keadaan repository. Periksa remote yang sudah ada sebelum menulis contoh perintah. Jika remote tujuan belum diketahui, gunakan [URL_REPOSITORY_TUJUAN] dalam petunjuk dan jangan menggantinya dengan URL repository contoh.

Tidak perlu mengaktifkan hosting atau membuat workflow CI/CD untuk menyelesaikan task ini. Dokumentasi boleh menjelaskan GitHub Pages sebagai opsi berikutnya. Laporkan status commit/push/deployment secara faktual; jangan mengklaim tindakan yang belum dilakukan.

### 11. Cara mengerjakan dan memeriksa

Setelah membaca konteks, berikan ringkasan pendek tentang konsep dan file yang akan dibuat, lalu langsung implementasikan. Tidak perlu berhenti untuk meminta persetujuan layout. Ambil keputusan kecil secara mandiri sesuai brief.

Sesudah selesai:

- Periksa semua elemen wajib tugas dari header sampai footer.
- Periksa stylesheet, placeholder yang benar-benar ada, target id tautan internal, link eksternal, dan mailto.
- Periksa docs/ASSETS.md: tujuh ID aset, path, rasio, arahan, dan status harus sesuai dengan HTML.
- Periksa tautan dan gambar README, animasi header SVG lokal, LICENSE, serta isi .gitignore.
- Periksa bahwa website dapat dibuka dari index.html dan dari hasil ekspor pengumpulan tanpa path rusak. Jangan menyembunyikan status foto/logo yang belum diberikan.
- Uji native validation pada form dengan input kosong dan email tidak valid, lalu input contoh yang valid.
- Jika browser tersedia, periksa pada lebar sekitar 1440px, 768px, dan 390px; cek pula bahwa lebar 320px tetap dapat digunakan. Lihat screenshot dan perbaiki teks terpotong, tumpang tindih, menu, tabel, serta form. Simpan preview dokumentasi yang memang diambil, dengan keterangan bahwa gambar website masih placeholder bila demikian.
- Gunakan pemeriksaan bawaan skill hanya sepanjang sesuai HTML/CSS, skeuomorphism, dan lingkup tugas. Jangan menghapus efek material yang diminta hanya untuk lolos aturan estetika skill.
- Tidak perlu membuat rangkaian unit test untuk halaman statis ini. Pemeriksaan visual dan fungsi HTML harus konkret.
- Bila pemeriksaan tertentu tidak dapat dijalankan, nyatakan apa yang belum diperiksa.

Jawaban akhir berisi struktur file yang dibuat, cara preview, checklist singkat kesesuaian tugas, hasil pemeriksaan, status persiapan GitHub, serta daftar logo/foto yang perlu saya sediakan. Pisahkan status layout yang sudah selesai dari status aset final yang masih menunggu saya. Jangan menyatakan website siap dikumpulkan sepenuhnya selama logo/foto yang diperlukan masih berupa placeholder. Jelaskan alur struktur HTML serta pembagian peran Flexbox/Grid dengan bahasa sederhana agar saya bisa mempresentasikan kodenya.

Mulai kerjakan sekarang dan selesaikan implementasinya.
