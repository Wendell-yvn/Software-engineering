# 📄 Product Requirements Document (PRD)

**Proyek:** SolKu — Aplikasi Marketplace Jasa Sol Sepatu
**Versi:** 1.0 (MVP)
**Status:** 🟡 Draft
**Terakhir Diperbarui:** Juni 2026

---

## Daftar Isi

- [Overview](#overview)
- [Latar Belakang & Problem Statement](#latar-belakang--problem-statement)
- [Tujuan Produk](#tujuan-produk)
- [Target Pengguna](#target-pengguna)
- [Scope MVP](#scope-mvp)
- [User Stories](#user-stories)
- [Alur Pengguna](#alur-pengguna)
- [Fitur Detail](#fitur-detail)
- [Fitur di Luar Scope MVP](#fitur-di-luar-scope-mvp)
- [Metrik Keberhasilan](#metrik-keberhasilan)
- [Asumsi & Keterbatasan](#asumsi--keterbatasan)
- [Risiko](#risiko)
- [Referensi](#referensi)

---

## Overview

SolKu adalah platform marketplace mobile dua sisi (**two-sided marketplace**) yang menghubungkan pembeli dengan penyedia jasa sol sepatu. Aplikasi berperan sebagai sistem koordinasi dan manajemen order — bukan perantara finansial atau penyedia logistik.

> **One-liner:** *Temukan dan pesan tukang sol sepatu terpercaya di sekitarmu, kapan saja.*

---

## Latar Belakang & Problem Statement

### Konteks

Jasa sol sepatu adalah kebutuhan yang ada di hampir setiap kota, termasuk Manado. Penyedia jasa beroperasi dalam dua model: **tetap** (kios di pasar) dan **mobile** (keliling). Namun selama ini, pertemuan antara pembeli dan penyedia jasa masih bergantung pada cara-cara konvensional.

### Masalah dari Sisi Penyedia Jasa

| Masalah | Dampak |
|---|---|
| Pelanggan tidak datang secara konsisten | Pendapatan tidak stabil dan tidak bisa diprediksi |
| Bergantung pada hari pasar atau rute keliling | Jangkauan pasar terbatas secara geografis dan waktu |
| Promosi hanya dari mulut ke mulut | Sulit menjangkau pelanggan baru |
| Komunikasi dan negosiasi harga dilakukan manual | Tidak efisien, rawan miskomunikasi |

### Masalah dari Sisi Pembeli

| Masalah | Dampak |
|---|---|
| Sulit menemukan penyedia jasa yang terpercaya | Sering kecewa dengan kualitas hasil |
| Tidak tahu harga sebelum datang | Pernah mendapat harga berbeda dari kesepakatan awal |
| Tidak ada referensi kualitas yang objektif | Pilihan hanya berdasarkan kebetulan atau rekomendasi informal |
| Harus menunggu tukang keliling atau pergi ke pasar | Tidak praktis dan bergantung pada jadwal penyedia jasa |

### Insight Kunci

- Semua pembeli yang diwawancara menyebut **kualitas** dan **transparansi harga** sebagai faktor utama
- Semua penyedia jasa menyebut **kesulitan mendapat pelanggan secara konsisten** sebagai masalah utama
- Teknologi dasar (smartphone, WhatsApp) sudah digunakan oleh kedua pihak

---

## Tujuan Produk

### Tujuan Bisnis

1. Menjadi platform koordinasi jasa sol sepatu pertama di Manado
2. Onboard minimal **10 penyedia jasa aktif** sebelum soft launch
3. Mencapai **100 transaksi pertama** dalam 3 bulan pertama setelah launch

### Tujuan Pengguna

| Pengguna | Tujuan |
|---|---|
| Pembeli | Menemukan penyedia jasa terpercaya dengan mudah, mengetahui status pekerjaan tanpa harus bertanya manual |
| Penyedia Jasa | Mendapatkan pelanggan baru yang lebih konsisten tanpa harus terus berkeliling atau menunggu di pasar |

---

## Target Pengguna

### Pembeli

- **Demografi:** Pria/wanita, 18–45 tahun, pengguna smartphone aktif
- **Perilaku:** Memiliki sepatu yang perlu diperbaiki 1–6 bulan sekali
- **Pain point utama:** Kesulitan menemukan penyedia jasa berkualitas yang bisa dipercaya
- **Jenis sepatu:** Sneakers, formal, dan sepatu kasual

### Penyedia Jasa

- **Profil:** Individu atau usaha kecil dengan pengalaman perbaikan sepatu
- **Tipe:** Penyedia tetap (kios di pasar) dan penyedia mobile (keliling)
- **Teknologi:** Sudah familiar dengan smartphone Android dan WhatsApp
- **Motivasi:** Ingin pendapatan lebih stabil dan jangkauan pelanggan lebih luas

---

## Scope MVP

### Yang Masuk MVP ✅

| Fitur | Deskripsi Singkat |
|---|---|
| Autentikasi | Registrasi, login, dan verifikasi via OTP |
| Profil Penyedia Jasa | Setup profil, lokasi, area layanan, dan slot waktu |
| Portfolio | Upload dan tampilkan foto hasil pekerjaan |
| Daftar & Pencarian Penyedia Jasa | Browse penyedia jasa berdasarkan lokasi |
| Validasi Geolocation | Cek radius layanan sebelum booking (untuk penyedia mobile) |
| Sistem Booking | Pembeli membuat pesanan dengan memilih layanan dan slot waktu |
| Konfirmasi Order (HITL) | Penyedia jasa konfirmasi atau tolak pesanan secara manual |
| Tracking Status | Update dan pantau status pekerjaan secara real-time |
| Notifikasi | Push notification untuk setiap perubahan status order |
| Riwayat Transaksi | Daftar semua pesanan yang pernah dibuat/diterima |

### Yang Tidak Masuk MVP ❌

Lihat bagian [Fitur di Luar Scope MVP](#fitur-di-luar-scope-mvp).

---

## User Stories

### Pembeli

```
Sebagai pembeli,
saya ingin melihat daftar penyedia jasa di sekitar lokasi saya,
agar saya dapat memilih penyedia jasa yang paling sesuai dengan kebutuhan saya.

Sebagai pembeli,
saya ingin melihat portfolio foto hasil pekerjaan penyedia jasa,
agar saya dapat menilai kualitas pekerjaan mereka sebelum memesan.

Sebagai pembeli,
saya ingin membuat pesanan dengan memilih slot waktu yang tersedia,
agar jadwal pengerjaan sepatu saya terkoordinasi dengan baik.

Sebagai pembeli,
saya ingin menerima notifikasi saat status pesanan saya berubah,
agar saya tidak perlu bertanya manual tentang progres pekerjaan.

Sebagai pembeli,
saya ingin dapat membatalkan pesanan yang belum dikonfirmasi,
agar saya tidak terikat pada pesanan yang tidak lagi saya butuhkan.
```

### Penyedia Jasa

```
Sebagai penyedia jasa,
saya ingin mengatur profil usaha dan area layanan saya,
agar calon pelanggan dapat menemukan dan menilai layanan saya dengan mudah.

Sebagai penyedia jasa,
saya ingin mengunggah foto hasil pekerjaan ke portfolio saya,
agar saya dapat membangun kepercayaan calon pelanggan baru.

Sebagai penyedia jasa,
saya ingin menerima notifikasi saat ada pesanan baru masuk,
agar saya dapat segera merespons dan tidak kehilangan pelanggan.

Sebagai penyedia jasa,
saya ingin dapat mengkonfirmasi atau menolak pesanan yang masuk,
agar saya memiliki kendali penuh atas pekerjaan yang saya terima.

Sebagai penyedia jasa,
saya ingin memperbarui status pesanan secara bertahap,
agar pembeli dapat memantau progres pekerjaan mereka secara real-time.
```

---

## Alur Pengguna

### Alur Utama: Booking Pesanan

```
[PEMBELI]

1. Buka aplikasi & login
2. Izinkan akses lokasi
3. Lihat daftar penyedia jasa terdekat
4. Buka halaman detail penyedia jasa
   └── Lihat profil, layanan, dan portfolio
5. Pilih layanan + slot waktu tersedia
6. (Untuk penyedia mobile) Sistem validasi radius otomatis
   ├── Dalam radius → lanjut ke langkah 7
   └── Di luar radius → sistem tampilkan pesan, sarankan penyedia lain
7. Submit form booking + catatan opsional
8. Terima konfirmasi pesanan berhasil dibuat
9. Tunggu notifikasi dari penyedia jasa

[PENYEDIA JASA]

10. Terima push notification pesanan baru
11. Buka dashboard, lihat detail pesanan
12. Pilih: Konfirmasi atau Tolak
    ├── Konfirmasi → status: Dikonfirmasi, notifikasi ke pembeli
    └── Tolak → isi alasan → status: Dibatalkan, notifikasi ke pembeli
13. Mulai kerjakan → update status: Sedang Dikerjakan
14. Selesai → update status: Selesai
15. Pembeli terima notifikasi, order ditutup & disimpan ke riwayat
```

### Alur Status Pesanan

```
Menunggu Konfirmasi
       │
       ├──[Ditolak]──────────────────→ Dibatalkan
       │
       ▼
  Dikonfirmasi
       │
       ├──[Dibatalkan penyedia jasa]→ Dibatalkan
       │
       ▼
Sedang Dikerjakan
       │
       ▼
    Selesai
       │
       ▼
    Ditutup
```

---

## Fitur Detail

### 1. Autentikasi

- Registrasi dengan nomor telepon + OTP (berlaku 5 menit, sekali pakai)
- Pilih tipe akun: Pembeli atau Penyedia Jasa
- Login dengan nomor telepon + kata sandi
- Reset kata sandi via OTP

### 2. Profil Penyedia Jasa

- **Data profil:** nama usaha, foto profil, deskripsi layanan, nomor telepon, tipe layanan (tetap/mobile)
- **Lokasi:**
  - Penyedia tetap: koordinat lokasi tetap di peta
  - Penyedia mobile: titik operasional utama + radius layanan (km)
- **Slot waktu:** atur jam buka/tutup dan interval slot per hari; slot yang sudah dipesan otomatis terkunci

### 3. Portfolio

- Upload foto hasil pekerjaan (maks. 20 foto per akun di MVP)
- Keterangan singkat per foto (opsional)
- Tampil di halaman profil publik penyedia jasa
- Penyedia jasa dapat menghapus foto

### 4. Daftar & Pencarian Penyedia Jasa

- Daftar penyedia jasa berdasarkan jarak dari lokasi pembeli
- Setiap item menampilkan: nama usaha, foto profil, tipe layanan, jarak
- Filter: tipe layanan (tetap/mobile), jenis layanan (sol, jahit, lem, dll.)
- Halaman detail: profil lengkap, layanan & kisaran harga, portfolio, slot tersedia, lokasi di peta

### 5. Validasi Geolocation (Penyedia Mobile)

- Sistem menghitung jarak antara lokasi pembeli dan titik operasional penyedia mobile
- Jika dalam radius → booking dapat dilanjutkan
- Jika di luar radius → sistem menolak dan menyarankan penyedia lain
- Penyedia jasa dapat mengoreksi titik lokasi secara manual

### 6. Sistem Booking

- Pembeli memilih: layanan, slot waktu, catatan tambahan (opsional)
- Sistem validasi ketersediaan slot dan radius sebelum order dibuat
- Order dikirim ke dashboard penyedia jasa sebagai pesanan masuk

### 7. Konfirmasi Order — HITL

> ⚠️ **Human-in-the-Loop:** Konfirmasi pesanan tidak diotomasi. Keputusan sepenuhnya ada di tangan penyedia jasa karena mereka perlu menilai kapasitas aktual, kondisi cuaca (untuk penyedia mobile), dan kelayakan permintaan secara subjektif.

- Penyedia jasa mendapat notifikasi pesanan baru
- Opsi: **Konfirmasi** atau **Tolak** (wajib isi alasan jika tolak)
- Jika tidak direspons dalam 2 jam: sistem kirim reminder notifikasi

### 8. Tracking Status

| Status | Diubah Oleh | Notifikasi ke |
|---|---|---|
| Menunggu Konfirmasi | Sistem (otomatis saat order dibuat) | Penyedia Jasa |
| Dikonfirmasi | Penyedia Jasa | Pembeli |
| Sedang Dikerjakan | Penyedia Jasa | Pembeli |
| Selesai | Penyedia Jasa | Pembeli |
| Ditutup | Pembeli (konfirmasi penerimaan) | — |
| Dibatalkan | Pembeli atau Penyedia Jasa | Kedua pihak |

- Status hanya bergerak maju (tidak bisa kembali ke status sebelumnya)
- Riwayat perubahan status ditampilkan kronologis di halaman detail pesanan

### 9. Notifikasi

Push notification dikirim untuk:
- Pesanan baru masuk (→ penyedia jasa)
- Pesanan dikonfirmasi atau ditolak (→ pembeli)
- Status pesanan berubah (→ pembeli)
- Pesanan dibatalkan (→ kedua pihak)
- Reminder pesanan belum direspons dalam 2 jam (→ penyedia jasa)

### 10. Riwayat Transaksi

- Pembeli: semua pesanan yang pernah dibuat beserta status
- Penyedia jasa: semua pesanan yang pernah diterima beserta status
- Tersimpan permanen sebagai dasar fitur rating & review di v1.1

---

## Fitur di Luar Scope MVP

| Fitur | Alasan Ditunda | Target Versi |
|---|---|---|
| Rating & Review | Belum ada cukup data transaksi untuk review yang kredibel | v1.1 |
| Estimasi Harga Otomatis | Harga variatif tergantung kondisi fisik sepatu | v1.1 |
| Chat In-App | Pengguna masih bisa pakai WhatsApp untuk komunikasi awal | v1.1 |
| Pembayaran Online / Escrow | Memerlukan integrasi payment gateway dan sistem mediasi dispute | v1.2 |
| Sistem Dispute / Mediasi | Bergantung pada adanya mekanisme pembayaran online terlebih dahulu | v1.2 |
| Dashboard Admin | Tidak kritis pada tahap awal | v1.2 |
| Layanan Antar-Jemput Pihak Ketiga | Memerlukan integrasi logistik eksternal | v2.0 |

---

## Metrik Keberhasilan

### Metrik Akuisisi

| Metrik | Target (3 Bulan Pertama) |
|---|---|
| Jumlah penyedia jasa aktif (supply) | ≥ 10 penyedia jasa |
| Jumlah pembeli terdaftar (demand) | ≥ 200 akun |
| Jumlah transaksi pertama | ≥ 100 pesanan |

### Metrik Engagement

| Metrik | Target |
|---|---|
| Order completion rate | ≥ 70% (pesanan yang berakhir Selesai, bukan Dibatalkan) |
| Response time penyedia jasa | ≤ 2 jam rata-rata |
| Repeat order rate | ≥ 30% dalam 3 bulan pertama |

### Metrik Teknis

| Metrik | Target |
|---|---|
| Waktu muat halaman daftar penyedia jasa | < 3 detik (koneksi 4G) |
| Delay notifikasi status | < 5 detik |
| Uptime sistem | ≥ 99% per bulan |

---

## Asumsi & Keterbatasan

### Asumsi

- Pengguna memiliki smartphone Android 8.0+ atau iOS 13+ dengan koneksi internet
- Penyedia jasa mampu mengoperasikan aplikasi secara mandiri setelah onboarding
- Pembayaran dilakukan sepenuhnya di luar aplikasi (offline/cash)
- Penyedia jasa bersedia meluangkan waktu untuk setup profil dan portfolio awal

### Keterbatasan MVP

- Tidak ada sistem dispute atau perlindungan finansial dalam aplikasi
- Tidak ada chat in-app; komunikasi tambahan melalui WhatsApp
- Rating & review belum tersedia di versi pertama
- Estimasi harga bersifat indikatif; harga final ditentukan penyedia jasa setelah melihat kondisi sepatu

---

## Risiko

| # | Risiko | Tingkat | Mitigasi |
|---|---|---|---|
| 1 | Validasi pasar masih anekdotal (5 responden) | 🔴 Tinggi | Survei kuantitatif ke ≥ 50 calon pengguna sebelum pengembangan penuh |
| 2 | Cold start — tidak ada penyedia jasa saat launch | 🔴 Tinggi | Akuisisi manual ≥ 10 penyedia jasa aktif di Manado sebelum soft launch |
| 3 | Tidak ada perlindungan transaksi di MVP | 🟡 Sedang | Tambahkan disclaimer; percepat implementasi rating di v1.1 |
| 4 | Penyedia jasa enggan onboarding (literasi teknologi rendah) | 🟡 Sedang | Panduan onboarding berbasis video; pendampingan langsung di awal |
| 5 | Akurasi geolocation rendah di area pasar tradisional | 🟢 Rendah | Izinkan penyedia jasa koreksi titik lokasi secara manual |

---

## Referensi

| Dokumen | Keterangan |
|---|---|
| [`PRODUCT_DISCOVERY.md`](./product-discovery-solku.md) | Transkrip sesi product grilling dan keputusan desain |
| [`SRS_SolKu_MVP_v1.0.docx`](./SRS_SolKu_MVP_v1.0.docx) | Software Requirements Specification lengkap |
| [`vertical-slice-issues-solku.md`](./vertical-slice-issues-solku.md) | Vertical slice issues untuk GitHub |
| Notulen Wawancara | Hasil wawancara 2 penyedia jasa dan 3 pembeli di Manado |

---

*SolKu PRD v1.0 — Dokumen ini bersifat living document dan akan diperbarui seiring perkembangan produk.*
