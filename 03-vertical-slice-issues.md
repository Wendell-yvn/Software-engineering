## 🔻 Vertical Slice Issues (End-to-End System)

### 1. **Service Discovery Problem (Awal Funnel)**

Masalah:
Pengguna tidak punya alasan kuat untuk memilih penyedia jasa tertentu saat pertama kali membuka aplikasi.

Dampak:

* Tidak ada trust awal
* Booking tidak terjadi tanpa rating/portfolio yang kuat
* Cold start problem

---

### 2. **Uncertain Pricing Problem**

Masalah:
Harga jasa sol sepatu tidak selalu fixed dan tergantung kondisi barang.

Dampak:

* Pembeli ragu untuk booking
* Potensi cancel setelah estimasi
* Konflik ekspektasi harga

---

### 3. **Scheduling & Availability Conflict**

Masalah:
Penyedia jasa (terutama mobile) punya jadwal fleksibel dan tidak selalu terstruktur.

Dampak:

* Double booking
* Ketidaksesuaian waktu kedatangan
* Ketergantungan komunikasi manual jika tidak diatur dengan baik

---

### 4. **Location Matching Problem (Mobile Service)**

Masalah:
Tidak semua penyedia jasa bisa melayani semua lokasi pembeli.

Dampak:

* Booking gagal setelah dibuat
* Banyak cancel di tahap akhir
* Sistem harus punya geofencing atau radius logic

---

### 5. **Service Handoff Problem (Physical Goods Flow)**

Masalah:
Tidak ada standar mekanisme perpindahan sepatu dari pembeli ke penyedia jasa.

Dampak:

* Proses tidak konsisten (drop-off vs pick-up vs delivery)
* Potensi miskomunikasi
* Sulit diotomasi

---

### 6. **Trust & Quality Uncertainty**

Masalah:
Pembeli tidak tahu kualitas hasil sebelum transaksi terjadi.

Dampak:

* Ragu untuk booking pertama kali
* Ketergantungan pada review/portfolio (yang belum terbentuk di awal MVP)

---

### 7. **No Payment Protection (Dispute Risk)**

Masalah:
Tidak ada escrow atau sistem jaminan pembayaran.

Dampak:

* Risiko pembeli tidak membayar
* Risiko penyedia jasa tidak menyelesaikan pekerjaan
* Sistem tidak bisa menyelesaikan konflik

---

### 8. **Operational Dependency on Manual Behavior**

Masalah:
Banyak proses masih bergantung pada kebiasaan manusia (datang tepat waktu, jujur status, dll).

Dampak:

* Sistem tidak fully enforceable
* UX sangat tergantung disiplin user
