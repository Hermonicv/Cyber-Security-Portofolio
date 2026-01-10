# 🛡️ OWASP Top 10 (2025)

OWASP Top 10 adalah daftar kategori risiko keamanan aplikasi web yang paling dominan dan berbahaya.  
Versi **2025** merupakan pembaruan terbaru, menggantikan edisi 2024, berdasarkan tren kerentanan global, eksploitasi nyata, dan data industri.

---

## 🔟 Daftar Top 10 Risiko Utama (OWASP 2025)

### 1️⃣ A01: Broken Access Control
Akses pengguna tidak dibatasi atau divalidasi secara benar.
- User dapat melakukan aksi tanpa haknya
- Data atau fitur bocor karena kontrol izin lemah

### 2️⃣ A02: Security Misconfiguration
Konfigurasi sistem, server, API, atau cloud dibiarkan dalam kondisi tidak aman.
- Default credentials
- Debug mode menyala
- Permissions salah set

### 3️⃣ A03: Software Supply Chain Failures
Aplikasi mengandalkan komponen pihak ketiga yang rentan atau berbahaya.
- Dependency berisi malware
- Library usang yang punya exploit
- Dependency chain tidak diverifikasi

### 4️⃣ A04: Cryptographic Failures
Kesalahan dalam perlindungan data sensitif, baik saat transit maupun penyimpanan.
- Tidak pakai HTTPS
- Hashing lemah
- Data pribadi bocor

### 5️⃣ A05: Injection
Input tidak aman mengalir langsung ke sistem backend.
- SQL injection
- Command injection
- NoSQL / LDAP / deserialization

### 6️⃣ A06: Insecure Design
Masalah keamanan berasal dari pola pikir desain awal
- Tidak ada threat model
- Fitur dibuat dulu, keamanan nyusul
- Tidak ada batasan akses dari sisi arsitektur

### 7️⃣ A07: Authentication Failures
Sistem gagal memvalidasi dan melindungi identitas pengguna.
- Brute force tak dibatasi
- Session management lemah
- Token mudah ditebak

### 8️⃣ A08: Software & Data Integrity Failures
Integritas data, file, atau proses build tidak terjamin.
- Update tanpa verifikasi
- Paket bisa diganti di tengah jalan
- CI/CD pipeline tidak aman

### 9️⃣ A09: Logging and Monitoring Failures
Aplikasi tidak mencatat aktivitas kritis atau gagal memberikan alert.
- Serangan tidak terdeteksi
- Forensik mustahil dilakukan
- Insiden terlambat diketahui

### 🔟 A10: Mishandling of Exceptional Conditions
Aplikasi salah menangani error, crash, edge-case, atau input abnormal.
- Error message mengungkap detail internal
- Buffer overflow di kasus tertentu
- Server crash ketika kondisi ekstrem

---

## 🎯 Kenapa OWASP 2025 Penting Dipahami?
- Risiko makin bergeser dari **bug coding** ke **desain, supply chain, dan proses**
- Banyak serangan modern memanfaatkan dependency dan pipeline CI/CD
- Menjadi rujukan industri global (developer, tester, pentester, SOC)

---

## 🧠 Insight Pribadi
Dari daftar ini, pola kerentanan modern berakar pada:
- arsitektur yang kurang aman sejak awal,
- ketergantungan berlebihan pada third-party,
- kurangnya kontrol dan observabilitas sistem.

Memahami OWASP 2025 membantu saya:
- memetakan risiko sejak fase awal pengujian,
- mengarahkan recon ke area yang lebih berbahaya,
- mendukung komunikasi temuan ke developer/IT internal.

