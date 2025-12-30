# KasFlow - Platform Akuntabilitas Keuangan Berbasis Blockchain 

**"Transparency is not a Policy, it's a Code."**

KasFlow adalah prototipe sistem manajemen keuangan instansi yang menggabungkan kecepatan **Cloud Database** dengan keamanan mutlak **Blockchain** untuk mencegah manipulasi data. Sistem ini memastikan setiap transaksi memiliki "sidik jari digital" (hash) unik yang dicatat secara permanen, sehingga integritas data terjamin 100%.

## Tautan Akses
* **Live Demo (Netlify)**: [https://kasflowapp.netlify.app/](https://kasflowapp.netlify.app/)
* **Repositori Kode**: [https://github.com/McDaveStar/kasFlow](https://github.com/McDaveStar/kasFlow)

---

## Arsitektur Sistem (3-Layer Architecture)
KasFlow dibangun menggunakan arsitektur tiga lapis yang saling terintegrasi untuk menjamin performa dan keamanan:
1. **Frontend Layer**: Antarmuka web responsif berbasis Tailwind CSS untuk pengalaman pengguna yang intuitif.
2. **Supporting Layer (Supabase)**: Mengelola autentikasi, metadata instansi, dan penyimpanan log transaksi secara real-time.
3. **Blockchain Layer (Node.js & Sepolia)**: Bertindak sebagai jembatan kriptografi untuk melakukan hashing data dan penguncian permanen pada jaringan Ethereum Sepolia Testnet.

---

## Kredensial Akses Pengujian (Reviewer Only)
Untuk memudahkan dewan juri melakukan pengujian fungsionalitas penuh tanpa perlu registrasi manual, silakan gunakan akun berikut:
* **Email**: `juri@kasflow.id`
* **Password**: `pkmkc2026`
* **Role**: Administrator (Akses Penuh Verifikasi Blockchain)

---

## 🛠️ Panduan Alur Pengujian (End-to-End Flow)
Dewan juri disarankan mengikuti urutan langkah berikut untuk memvalidasi fungsionalitas sistem KasFlow:

### 1. Autentikasi & Personalisasi
* Masuk melalui modal **Akses Dashboard** menggunakan kredensial di atas.
* Dashboard akan secara otomatis menampilkan nama **"Juri PKM-KC"** dan instansi terkait sebagai bentuk personalisasi data.

### 2. Aktivasi Fitur SaaS (Sandbox Payment)
* Fitur pencatatan blockchain merupakan fitur **Enterprise** pada model bisnis KasFlow.
* Gulir ke bagian **Pricing**, pilih paket **Instansi**, dan klik **"Pilih Pro"**.
* Klik **"Bayar Sekarang"** (Simulasi/Sandbox) untuk mengaktifkan izin penulisan data ke Blockchain Layer.

### 3. Pencatatan & Verifikasi Blockchain (Fitur Utama)
* Kembali ke Dashboard dan klik tombol **"Tambah Transaksi"**.
* Masukkan detail transaksi (Contoh: "Dana Hibah Penelitian PKM").
* Setelah disimpan, sistem akan menjalankan alur otomatis:
    - **Tahap 1**: Pencatatan ke Supporting Layer (Supabase).
    - **Tahap 2**: Hashing dan pengiriman data ke jaringan Ethereum oleh Node.js Bridge.
* Tunggu beberapa saat hingga status berubah menjadi hijau: **"verified on-chain"**.

### 4. Audit Publik (Transparansi Mutlak)
* Klik pada **Transaction Hash** (kode biru `0x...`) yang muncul di tabel dashboard.
* Anda akan diarahkan ke **Sepolia Etherscan** untuk memverifikasi secara independen bahwa data tersebut telah terkunci secara kekal di blockchain global.

### 5. Selesai Sesi
* Klik tombol **Logout** untuk menghapus sesi dan kembali ke halaman utama.

---

## Instalasi Lokal (Opsional)
Untuk menjalankan server backend di lingkungan lokal:
```bash
cd Backend
npm install
node server.js
