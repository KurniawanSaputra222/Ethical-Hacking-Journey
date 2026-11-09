# Modul 8: Hacking IoT, OT, and Mobile Platforms

Laporan praktikum simulasi peretasan berantai (*vulnerability chaining*) terhadap infrastruktur *Smart Factory Gateway* PT Industri Otomasi Sejahtera, mulai dari analisis statis aplikasi mobile, pembobolan panel SCADA, hingga eksekusi perintah sistem di perangkat IoT

👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar
- Robin Felix Hama

📋 Ringkasan Misi & Pembahasan
1. Misi 1: Mobile App Static Analysis (The Entry Point)
   - Melakukan bedah file APK menggunakan teknik *Static Analysis* pada `strings.xml` untuk mengekstrak *hardcoded* API Key (`gateway_api_key`)
   - Menemukan kerentanan *Improper Component Export* pada `GatewayMaintenanceActivity` di `AndroidManifest.xml` yang terekspos tanpa izin proteksi
2. Misi 2: IoT & OT Gateway Exploitation (The Pivot)
   - Memanfaatkan API Key curian untuk login ke dasbor IoT Gateway dan menembus otorisasi panel SCADA menggunakan *Default Credentials*
   - Mengeksploitasi celah *Command Injection* pada fitur pembaruan firmware sensor untuk menjalankan perintah sistem (`whoami`, `cat /etc/passwd`) dan mer Иль (*flag*) kemenangan
3. Misi 3: Threat Modeling & Defensive Architecture
   - Menyusun analisis ancaman menggunakan framework **STRIDE** (Spoofing, Tampering, Repudiation, Information Disclosure, DoS, Elevation of Privilege)
   - Merekomendasikan penerapan **Purdue Model** untuk segmentasi jaringan industri agar IT dan OT terisolasi dengan aman, serta mengganti penyimpanan kredensial statis dengan **Android Keystore System**

📁 Catatan: File laporan lengkap beserta bukti tangkapan layar (screenshot) dapat diunduh pada file `Kelompok 8_Cybersecurity Ethical Hacker_Modul 8.pdf` di folder ini
