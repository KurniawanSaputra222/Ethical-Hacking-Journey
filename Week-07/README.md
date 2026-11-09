# Modul 7: Cloud Security, SSRF & IAM Misconfiguration

Laporan praktikum audit keamanan portal Wi-Fi Tamu (Captive Portal) berbasis AWS Cloud, mencakup eksploitasi celah *Server-Side Request Forgery* (SSRF), ekstraksi kredensial metadata instance, hingga pengambilan alih cloud storage (*Cloud Takeover*)

👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar
- Robin Felix Hama

📋 Ringkasan Misi & Pembahasan
1. Misi 1: Discovery & SSRF Exploitation
   - Membuktikan kerentanan SSRF pada fitur tes koneksi (`/diagnostic`) dengan mengarahkan request ke layanan lokal AWS Instance Metadata Service (`169.254.169.254`)
   - Menelusuri direktori metadata IAM dan mengekstrak kredensial sementara (`AccessKeyId`, `SecretAccessKey`, dan `Token`) dari `admin-role`
2. Misi 2: Cloud Takeover
   - Melakukan *reconnaissance* manual melalui *View Page Source* dan direktori tersembunyi untuk menemukan endpoint *Internal Cloud Storage* (`/internal-storage`)
   - Menggunakan kredensial IAM curian untuk mengotentikasi diri pada konsol internal dan berhasil membaca dokumen rahasia `tas-secure-internal-backup-s3` serta mendapatkan flag kelulusan
3. Misi 3: Remediasi & Cloud Architecture
   - Merancang perbaikan SSRF melalui validasi *URL allowlist* dan pemblokiran routing ke IP privat/loopback
   - Menerapkan prinsip *Least Privilege* pada kebijakan IAM serta bermigrasi ke **IMDSv2** yang mewajibkan mekanisme berbasis token sesi (*token-authenticated requests*) untuk mencegah SSRF sederhana

📁 Catatan: File laporan lengkap beserta bukti tangkapan layar (screenshot) dapat diunduh pada file `Kelompok 8_Cybersecurity Ethical Hacker_Modul 7.pdf` di folder ini
