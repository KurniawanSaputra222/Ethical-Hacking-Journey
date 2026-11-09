# Modul 9: Cryptography, Reverse Engineering & Penetration Testing (Operation Deadlock)

Laporan penugasan *Advanced Reverse Engineering* dan *Cryptanalysis* pada biner Linux x86_64 (`deadlock_crackme.elf`) berstatus *stripped*

👥 Kelompok 8
- Afnan Yazid Pradana
- Kelvin Febrianto
- Kurniawan Saputra
- Rishfan Mailizar
- Robin Felix Hama

📋 Ringkasan Misi & Pembahasan
1. **Advanced Static Analysis & Anti-Debugging Bypass**: Melakukan analisis biner dengan `checksec` (No RELRO, No Canary, NX enabled, No PIE) serta melumpuhkan proteksi anti-debugging `ptrace` menggunakan teknik *patching* (mengubah instruksi `je` menjadi `NOP` / `0x90` pada offset `0x195a`)
2. **Dynamic Memory Analysis & Key Extraction**: Menjalankan biner via GDB, memasang *breakpoint* pada fungsi validasi, serta melakukan *memory dump* untuk mengekstrak 16-byte `SECRET_KEY` dan 28-byte `TARGET_CIPHERTEXT`
3. **Cryptanalysis & Decryption Automation**: Membalikkan algoritma enkripsi berantai (XOR, ROL 3-bit, penambahan modular 8-bit, dan *chained feedback*) dengan skrip Python kustom hingga berhasil merekonstruksi flag asli: `FLAG{DL_KELOMPOK_08_245D}`
4. **Exploitation & PTES Standard Reporting**: Memvalidasi flag pada biner asli yang menghasilkan pesan `[+] ACCESS GRANTED. The flag is valid!` serta menyusun laporan eksekutif berstandar PTES lengkap dengan analisis risiko CVSS v3.1 (Score: 7.7 High)

📁 Catatan: Laporan lengkap tersedia pada berkas `KELOMPOK_08_Operation_Deadlock_PTES_Report.pdf`
