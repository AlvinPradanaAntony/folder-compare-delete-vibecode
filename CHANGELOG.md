# Changelog

Semua perubahan penting pada proyek ini akan dicatat dalam file ini.

## [2.4.0] - 2026-04-09

### Ditambahkan
- Fitur **Bulk Sync (Sinkronisasi Massal)** pada file duplikat (hijau) yang mising atau kurang di direktori target, menyalin secara instan ke seluruh folder pembanding tanpa proses scan ulang.
- Tombol konteks **Tampilkan di File Explorer** untuk mengakses file asli pada sistem operasi dengan cepat.
- Implementasi baru indikator visual loading menggunakan **PyQt WaitingSpinner** demi antarmuka pengguna yang jauh lebih halus.

### Diperbarui
- Konteks rekaman di *Undo Stack* dan *History* kini dioptimalkan lebih spesifik dengan melacak riwayat *affected file names*.
- Perbaikan rilis GitHub Actions (CI/CD) mendukung injeksi direktori aset dan folder komponen eksternal.

## [2.3.0] - 2026-04-07

### Ditambahkan
- Sistem **Pembaruan Otomatis (Auto Updater)** terintegrasi dengan GitHub API untuk mengecek dan mengunduh rilis langsung dari dalam aplikasi.
- Tombol *Sync* baru di sidebar untuk memeriksa pembaruan (Status dialog & Loading progress bar animasi).
- Dukungan icon taskbar spesifik untuk Windows (`myappid`) serta `app_icon.png` bawaan untuk mencegah konflik icon dengan aplikasi python lain.
- Layout dan visual Modernisasi untuk `FileDetailOverlayDialog` termasuk animasi hover tombol biru `PRIMARY`.

### Diperbarui
- Penyesuaian pada kolom riwayat/history `("Nama File")` untuk menampilkan detail yang lebih kontekstual pada nama file.
- Penyelesaian masalah status sinkronisasi tabel (label yang tersalin/terpindah) sehingga tak lagi memerlukan scan manual berulang kali.

<details>
<summary><strong>Lihat Riwayat Versi Sebelumnya</strong></summary>

<br>

## [2.2.0] - 2026-04-04

### Ditambahkan
- Sistem **Trash Internal** khusus aplikasi. File yang dihapus bisa disimpan dalam direktori aman internal untuk menghindari penggunaan Recycle Bin Windows secara langsung.
- Dialog interaktif `FileDetailOverlayDialog` saat Anda melakukan *double klik* pada file di tabel. Tampilan detail baru memuat informasi path, status sinkronisasi, ukuran dan opsi tindakan sinkronisasi (`copy` atau `move` ke folder pembanding).
- Penyempurnaan UX *undo* dan pengelolaan navigasi menu secara persisten di aplikasi berbasis *State* (`trash_db.json`).
- Tab menu baru khusus pengaturan dan pemantauan berkas yang berada dalam keranjang sampah (Trash) internal dengan total perhitungan kapasitas secara *real time*.

### Diperbarui
- Refaktor mode Recycle bin menjadi *Trash Internal* yang lebih dapat disesuaikan dan di-undo tanpa campur tangan dari OS layer.

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

</details>
