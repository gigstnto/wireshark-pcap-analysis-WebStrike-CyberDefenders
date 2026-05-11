# 🕒 Incident Timeline

Urutan kejadian berdasarkan analisis paket data (Network Forensics):

| Fase | Aktivitas | Source IP | Deskripsi |
| :--- | :--- | :--- | :--- |
| **Reconnaissance** | Initial Access | 117.11.88.124 | Penyerang mengakses situs via Firefox (User-Agent teridentifikasi). |
| **Exploitation** | Web Shell Upload | 117.11.88.124 | Berhasil mengunggah `image.jpg.php` ke direktori `/uploads/`. |
| **Command & Control**| Reverse Shell | 24.49.63.79 | Server membuka koneksi outbound ke IP penyerang pada port **8080**. |
| **Exfiltration** | Data Theft | 24.49.63.79 | Upaya pencurian file `/etc/passwd` terdeteksi via perintah `curl`. |

![Attacker Profile](../evidence/attacker_info.jpg)
