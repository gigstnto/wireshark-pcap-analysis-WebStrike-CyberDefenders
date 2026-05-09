# 🌐 Network Topology - Lab Setup

Dokumentasi ini menjelaskan pengaturan jaringan yang digunakan dalam analisis lab.

### 1. Ringkasan Jaringan
* **Nama Lab:** WebStrike Lab
* **Tipe Jaringan:** Jaringan Virtual Terisolasi (Private)
* **Subnet:** 24.49.63.0/24
* **Gateway:** 24.49.63.1

### 2. Informasi Host (Mesin)
* **Web Server (Victim):**
  - IP Address: 24.49.63.79
  - Sistem Operasi: Linux (Ubuntu)
  - Layanan: Apache Web Server (Port 80)

* **Analyst Station (Mesin Saya):**
  - IP Address: 172.31.25.155
  - Fungsi: Melakukan monitoring lalu lintas data dan analisis file.

* **External Attacker (Penyerang):**
  - IP Address: 117.11.88.124
  - Lokasi: Tianjin, China

### 3. Alur Komunikasi
1. Penyerang mengakses port 80 pada Web Server untuk mengunggah file berbahaya.
2. Web Server melakukan koneksi keluar (outbound) ke IP penyerang melalui port 8080.
