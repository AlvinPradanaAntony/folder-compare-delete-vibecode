# Changelog

Semua perubahan penting pada proyek ini akan dicatat dalam file ini.

## [1.0.0] - 2026-04-02

### Ditambahkan

- Implementasi awal aplikasi `Folder Compare & Delete`.
- Fitur pemindaian dan perbandingan isi dari beberapa folder sekaligus.
- Antarmuka pengguna (UI) responsif menggunakan PySide6.
- Fitur hashing (SHA-256) untuk memastikan akurasi pencocokan isi file.
- Dialog presentasi yang informatif (Error, Success, Confirm, Processing overlays).
- Ekspor hasil perbandingan ke format CSV dan Excel (jika pustaka `openpyxl` terinstal).
- Ekspor hasil mendukung peringatan aman.

### Diperbarui

- Peningkatan kinerja pemrosesan berkas secara asynchronous.
