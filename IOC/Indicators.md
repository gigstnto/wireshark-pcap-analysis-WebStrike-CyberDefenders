# 🛡️ Detailed Indicators of Compromise (IOC)

## 🌐 Network Indicators
| Indicator | Value | Description |
| :--- | :--- | :--- |
| **Attacker IP** | 117.11.88.124 | Source of the attack |
| **Target IP** | 24.49.63.79 | Compromised Web Server |
| **C2 Port** | 8080 | Potential Reverse Shell outbound port |
| **Origin City** | Tianjin, CN | Identified via Geolocation |

## 📁 File & Host Indicators
| Indicator | Value | Description |
| :--- | :--- | :--- |
| **Filename** | `image.jpg.php` | Malicious PHP Web Shell |
| **Path** | `/reviews/uploads/` | Upload destination directory |
| **Target File** | `/etc/passwd` | File targeted for exfiltration |

## 🛠️ Artifacts (HTTP Metadata)
* **User-Agent:** `Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0`
* **Request Method:** `HTTP POST`
* **Status Code:** `200 OK` (Successful Upload)

## 🕒 Incident Timeline
* **Detected at:** Nov 30, 2023 18:44:19 UTC
* **Severity:** 🔴 **CRITICAL** (Unauthorized Remote Access)
