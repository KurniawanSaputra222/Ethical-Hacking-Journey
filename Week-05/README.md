# Modul 5: DoS (App-Layer), Evasion Detection, & WAF Mitigation

Laporan praktikum evaluasi praktikal keamanan siber mengenai analisis forensik log *Application-Layer DoS*, dekonstruksi teknik *evasion* (URL encoding/obfuscation), serta konfigurasi arsitektur pertahanan WAF dan *Rate Limiting* pada portal PT Teknologi Aman Sejahtera

👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar
- Robin Felix Hama

📋 Ringkasan Misi & Pembahasan
1. Misi 1: Forensik Lalu Lintas Data (App-Layer DoS Analysis)
   - Mengidentifikasi anomali trafik dan 3 IP paling dominan yang menyerang endpoint `/api/data-export`
   - Menganalisis alasan lonjakan trafik diklasifikasikan sebagai *Application-Layer DoS (HTTP Flood)* alih-alih *Flash Crowd* berdasarkan *User-Agent Spoofing* dan pola request berulang
   - Menjelaskan dampak lonjakan beban pada resource CPU/RAM server dibandingkan serangan volumetrik *Network Layer*
2. Misi 2: Dekonstruksi Teknik Evasion
   - Menemukan baris log anomali pada endpoint `/search` yang menggunakan teknik *Double URL Encoding* untuk mengelabui IDS berbasis *signature*
   - Melakukan proses de-obfuscation / *URL Decoding* bertahap menggunakan skrip Python untuk mengekstrak payload asli berupa SQL Injection (`' OR 1=1`)
3. Misi 3: Konfigurasi Arsitektur Mitigasi (WAF & Rate Limit)
   - Mengonfigurasi *Rate Limiting* pada dasbor WAF (15 Request per Menit) dan menguji pembatasan akses hingga server mengembalikan status HTTP `429 Too Many Requests`
   - Menambahkan *Blocked Keywords* setelah proses normalisasi WAF (*multi-layer decoding*) sehingga payload evasion berhasil diblokir dengan status HTTP `403 Forbidden`

📁 Catatan: File laporan lengkap beserta bukti tangkapan layar (screenshot) dapat diunduh pada file `Kelompok 8_Cybersecurity Ethical Hacker_Tugas Modul 5 .pdf` di folder ini
