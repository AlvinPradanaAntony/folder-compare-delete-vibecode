# Changelog

Semua perubahan penting pada proyek ini akan dicatat dalam file ini.

## [2.1.0] - 2026-04-04

### Ditambahkan

- Navigasi menu _sidebar_ baru (Dashboard, Riwayat & Undo, Trash Internal) beserta ikon visual.
- Sistem pencatatan riwayat (History) untuk setiap aksi penting (Scan, Hapus, Salin, Pindah, dll).
- Fitur _Undo_ yang memungkinkan pengguna membatalkan dan mengembalikan rincian aksi sebelumnya (seperti membatalkan penghapusan atau penyalinan file).
- Opsi tambahan untuk mengizinkan penghapusan paksa hasil oranye (file unik di sumber) dan hasil merah (nama sama beda isi).
- Fitur "Salin Terpilih" dan "Pindah Terpilih" (termasuk saran pintar sinkronisasi ke folder pembanding).
- Ikon SVG kustom untuk mendukung tampilan _sidebar_ (`dashboard.svg`, `history.svg`, `trash-can.svg`).

### Diperbarui

- Perombakan antarmuka tabel dan overlay dialog untuk mendukung kemajuan status _progress_ yang baru.

## [2.0.0] - 2026-04-02

### Ditambahkan

- Migrasi antarmuka pengguna secara penuh dari `Tkinter` ke `PySide6` untuk tampilan yang lebih modern, dinamis, dan responsif.
- Implementasi overlay dialog dengan efek blur latar belakang dan transisi mulus (`ErrorOverlayDialog`, dll).
- Otomatisasi proses rilis CI/CD menggunakan GitHub Actions untuk Windows (.exe, Setup.exe), Linux (.AppImage, .deb), dan macOS (.dmg).
- Sistem styling UI tersentralisasi menggunakan Qt Style Sheets.

### Diperbarui

- Pengoptimalan asinkron background scanning.
- Penanganan error aplikasi secara keseluruhan (SafeApplication) yang menangkap _uncaught exceptions_ dengan bersih.
- Pengunaan `send2trash` tetap dipertahankan untuk keamanan penghapusan file.

## [1.0.1] - 2026-04-02

### Ditambahkan

- Implementasi awal aplikasi `Folder Compare & Delete`.
- Fitur pemindaian dan perbandingan isi dari beberapa folder sekaligus.
- Antarmuka pengguna visual berbasis Treeview menggunakan pustaka bawaan `Tkinter/ttk` (tanpa dependensi UI eksternal).
- Dua mode pembandingan: mode cepat (Nama + Ukuran) & mode akurat (Hash SHA-256 + Ukuran).
- Sistem pemrosesan pemindaian berjalan secara asinkron (_thread-based background scanning_) sehingga antarmuka tetap responsif.
- Fitur penghapusan _recycle bin_ untuk memastikan file terhapus dengan aman (menggunakan paket `send2trash`).
- Konfirmasi penghapusan massal untuk meminimalisasi kesalahan.
- Tabel hasil warna warni untuk hasil perbandingan yang intuitif (Hijau untuk duplikat sama persis, Merah untuk nama sama isi berbeda, Oranye untuk file unik).
- Fitur ekspor hasil perbandingan log lengkap ke format CSV dan Excel (`openpyxl`).

### Diperbarui

- Pengoptimasian kode dan penyesuaian GUI agar dapat dijalankan di Windows, macOS, dan Linux.
