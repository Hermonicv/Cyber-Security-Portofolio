# 🔎 Reconnaissance Workflow

Dokumen ini merangkum alur dasar reconnaissance untuk memahami permukaan serangan (attack surface) suatu target secara legal dan terkontrol.  
Fokus pada pengumpulan informasi tanpa eksploitasi.

---

## 🧩 Tahapan Utama

### 1️⃣ Pengumpulan Informasi Pasif
Tujuan: Mengenali aset tanpa berinteraksi langsung pada server
Contoh aktivitas:
- Enumerasi subdomain (subfinder)
- OSINT sederhana
- Pencarian aset publik

Output:
- Domain/subdomain terkumpul dalam daftar

---

### 2️⃣ Validasi Host Aktif
Menentukan endpoint mana yang dapat diakses, dan bagaimana responsnya.

Tool:
- httpx

Informasi yang dicari:
- Status code (200/302/403/404)
- Halaman redirect
- SSL/HTTPS aktif atau tidak
- Judul halaman (title)

Output:
- Daftar host aktif yang relevan untuk dianalisis lebih lanjut

---

### 3️⃣ Enumerasi Layanan / Port (Opsional dan Legal)
Mengidentifikasi layanan yang terbuka pada target legal.

Tool:
- nmap

Tujuan:
- Mengetahui port terbuka
- Memahami layanan yang berjalan (web server, ssh, ftp, dll)

---

### 4️⃣ Observasi Manual
Kunjungan langsung menggunakan browser atau burp suite:
- Mencari fungsi/login
- Melihat struktur URL
- Mencatat perilaku respons

---

### 5️⃣ Dokumentasi
Setiap langkah menghasilkan:
- File hasil (txt/log)
- Screenshot terminal
- Temuan kecil (jika ada)

---

## ⚖️ Catatan Etika
- Tidak melakukan fuzzing / exploit tanpa izin
- Hanya bekerja pada aset legal atau lab pribadi
- Respect terhadap privasi dan batas akses

---

## 🧠 Pelajaran Inti
- Recon adalah fondasi sebelum pentesting
- Informasi pasif sudah cukup memberi gambaran risiko
- Tools hanya membantu, yang penting alurnya jelas
