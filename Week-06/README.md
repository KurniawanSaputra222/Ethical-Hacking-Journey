# Modul 6: OWASP Top 10 - Vulnerability Chaining, Filter Bypassing & Secure Coding

Laporan praktikum pengujian keamanan portal Helpdesk Internal PT Teknologi Aman Sejahtera, berfokus pada pembuktian kelemahan filter *blacklist* statis, teknik *vulnerability chaining* dari Stored XSS ke CSRF, serta implementasi *secure coding*

👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar
- Robin Felix Hama

📋 Ringkasan Misi & Pembahasan
1. Misi 1: Authentication Bypass & Filter Evasion (SQLi)
   - Menganalisis kelemahan filter berbasis `replace()` berantai yang memblokir spasi, string `OR`, dan `1=1`
   - Merancang payload SQL Injection kustom (`admin'oOrR'1'='1`) menggunakan komentar SQL (`/**/`) dan variasi logika untuk melewati filter serta membobol autentikasi login
2. Misi 2: Vulnerability Chaining (Stored XSS to CSRF)
   - Mengeksploitasi filter XSS dengan metode *Tag Nesting* (`<scr<script>ipt>`) pada formulir tiket karena sanitasi hanya dilakukan satu kali iterasi (*single-pass replacement*)
   - Menggabungkan Stored XSS dengan ketiadaan CSRF Token pada endpoint `/api/update-role` untuk memaksa sesi browser Admin melakukan *Privilege Escalation* secara otomatis (*vulnerability chaining*)
3. Misi 3: Remediasi dan Secure Coding
   - Menuliskan ulang kueri database menggunakan *Prepared Statements / Parameterized Queries* untuk mengamankan sistem dari SQLi secara absolut
   - Mengusulkan penggunaan *HTML Entity Encoding* (`html.escape()`) alih-alih *blacklist* serta penerapan *Anti-CSRF Token (Synchronizer Token Pattern)*

📁 Catatan: File laporan lengkap beserta bukti tangkapan layar (screenshot) dapat diunduh pada file `Kelompok 8_Cybersecurity Ethical Hacker_Modul 6.pdf` di folder ini
