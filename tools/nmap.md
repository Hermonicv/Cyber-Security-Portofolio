# 🔍 Nmap

## 📌 Deskripsi
Nmap (**Network Mapper**) adalah tool open-source untuk melakukan pemindaian jaringan.  
Tool ini digunakan untuk mengidentifikasi:
- port yang terbuka
- layanan (services) yang berjalan
- versi aplikasi
dan informasi jaringan lainnya pada target legal.

Nmap termasuk tool dasar yang umum dipakai dalam tahap pengumpulan informasi dan analisis permukaan.

---

## 🎯 Kegunaan Utama
- Memetakan **port terbuka**
- Mengetahui service yang berjalan di balik port
- Melihat versi software (jika tersedia)
- Membantu memetakan attack surface pada host

---

## 🚀 Contoh Penggunaan

### 🟦 Scan dasar ke target legal
```bash
nmap scanme.nmap.org
```

### 🟩 Scan dengan deteksi versi service
```bash
nmap -sV scanme.nmap.org
```

### 🟨 Scan OS dan informasi tambahan (opsional)
```bash
nmap -O scanme.nmap.org
```

### 🟧 Simpan output ke file
```bash
nmap -sV scanme.nmap.org -oN scan_output.txt
```

---

## 🧪 Mode Pemindaian Populer

- -sS → SYN scan (lebih stealth)
- -sV → Deteksi versi service
- -O → Identifikasi OS (perkiraan)
- -p → Scan port tertentu
- -A → Aggressive scan (gunakan hati-hati)

Contoh:
```bash
nmap -sS -sV -p 1-1000 scanme.nmap.org
```

---

## 🔗 Workflow Rekomendasi
Umumnya digunakan setelah menemukan host aktif dari httpx/subfinder:

1. Subfinder — cari subdomain
2. Httpx — pilih host aktif
3. Nmap — identifikasi port & service
4. Manual inspection / burp suite / exploit lab

---

## 📎 Catatan
- Gunakan hanya pada target legal atau sistem lab
- Beberapa mode scan dapat menghasilkan banyak traffic
- Semakin besar scope port → semakin lama proses
- Hasil scan yang baik sangat membantu troubleshooting dan profiling aplikasi

---

## 🧠 Pembelajaran dari Penggunaan Nmap

Melalui latihan menggunakan nmap, saya memahami:

- Bagaimana server dan jaringan diekspos melalui port
- Kenapa port yang terbuka berpotensi menjadi entry point
- Macam layanan umum (HTTP, SSH, FTP, DNS, dll)
- Nilai penting validasi service sebelum eksplorasi lanjutan

---
