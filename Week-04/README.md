# Modul 4: Social Engineering & Session Hijacking

Laporan evaluasi praktikal keamanan siber dan analisis kerentanan pada portal finansial simulasi **PT Teknologi Aman Sejahtera** (*Vinix Seven Internship Program*).

## 👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar

---

## 📋 Ringkasan Materi & Evaluasi Misi

1. **Analisis Simulasi Phishing & Security Awareness**
   - Mengidentifikasi *Red Flags* pada halaman phishing tiruan (domain logo mencurigakan, teknik manipulasi psikologis *urgency/countdown timer*, dan *typosquatting* pada footer).
   - Menganalisis metrik kampanye phishing, penanganan privasi tanpa menyimpan kata sandi pengguna secara langsung, serta penerapan budaya *no-blame culture* untuk edukasi pegawai.

2. **Pengujian Manajemen Sesi & Kerentanan Session Hijacking**
   - Mengamati atribut cookie awal (`session_token`) yang tidak mengaktifkan flag `HttpOnly` dan `Secure`.
   - Melakukan pembuktian celah keamanan melalui *Console* browser (`document.cookie`), di mana token sesi dapat dibaca oleh skrip sisi klien (*Client-Side Script*).
   - Mensimulasikan *Session Hijacking* dan menguji penerapan mitigasi `HttpOnly=True` untuk memblokir akses JavaScript terhadap token sesi.

3. **Analisis Log Server & Deteksi Anomali Sesi**
   - Menyelidiki indikasi *IP Address Shift* dan *User-Agent Mismatch* (akses mencurigakan menggunakan alat otomatisasi seperti cURL atau Python-urllib).
   - Membuktikan pentingnya penerapan mekanisme *Session Binding* dan *Session Regeneration* pada sisi server.

4. **Rekomendasi Teknis & Tata Kelola Keamanan**
   - **Aspek Teknis Aplikasi:** Konfigurasi cookie yang aman (`HttpOnly`, `Secure`, `SameSite=Strict`), pencegahan *Session Fixation*, dan implementasi *Session Binding*.
   - **Aspek Tata Kelola & SDM:** SOP verifikasi kanal komunikasi internal resmi serta pelaksanaan simulasi *phishing* berkala yang edukatif.

---
📁 *Catatan: Laporan lengkap beserta dokumentasi pengujian dan bukti tangkapan layar (screenshot) dapat diunduh pada file **Kelompok 8_Modul 4.pdf** di folder ini.*
