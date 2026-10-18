# Catatan belajar dan penjelasan kode

Dokumen ini membantu menjelaskan kode saat presentasi. Buka [index.html](../index.html) berdampingan dengan [style.css](../assets/css/style.css): HTML menyimpan isi dan makna, sedangkan CSS mengatur ukuran, warna, jarak, dan susunannya.

## Alur HTML dari atas ke bawah

1. **`head`** menyimpan judul tab, deskripsi, pengaturan viewport agar tampilan mengikuti perangkat, favicon simbol pengguna, dan satu tautan CSS eksternal. `lang="id"` memberi tahu bahasa halaman.
2. **Skip link** menuju `#utama` membantu pengguna keyboard melewati navigasi dan langsung membaca konten.
3. **`header` dan `nav`** berisi logo horizontal asli serta tautan ke `#cerita`, `#aktivitas`, `#info`, dan `#kontak`. Desktop menampilkan menu langsung; ponsel maksimal 650 px memakai `details`/`summary` dengan label **Menu/Tutup**. Hanya salah satu navigasi ditampilkan pada tiap ukuran layar. Header memakai `position: sticky`; lapisan kertasnya dapat berubah menjadi mengambang mengikuti scroll dengan CSS.
4. **`main`** memuat hero, cerita, aktivitas, informasi kunjungan, kontak, dan rekomendasi. Setiap bagian memiliki heading yang menjelaskan topiknya.
5. **Hero** berisi satu `h1`, satu `figure`, lalu catatan lokasi/pengantar, CTA, dan tautan Maps. Judul melintasi dua kolom di desktop dengan ukuran maksimal 64 px; foto di kiri dan catatan sejajar tengah di kanan. Lebar hero dibatasi 1100 px. Pada mobile, urutan visual mengikuti dokumen: judul, foto, lalu catatan beserta tombol.
6. **Cerita** memakai paragraf untuk narasi dan dua pasangan `figure`/`figcaption` untuk media. Foto jalur pengunjung Sukomakmur tampil lebih dahulu dalam HTML dan lebih besar; foto kebun berkabut menjadi konteks kawasan yang lebih kecil. Urutan aset cerita kini DEST-03 lalu DEST-02. Alt menjelaskan isi foto dan caption membedakan kedua lokasi secara jujur.
7. **Aktivitas** memakai `ul` karena aktivitas tidak memiliki urutan wajib. **Persiapan** memakai `ol` karena langkahnya berurutan. Catatan persiapan diletakkan dalam `aside` sebagai informasi pendamping.
8. **Informasi kunjungan** berisi pita alamat dan tautan Maps di atas tabel fasilitas selebar konten. `caption` menjelaskan isi tabel, `thead`/`tbody` memisahkan kepala dan data, serta `scope="col"`/`scope="row"` membantu hubungan header dengan sel.
9. **Kontak** memakai `form`, label terlihat, dua input, textarea, dan tombol submit. Batas demo dijelaskan sebelum isian.
10. **Rekomendasi** terdiri atas tiga bingkai foto besar dengan nama destinasi dan tautan informasi. Bingkai berjajar tiga kolom di desktop/tablet, lalu menjadi satu kolom pada lebar maksimal 650 px. Foto ditempatkan di atas teks.
11. **`footer`** memuat simbol logo, nama pembuat, tautan portofolio/Instagram/email, identitas proyek, serta kredit foto. Tautan tulisan kembali ke atas di footer dihapus; logo header tetap menuju `#atas`. Elemen `details` dan `summary` membuat kredit dapat dibuka/tutup dengan kemampuan bawaan HTML.

`section` menandai kelompok topik, sedangkan `div` digunakan saat hanya perlu pembungkus tata letak. Heading mengikuti hierarki `h1` → `h2` → `h3`; tidak perlu memakai semua tingkat sampai `h6`.

## Flexbox dan Grid

Flexbox cocok untuk menyusun satu kelompok elemen dalam baris yang dapat membungkus. Grid cocok ketika area halaman perlu dibagi menjadi beberapa kolom yang teratur.

| Teknik | Class utama dalam CSS | Peran |
| --- | --- | --- |
| Flexbox | `.header-inner`, `.nav-links` | Menyusun logo dan menu desktop dalam satu baris. Pada ponsel, header dan menu menggunakan aturan tersendiri. |
| Flexbox | `.hero-actions` | Menyusun tombol utama dan tautan Maps dengan jarak yang konsisten. |
| Flexbox | `.footer-main`, `.footer-brand`, `.footer-links`, `.footer-bottom` | Menyelaraskan identitas, logo, dan kelompok tautan footer. |
| Flexbox | `.location-note` | Menyusun alamat dan tautan Maps dalam pita di atas tabel; menjadi vertikal pada layar sempit. |
| Grid | `.hero`, `.hero-note`, `.hero-photo` | Memberi nama area judul, foto, dan catatan agar posisi desktop/mobile mudah diatur. |
| Grid | `.story-layout`, `.story-place`, `.story-detail` | Menyisipkan foto lokasi besar dan foto konteks yang lebih kecil ke dalam alur cerita. |
| Grid | `.activity-grid` | Memberi daftar aktivitas ruang lebih lebar daripada catatan persiapan di sampingnya. |
| Grid | `.visit-grid` | Menyusun pita alamat dan tabel dalam satu kolom dengan jarak teratur. |
| Grid | `.postcard` | Membagi kartu pos menjadi pengantar dan area form yang lebih lebar. |
| Grid | `.recommendation-list` | Menyusun tiga bingkai foto dalam kolom setara; menjadi satu kolom pada ponsel. |
| Grid | `.mobile-menu .nav-links` | Menyusun empat tautan dalam dua kolom ketika menu ponsel dibuka. |

Contoh konsep Grid yang digunakan:

```css
.hero {
  display: grid;
  grid-template-columns: minmax(0, 1.85fr) minmax(0, 1fr);
  grid-template-areas: "title title" "photo note";
  align-items: center;
  max-width: 1100px;
  gap: 2rem 3rem;
}

h1 { grid-area: title; }
.hero-photo { grid-area: photo; }
.hero-note { grid-area: note; }
```

`1.85fr 1fr` membagi sisa ruang menjadi dua kolom dengan rasio 1,85:1. `minmax(0, ...)` mengizinkan kolom menyusut tanpa dipaksa melebar oleh isi. `grid-template-areas` memberi nama posisi: judul melintasi dua kolom, kemudian foto di kiri dan catatan di kanan. `align-items: center` menyelaraskan catatan ke tengah tinggi bingkai foto; `gap` mengatur jarak antarbaris dan antarkolom. Ukuran judul memakai `clamp(2.25rem, 4.5vw, 4rem)`, sehingga membesar mengikuti layar sampai batas 64 px pada ukuran font dasar 16 px.

Pada media query maksimal 850 px, area hero berubah menjadi `"title" "photo" "note"` dalam satu kolom. Di 768 px, isi catatan masih dapat memakai dua kolom kecil untuk teks dan tombol. Di bawah 540 px, seluruh catatan kembali mengikuti alur blok biasa. HTML berurutan judul, foto, catatan sehingga halaman tetap masuk akal saat CSS tidak diterapkan.

Pada cerita, `.story-place` menempati kolom kanan dan merentang dua baris di desktop, sedangkan `.story-detail` dibatasi hingga 22 rem. Di mobile, keduanya kembali ke urutan HTML, dengan foto konteks selebar 82% agar tetap terlihat sebagai pendamping. Rekomendasi memakai `repeat(3, minmax(0, 1fr))` agar tiga bingkai mendapat ruang setara, lalu `minmax(0, 1fr)` pada lebar maksimal 650 px agar gambar tetap cukup besar di ponsel.

Class `.container` menyamakan batas lebar dan sisi kiri/kanan antarbagiannya. Class berulang seperti `.button`, `.photo-print`, dan `.text-link` menjaga gaya konsisten tanpa menyalin semua deklarasi pada tiap elemen. Nomor bab dan label kecil di atas setiap judul dihapus; hierarki kini dibentuk oleh ukuran judul, ruang, dan komposisi konten.

## Pemetaan materi dan ketentuan tugas

| Materi / kebutuhan | Penerapan | Tempat mencarinya |
| --- | --- | --- |
| Struktur HTML5 dan semantic HTML | `doctype`, `html`, `head`, `body`, `header`, `nav`, `main`, `section`, `aside`, `footer` | Seluruh `index.html` |
| Heading dan paragraf | Satu `h1`, judul bagian `h2`, subjudul `h3`, narasi `p` | Hero dan setiap section |
| Ordered/unordered list | Aktivitas `ul`, persiapan `ol`; menu juga berupa daftar | `#aktivitas` dan header |
| Tabel | `table`, `caption`, `thead`, `tbody`, `tr`, `th`, `td` | `#info` |
| Media gambar | Logo SVG asli dan enam foto JPG lokal melalui `img` | Header, hero, cerita, rekomendasi, footer |
| Tautan internal | `href="#info"`, `#cerita`, `#aktivitas`, `#kontak`, `#atas`, `#utama` | Navbar, CTA, logo header, skip link |
| Tautan eksternal | Google Maps, referensi artikel, destinasi rekomendasi, portofolio, Instagram | Hero, informasi, rekomendasi, footer |
| Tautan email | `mailto:hasanshofiyyur@gmail.com` | Kontak dan footer |
| Form sederhana | `label`, `input`, `textarea`, `button`, `required` | `#kontak` |
| CSS eksternal dan selector | Class, grouping selector, descendant selector, pseudo-class/element | `assets/css/style.css` |
| Satuan dan nilai | `px`, `rem`, `%`, `fr`, HEX, custom properties | Ukuran, jarak, warna, Grid |
| Box model | `box-sizing: border-box`, margin, padding, border | Reset, container, foto, tombol, form |
| Position | `relative`/`absolute` untuk selotip dan skip link; `sticky` untuk navbar | `.hero-photo`, `.skip-link`, `.site-header` |
| Flexbox/Grid | Kelompok kecil versus area utama | Tabel penjelasan layout di atas |

Contoh materi yang tidak lengkap atau salah sintaks tidak disalin mentah. Proyek memakai `lang="id"`, tautan stylesheet eksternal yang utuh, dan deklarasi CSS yang valid sesuai kebutuhan halaman.

## Tambahan CSS dan alasan penggunaannya

| Teknik | Kegunaan dalam proyek |
| --- | --- |
| Custom properties `--...` | Menyimpan beberapa warna bersama agar perubahan tema tidak tersebar. |
| `box-shadow` | Menunjukkan bingkai foto seperti kertas cetak, tombol sedikit terangkat, dan input sedikit masuk ke permukaan (`inset`). |
| `linear-gradient` yang tipis | Memberi perbedaan cahaya kecil pada tombol. Bukan latar dekorasi besar. |
| `border-radius` | Melunakkan sudut navbar, tombol, dan field tanpa mengubah struktur kontennya. |
| `object-fit: cover` dan `aspect-ratio: 4 / 3` | Mengisi bingkai foto cerita dan rekomendasi. Pinggir foto dapat terpotong, sehingga crop perlu ditinjau. |
| `height: auto`, `aspect-ratio: auto`, dan `object-fit: contain` | Foto hero mengikuti rasio intrinsik 1600:1067 agar seluruh lanskap terlihat. Logo juga memakai `contain` untuk menjaga proporsi aslinya. |
| `transform: rotate(...)` | Memiringkan detail selotip saja. Bingkai dan foto tetap tegak. |
| `::before` dan position | Membuat detail selotip pada bingkai hero dan lapisan kertas navbar tanpa menambah konten bacaan. |
| `transition`, `:hover`, `:active` | Memberi umpan balik singkat saat tautan/tombol digunakan. Konten utama selalu terlihat. |
| `:focus-visible` | Membuat posisi fokus keyboard terlihat jelas. |
| Media query | Mengubah kolom, spacing, dan ukuran pada breakpoint 1100, 850, 650, dan 540 px. Breakpoint 650 px khusus pergantian menu dan rekomendasi. |
| `grid-template-areas`, `grid-column`, `grid-row` | Mengatur posisi hero serta hubungan foto dan teks cerita tanpa mengubah isi HTML. |
| `clamp()` dan `minmax()` | Membatasi ukuran judul dan memberi kolom ruang yang dapat menyusut saat layar mengecil. |
| `prefers-reduced-motion` | Menonaktifkan atau mengurangi gerak bagi pengguna yang memilih pengaturan tersebut. |
| `overflow-x: auto` | Mengizinkan tabel digeser di dalam pembungkusnya tanpa memperlebar seluruh halaman. |
| `@supports`, `animation-timeline`, `animation-range` | Menjalankan perubahan navbar hanya ketika browser mendukung animasi yang mengikuti scroll. |
| `:target`, `:has()`, dan `[open]` | Menandai tautan anchor yang dipilih serta menyesuaikan ruang scroll ketika menu ponsel dibuka. |

Palet memakai putih kertas hangat, hijau hutan, sage, dan teks gelap. Maksimal dua keluarga font dipakai: Georgia untuk judul dan Arial untuk isi, dengan fallback sistem. Font sistem membuat tampilan tetap terbaca ketika offline.

## Cara kerja navbar tanpa JavaScript

Navbar memiliki dua bagian: `.site-header` menempel pada layar, sedangkan `.header-inner` menyusun logo dan menu desktop dengan Flexbox. Tinggi header tertutup sekitar 60 px, dengan logo 200 px di desktop, 180 px di tablet, dan 170 px di ponsel. Tautan berukuran teks 14 px tetap memiliki tinggi target minimal 44 px. `position: sticky; top: 0` menjaga header tetap di atas saat halaman digulir. Properti `z-index` menempatkannya di depan konten.

Pada awal halaman, lapisan `::before` selebar layar dan tanpa sudut melengkung. Di browser yang mendukung, `animation-timeline: scroll(root block)` menghubungkan progres `@keyframes` dengan scroll dokumen. `animation-range: 0px 160px` berarti perubahan selesai setelah 160 px pertama. Header bergeser turun 12 px, sementara sisi lapisan kertas masuk mengikuti batas `.container` dan sudutnya menjadi 8 px. Ukuran logo, teks, dan tinggi navbar tetap sehingga isi halaman tidak melompat.

```css
.site-header {
  position: sticky;
  top: 0;
  z-index: 20;
}

/* Potongan berikut ada di dalam @supports dan media query no-preference. */
.site-header {
  animation: header-float 1ms linear both;
  animation-timeline: scroll(root block);
  animation-range: 0px 160px;
}
```

`1ms` adalah nilai durasi deklarasi; progres sebenarnya dikendalikan scroll, bukan timer satu milidetik. `linear` membuat perubahan sebanding dengan jarak scroll, dan `both` mempertahankan keadaan awal/akhir. Deklarasi timeline dan range harus ditulis setelah shorthand `animation` karena shorthand tersebut dapat meresetnya. Menggulir kembali ke atas membalikkan perubahan secara alami.

Browser tanpa dukungan CSS ini memakai navbar sticky biasa. Pengguna dengan `prefers-reduced-motion: reduce` juga mendapat versi sticky tanpa pergeseran. CSS `scroll-padding-top` memberi ruang 6 rem bagi header saat menuju anchor. Ketika menu ponsel dibuka, `html:has(.mobile-menu[open])` menaikkannya menjadi 14 rem agar tujuan tidak tertutup panel navigasi. `scroll-margin-top` memberi tambahan jarak kecil pada bagian tujuan.

Pada lebar maksimal 650 px, `.desktop-nav` disembunyikan dan `.mobile-menu` ditampilkan. Elemen `summary` dapat diaktifkan dengan mouse, sentuhan, atau keyboard; browser menambah/menghapus atribut `open` pada `details`. CSS `[open]` mengganti label **Menu** menjadi **Tutup**, menampilkan ikon silang, dan membuka daftar tautan dua kolom. Panel berada di alur dokumen sehingga ikut menambah tinggi header. Menu tetap terbuka setelah tautan anchor dipilih; pengguna menutupnya melalui **Tutup**. Ini merupakan perilaku yang sengaja dipertahankan tanpa JavaScript.

Navigasi memakai `nav`, daftar, dan tautan biasa, bukan `role="menu"` yang membawa tuntutan perilaku keyboard berbeda. Referensi pola: [MDN tentang `details`](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/details) untuk interaksi native dan [W3C Disclosure Navigation](https://www.w3.org/WAI/ARIA/apg/patterns/disclosure/examples/disclosure-navigation/) untuk prinsip navigasi yang dapat dibuka/tutup. Contoh W3C memakai JavaScript; proyek hanya memakai prinsip susunannya dan kemampuan native HTML.

Tautan mendapat latar lembut saat hover/fokus. Selector seperti `body:has(#cerita:target)` menandai tautan yang sesuai dengan fragment URL. Penanda tersebut mengikuti anchor terakhir yang dipilih, bukan berpindah otomatis saat pengguna menggulir halaman. Karena bukan pelacakan scroll, tidak ada klaim bahwa menu selalu menunjukkan bagian yang sedang terlihat.

Ini merupakan tambahan CSS di luar materi inti, sehingga tidak diperlukan untuk menjelaskan seluruh konsep dasar. Referensi: [MDN animation-timeline](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/animation-timeline), [animation-range](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/animation-range), [animation-duration](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/animation-duration), dan [reduced motion](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion).

## Perilaku form demo

`for="email"` pada label terhubung dengan `id="email"` pada input. `name="email"` menentukan nama parameter saat form diproses browser. `type="email"` meminta validasi format email, dan `required` meminta isian terisi. Nama dan pesan juga wajib diisi.

Tombol **Coba Formulir** memiliki `type="submit"`. Browser menjalankan validasi HTML terlebih dahulu, tanpa JavaScript. `method="get"` memasukkan nilai ke query URL, lalu `action="#kontak"` mengarahkan kembali ke bagian kontak pada dokumen yang sama.

Contoh hasil dengan data latihan:

```text
index.html?nama=Teman+Perjalanan&email=contoh%40example.com&pesan=Ini+pesan+latihan.#kontak
```

Pengodean spasi dapat berbeda pada browser. Nilai terlihat di alamat browser; tidak ada endpoint penerima, penyimpanan aplikasi, konfirmasi terkirim, atau reservasi. Tautan email adalah tindakan terpisah yang membuka aplikasi email pengguna.

## Responsivitas dan aksesibilitas

Kolom utama menjadi satu pada layar yang lebih sempit; menu ponsel memakai tombol buka/tutup agar header tidak dipenuhi tautan. Kontrol menu dan tautannya memiliki tinggi minimal 44 px, dengan fokus keyboard terlihat. Tabel memiliki pembungkus yang bisa difokuskan dengan keyboard dan digulir sendiri. Semua field memiliki label terlihat, bukan mengandalkan placeholder sebagai nama field.

Gambar memiliki ukuran intrinsik agar ruangnya dapat disiapkan browser. Hero dimuat segera dengan `fetchpriority="high"`; gambar di bawah menggunakan `loading="lazy"`. Enam foto sudah tersedia lokal. Foto utama dan foto berkabut adalah konteks kawasan Sumbing/Magelang; foto jalur pengunjung terverifikasi sebagai Negeri Sayur Sukomakmur. [Panduan aset](ASSETS.md) menjelaskan sumber, dimensi, crop, dan lisensinya.

Tautan yang membuka tab baru memakai `rel="noopener noreferrer"`. Panah dekoratif sudah dihapus sesuai evaluasi pengguna. Header sticky memiliki ruang anchor agar bagian tujuan tetap terlihat. Efek gerak hover hanya berlaku untuk perangkat dengan pointer halus dan kemampuan hover; mode reduced motion mematikan gerak tombol.

Instruksi mini project meminta layout HTML/CSS beserta tautan dan form, tetapi tidak secara khusus mewajibkan JavaScript, aplikasi mobile, atau breakpoint tertentu. **Responsif** berarti susunan website menyesuaikan layar desktop/ponsel. **Interaktif** berarti pengguna dapat melakukan tindakan, misalnya berpindah bagian, membuka tautan, membuka menu ponsel/kredit foto, atau mencoba validasi form. Keduanya dapat diwujudkan di proyek ini dengan HTML dan CSS saja.

## Pemeriksaan dan status skill

Evaluasi 18 Oktober 2026 menyempurnakan proporsi pembuka, header, dan rekomendasi berdasarkan masukan pengguna. Warna kertas dan hijau, Georgia/Arial, dua logo asli, bingkai foto, serta perilaku tanpa JavaScript dipertahankan. [Ulasan desain](DESIGN-REVIEW.md) mencatat penilaian, perubahan, dan hasil pemeriksaan. Riwayat evaluasi 17 Oktober dipisahkan dari pemeriksaan revisi ini.

| Before | After | Why |
| --- | --- | --- |
| Judul hero mencapai 96 px dan foto sangat dominan | Judul maksimal 64 px; hero dibatasi 1100 px dengan kolom 1,85:1 | Pembuka lebih proporsional tanpa menghilangkan nama destinasi. |
| Foto hero mengisi bingkai 16:10 dengan crop | Foto mengikuti rasio asli 1600:1067 dan tampil utuh | Lanskap tidak kehilangan bagian tepi; ukuran bingkai lebih terkendali. |
| Catatan lokasi dan CTA menempel ke bawah foto | Catatan sejajar tengah di desktop; berada setelah foto pada ponsel | Teks terasa menyatu dengan bingkai dan urutan baca lebih jelas. |
| Header desktop besar dan menu dipaksa membungkus di ponsel | Header tertutup sekitar 60 px; ponsel memiliki disclosure Menu/Tutup sendiri | Menghemat ruang dengan target sentuh tetap minimal 44 px. |
| Tautan navigasi tampak rata | Latar hover/fokus, aksen Kontak, serta penanda tujuan anchor | Pengguna memperoleh petunjuk interaksi tanpa gerak dekoratif. |
| Tiga baris rekomendasi dengan gambar kecil | Tiga bingkai besar berjajar; satu kolom pada ponsel | Mengikuti preferensi pengguna agar foto destinasi lebih terlihat. |
| Footer memiliki tulisan kembali ke atas | Tautan tulisan tersebut dihapus; logo header tetap menuju awal | Footer lebih ringkas sesuai evaluasi pengguna. |

| Pemeriksaan | Hasil |
| --- | --- |
| Dokumen tugas | Prompt proyek, instruksi mini project, dan materi SCFE Basic P1–P4 sudah dibaca. |
| Sumber dan ekspor, 18 Oktober 2026 | Sumber lolos 35/35 dan HTML ekspor 37/37. Diperiksa melalui `file://` pada lebar 1440, 768, 390, dan 320 px dengan JavaScript dinonaktifkan: delapan gambar lokal, satu CSS, anchor, overflow, fokus keyboard, reduced motion, serta validasi dan submit GET formulir. |
| Navbar, 18 Oktober 2026 | 84/84 pemeriksaan lolos, termasuk menu yang benar-benar tampil pada desktop/ponsel, anchor dan keyboard, keadaan menempel/mengambang, reduced motion, serta simulasi fallback animasi scroll di Chrome. |
| Proporsi dan menu, 18 Oktober 2026 | 66/66 pemeriksaan tambahan lolos pada viewport 1440 × 900, 1366 × 768, 768 × 1024, 390 × 844, dan 320 × 760. Cakupannya meliputi Menu/Tutup melalui keyboard serta simulasi mouse/sentuhan, ruang anchor saat menu terbuka, rasio asli foto hero, judul maksimal 64 px, catatan sejajar tengah, bingkai hero utuh pada viewport desktop, kolom rekomendasi, dan tidak adanya tautan tulisan kembali ke atas di footer. |
| Tinjauan visual, 18 Oktober 2026 | Peninjauan independen screenshot tidak menemukan masalah visual pada area revisi. Header tertutup berukuran sekitar 60 px; bingkai foto hero sekitar 683 px pada viewport 1440 px. |
| Riwayat pemeriksaan 17 Oktober 2026 | Sumber versi sebelumnya lolos 35/35, ekspor 37/37, dan navbar 84/84. Chrome melalui `file://` diperiksa pada lebar 1440, 768, 390, dan 320 px dengan JavaScript dinonaktifkan. Angka ini tidak digunakan sebagai hasil revisi 18 Oktober. |
| Screenshot | [Hero](media/preview-hero.png), [desktop](media/preview-desktop.png), [ponsel](media/preview-mobile.png), dan [menu ponsel terbuka](media/preview-mobile-menu.png) mendokumentasikan revisi 18 Oktober. [Pembuka sebelumnya](media/preview-before-proportion.png) menjadi pembanding. |
| Batas pengujian | Chrome Windows dengan JavaScript dinonaktifkan; Safari/Firefox, perangkat fisik, pembaca layar, dan zoom browser 200% belum diuji. Simulasi sentuhan/fallback di Chrome tidak sama dengan pengujian perangkat atau browser lain. |
| Repository dan deployment | Repository tujuan [yurnszzz/negeri-sayur-sukomakmur](https://github.com/yurnszzz/negeri-sayur-sukomakmur), branch utama `main`. GitHub Pages dan workflow deployment belum dikonfigurasi. |

**Taste Skill** tersedia di [SKILL.md](../.agents/skills/design-taste-frontend/SKILL.md). Pada revisi 18 Oktober, perhatian diarahkan pada proporsi judul terhadap foto, foto hero yang utuh, serta hubungan catatan dengan bingkai. Tiga rekomendasi besar mengikuti preferensi pengguna. Lint revisi ini menghasilkan 17 FAIL dan 4 WARN; inspector browser menghasilkan 6 kategori FAIL dan 8 kategori WARN. Material kertas, bingkai, serta bentuk kontrol dipertahankan sesuai konteks desain. Temuan focal-point meminta judul atau foto diperbesar, bertentangan dengan permintaan terbaru pengguna; proporsi baru dipertahankan setelah ditinjau pada screenshot. Sebagai riwayat, lint 17 Oktober menghasilkan 14 FAIL dan 5 WARN; inspector browser saat itu menghasilkan 6 FAIL dan 9 WARN. Pemeriksaan mempertimbangkan brief, batas tanpa JavaScript, serta tabel yang perlu bergulir pada ponsel; bukan klaim lolos seluruh aturan estetika skill. Rincian ada di [ulasan desain](DESIGN-REVIEW.md).

**UI UX Pro Max** tersedia di [SKILL.md](../.agents/skills/ui-ux-pro-max/SKILL.md). Panduan navigasi, ukuran target sentuh, fokus keyboard, form, responsivitas, dan reduced motion dibaca dan digunakan. Penerapannya tetap memakai HTML/CSS native.

**Impeccable** berasal dari repository resmi `pbakaus/impeccable` dan tersedia di [SKILL.md](../.agents/skills/impeccable/SKILL.md). Revisi 18 Oktober meninjau hierarki, proporsi, keterbacaan navigasi, dan penyesuaian khusus ponsel. Pemindaian dengan lingkup layout menghasilkan satu warning padding aktivitas yang dinilai false positive setelah ditinjau dalam konteks pembungkusnya. Pada evaluasi sebelumnya tanggal 17 Oktober, dua agen menilai desain dan bukti detektor secara independen; pemindaian saat itu turun dari 12 temuan menjadi 5 warning. Lingkup kedua pemindaian berbeda, sehingga angkanya tidak dibandingkan sebagai skor peningkatan. Tidak ada overlay browser yang ditampilkan; bukti visual berasal dari screenshot dan pemeriksaan Chrome. [Ulasan desain](DESIGN-REVIEW.md) memuat rincian dan batas metode.

**Emil Design Engineering** dipasang dari repository `emilkowalski/skills` dan tersedia di [SKILL.md](../.agents/skills/emil-design-eng/SKILL.md). Skill utama yang dipilih adalah `emil-design-eng`. Prinsip yang digunakan: animasi memiliki tujuan, isi tidak berubah ukuran saat bergerak, perubahan scroll bersifat langsung, hover disesuaikan perangkat, dan preferensi reduced motion dihormati. Library animasi JavaScript dalam contoh skill tidak digunakan.

Taste sudah tersedia sebelum evaluasi ini, sehingga tidak dipasang ganda. UI UX Pro Max serta skill pendukung lama dipertahankan. [AGENTS.md](../AGENTS.md) menyimpan preferensi pengguna dan panduan penggunaan empat skill utama untuk pekerjaan berikutnya. Semua skill bekerja saat pengembangan; browser pengunjung hanya membutuhkan HTML, CSS, dan gambar lokal.

Izin terbaru pengguna untuk mencari keenam foto menggantikan larangan pencarian foto pada brief awal. Dua logo tetap berasal dari pengguna. Foto Pexels menunjukkan konteks kawasan; lokasi persis hanya disebut ketika sumber mendukungnya. Kredit dan lisensi berada di footer dan [ASSETS.md](ASSETS.md). Kode proyek berlisensi MIT, sedangkan foto, logo, dan skill mengikuti ketentuan masing-masing.

## Cara menjelaskan saat presentasi

“Saya membuat satu halaman pengenalan Negeri Sayur Sukomakmur. HTML menyusun informasi dari header sampai footer, sementara satu stylesheet mengatur tampilannya. Flexbox dipakai untuk menu desktop dan kelompok tombol, sedangkan Grid membagi area besar menjadi kolom. Media query menyesuaikan susunan di ponsel, termasuk menu buka/tutup memakai details dan summary tanpa JavaScript. Navbar memakai sticky dan tambahan animasi scroll CSS; browser yang tidak mendukung tetap mendapat navigasi sticky. Foto utama mengikuti ukuran aslinya agar utuh, sedangkan rekomendasi memakai tiga bingkai sejajar. Logo adalah SVG asli saya, dan foto memiliki sumber serta lisensi yang dicatat. Form ini latihan validasi HTML; hasilnya muncul sebagai parameter URL dan belum mengirim pesan ke server.”

Untuk mendemonstrasikan kode, mulai dari pasangan `href="#cerita"` dan `id="cerita"`, lanjutkan daftar aktivitas, tabel, serta label/input. Buka class Grid dan media query pada CSS, lalu ubah ukuran browser. Pada ukuran ponsel, buka **Menu**, pilih tujuan, lalu tekan **Tutup**. Jelaskan bahwa penanda navigasi mengikuti anchor, bukan scroll. Gulir halaman untuk memperlihatkan navbar, aktifkan reduced motion, buka kredit foto dengan keyboard, dan coba form memakai data contoh.
