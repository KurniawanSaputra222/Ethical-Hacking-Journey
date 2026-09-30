# Modul 3: System Hacking & Malware Analysis

Laporan praktikum simulasi serangan otentikasi, analisis kontrol akses, eskalasi hak istimewa, serta ekstraksi *Indicator of Compromise* (IOC) dari sampel malware

## 👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar

---

## 📋 Ringkasan Misi & Pembahasan

1. **System Hacking & Password Attack (THC Hydra)**
   - Membuat *wordlist* kustom dan menjalankan *dictionary attack* menggunakan tools **THC Hydra** terhadap layanan SSH pada mesin target (Metasploitable) hingga berhasil menemukan kredensial valid (`msfadmin:msfadmin`)
   - Melakukan login SSH dan mendapatkan akses awal (*initial access*) ke dalam sistem target
2. **Access Control & Privilege Escalation**
   - Menguji perintah `id` dan mencoba membaca berkas sensitif `/etc/shadow`, yang menghasilkan *Permission denied*.
   - Menganalisis mekanisme *Discretionary Access Control* (DAC) di Linux serta mempelajari konsep teoritis *Privilege Escalation* (seperti eksploitasi celah dan penyalahgunaan konfigurasi `sudo`).

3. **Malware Sandboxing & Ekstraksi IOC**
   - Menganalisis sampel malware (simulasi *WannaCry Ransomware*) berdasarkan hash SHA-256 menggunakan platform sandbox publik (VirusTotal).
   - Mengidentifikasi properti file (MD5/SHA-1), perilaku terhadap berkas dan *registry*, serta *Network Indicators* (domain URL *Kill-Switch* / port target).

4. **Laporan Mitigasi & System Hardening**
   - Merancang kebijakan kata sandi yang kuat serta penerapan autentikasi dua faktor (**2FA**) untuk layanan SSH
   - Menerapkan prinsip *Principle of Least Privilege* (PoLP) dan pemblokiran port/IOC pada jaringan untuk mencegah penyebaran malware

---
📁 *Catatan: File laporan lengkap beserta bukti tangkapan layar (*screenshot*) pengujian dapat diunduh pada file **Kelompok 8_Modul 3.pdf** di folder ini.*
