# **WS04: Problem Identification & Scope**

**Mata Kuliah**: Konsep Sistem Informasi (KSI)  
**Kerangka Kerja**: Project-Based Learning (PBL) Level 1  
**Fase Learning Spine**: **Fase 2 — Frame (Problem Discovery & Scope)**  
**Minggu / Alokasi Waktu**: Minggu 2 / 14 Jam Belajar  
**Sub-CPMK / SFIA**: S-01.1 (Introduce \- Problem Framing) \| SFIA BUSA L1 (*Business Analysis*), IRMG L1  
**Penanggung Jawab Fase**: **Phase Lead 2 (Frame — Mahasiswa B)**  
**Keterkaitan Deliverable**: Sumber Utama Penyusunan **Deliverable D1 (Problem Brief \- TPL-01)**

---

## **1\. Identifikasi Tim & Objek Proyek**

| Elemen Informasi | Rincian Identitas Kelompok & Mitra |
| :---- | :---- |
| **Nama Kelompok / Kelas** | Gacor\_Kang / B |
| **Phase Lead 2 (Frame \- M2)** | Arbain Royyan Zein Alhadad — 2600016065 |
| **Nama UMKM Mitra Lapangan** | Cleanwave Laundry  |
| **Pemilik / Kontak Mitra** | Cleanwave Laundry  |

---

## **2\. Matriks Problem Framing & Analisis Akar Masalah (Root Cause Analysis)**

Gunakan temuan kuantitatif dari `WS03` untuk memisahkan antara **Gejala Permukaan (*Symptoms*)** dan **Akar Masalah Utama (*Root Cause*)** operasional bisnis mitra:

| No | Kategori Observasi | Gejala Permukaan (*Symptoms*) | Akar Masalah Operasional (*Root Cause*) | Bukti Kuantitatif (*Baseline Data*) |
| :---: | :---- | :---- | :---- | :---- |
| **1** | **Proses Transaksi Kasir** | Terjadi antrean dan pelayanannya relatif lama saat jam sibuk.  | Proses pencatatan pesanan, konfirmasi detail, dan penerimaan transaksi masih memerlukan langkah manual serta verifikasi ganda.  | Rata-rata waktu transaksi \= **5 menit/pelanggan** (dengan beban puncak hingga 20 orang pada jam sibuk).  |
| **2** | **Pengelolaan Stok Barang** | Pengisian dan pemantauan stok bahan baku (detergen & pewangi) rentan terlambat atau tidak terkontrol saat pesanan menumpuk.  | Pemakaian bahan baku seperti detergen dan pewangi masih dicatat secara manual di buku catatan terpisah (belum terintegrasi otomatis dengan setiap transaksi).  | Pencatatan bahan baku masih **manual di buku catatan**.  |
| **3** | **Rekapitulasi Keuangan** | Kasir/pemilik harus meluangkan waktu ekstra setiap akhir operasional untuk menghitung ulang pendapatan.  | Total pendapatan dan pencocokan ringkasan transaksi dari aplikasi dengan fisik uang masih dihitung serta divalidasi secara manual di akhir jam kerja.  | Durasi rekap harian \= **25 menit/malam** dengan frekuensi selisih nota fisik dan uang tunai **1–2 kali/minggu**.  |

---

## **3\. Perumusan Problem Statement Kontekstual**

Berdasarkan analisis di atas, rumuskan **Problem Statement** utama dalam 1–2 paragraf terstruktur.  
*Petunjuk*: Hindari mendefinisikan masalah sebagai *"Mitra belum memiliki aplikasi Python/komputer"*. Definisikan dari hambatan bisnis nyata mitra\!

> **Rumusan Problem Statement Kelompok**:  
> ""Proses pencatatan penggunaan bahan baku (detergen dan pewangi) yang masih dilakukan secara manual pada buku catatan terpisah serta proses validasi rekapitulasi harian di akhir operasional pada Cleanwave Laundry menyebabkan bottleneck operasional. Kondisi ini berdampak pada durasi pelayanan transaksi yang mencapai 5 menit per pelanggan saat jam sibuk (mencapai 20 pelanggan), waktu rekapitulasi harian yang memerlukan durasi 25 menit setiap malam, serta adanya risiko kesalahan pencatatan atau selisih nota dengan fisik uang tunai sebanyak 1–2 kali per minggu. Jika tidak ditangani, hal ini menghambat efisiensi pelayanan operasional dan akurasi pelaporan harian mitra." "

---

## **4\. Menetapkan Batasan Sistem (System Boundary / Scope Alignment)**

Untuk mencegah terjadinya pembengkakan fitur (*Scope Creep*) yang membahayakan penyelesaian proyek dalam 1 semester, tentukan secara tegas apa yang **Masuk Cakupan (*In-Scope*)** dan apa yang **Di Luar Cakupan (*Out-of-Scope*)**:

 ┌─────────────────────────────────────────────────────────────────────────┐  
│                    SYSTEM BOUNDARY (BATASAN SISTEM)                     │  
│                                                                         │  
│   \[ IN-SCOPE: Fitur yang Akan Dibangun \]                                │  
│   1\. Input transaksi kasir & kalkulasi biaya berbasis CLI/konsol.       │  
│   2\. Pencatatan & update otomatis penggunaan stok bahan baku.          │  
│   3\. Pembuatan dan pencetakan ringkasan laporan rekap harian.           │  
│                                                                         │  
│─────────────────────────────────────────────────────────────────────────│  
│                                                                         │  
│   \[ OUT-OF-SCOPE: Di Luar Cakupan Proyek \]                              │  
│   1\. Integrasi API payment gateway e-wallet / QRIS otomatis.            │  
│   2\. Fitur penggajian karyawan / manajemen HRD.                         │  
│   3\. Integrasi pemesanan bahan baku otomatis ke supplier luar.          │  
└─────────────────────────────────────────────────────────────────────────┘

### **Tabel Penegasan Cakupan Proyek (*Scope Alignment Table*)**

| No | Modul / Fitur Sistem | Status Cakupan (*In-Scope / Out-of-Scope*) | Alasan Pertimbangan Kelayakan (O'Brien) |
| :---: | :---- | :---: | :---- |
| **1** | Input Transaksi & Kalkulasi Total Biaya  | **IN-SCOPE** | Mempercepat waktu transaksi kasir dan meminimalkan antrean pelanggan pada jam sibuk.  |
| **2** | Update & Tracking Stok Bahan Baku  | **IN-SCOPE** | Sangat memungkinkan untuk diimplementasikan menggunakan logika struktur data Python dan penyimpanan data loka  |
| **3** | Laporan Rekap Harian (Laba/Rugi)  | **IN-SCOPE** | **Kelayakan Ekonomi:** Memberikan nilai *Value of Information* bagi pemilik usaha (mahasiswa UAD) agar tidak perlu merekap manual selama 25 menit tiap malam.  |
| **4** | Pembayaran Online / Payment Gateway  | **OUT-OF-SCOPE** | **Keterbatasan Teknis & Waktu:** Memiliki kompleksitas integrasi API eksternal yang belum realistis untuk cakupan 1 semester PBL Level 1\.  |
| **5** | Multi-Branch / Manajemen HRD & Penggajian  | **OUT-OF-SCOPE** | **Kelayakan Operasional:** Mitra saat ini memfokuskan kegiatan operasional pada 1 lokasi usaha.  |

---

## **5\. Target Metrik Keberhasilan Solusi (To-Be Targets)**

Tentukan target kuantitatif perbaikan yang ingin dicapai melalui solusi sistem informasi To-Be:

| Indikator Kinerja | Kondisi As-Is (Baseline) | Target To-Be (Expected) | Estimasi Persentase Peningkatan |
| :---- | :---: | :---: | :---: |
| **Waktu Pelayanan Transaksi Kasir** | 90 detik / pelanggan | **\< 30 detik / pelanggan** | Peningkatan efisiensi **\> 60%**  |
| **Durasi Rekapitulasi Harian** | 60–90 menit / malam | **\< 10 menit / malam** | Penghematan waktu **80%**  |
| **Akurasi Pencatatan Stok** | Selisih 1–2 kali / minggu  | **0 kali selisih (Akurasi 100%)**  | Penurunan tingkat kesalahan **100%**  |

---

## **6\. Refleksi & Lembar Pengesahan Phase Lead**

### **A. Pertanyaan Refleksi Tim**

1. *Bagaimana tim memastikan bahwa batasan proyek yang ditetapkan realistis untuk diselesaikan dalam 16 minggu?*  
   * **Jawab**: tim melakukan analisis kelayakan teknis (Technical Feasibility) dengan berfokus pada pengembangan aplikasi berbasis konsol (CLI) menggunakan bahasa pemrograman Python. Fitur utama dibatasi pada 3 modul inti: transaksi pesanan, pemantauan stok bahan baku (detergen/pewangi), dan rekapitulasi harian. Fitur tingkat lanjut seperti API Payment Gateway eksternal dan manajemen multi-cabang ditetapkan sebagai *Out-of-Scope* untuk memastikannya selesai tepat waktu dalam alokasi 16 minggu.   
2. *Apakah pemilik usaha mitra telah menyetujui batasan sistem yang diusulkan oleh kelompok?*  
   * **Jawab**: Ya, pemilik Cleanwave Laundry telah memberikan konfirmasi setuju terhadap batasan sistem ini. Solusi difokuskan untuk menyelesaikan hambatan utama mereka, yaitu otomatisasi rekapitulasi harian serta integrasi pemantauan stok bahan baku tanpa membebani proses operasional yang ada. 

### **B. Tanda Tangan Pengesahan Phase Lead 2**

`Disusun oleh Phase Lead 2 (Frame): [ Arbain Royyan Zein Alhadad - 2600016065 ]`  
`Tanggal Penyusunan: [ 27/10/2026 ]`

`Tanda Tangan Phase Lead 2: ____________________`

`Diverifikasi oleh Dosen Pengampu / Coach:`  
`Tanggal: [ Tanggal ] | Status Checkpoint: [ APPROVED / REVISION NEEDED ]`  
`Catatan Dosen: __________________________________________________`  
