# Modul 2: Scanning & Vulnerability Analysis (Hard Mode)

Laporan praktikum *Black-Box Assessment* pemindaian jaringan, analisis kerentanan tingkat lanjut (*Advanced Level*), dan validasi celah keamanan pada mesin virtual target (Metasploitable 2) menggunakan lingkungan lab terisolasi

## 👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar

---

## 📋 Ringkasan Misi & Pembahasan

1. **Host Discovery & Stealth Scanning**
   - Melakukan *Ping Sweep* (`-sn`) untuk memetakan IP aktif dan pemindaian port TCP/UDP dengan modifikasi waktu (`-T2 / Polite`) serta fragmentasi paket (`-f`) guna menghindari deteksi IDS/Firewall
   - Merekam lalu lintas jaringan secara langsung menggunakan Wireshark di Kali Linux

2. **Deep Fingerprinting & Manual Banner Grabbing**
   - Menjalankan Nmap dengan opsi agresi versi (`-sV --version-all`) serta melakukan validasi banner layanan secara manual menggunakan **Netcat** (`nc`) pada port FTP (21), SSH (22), dan HTTP (80)

3. **Vulnerability Scanning Berbasis Engine (Nessus & NSE)**
   - Melakukan pemindaian kerentanan otomatis menggunakan **Nessus** (Basic Network Scan) yang mendeteksi berbagai celah tingkat *Critical* dan *High* (seperti OS EoL, VNC Weak Password, dan Ghostcat)
   - Menggunakan Nmap Scripting Engine (`--script vuln, exploit, auth`) sebagai perbandingan dan validasi awal

4. **Validasi False Positive & Perhitungan CVSS v3.1**
   - Melakukan pengujian eksploitasi manual pada layanan *Anonymous FTP Allowed* untuk membuktikan *True Positive*
   - Melakukan penilaian risiko menggunakan kalkulator **CVSS v3.1** (Vector: `CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N` dengan skor Base Score **7.5 / High**)

5. **Enterprise-Grade Mitigation Matrix**
   - Menyusun matriks prioritas perbaikan taktis dan strategis bagi tim IT Operations dan manajemen

---
📁 *Catatan: File laporan lengkap beserta bukti tangkapan layar (*screenshot*) terminal dan Nessus dapat diunduh pada file **Kelompok8_Modul 2.pdf** di folder ini.*
