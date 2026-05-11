# 🦈 Wireshark PCAP Analysis: WebStrike (CyberDefenders)

## 📌 Project Overview
Proyek ini berisi dokumentasi investigasi insiden keamanan siber berdasarkan tantangan "WebStrike" dari platform CyberDefenders. Fokus utama adalah melakukan **Network Forensics** menggunakan Wireshark untuk menganalisis serangan berbasis web, mengidentifikasi profil penyerang, dan memahami aktivitas *post-exploitation*.

## 🛠️ Lab Environment
Untuk melakukan analisis ini, lingkungan kerja yang digunakan meliputi:
- **Network Analysis Tool:** Wireshark
- **OS:** Kali Linux / Windows 10
- **Documentation:** Markdown (GitHub)
- **Dataset:** `WebStrike.pcap` (Network traffic log)

## 📂 Repository Structure
```text
├── analysis/
│   ├── Incident-Timeline.md     # Urutan kronologis serangan
│   ├── Web-Attack-Analysis.md   # Detail eksploitasi & profil penyerang
│   └── Post-Exploitation.md     # Aktivitas penyerang setelah akses didapat
├── evidence/
│   ├── attacker_info.jpg        # Screenshot profil penyerang
│   ├── webshell_upload.jpg      # Bukti upload file berbahaya
│   └── reverse_shell_exfiltr.jpg # Bukti terminal & pencurian data
└── README.md                    # Dokumentasi utama
```
🕵️ Analysis Summary
1. Incident Timeline
Investigasi dimulai dengan mengidentifikasi aktivitas mencurigakan dari IP eksternal. Urutan kejadian secara singkat:
- **Reconnaissance: Penyerang memindai direktori web.
- **Exploitation: Berhasil mengunggah webshell image.jpg.php.
- **Command & Control: Membuka koneksi balik (Reverse Shell) pada port 8080.
- **Exfiltration: Mencoba mencuri data sensitif /etc/passwd.

2. Attacker Profile
- **IP Address: 117.11.88.124
- **Location: Tianjin, China
- **User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0

🚀 Key Takeaways
- **Pentingnya memvalidasi ekstensi file pada form upload (mencegah Double Extension Bypass).
- **Monitoring koneksi outbound yang tidak wajar (Egress filtering) dapat mendeteksi adanya Reverse Shell.
- **Analisis Follow TCP Stream sangat krusial untuk melihat apa yang diketik penyerang di terminal.
