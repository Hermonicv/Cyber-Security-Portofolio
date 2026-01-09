# 🌍 httpx

## 📌 Deskripsi
httpx adalah tool command-line yang digunakan untuk **memvalidasi host atau subdomain yang aktif** melalui protokol HTTP/HTTPS.  
Tool ini sangat umum digunakan setelah enumerasi subdomain untuk mengetahui endpoint mana yang merespons dan layak dianalisis lebih lanjut.

---

## 🎯 Kegunaan Utama
- Mengecek subdomain yang **alive / reachable**
- Mendapatkan metadata dasar dari server
- Mengidentifikasi status HTTP, redirect, dan title
- Memfilter aset yang relevan dari hasil subfinder atau enumerasi lainnya

---

## 🚀 Contoh Penggunaan

### 🟦 Validasi host dari daftar file
```bash
httpx -l subdomains.txt
```

### 🟨 Cek host HTTPS dengan silent mode
```bash
httpx -l subdomains.txt -silent -tls-probe
```

### 🟦 Simpan hasil ke file
```bash
httpx -l subdomains.txt -o live-hosts.txt
```

---

## 🔗 Workflow Rekomendasi
Biasanya httpx tidak digunakan sendirian, tetapi sebagai bagian dari alur recon:

1. Subfinder → kumpulkan subdomain.
2. Httpx → cek mana yang aktif
3. Manual check / nmap / burp untuk eksplorasi lanjut

Contoh pipeline praktis:
```bash
subfinder -d example.com -silent | httpx -silent -status-code -title -o valid.txt
```

---

## 📎 Catatan Penggunaan
- Bersifat pasif (tidak menyerang server)
- Cocok untuk memilih target penting sebelum scanning lanjutan
- Hasilnya bisa digunakan:
1. audit permukaan
2. prioritas scanning
3. dokumentasi aset
- Output ideal disimpan agar dapat dibandingkan pada pemeriksaan berikutnya

---

## 🧠 Pembelajaran dari Penggunaan httpx
Menggunakan httpx membantu saya memahami:

- Perbedaan host aktif vs pasif
- Pentingnya memfilter aset sebelum testing
- Bagaimana server merespons secara berbeda (200, 302, 403, dsb)
- Respons sederhana bisa menunjukkan konfigurasi yang lemah atau endpoint menarik
