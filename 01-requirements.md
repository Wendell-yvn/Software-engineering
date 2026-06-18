# 📋 Product Discovery: Sesi Klarifikasi Kebutuhan menggunakan metode Grill-me oleh Claude.ai

**Proyek:** SolKu — Aplikasi Marketplace Jasa Sol Sepatu
**Format:** Product Grilling (Wawancara Teknis Produk)
**Tanggal:** Juni 2026

---

## Daftar Isi

- [Ringkasan Sesi](#ringkasan-sesi)
- [Transkrip Tanya Jawab](#transkrip-tanya-jawab)
- [Keputusan Desain Produk](#keputusan-desain-produk)
- [Risiko yang Diidentifikasi](#risiko-yang-diidentifikasi)

---

## Ringkasan Sesi

| Item | Keterangan |
|---|---|
| **Tujuan** | Menggali dan memvalidasi ide produk hingga cukup jelas untuk ditulis sebagai dokumen requirements |
| **Format** | Wawancara teknis satu pertanyaan per giliran |
| **Jumlah Pertanyaan** | 10 pertanyaan |
| **Topik yang Dicakup** | Validasi pasar, cold start problem, value proposition, prioritas fitur MVP, alur transaksi, model logistik, geolocation, mekanisme dispute |
| **Output** | Scope produk terdefinisi → SRS MVP |

### Scope Produk yang Disepakati

> Platform marketplace jasa sol sepatu yang menghubungkan pembeli dengan penyedia jasa melalui sistem booking berbasis slot waktu dan geolocation, dengan tracking status pekerjaan real-time, untuk dua model layanan: penyedia jasa tetap dan mobile.

---

## Transkrip Tanya Jawab

### ❓ Pertanyaan 1 — Validasi Pasar

> Dari notulen ini, kamu mewawancarai 2 penyedia jasa dan 3 pembeli — sampel yang sangat kecil. Apa justifikasimu bahwa masalah yang ditemukan ini cukup signifikan untuk dibuatkan aplikasi? Ada data pendukung lain selain wawancara ini?

**Jawaban:**
Di Manado terdapat banyak penyedia jasa sol sepatu keliling selain 2 sampel yang diwawancara, dan banyak orang di sekitar yang mencari jasa tersebut. Masalah utama: pengguna kesulitan menemukan penyedia jasa yang terpercaya, dan penyedia jasa kesulitan mendapatkan pelanggan secara konsisten.

**Verdict:** ⚠️ DITERIMA DENGAN CATATAN

> **Catatan:** Validasi pasar masih lemah dan anekdotal. Tidak ada data kuantitatif yang mendukung skala pasar. Ini dicatat sebagai **Risiko #1**.

---

### ❓ Pertanyaan 2 — Prioritas Sisi Pengguna

> Aplikasi ini untuk siapa yang diprioritaskan? (A) Pembeli dulu, (B) Penyedia jasa dulu, atau (C) Dua-duanya sekarang?

**Jawaban Awal:** C — karena aplikasi ditujukan untuk mempertemukan keduanya.

**Verdict:** ❌ DITANTANG

> **Catatan:** Jawaban C tanpa strategi dianggap naif. Pewawancara mengidentifikasi **chicken-and-egg problem** — tanpa penyedia jasa, pembeli tidak mau download; tanpa pembeli, penyedia jasa tidak mau daftar.

---

### ❓ Pertanyaan 3 — Strategi Akuisisi Hari Pertama

> Pada hari pertama aplikasi launch — siapa yang diakuisisi duluan, dan bagaimana caranya?

**Jawaban:**
Fokus mengakuisisi **penyedia jasa terlebih dahulu**. Alasan: pengguna tidak akan tertarik jika belum ada penyedia jasa di platform. Sebaliknya, penyedia jasa lebih mungkin tertarik karena melihat peluang mendapatkan pelanggan tambahan.

**Verdict:** ✅ DITERIMA

> **Catatan:** Jawaban menunjukkan pemahaman dasar tentang supply-side acquisition pada two-sided marketplace.

---

### ❓ Pertanyaan 4 — Value Proposition ke Penyedia Jasa

> Opa Ferry sudah punya 20–30 pelanggan per hari tanpa aplikasi. Uncle sudah pakai WhatsApp. Kenapa mereka mau pindah ke atau menambah platform ini? Apa value proposition konkret yang tidak bisa mereka dapatkan dari WhatsApp?

**Jawaban:**
Tujuan aplikasi bukan menggantikan WhatsApp, tapi menambah nilai yang belum ada. Masalah utama bukan jumlah pelanggan saat ramai, tapi **ketidakstabilan**:
- Uncle mengeluhkan pelanggan tidak konsisten
- Opa Ferry sangat bergantung pada hari pasar (hanya 2x seminggu) dan tidak semua orang mau ke pasar

Value proposition: **akses ke pelanggan yang lebih luas dan lebih konsisten, tidak terbatas waktu dan lokasi.**

**Verdict:** ✅ DITERIMA

---

### ❓ Pertanyaan 5 — Prioritas Fitur MVP

> Dari 7 fitur di notulen, pilih maksimal 3 untuk MVP dan jelaskan mengapa.

**Jawaban Awal:** Sistem booking, tracking status, dan portfolio hasil pekerjaan.

**Verdict:** ❌ DITANTANG

> **Catatan:** Pewawancara mempertanyakan mengapa estimasi harga dan rating & review — yang disebut oleh semua 3 pembeli — tidak masuk MVP.

---

### ❓ Pertanyaan 6 — Justifikasi Penundaan Estimasi Harga & Review

> Semua 3 pembeli menyebut estimasi harga dan rating & review. Buktikan bahwa pengguna mau booking tanpa tahu harga dan tanpa bisa lihat review.

**Jawaban:**
Pemisahan antara dua jenis faktor:
- **Faktor yang membuat orang booking pertama kali** → ditangani oleh alur operasional
- **Faktor yang membangun kepercayaan jangka panjang** → ditangani di versi berikutnya

**Estimasi harga ditunda** karena harga bersifat variatif tergantung kondisi fisik sepatu — harga final lebih realistis setelah penilaian langsung oleh penyedia jasa.

**Rating & review ditunda** karena di awal belum ada cukup transaksi untuk menghasilkan data yang kredibel.

**Verdict:** ✅ DITERIMA

---

### ❓ Pertanyaan 7 — Alur Transaksi End-to-End

> Gambarkan alur transaksi end-to-end secara spesifik, langkah demi langkah.

**Jawaban:**

```
Pembeli buka aplikasi
  → Lihat daftar penyedia jasa
  → Buka halaman detail
  → Pilih layanan + slot waktu
  → Submit form booking
  → Order masuk ke dashboard penyedia jasa
  → Penyedia jasa konfirmasi
  → Penyedia jasa mulai kerjakan
  → Update status bertahap (Dikonfirmasi → Sedang Dikerjakan → Selesai)
  → Pembeli terima notifikasi real-time
  → Penyedia jasa tandai Selesai
  → Order ditutup dan disimpan sebagai riwayat
```

**Verdict:** ✅ DITERIMA

> **Catatan:** Alur cukup jelas, namun ditemukan celah — tidak ada penjelasan mekanisme pengiriman fisik barang. Dilanjutkan ke pertanyaan 8.

---

### ❓ Pertanyaan 8 — Model Logistik

> Bagaimana sepatu berpindah dari pembeli ke penyedia jasa? (A) Pembeli datang ke penyedia, (B) Penyedia datang ke pembeli, (C) Pihak ketiga, atau (D) Kombinasi?

**Jawaban:** Model **D — Kombinasi**, dibatasi per tipe penyedia jasa:

| Tipe Penyedia Jasa | Model Logistik |
|---|---|
| Penyedia Tetap (contoh: Opa Ferry di pasar) | Pembeli datang ke lokasi setelah booking |
| Penyedia Mobile (contoh: Uncle keliling) | Penyedia datang ke lokasi pembeli |

Model C (pihak ketiga) tidak dimasukkan MVP — terlalu kompleks dan di luar scope. Aplikasi hanya berfungsi sebagai **sistem koordinasi**, bukan penyedia logistik.

**Verdict:** ✅ DITERIMA

---

### ❓ Pertanyaan 9 — Validasi Geolocation

> Bagaimana sistem menentukan apakah penyedia jasa mobile bisa melayani lokasi pembeli tertentu?

**Jawaban:**
- Penyedia jasa mobile mendefinisikan **radius layanan dalam kilometer** dari titik operasional utamanya
- Validasi dilakukan **otomatis oleh sistem** (bukan manual) menggunakan geolocation
- Jika lokasi pembeli **dalam radius** → booking dapat dilanjutkan
- Jika lokasi pembeli **di luar radius** → sistem menolak dan menyarankan penyedia jasa lain

**Verdict:** ✅ DITERIMA

> **Catatan:** Keputusan teknis realistis dan dapat diimplementasikan. Menghilangkan kebutuhan negosiasi manual antara dua pihak.

---

### ❓ Pertanyaan 10 — Mekanisme Dispute

> Skenario: pembeli menolak bayar, atau penyedia jasa tidak menyelesaikan pekerjaan. Bagaimana sistem menangani dispute? Apa risikonya jika ditunda?

**Jawaban:**
MVP **tidak membangun sistem dispute atau escrow**. Pembayaran terjadi sepenuhnya di luar aplikasi (offline). Aplikasi tidak memegang uang.

Resolusi konflik bergantung pada kepercayaan antarpihak — mengikuti realita yang sudah berjalan di pasar tradisional.

**Risiko yang diakui:** tidak ada kontrol penuh terhadap konflik transaksi.

**Trade-off yang disepakati:** ini wajar untuk MVP karena fokus utama adalah memastikan alur booking dan tracking operasional berjalan dulu sebelum masuk ke financial trust layer.

**Verdict:** ⚠️ DITERIMA DENGAN CATATAN

> **Catatan:** Dicatat sebagai **Risiko #3**. Mitigasi: percepat implementasi rating di v1.1 dan tambahkan disclaimer di aplikasi.

---

## Keputusan Desain Produk

| # | Keputusan | Rasionalisasi |
|---|---|---|
| 1 | Supply-side acquisition first | Onboard penyedia jasa sebelum soft launch untuk menghindari chicken-and-egg problem |
| 2 | Value proposition: stabilitas & jangkauan pelanggan | Bukan menggantikan WhatsApp, tapi menambah kanal akuisisi yang lebih luas dan konsisten |
| 3 | MVP: booking + tracking + portfolio | Fokus pada alur operasional end-to-end sebelum lapisan kepercayaan (rating, escrow) |
| 4 | Estimasi harga & rating ditunda ke v1.1 | Harga variatif tergantung kondisi barang; rating tidak kredibel tanpa data transaksi awal |
| 5 | Model logistik kombinasi (A+B), tanpa pihak ketiga | Mengikuti realita operasional existing; aplikasi hanya koordinasi, bukan logistik |
| 6 | Validasi area layanan mobile via radius geolocation | Sistem yang memvalidasi, bukan manusia — menghilangkan negosiasi manual |
| 7 | Pembayaran offline, tanpa escrow di MVP | Menghindari kompleksitas payment gateway dan dispute di versi pertama |

---

## Risiko yang Diidentifikasi

| # | Risiko | Tingkat | Mitigasi |
|---|---|---|---|
| 1 | Validasi pasar masih anekdotal — hanya 5 responden, tidak ada data kuantitatif | 🔴 Tinggi | Lakukan survei ke minimal 50 calon pengguna sebelum pengembangan penuh |
| 2 | Cold start problem — tidak ada penyedia jasa saat launch | 🔴 Tinggi | Akuisisi manual minimal 10 penyedia jasa aktif di Manado sebelum soft launch |
| 3 | Tidak ada perlindungan transaksi di MVP | 🟡 Sedang | Tambahkan disclaimer; percepat implementasi rating & review di v1.1 |
| 4 | Penyedia jasa enggan onboarding karena keterbatasan literasi teknologi | 🟡 Sedang | Panduan onboarding berbasis video; pertimbangkan pendampingan langsung di awal |
| 5 | Akurasi geolocation rendah di area tertentu (pasar tradisional) | 🟢 Rendah | Izinkan penyedia jasa mengoreksi titik lokasi secara manual |

---

*Dokumen ini merupakan output dari sesi product discovery grilling dan menjadi dasar penulisan [SRS MVP SolKu](./SRS_SolKu_MVP_v1.0.docx).*




# NOTULEN HASIL WAWANCARA

## Pengembangan Aplikasi Jasa Sol Sepatu

---

# A. DATA RESPONDEN

## Penyedia Jasa

1. Uncle (Penyedia Jasa Mobile/Keliling)
2. Opa Ferry (Penyedia Jasa Tradisional/Pasar)

## Pembeli

1. Pembeli 1
2. Pembeli 2
3. Pembeli 3

---

# B. HASIL WAWANCARA PENYEDIA JASA

## 1. Penyedia Jasa 1 – Uncle

### Profil Usaha

* Lama usaha: ±1 tahun
* Layanan:

  * Sol sepatu
  * Jahit sepatu
  * Lem sepatu
  * Perbaikan sepatu
  * Jahit dan perbaikan baju

### Operasional

* Pelanggan per hari: 7–10 orang
* Sistem kerja:

  * Door-to-door
  * Pemesanan melalui WhatsApp

### Penentuan Harga

* Berdasarkan tingkat kesulitan dan bahan yang digunakan
* Kisaran harga:

  * Jahit ringan: Rp25.000
  * Kerusakan berat: Rp35.000–Rp40.000

### Waktu Pengerjaan

* ±20–25 menit per sepatu

### Kendala

* Sulit mendapatkan pelanggan
* Cuaca buruk
* Persaingan dengan tukang lain
* Komunikasi dengan pelanggan
* Negosiasi harga

### Penggunaan Teknologi

* Smartphone
* WhatsApp

### Kebutuhan Fitur Aplikasi

* Promosi usaha
* Estimasi harga
* Upload foto sepatu
* Tracking pekerjaan
* Rating dan review

### Harapan

* Usaha lebih stabil
* Tidak perlu terus berkeliling
* Pendapatan lebih konsisten

---

## 2. Penyedia Jasa 2 – Opa Ferry

### Profil Usaha

* Lama usaha: sejak sekitar tahun 1973
* Layanan:

  * Perbaikan semua jenis sepatu
  * Tas
  * Payung
  * Perbaikan barang lainnya

### Operasional

* Pelanggan:

  * Bisa 20–30 orang per hari saat ramai
  * Ramai terutama saat hari pasar
* Pelanggan datang langsung atau melalui rekomendasi

### Penentuan Harga

* Berdasarkan tingkat kerusakan
* Berdasarkan jenis sepatu
* Kisaran pekerjaan berat:

  * Rp35.000–Rp40.000

### Waktu Pengerjaan

* ±15 menit

### Kendala

* Kadang sulit mendapatkan pelanggan
* Bergantung pada kondisi pasar

### Penggunaan Teknologi

* Smartphone Android
* WhatsApp
* Facebook
* Grup jual beli

### Kebutuhan Fitur Aplikasi

* Estimasi harga
* Upload foto sepatu
* Rating dan review

### Harapan

* Mendapatkan lebih banyak pelanggan
* Usaha semakin berkembang

---

# C. HASIL WAWANCARA PEMBELI

## 1. Pembeli 1

### Pengalaman

* Pernah menggunakan jasa sol sepatu
* Frekuensi: sekitar 1 bulan sekali
* Jenis sepatu: sneakers

### Cara Mencari Jasa

* Mencari langsung di pasar

### Pertimbangan Memilih Jasa

* Kualitas hasil perbaikan

### Kendala

* Sulit menemukan jasa berkualitas
* Pernah kecewa dengan hasil
* Harga terkadang berubah dari kesepakatan awal

### Fitur yang Diinginkan

* Daftar jasa terdekat
* Rating dan review
* Upload foto sepatu
* Estimasi harga
* Chat dengan penyedia jasa
* Pembayaran online

### Harapan

* Kualitas hasil yang baik
* Pelayanan yang memudahkan pengguna

---

## 2. Pembeli 2

### Pengalaman

* Pernah menggunakan jasa sol sepatu sekitar 2 kali
* Jenis sepatu:

  * Formal
  * Sneakers

### Cara Mencari Jasa

* Mencari di sekitar lokasi yang dikenal

### Pertimbangan Memilih Jasa

* Kualitas
* Harga

### Kendala

* Sulit menemukan tukang sol
* Pernah mendapatkan jahitan kurang rapi
* Sulit mengetahui harga sebelum datang

### Fitur yang Diinginkan

* Estimasi harga
* Rating dan review
* Upload foto sepatu
* Layanan antar-jemput

### Harapan

* Harga terjangkau
* Kualitas baik

---

## 3. Pembeli 3

### Pengalaman

* Menggunakan jasa sekitar 6 bulan sekali
* Jenis sepatu: sneakers

### Cara Mencari Jasa

* Mengandalkan tukang keliling

### Pertimbangan Memilih Jasa

* Kemudahan
* Harga terjangkau

### Kendala

* Sulit menemukan jasa berkualitas tinggi
* Kurang yakin terhadap kualitas tukang
* Harga sulit diperkirakan sebelumnya

### Fitur yang Diinginkan

* Daftar jasa terdekat
* Rating dan review
* Estimasi harga
* Portfolio hasil kerja
* Antar-jemput

### Harapan

* Kualitas terjaga
* Ada bukti hasil pekerjaan sebelumnya

---

# D. TEMUAN UTAMA (KEY INSIGHTS)

## Dari Penyedia Jasa

* Penyedia jasa masih mengandalkan metode tradisional.
* Kesulitan utama adalah mendapatkan pelanggan secara konsisten.
* Teknologi seperti WhatsApp sudah membantu operasional.
* Penyedia jasa tertarik menggunakan aplikasi jika mudah digunakan.

## Dari Pembeli

* Faktor paling penting adalah kualitas hasil pekerjaan.
* Pengguna kesulitan menemukan jasa yang terpercaya.
* Transparansi harga menjadi kebutuhan utama.
* Rating dan review sangat penting untuk membangun kepercayaan.
* Pengguna tertarik pada fitur upload foto untuk estimasi awal.

---

# E. KESIMPULAN

Berdasarkan hasil wawancara terhadap dua penyedia jasa dan tiga pembeli, ditemukan bahwa terdapat kebutuhan akan platform digital yang mampu menghubungkan penyedia jasa dan pelanggan secara lebih efektif. Masalah utama yang ditemukan adalah kesulitan memperoleh pelanggan secara konsisten dari sisi penyedia jasa serta kurangnya transparansi harga dan informasi kualitas jasa dari sisi pelanggan.

Fitur yang paling dibutuhkan dalam aplikasi meliputi:

1. Estimasi harga.
2. Upload foto sepatu.
3. Rating dan review.
4. Portfolio hasil pekerjaan.
5. Sistem booking.
6. Tracking status pekerjaan.
7. Layanan antar-jemput atau panggil tukang.

Solusi yang dirancang diharapkan mampu meningkatkan kepercayaan pelanggan sekaligus memperluas jangkauan pasar bagi penyedia jasa sol sepatu.
