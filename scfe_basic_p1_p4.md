# SCFE_BASIC_P1-P4

## File 1: P1 - Pengenalan HTML.pdf

### Slide 1
Pertemuan 1 | Mei, 2026
# PENGENALAN HTML
SC Frontend Basic

### Slide 2
## SETUP IDE

* **IDE**: VSCode
* **EXTENSION**: Live Server / Five Server
* **BROWSER**: Browser Kesayangan Masing-masing

### Slide 3
## APA ITU HTML?

HTML (HyperText Markup Language) adalah bahasa markup untuk menyusun konten halaman web (judul, paragraf, gambar, hingga tautan). Browser membaca file HTML lalu menerjemahkannya menjadi tampilan visual yang kita lihat sehari-hari.

### Slide 4
## STRUKTUR DASAR

Setiap dokumen HTML diawali `<!DOCTYPE html>` yang menandakan versi HTML5, lalu dibungkus tag `<html>` yang terbagi menjadi `<head>` berisi metadata & judul, dan `<body>` berisi konten yang benar-benar tampil di browser.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pertemuan 1</title>
</head>
<body>
    
</body>
</html>
```

### Slide 5
## HTML CONCEPT

Sebuah elemen HTML umumnya terdiri dari tag pembuka, konten, dan tag penutup, misalnya `<p>Teks</p>`. Beberapa elemen bersifat void/self-closing seperti `<img>` dan `<br>` yang tidak memerlukan tag penutup.

Terdapat beberapa tag dasar penting yang sering digunakan untuk membuat website, yaitu:
* `<h1>` - `<h6>` = Digunakan untuk menampilkan judul pada website.
* `<p>` = Digunakan untuk menampilkan kalimat/paragraf.
* `<li>` = Digunakan untuk menampilkan list.
* `<img>` = Digunakan untuk menambahkan gambar pada website.
* `<a>` = Berfungsi untuk menghubungkan ke halaman lain.
* `<button>` = Digunakan untuk membuat tombol.

### Slide 6
## TAG, ELEMENT, ATTRIBUTE

* **TAG**
  Tanda pembuka/penutup berupa kurung siku yang memberi instruksi pada browser.
  **Contoh: `<p>` dan `</p>`**

* **ELEMENT**
  Keseluruhan blok dari tag pembuka, isi konten, hingga tag penutup.
  **Contoh: `<p>Teks ini</p>`**

* **ATTRIBUTE**
  Informasi atau konfigurasi tambahan yang diletakkan di dalam tag pembuka.
  **Contoh: `class="title"` `src="img.png"`**

```html
<a href="/login">Konten</a>
```

### Slide 7
## HTML LIST

* **ORDERED LIST**
  Daftar berurutan menggunakan angka, huruf, atau angka romawi.
  ```html
  <ol>
      <li>Aku</li>
      <li>Kamu</li>
  </ol>
  ```

* **UNORDERED LIST**
  Daftar tanpa urutan khusus, ditandai simbol bullet / titik mendatar.
  ```html
  <ul>
      <li>Aku</li>
      <li>Kamu</li>
  </ul>
  ```

* **DESCRIPTION LIST**
  Daftar istilah beserta penjelasannya (istilah & deskripsi).
  ```html
  <dl>
      <dt>Lorem</dt>
      <dd>Asik</dd>
  </dl>
  ```

### Slide 8
## HTML TABLE

Table dibangun dari:
* `<table>` sebagai pembungkus,
* `<tr>` untuk baris,
* `<th>` untuk header,
* `<td>` untuk data.

Cocok menampilkan data tabular seperti jadwal atau laporan, tapi bukan untuk mengatur layout halaman.

```html
<table border="1">
    <thead>
        <tr>
            <th>No</th>
            <th>Nama</th>
            <th>Jurusan</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Andi</td>
            <td>Teknik Informatika</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Siti</td>
            <td>Sistem Informasi</td>
        </tr>
    </tbody>
</table>
```

### Slide 9
## SEMANTIC HTML

### Slide 10
## APAAN TUH SEMANTIC?

Semantic HTML adalah penggunaan elemen atau tag HTML yang secara jelas menjelaskan makna, peran, dan fungsi dari konten yang ada di dalamnya, bukan sekadar mengatur tampilan

### BEDANYA??
* **SEMANTIC**
  Tag yang dengan jelas mendeskripsikan arti maknanya kepada browser dan developer.
* **NON-SEMANTIC**
  Tag seperti `<div>` dan `<span>` tidak memiliki arti makna konten khusus.

### Slide 11
## STRUKTUR SEMANTIC

* `<header>` : Bagian kepala / navigasi atas.
* `<nav>` : Wadah menu navigasi.
* `<main>` : Konten utama unik halaman.
* `<footer>` : Informasi di bagian akhir/bawah halaman.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pertemuan 1</title>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li>Home</li>
            </ul>
        </nav>
    </header>

    <main>
        <section>
            <h1>Hello World!</h1>
        </section>
    </main>

    <footer>&copy; Veterantech 2026</footer>
</body>
</html>
```

### Slide 12
## HTML FORM

### Slide 13
## HTML FORM

Form dibangun dari tag `<form>` yang membungkus berbagai elemen input, seperti input text untuk teks bebas, checkbox untuk pilihan ganda, radio button untuk pilihan tunggal, dan textarea untuk teks panjang.

* **`<label>`**
  Berfungsi untuk memberikan keterangan atau judul penjelas pada elemen formulir seperti input, checkbox, radio button, atau select

* **`<input>`**
  Input adalah sebuah elemen HTML yang digunakan untuk menerima masukan dari pengguna.
  Atribut input memiliki berbagai jenis, yaitu :
  * `type="text"`: Membuat kolom untuk memasukkan teks singkat satu baris, seperti nama atau alamat.
  * `type="password"`: Membuat kolom teks yang disamarkan (biasanya berupa titik atau bintang) untuk menjaga kerahasiaan kata sandi.
  * `type="number"`: Membatasi masukan hanya berupa angka.
  * `type="checkbox"`: Membuat kotak centang untuk memilih lebih dari satu opsi.
  * `type="radio"`: Membuat tombol pilihan bundar di mana pengguna hanya bisa memilih satu dari beberapa opsi.
  * `type="submit"`: Membuat tombol untuk mengirimkan seluruh data formulir. [1, 2, 3, 4, 5, 6, 7]

### Slide 14
## HTML MEDIA & HYPERLINK INTEGRATION

### Slide 15
## HTML IMAGE & MEDIA

* **Image**
  Untuk menampilkan gambar pada web, diperlukan tag `<img>` yang diikuti atribut “src” (sumber file) dan “alt” (teks alternatif).
  ```html
  <img src="fotogua.jpg" alt="Ini foto gua">
  ```

* **Media**
  * `<video>` untuk menampilkan video.
  * `<audio>` untuk menampilkan audio.
  Memiliki atribut berupa controls, autoplay, dan loop
  ```html
  <video width="640" height="360" controls poster="gambar-thumbnail.jpg">
      <source src="keren.mp4" type="video/mp4">
  </video>

  <audio controls>
      <source src="pure.mp3" type="audio/mpeg">
  </audio>
  ```

### Slide 16
## VARIASI HTML LINK

* **EXTERNAL LINK**
  Link yang digunakan untuk menghubungkan ke domain lain.
  ```html
  <h1><a href="https://instagram.com/irsyaadya23">Ini adalah instagram saya</a></h1>
  ```

* **INTRA-PAGE LINK**
  Link yang digunakan untuk melompat ke bagian id di halaman yang sama.
  ```html
  <nav>
      <ul>
          <li><a href="#about">About</a></li>
      </ul>
  </nav>
  ```

* **EMAIL LINK**
  Link yang digunakan untuk membuka aplikasi email.
  ```html
  <a href="mailto:sapikuning@gmail.com">Kirim Email ke Kami</a>
  ```

### Slide 17
## ADAKAH PERTANYAAN?

### Slide 18
## TERIMA KASIH


## File 2: P2 - CSS Lanjutan.pdf

### Slide 1
KELAS FRONTEND BASIC
# Pertemuan 3: CSS Lanjutan
## Value, Box Model, Position & Selector
Memahami cara CSS menuliskan nilai, membentuk ruang sebuah elemen, mengatur posisi di halaman, dan menargetkan elemen HTML secara presisi.

### Slide 2 (02)
AGENDA PERTEMUAN
## Apa yang Akan Kita Pelajari Hari Ini

1. **CSS Value Rules**
   Aturan penulisan nilai pada properti CSS: satuan, warna, keyword, dan fungsi.
2. **Box Model dalam CSS**
   Cara setiap elemen HTML dianggap sebagai kotak: content, padding, border, margin.
3. **CSS Position**
   Menentukan bagaimana sebuah elemen diletakkan pada halaman web.
4. **Selector Lanjutan**
   Menargetkan elemen HTML secara presisi dengan combinator, grouping, atribut & pseudo.

### Slide 3 (03)
## 01 — CSS Value Rules
Aturan penulisan nilai yang ditetapkan pada properti CSS untuk menentukan tampilan elemen HTML.

### Slide 4 (04)
01 CSS VALUE RULES
## Anatomi Sebuah Deklarasi CSS

Setiap properti CSS pasti diikuti oleh sebuah value (nilai) yang menentukan bagaimana elemen HTML akan tampil. Value bisa berupa angka dengan satuan, kata kunci, warna, atau bahkan hasil dari sebuah fungsi.

* **Satuan Ukuran**: `px, %, em, rem, vw/vh`
* **Nilai Warna**: `name, HEX, RGB(A), HSL(A)`
* **Keyword**: `auto, inherit, initial, unset`
* **Fungsi**: `calc(), var(), rgba()`

```css
selector {
  property: value;
}

.box {
  width: 100%;
  color: #ff0000;
  margin: auto;
}
```
*property : value ; → satu deklarasi CSS*

### Slide 5 (05)
01 CSS VALUE RULES
## Satuan Ukuran: Absolute vs Relative

* **`px` Absolute Units**
  Satuan pasti — ukurannya tetap, tidak menyesuaikan elemen lain. Cocok untuk ukuran yang memang harus presisi.
  * `px` : pixel — 1px = 1 titik layar
  * `pt` : point — umum di dunia cetak
  * `cm` : centimeter — satuan fisik

* **`%` Relative Units**
  Satuan yang menyesuaikan ukuran elemen induk atau layar — kunci utama membuat layout responsif.
  * `%` : relatif terhadap elemen induk
  * `em` : relatif thd font-size induk
  * `rem` : relatif thd font-size root `<html>`
  * `vw/vh` : relatif thd lebar/tinggi viewport

### Slide 6 (06)
01 CSS VALUE RULES
## em vs rem — Contoh Perhitungan

em mengikuti font-size induknya secara berjenjang (bisa "menumpuk"), sedangkan rem selalu mengacu pada satu acuan yang sama: font-size elemen `<html>` (root).

* **`<html>` `font-size: 16px`**
  * **`.parent` `font-size: 1.5em` → `24px`**
    * **`.child` `font-size: 1.5em` → `24px × 1.5 = 36px`**
  * *em: ikut menumpuk dari induk ke induk*

```css
html { font-size: 16px; }

.parent {
  font-size: 1.5em;  /* 24px */
}
.child {
  font-size: 1.5rem; /* 24px */
}

/* rem TIDAK terpengaruh */
/* oleh font-size .parent  */
```

### Slide 7 (07)
01 CSS VALUE RULES
## Nilai Warna (Color Values)

* **Color Name**
  Nama warna bawaan CSS
  ```css
  color: red;
  ```

* **HEX Code**
  Kode heksadesimal RGB
  ```css
  color: #ff0000;
  ```

* **RGB / RGBA**
  Alpha (A) = transparansi
  ```css
  color: rgba(255,0,0,.5);
  ```

* **HSL / HSLA**
  Hue, Saturation, Lightness
  ```css
  color: hsl(0,100%,50%);
  ```

*rgba() dan hsla() menambahkan channel Alpha untuk mengatur tingkat transparansi (0 = tembus pandang, 1 = solid).*

### Slide 8 (08)
01 CSS VALUE RULES
## Keywords & Functions

### Keyword Umum
* `auto` : browser menghitung nilai otomatis
* `inherit` : menurunkan nilai dari elemen induk
* `initial` : mengembalikan ke nilai default CSS
* `unset` : gabungan inherit / initial sesuai konteks

### Fungsi calc()
Memungkinkan perhitungan matematis langsung di dalam value — boleh mencampur satuan berbeda (mis. % dengan px).

```css
.sidebar {
  width: calc(100% - 250px);
}

.box {
  padding: calc(1rem + 5px);
}
```

### Slide 9 (09)
## 02 — Box Model dalam CSS
Setiap elemen HTML dianggap sebagai sebuah kotak (box) yang memiliki struktur pembentuk ukuran.

### Slide 10 (10)
02 BOX MODEL
## Struktur Box Model: Dari Dalam ke Luar

*(Susunan lapisan pada diagram kotak dari luar ke dalam: `MARGIN` → `BORDER` → `PADDING` → `CONTENT`)*

* **Content**
  Area utama tempat teks, gambar, atau media ditampilkan.
* **Padding**
  Ruang kosong di antara content dan border (area dalam kotak).
* **Border**
  Garis tepi yang mengelilingi padding dan content.
* **Margin**
  Ruang kosong di luar border yang memisahkan elemen dari elemen lain.

### Slide 11 (11)
02 BOX MODEL
## box-sizing: content-box vs border-box

* **content-box (default)**
  ```css
  .box {
    box-sizing: content-box;
    width: 200px;
    padding: 20px;
    border: 5px solid;
  }
  ```
  **Total lebar sebenarnya:**
  `200 + (20×2) + (5×2) = 250px`
  *width hanya menghitung content — padding & border menambah ukuran total.*

* **border-box (direkomendasikan)**
  ```css
  .box {
    box-sizing: border-box;
    width: 200px;
    padding: 20px;
    border: 5px solid;
  }
  ```
  **Total lebar sebenarnya:**
  `tetap 200px`
  *padding & border dihitung DI DALAM width — ukuran total tetap sesuai rencana. Ideal untuk responsive layout.*

### Slide 12 (12)
## 03 — CSS Position
Menentukan bagaimana posisi suatu elemen diletakkan pada halaman web.

### Slide 13 (13)
03 CSS POSITION
## 5 Jenis Nilai Position

* **`static`**
  Default. Elemen mengikuti alur dokumen normal — mengabaikan top/bottom/left/right.
* **`relative`**
  Digeser relatif dari posisi normalnya, tanpa mengganggu elemen di sekitarnya.
* **`absolute`**
  Diposisikan relatif terhadap induk terdekat yang memiliki position selain static.
* **`fixed`**
  Terkunci relatif terhadap viewport — tidak ikut bergeser saat halaman di-scroll.
* **`sticky`**
  Kombinasi relative + fixed: normal dulu, lalu menempel setelah titik scroll tertentu.

### Slide 14 (14)
03 CSS POSITION
## relative vs absolute — Ilustrasi

* **Ilustrasi Kotak**:
  * `position: relative;` pada `.container`
  * `elemen lain (mengalir normal)`
  * `position: absolute; top:0; right:0;`
  * *fixed → posisinya dihitung dari viewport (layar), bukan dari .container.*

### Properti Pendukung
* **`top / right / bottom / left`**
  Mengatur besarnya pergeseran posisi dari sisi terkait.
* **`z-index`**
  Mengatur urutan tumpukan (stack order) — nilai lebih besar tampil lebih depan.

```css
.dropdown {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 10;
}
```

### Slide 15 (15)
## 04 — Selector Lanjutan
Menggunakan pemilih (selector) yang lebih spesifik untuk menargetkan elemen HTML secara presisi.

### Slide 16 (16)
04 SELECTOR LANJUTAN
## Combinators (Penggabung Selector)

* **`A B` — Descendant Selector**
  Memilih semua elemen B di dalam elemen A (di kedalaman berapa pun).
  ```css
  div p { color: green; }
  ```

* **`A > B` — Child Selector**
  Memilih elemen B yang merupakan anak langsung dari A.
  ```css
  ul > li { list-style: none; }
  ```

* **`A + B` — Adjacent Sibling**
  Memilih elemen B yang berada persis/langsung setelah elemen A.
  ```css
  h2 + p { margin-top: 0; }
  ```

* **`A ~ B` — General Sibling**
  Memilih semua elemen B yang sejajar setelah elemen A.
  ```css
  h2 ~ p { color: gray; }
  ```

### Slide 17 (17)
04 SELECTOR LANJUTAN
## Grouping & Attribute Selector

* **Grouping Selector**
  Menerapkan gaya yang sama ke beberapa selector sekaligus menggunakan tanda koma (,), sehingga kode lebih ringkas.
  ```css
  h1, h2, h3 {
    font-family: Arial;
    color: #222;
  }

  /* setara dengan menulis */
  /* h1{...} h2{...} h3{...} */
  ```

* **Attribute Selector**
  Memilih elemen berdasarkan keberadaan atribut, atau berdasarkan nilai spesifik dari atribut tersebut.
  ```css
  [disabled] {
    opacity: 0.5;
  }

  input[type="text"] {
    border: 1px solid #ccc;
  }
  ```

### Slide 18 (18)
04 SELECTOR LANJUTAN
## Pseudo-Classes vs Pseudo-Elements

* **`:` Pseudo-Classes**
  Memilih elemen berdasarkan status atau kondisi tertentu — ditulis dengan satu titik dua (`:`).
  * `:hover` : saat kursor berada di atas elemen
  * `:focus` : saat elemen sedang aktif/dipilih
  * `:nth-child()` : berdasar urutan posisi elemen
  ```css
  button:hover {
    background: #028090;
  }
  ```

* **`::` Pseudo-Elements**
  Memilih atau memberi gaya pada bagian tertentu dari elemen — ditulis dengan titik dua ganda (`::`).
  * `::before` : menyisipkan konten sebelum elemen
  * `::after` : menyisipkan konten setelah elemen
  * `::first-letter` : menargetkan huruf pertama teks
  ```css
  p::first-letter {
    font-size: 200%;
  }
  ```

### Slide 19 (19)
PENUTUP
## Ringkasan & Latihan Mandiri

1. **Value Rules**: Satuan absolute/relative, warna, keyword & fungsi calc().
2. **Box Model**: Content → Padding → Border → Margin, dan box-sizing.
3. **Position**: static, relative, absolute, fixed, sticky + z-index.
4. **Selector Lanjutan**: Combinator, grouping, atribut, pseudo-class/element.

* **Latihan Mandiri**
  Buat sebuah card profil sederhana: gunakan rem untuk ukuran teks, atur box-sizing: border-box, buat badge "Online" dengan position: absolute di pojok kanan atas, lalu tambahkan efek ::before pada judul card.


## File 3: P3 - Pengenalan CSS.pdf

### Slide 1
Pertemuan 2
# PENGENALAN CSS
SC Frontend Basic

### Slide 2
## APA ITU CSS?

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mengatur tampilan dan tata letak halaman web.

### FUNGSINYA
1. Desain Visual: Mengatur warna, font, ukuran halaman website.
2. Layouting: Mengatur/menyusun posisi elemen agar responsif di semua layar.
3. Pemisah Peran: Memisahkan isi konten HTML dari tampilan desain.

### Slide 3
## HUBUNGAN HTML & CSS??

* **HTML**
  Membangun kerangka dasar, teks, gambar, dan tombol tanpa gaya tampilan

* **CSS**
  Memberikan warna, tata letak, ukuran, dan keindahan visual.

### Slide 4
## 3 METODE PENGGUNAAN CSS

* **INLINE**
  Ditulis langsung di tag HTML.
  ```html
  <h1 id="contact-title" style="font-size: 20px; color: red;">Contact</h1>
  ```

* **INTERNAL**
  Ditulis dalam dokumen HTML di bagian head.
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">

      <link rel="stylesheet" href="style.css">
      <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0&icon_names=account_circle" />

      <title>Contact</title>

      <style>
          p {
              font-size: 1rem;
              color: red;
          }
      </style>
  </head>
  ```

* **EXTERNAL**
  Terpisah menggunakan file CSS.
  ```css
  /* style.css */
  @import url('https://fonts.googleapis.com/css2?family=Cormorant:ital,wgh

  * {
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
  }
  ```

### Slide 5
## STRUKTUR KODE CSS

```css
p {
  color: #2563eb;
  font-size: 18px;
}
```

* **SELECTOR**
  Elemen HTML yang ditargetkan untuk dihias.
* **PROPERTY**
  Atribut gaya yang ingin diubah.
* **VALUE**
  Nilai atau besaran yang diberikan pada property.

### Slide 6
## MACAM-MACAM PROPERTY CSS YANG SERING DIGUNAKAN

* **TIPOGRAFI & TEKS**
  * font-size: Mengatur ukuran teks.
  * font-family: Mengatur font yang digunakan.
  * text-align: Mengatur posisi teks (rata kanan/kiri/center.

* **WARNA & LATAR**
  * color: Mengatur warna teks yang diinginkan.
  * background-color: Mengatur warna background.

* **SPACE (BOX MODEL)**
  * margin: Mengatur jarak elemen dengan tepi luar.
  * padding: Mengatur jarak tepi elemen dengan isi konten di dalam elemen.

* **UKURAN & LAYOUT**
  * width: Menentukan nilai lebar.
  * height: menentukan nilai tinggi.
  * display: Menentukan jenis layout.

### Slide 7
## MARGIN & PADDING

*(Ilustrasi kotak berlapis: `Margin` di lapisan luar, `Padding` di lapisan tengah, dan kotak merah di bagian dalam)*

### Slide 8
## FORMAT PEWARNAAN DALAM CSS

* **COLOR NAME**
  Menggunakan nama warna memakai bahasa inggris. Seperti: green, black, red.

* **HEX CODE**
  Menggunakan kode heksadesimal 6 karakter. Seperti: #2563eb

* **RGB FORMAT**
  Menggunakan kombinasi Red, Green, Blue. Seperti: rgb(37, 99, 235).

* **HSL FORMAT**
  Menggunakan kombinasi Hue, Saturation, Lightness. Seperti: hsl(217, 91%, 60%).

### Slide 9
## ADAKAH PERTANYAAN?

### Slide 10
## TERIMA KASIH


## File 4: P4 - CSS Layouting.pdf

### Slide 1
FRONTEND BASIC · PERTEMUAN 4
# CSS Layouting
## Mengatur tata letak halaman web dengan Flexbox & CSS Grid
Materi ini membahas konsep layouting, properti Flexbox dan CSS Grid, serta studi kasus implementasinya.

### Slide 2 (3)
DAFTAR ISI
## Apa yang akan kita pelajari

* **01 — Pengertian CSS Layouting**
  Konsep dasar dan kegunaannya
* **02 — Flexbox (1D Layout)**
  Container, item, dan properti utamanya
* **03 — Studi Kasus Flexbox**
  Navbar, card, dan centering
* **04 — CSS Grid (2D Layout)**
  Container, item, dan area grid
* **05 — Studi Kasus Grid**
  Layout halaman, galeri, dashboard
* **06 — Perbandingan & Tugas**
  Flexbox vs Grid dan instruksi tugas

### Slide 3 (4)
BAB 1 · PENGANTAR
## Apa itu CSS Layouting?

* **DEFINISI**
  Teknik menyusun dan mengatur posisi elemen-elemen HTML di halaman web.
  Dibangun di atas CSS modern: Flexbox dan CSS Grid.

1. **Membentuk struktur rapi**
   Halaman web menjadi tertata, responsif, dan estetik di berbagai ukuran layar.
2. **Memudahkan navigasi**
   Pengguna dapat membaca dan berpindah antar bagian halaman dengan mudah.
3. **Standar modern**
   Flexbox dan Grid menggantikan teknik lama seperti float dan positioning.

### Slide 4 (5)
BAB 2 · FLEXBOX
## Pengenalan Flexbox (1D Layout)

Flexible Box Layout adalah model tata letak satu dimensi yang mengatur elemen secara baris atau kolom.

* **Fungsi**: menyelaraskan (align) dan membagi ruang (space) antar elemen secara dinamis.
* **Responsif**: menyesuaikan diri dengan berbagai ukuran layar.
* **Centering**: memudahkan perataan tengah sebuah elemen.

*(Ilustrasi visual)*:
* `flex-direction: row` : `[ 1 ] [ 2 ] [ 3 ]`
* `flex-direction: column` : `[ 1 ]` / `[ 2 ]` / `[ 3 ]`

### Slide 5 (6)
BAB 2 · FLEXBOX
## Properti Flex Container (Parent)
Diterapkan pada elemen induk yang diberi display: flex;

* **`flex-direction`**
  Menentukan arah sumbu utama (baris atau kolom).
  `Nilai: row | column | row-reverse | column-reverse`

* **`justify-content`**
  Meratakan item pada sumbu utama (horizontal jika row).
  `Nilai: flex-start | center | space-between | space-around`

* **`align-items`**
  Meratakan item pada sumbu silang (vertikal jika row).
  `Nilai: flex-start | center | stretch | flex-end`

* **`flex-wrap`**
  Mengatur apakah item turun ke baris baru saat ruang penuh.
  `Nilai: nowrap | wrap | wrap-reverse`

### Slide 6 (7)
BAB 2 · FLEXBOX
## Contoh: Membuat Flex Container

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 16px;
}
```

```html
<div class="container">
  <div class="box">1</div>
  <div class="box">2</div>
  <div class="box">3</div>
</div>
```

### Yang terjadi
* **space-between**: item pertama di kiri, terakhir di kanan, sisanya merata.
* **align-items: center**: item rata tengah secara vertikal.
* **gap: 16px**: jarak antar item tanpa perlu margin.
* **flex-wrap: wrap**: item turun ke baris baru saat layar menyempit.

### Slide 7 (8)
BAB 2 · FLEXBOX
## Properti Flex Item (Child)

1. **`flex-grow`**
   Kemampuan item membesar mengisi sisa ruang. Default: 0.
2. **`flex-shrink`**
   Kemampuan item mengecil saat ruang kurang. Default: 1.
3. **`flex-basis`**
   Ukuran awal item sebelum sisa ruang dibagi.
4. **`align-self`**
   Perataan khusus untuk satu item, menimpa align-items.

**Tips**: Keempat properti tersebut bisa disingkat dengan `flex: 1 1 200px;` (grow, shrink, basis).

### Slide 8 (9)
BAB 2 · FLEXBOX
## Contoh: Mengatur Ukuran Item

```css
.item-utama {
  flex-grow: 2;
}

.item-samping {
  flex-grow: 1;
}

.item-khusus {
  align-self: flex-end;
}
```

* **flex-grow: 2** → mendapat 2/3 sisa ruang.
* **flex-grow: 1** → mendapat 1/3 sisa ruang.
* **align-self: flex-end** → diratakan ke bawah sendiri.

*(Ilustrasi visual)*:
* **flex-grow: 2 : 1** → `[ flex-grow: 2 ] [ flex-grow: 1 ]`
* **align-self: flex-end** → `[ 1 ]` `[ flex-end ]` `[ 3 ]`

### Slide 9 (10)
BAB 3 · STUDI KASUS
## Studi Kasus Flexbox

* **Navigation Bar**
  Menu horizontal yang rapi dengan jarak merata.
* **Card Component**
  Card berderet dan turun baris otomatis saat ruang habis.
* **Centering**
  Konten tepat di tengah, horizontal dan vertikal.

```css
.center { display: flex; justify-content: center; align-items: center; }
```

### Slide 10 (11)
BAB 4 · CSS GRID
## Pengenalan CSS Grid (2D Layout)

Grid adalah model tata letak dua dimensi yang mengatur elemen berdasarkan baris dan kolom sekaligus.

* **Struktur kompleks**: cocok untuk membuat tata letak halaman web yang rumit.
* **Presisi**: mempermudah pembagian area halaman secara akurat.
* **Layout-first**: kerangka halaman didefinisikan dulu, lalu diisi kontennya.

*(Ilustrasi visual)*:
* **Contoh grid 3 kolom × 2 baris**
  * Baris 1: `[ A · span 2 kolom ]` `[ B ]`
  * Baris 2: `[ C ]` `[ D ]` `[ E ]`

### Slide 11 (12)
BAB 4 · CSS GRID
## Properti Grid Container (Parent)
Diterapkan pada elemen induk yang diberi display: grid;

* **`grid-template-columns`**
  Menentukan jumlah dan ukuran kolom. Sama untuk grid-template-rows.
  `Contoh: repeat(3, 1fr) | 200px 1fr | auto`

* **`gap`**
  Memberi jarak antar kolom dan baris. Bisa juga grid-gap.
  `Contoh: gap: 16px; | gap: 16px 24px;`

* **`grid-template-areas`**
  Memberi nama pada area grid agar tata letak mudah dibaca.
  `Contoh: "header header" "sidebar main"`

* **`fr (fraction)`**
  Satuan pecahan dari sisa ruang yang tersedia.
  `Contoh: 1fr 2fr → kolom kedua 2x lebih lebar`

### Slide 12 (13)
BAB 4 · CSS GRID
## Properti Grid Item (Child)

1. **`grid-column-start / grid-column-end`**
   Menentukan di garis kolom mana item mulai dan berakhir.
2. **`grid-row-start / grid-row-end`**
   Menentukan di garis baris mana item mulai dan berakhir.
3. **`grid-area`**
   Menempatkan item ke area bernama yang sudah dibuat di grid-template-areas.

**Shorthand**: `grid-column: 1 / 3;` sama dengan `grid-column-start: 1;` dan `grid-column-end: 3;`

### Slide 13 (14)
BAB 4 · CSS GRID
## Contoh: Layout Halaman dengan Grid

```css
.page {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header  header"
    "sidebar main"
    "footer  footer";
  gap: 16px;
  min-height: 100vh;
}

.header  { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main    { grid-area: main; }
.footer  { grid-area: footer; }
```

### Hasil tampilan
*(Diagram visual: `header` di atas, `sidebar` di kiri dan `main` di kanan, `footer` di bawah)*
* Nama area menentukan posisi setiap elemen.
* Ubah grid-template-areas untuk mengubah tata letak tanpa mengubah HTML.

### Slide 14 (15)
BAB 5 · STUDI KASUS
## Studi Kasus CSS Grid

* **Layout Halaman**
  Header, sidebar, main content, dan footer disusun dalam satu grid.
* **Galeri Foto**
  Gambar dengan ukuran berbeda menyesuaikan area grid yang tersedia.
* **Dashboard Widget**
  Widget statistik dan grafik ditata dengan ukuran yang bervariasi.

### Slide 15 (16)
BAB 6 · PERBANDINGAN
## Flexbox vs CSS Grid

| Fitur | Flexbox | CSS Grid |
| :--- | :--- | :--- |
| **Dimensi** | 1 Dimensi (baris atau kolom) | 2 Dimensi (baris dan kolom) |
| **Fokus** | Konten (content-first) | Tata letak (layout-first) |
| **Penggunaan** | Komponen skala kecil: navbar, button, form | Struktur tata letak besar: seluruh halaman |
| **Contoh** | Menu navigasi, daftar card | Header-sidebar-main-footer, galeri |

**Aturan praktis**: gunakan Flexbox untuk komponen, Grid untuk kerangka halaman. Keduanya bisa dikombinasikan dalam satu proyek.

### Slide 16 (17)
TUGAS
## Instruksi Tugas 1

https://bit.ly/Tugas1_FEbasic_Irsyaad

### Slide 17
## Terima kasih!
Sampai jumpa di pertemuan berikutnya. Silakan ajukan pertanyaan jika ada yang belum jelas.

* **FLEXBOX**
  Layout satu dimensi: atur baris atau kolom.
* **CSS GRID**
  Layout dua dimensi: atur baris dan kolom sekaligus.
