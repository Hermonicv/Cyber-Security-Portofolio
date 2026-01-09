# 🌐 Subfinder

## 📌 Deskripsi
Subfinder adalah tool open-source untuk melakukan **enumerasi subdomain** secara pasif. 
Tool ini mengumpulkan daftar subdomain terkait suatu domain dari berbagai sumber OSINT (Open Source Intelligence) tanpa memberikan beban berarti ke target.

Subfinder biasa digunakan pada tahap awal reconnaissance untuk memahami cakupan aset digital dari sebuah domain.

---

## 🎯 Kegunaan Utama
- Mengumpulkan subdomain yang terkait dengan domain utama
- Membantu menemukan aset web yang tidak tercatat atau terlupakan
- Memperluas pemetaan attack surface sebelum proses analisis lebih lanjut

---

## 🚀 Contoh Penggunaan

### 🟦 Enumerasi dasar pada satu domain
```bash
subfinder -d example.com
```
### 🟩 Menyimpan hasil ke file
```bash
subfinder -d example.com -o subdomains.txt
```
### 🟨 Pipeline dengan httpx (recon cepat)
```bash
subfinder -d example.com -silent | httpx -silent
```

---

## 🔗 Workflow Rekomendasi
Urutan umum penggunaan:

1. Subfinder — kumpulkan subdomain
2. Httpx — validasi mana yang aktif
3. Nmap atau analisis manual — tahap lanjutan

Pipeline lengkap contoh: 
```bash
subfinder -d example.com -silent | httpx -silent -status-code -title
```

---

## 📎 Catatan
- Subfinder bersifat pasif, aman digunakan untuk target publik
- Tidak melakukan brute force atau eksploitasi
- Ideal untuk pemula dan profesional dalam fase recon
- Output sebaiknya disimpan untuk dianalisis lebih lanjut menggunakan tool tambahan

---

## 🧠 Pembelajaran dari Penggunaan Subfinder
Dari penggunaan subfinder, saya mempelajari bahwa:

- Enumerasi subdomain adalah langkah penting dalam keamanan aplikasi web
- Banyak aset publik yang tersembunyi dari halaman utama
- Subdomain yang “kecil” dapat menjadi entry point bagi serangan jika tidak dipantau
