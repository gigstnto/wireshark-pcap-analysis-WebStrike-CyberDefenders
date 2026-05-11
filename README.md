# 🦈 Wireshark PCAP Analysis: WebStrike (CyberDefenders)

## 📌 Project Overview
Proyek ini berisi dokumentasi investigasi insiden keamanan siber berdasarkan tantangan "WebStrike" dari platform CyberDefenders. Fokus utama adalah melakukan **Network Forensics** menggunakan Wireshark untuk menganalisis serangan berbasis web, mengidentifikasi profil penyerang, dan memahami aktivitas *post-exploitation*.

## 🛠️ Lab Environment
Untuk melakukan analisis ini, lingkungan kerja yang digunakan meliputi:
- **Network Analysis Tool:** Wireshark
- **OS:** Linux
- **Documentation:** Markdown (GitHub)
- **Dataset:** `WebStrike.pcap` (Network traffic log)

## 📂 Repository Structure
```text
├── Analysis/
│   ├── Incident-Timeline.md
│   ├── Post-Exploitation.md
│   ├── Web-Attack-Analysis.md
│   └── Wireshark-Filters.md
├── Evidence/
│   ├── attacker_info.jpg
│   ├── reverse_shell_exfiltr.jpg
│   ├── trackIP.jpg
│   └── webshell_upload.jpg
├── IOC/
│   └── Indicators.md
├── Lab-setup/
│   └── Infrastructure-Setup.md
└── README.md
```
## 🕵️ Analysis Summary
### 1. Incident Timeline
Investigasi dimulai dengan mengidentifikasi aktivitas mencurigakan dari IP eksternal. Urutan kejadian secara singkat:
- **Reconnaissance:** Penyerang memindai direktori web.
- **Exploitation:** Berhasil mengunggah webshell `image.jpg.php`.
- **Command & Control:** Membuka koneksi balik (Reverse Shell) pada port 8080.
- **Exfiltration:** Mencoba mencuri data sensitif `/etc/passwd`.

### 2. Attacker Profile
| Field | Value |
|---|---|
| IP Address | 117.11.88.124 |
| Location | Tianjin, China |
| User-Agent | Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0 |

## 🚀 Key Takeaways
- Pentingnya memvalidasi ekstensi file pada form upload (mencegah **Double Extension Bypass**).
- Monitoring koneksi outbound yang tidak wajar (**Egress filtering**) dapat mendeteksi adanya Reverse Shell.
- Analisis **Follow TCP Stream** sangat krusial untuk melihat apa yang diketik penyerang di terminal.
