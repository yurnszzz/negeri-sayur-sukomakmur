# Panduan pengerjaan proyek

Website mini project individu Hasan Shofiyyur Rahman untuk Study Club Frontend Basic KSM Veterantech UPNVJ 2026. Baca `instruksi_mini_project_frontend.md`, `Prompt_Codex_Web_Negeri_Sayur_Sukomakmur.md`, dan `scfe_basic_p1_p4.md` sebelum mengubah arah proyek.

## Preferensi pengguna yang sudah disepakati

- Pertahankan HTML5 dan satu CSS native. Website harus dapat dibuka langsung tanpa JavaScript, framework, build, atau backend. Node boleh dipakai untuk alat pengembangan.
- Pertahankan konsep jurnal perjalanan, warna kertas hangat dan hijau, Georgia/Arial, bingkai foto, serta skeuomorphism ringan. Pengguna sudah menyukai arah visual ini.
- Evaluasi lanjutan meminta layout lebih khas dan tidak terasa seperti template AI. Pertahankan judul yang proporsional (maksimal 64 px desktop), foto hero utuh tanpa crop dengan catatan sejajar tengah, foto cerita berukuran berbeda, dan tabel lapang. Hindari label bagian bernomor, eyebrow dekoratif, dan pola dua kolom yang sama pada setiap bagian.
- Preferensi terbaru: tiga rekomendasi memakai bingkai foto besar berjajar di desktop/tablet, lalu satu kolom di ponsel. Jangan mengembalikannya ke baris thumbnail kecil. Footer tidak memerlukan tautan kembali ke atas; logo header tetap menuju awal halaman.
- Gunakan dua logo SVG asli pengguna tanpa perubahan atau pemotongan.
- Judul tab: `Negeri Sayur Sukomakmur`. Jangan tambahkan panah dekoratif pada tautan atau tombol.
- Navbar menempel di atas, lalu mengambang saat scroll bila CSS browser mendukung. Fallback harus tetap sticky. Hormati reduced motion dan jangan menutupi tujuan anchor.
- Layout tetap responsif di desktop dan ponsel; navigasi selalu dapat digunakan tanpa JavaScript. Header desktop ringkas dengan tautan langsung. Pada lebar maksimal 650 px gunakan logo dan disclosure Menu/Tutup native, bukan memampatkan navbar desktop. Panel terbuka berada di alur dokumen; periksa jarak anchor saat panel terbuka.
- Izin terbaru pengguna menggantikan ketentuan foto lama dalam brief: boleh mencari dan memasang keenam foto. Gunakan sumber berlisensi yang sesuai, cocokkan lokasi, dan tulis atribusi di halaman serta `docs/ASSETS.md`. Foto kawasan sekitar tidak boleh disebut sebagai foto lokasi persis tanpa bukti.

## Skill untuk pekerjaan frontend berikutnya

Baca dan gunakan bagian yang relevan dari empat skill lokal ini ketika mengerjakan desain atau frontend proyek:

- [Taste Skill](.agents/skills/design-taste-frontend/SKILL.md): komposisi, tipografi, foto, dan pemeriksaan visual.
- [UI UX Pro Max](.agents/skills/ui-ux-pro-max/SKILL.md): responsivitas, keterbacaan, navigasi, form, dan aksesibilitas.
- [Impeccable](.agents/skills/impeccable/SKILL.md): evaluasi serta penyempurnaan antarmuka sesuai lingkup permintaan.
- [Emil Design Engineering](.agents/skills/emil-design-eng/SKILL.md): alasan penggunaan animasi, feedback interaksi, dan detail gerak.

Instruksi pengguna, ketentuan tugas, dan batas stack didahulukan. Jangan menambahkan framework, animasi wajib, atau mengganti tema hanya demi memenuhi aturan estetika skill. Jangan memasang ulang skill yang sudah tersedia tanpa kebutuhan.

## Sumber, ekspor, dan pemeriksaan

- Edit `index.html` dan `assets/css/style.css` sebagai sumber utama. `submission/` adalah salinan mekanis, bukan versi yang diedit terpisah.
- Perbarui README, catatan belajar, kredit aset, dan screenshot bila perubahan membuatnya tidak sesuai lagi.
- Periksa gambar lokal, tautan internal, form HTML, keyboard, overflow, scroll navbar, dan reduced motion pada lebar 1440, 768, 390, dan 320 px dengan JavaScript dinonaktifkan.
- Laporkan pemeriksaan yang benar-benar dijalankan dan batasnya. Jangan mengklaim sudah menguji browser yang tidak tersedia.
- Lisensi MIT kode tidak menggantikan hak logo, lisensi foto, atau lisensi skill pihak ketiga.
