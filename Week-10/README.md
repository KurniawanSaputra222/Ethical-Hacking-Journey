# Modul 10: Digital Forensics & Incident Response (Operation Chimera)

Laporan investigasi insiden siber pada server Internal HR Portal (`hr-portal.vinix.local`) milik PT Vinix Seven Aurum[cite: 70].

👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar
- Robin Felix Hama

📋 Ringkasan Misi & Pembahasan
1. **Evidence Integrity & Chain of Custody**: Melakukan verifikasi integritas 4 artefak bukti (`hr_portal.log`, `chimera_memo.wav`, `auth_cookie_audit.py`, dan `backup_manager.c`) menggunakan skrip `forensic_triage.py` untuk mencatat nilai hash SHA-256, ukuran file, dan nomor *inode*
2. **Timestamp Anomaly Detection**: Mendeteksi adanya manipulasi waktu (*timestomping*) pada file log dan audio (`mtime` diset ke tahun 1999) yang disengaja oleh penyerang untuk mengaburkan kronologi
3. **Tail-Byte / EOF Payload Inspection**: Memeriksa 50 byte terakhir dari file media `chimera_memo.wav` dan berhasil mengekstrak payload tersembunyi berupa flag: `FLAG{CHIMERA_GHOST_2026}`
4. **Attack Timeline & Root Cause Analysis**: Memetakan TTPs penyerang ke kerangka kerja **MITRE ATT&CK**, mengidentifikasi kerentanan *Insecure Deserialization* (`pickle.loads()`) pada manajemen sesi, serta celah *SUID Path Hijacking* pada binary `backup_manager.c` yang berujung pada eskalasi hak akses ke `root`
5. **Containment, Eradication & Remediation**: Memberikan rekomendasi penanganan insiden jangka pendek/panjang, perbaikan kode sumber yang aman (menggunakan JSON bertanda tangan HMAC alih-alih `pickle`), serta penguatan *hardening* sistem

📁 Catatan: Laporan lengkap tersedia pada berkas `Kelompok 08_Chimera_DFIR_Report.pdf`
