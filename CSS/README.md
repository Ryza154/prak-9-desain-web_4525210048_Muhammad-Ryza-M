# Muhammad Ryza Mahameru - [ 4525210048 ]
# Selaras Coffee - One Page Website UMKM

Tugas pembuatan website profil UMKM satu halaman (*One Page Website*) menggunakan Bootstrap 5 dan CSS kustom dengan identitas warna kopi (espresso, krem, sage, dan karamel).

---

## Ringkasan Pengerjaan

Website UMKM *Selaras Coffee* dibuat sebagai *One Page Website* menggunakan Bootstrap 5. Halaman disusun satu kolom dari atas ke bawah: navbar, hero, alert promo, tiga card produk, form kontak, dan footer, ditambah dua modal. Agar tidak terlihat seperti template bawaan, ditambahkan custom CSS berisi variabel warna espresso, krem, sage, dan karamel, serta font Playfair Display untuk judul. Gambar hero dan kemasan produk dibuat sebagai file SVG lokal.

Masalah pertama, navbar yang *fixed* menutupi bagian atas hero dan judul section saat menu diklik. Solusinya adalah menambah padding atas pada hero dan `scroll-padding-top` pada `html`. Masalah kedua, tiga tombol Detail awalnya membutuhkan tiga modal terpisah sehingga kodenya panjang dan berulang. Kami menggantinya dengan satu modal yang isinya diisi JavaScript dari atribut `data-*` tombol melalui event `show.bs.modal`. Masalah ketiga, form bisa terkirim walau kosong. Kami memakai `novalidate`, `checkValidity()`, dan class `was-validated` agar pesan kesalahan Bootstrap muncul, lalu menampilkan alert sukses setelah data valid. Masalah keempat, gambar dari internet berisiko tidak muncul saat presentasi tanpa koneksi, sehingga dipakai gambar lokal.

Hasilnya, layout tampil rapi di desktop maupun mobile dan semua komponen wajib terpenuhi.

---

## Checklist Kelengkapan Komponen

| No | Komponen Wajib | Implementasi pada Kode | Keterangan |
| :--- | :--- | :--- | :--- |
| 1 | Navbar Responsif | `<nav class="navbar navbar-expand-lg fixed-top ...">` | Collapse ke hamburger menu di mobile |
| 2 | Hero Section | `<header id="beranda" class="hero">` | Gambar, headline utama, dan tombol *call-to-action* |
| 3 | Minimal 3 Card | 3 kartu produk (`.card.product-card`) | Gayo Selaras, Kintamani Fresh, Robusta Malam beserta harga |
| 4 | Minimal 1 Alert | Alert promo (`.alert-promo.alert-dismissible`) dan alert sukses form | Notifikasi diskon yang bisa ditutup |
| 5 | Minimal 1 Modal | `#modalProduk` dan `#modalPromo` | Detail produk (isi dinamis) dan syarat promo |
| 6 | Form Kontak | `<form id="formKontak">` | Input nama, email, pesan, dengan validasi |
| 7 | Footer | `<footer class="footer">` | Alamat, kontak, dan ikon media sosial |
| 8 | Custom CSS | `style.css` | Variabel warna brand, font, tombol, hover card |

---

## Screenshot Output

### 1. Tampilan Desktop
![Screenshot desktop](screenshots/desktop.png)

### 2. Tampilan Mobile
![Screenshot mobile](screenshots/mobile.png)

## Pembagian Peran

| Nama | Peran |
| [Nama Kamu] | [contoh: struktur HTML, komponen Bootstrap, dan JavaScript] |
| Muhammad Ryza Mahameru | [contoh: custom CSS, gambar, dan pengujian tampilan mobile] |

---

## Teknologi yang Digunakan

*   **HTML5:** Struktur semantik website.
*   **Bootstrap 5.3.3:** Grid system, layout responsif, dan komponen UI (navbar, card, alert, modal, form).
*   **Bootstrap Icons:** Ikon pada navbar, alert, form, dan footer.
*   **Custom CSS3:** Palet warna, tipografi (Playfair Display dan DM Sans), dan efek transisi.
*   **JavaScript:** Isi modal dinamis dan validasi form kontak.
