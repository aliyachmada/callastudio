README CALLA PORTFOLIO!

# 🌷 Panduan Edit Konten Website Calla Creative Studio
**(Tanpa Perlu Ngoding HTML / CSS)**

Semua teks, daftar proyek portofolio, foto, dan harga paket di website Calla sudah dipusatkan di dalam **satu file saja**, yaitu:
👉 **`content/site-content.js`**

Sebelum mengedit, **selalu gandakan (copy-paste) file `site-content.js` sebagai backup** supaya kalau ada salah ketik tanda koma atau tanda petik, kamu tinggal mengembalikan file cadangannya.

---

## 1. Cara Menyembunyikan atau Menampilkan Proyek Portofolio
Buka `content/site-content.js`, lalu cari bagian `portfolioProjects: [`.
Di setiap proyek (misalnya `holly`, `maroo`, `minoe`, `kueboon`), ada baris pengaturan berikut:

```js
id: 'babytara',
publish: true,   // Ubah jadi false kalau mau disembunyikan dari website
featured: false, // Ubah jadi true kalau mau tampil di halaman awal (Karya Unggulan)


---------------------------------------------------------------------------------------------------

UBAH PORTOFLIO / TAMBAH GAMBAR

Masukkan file gambarmu ke dalam folder assets/ (disarankan format .webp atau .jpg agar ringan dibuka di HP).

Di dalam content/site-content.js, sesuaikan nama file pada baris coverImg (gambar sampul depan) dan detailImg (gambar kedua di dalam studi kasus):


coverImg: 'assets/holly-jolly-cover.webp',
detailImg: 'assets/holly-jolly-detail.webp',

---------------------------------------------------------------------------------------------------

Cara Mengubah Kategori Filter Proyek

Pada setiap proyek di content/site-content.js, baris category hanya boleh diisi dengan salah satu dari 3 kode huruf kecil berikut:

'identity' → Masuk ke tab Brand Identity

'mascot' → Masuk ke tab Mascot & Illustration

'packaging' → Masuk ke tab Packaging & F&B

---------------------------------------------------------------------------------------------------

Cara Mengubah Harga Paket (IDR & USD)
Scroll ke bagian paling bawah di file content/site-content.js sampai menemukan bagian pricingCatalog.

Bagian ID: adalah daftar harga untuk pasar Indonesia (IDR).

Bagian EN: adalah daftar harga untuk pasar International & ASEAN (USD).

Untuk mengubah harga, cukup ganti teks di bagian price, misalnya:


name: 'Single Hero Packaging',
price: 'Starting at Rp550.000',

----------------------------------------------------------------------------------------------------

TAMBAH CARD PORTOLIO

{
      id: 'seeri',
      publish: true,
      featured: false,
      name: 'Seeri (Malaysia)',
      category: 'packaging',
      statusBadge: 'GALLERY · D2C UNBOXING',
      frameBg: 'bg-[#F3E8FF]',
      coverImg: 'assets/seeri-cover.webp',
      detailImg: 'assets/seeri-detail.webp',
      altText: {
        ID: 'Desain kemasan polymailer lilac-pink untuk brand fashion Seeri Malaysia',
        EN: 'Seeri Malaysia lilac-pink D2C fashion polymailer packaging design'
      },
      pdfExportHint: 'Opsional: tambahkan seeri-cover (.webp/.jpg) ke folder assets/ jika ingin menampilkan foto.',
      ID: {
        categoryLabel: 'Fashion Identity & Polymailer Packaging',
        summary: 'Identitas visual dan desain kemasan polymailer e-commerce berwarna lilac-pink dengan pola geometris lembut dan pesan sapaan "You’re something special" untuk brand Malaysia.',
        deliverables: ['Primary Logotype & Monogram S', 'Desain Kemasan Polymailer Custom', 'Pola Grafis Pendukung Brand', 'Mockup Studio di Atas Kain Satin'],
        steps: [
          ['01 — TANTANGAN & TUJUAN KLIEN', 'Brand fashion asal Malaysia ini membutuhkan identitas logo sekaligus kemasan pengiriman online shop (polymailer) yang langsung mencuri perhatian saat paket tiba di rumah pembeli.'],
          ['02 — ARAH KONSEP & VISUAL', 'Memadukan warna lilac, kuning segar, dan magenta cerah dengan tipografi serif berlekuk khas serta pesan manis di bagian lipatan amplop.'],
          ['03 — SKETSA LOGO & POLA KEMASAN (GATE 1)', 'Merancang logotype SEERI dengan huruf S ikonis yang bisa berdiri sendiri sebagai monogram, ditemani komposisi depan-belakang kantong polymailer.'],
          ['04 — WARNA & ELEMEN PENDUKUNG (GATE 2)', 'Menerapkan pola lingkaran berulang di sisi belakang polymailer dan sapaan tulisan tangan "You’re something special" di sisi depan.'],
          ['05 — APLIKASI NYATA PADA PRODUK', 'Divisualisasikan pada mockup polymailer bertekstur doff di atas kain satin, lengkap dengan perluasan ke paper bag, hangtag, dan kertas tisu.'],
          ['06 — PAKET RELEVAN & FILE HANDOVER', 'Contoh nyata paket Single Hero Packaging (Rp550.000 / USD 55) atau Signature Branding Package (Rp550.000 / USD 75).']
        ]
      },
      EN: {
        categoryLabel: 'Fashion Identity & Polymailer Packaging',
        summary: 'Visual identity and custom lilac-pink D2C polymailer packaging featuring soft geometric patterns and "You’re something special" messaging for a Malaysian fashion brand.',
        deliverables: ['Primary Logotype & S Monogram', 'Custom D2C Polymailer Bag Design', 'Bespoke Supporting Brand Pattern', '3D Satin Fabric Staging Mockup'],
        steps: [
          ['01 — CLIENT GOAL & CHALLENGE', 'Designing an e-commerce mailer bag and identity for a Malaysian label that turns parcel delivery into a camera-ready unboxing moment.'],
          ['02 — CREATIVE DIRECTION', 'Vibrant lilac and berry-purple hues paired with a distinctive custom serif logotype and warm handwritten micro-copy.'],
          ['03 — LOGO & MAILER LAYOUT (GATE 1)', 'Developing the primary SEERI logotype, flowing S monogram, and front/back polymailer print layout.'],
          ['04 — PATTERN & COLOR APPLICATION (GATE 2)', 'Applying polka-ring repeat patterns on the reverse side and "You’re something special" typography on the front flap.'],
          ['05 — BRAND IN ACTION', 'Presented on matte-satin polymailer bags staged over draped silk fabric, alongside hangtags and tissue wrap.'],
          ['06 — PACKAGE & MASTER HANDOVER', 'Ideal showcase for Single Hero Packaging (USD 55) or Signature Branding Package (USD 75).']
        ]
      }
    },