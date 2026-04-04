# Folder Compare Delete

![Version](https://img.shields.io/badge/version-2.2.0-blue.svg)
![Developer](https://img.shields.io/badge/developed%20by-Tonzdev-brightgreen.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![PySide6](https://img.shields.io/badge/GUI-PySide6-orange.svg)

**Folder Compare Delete** adalah aplikasi desktop canggih dan komprehensif berbasis Python dan PySide6 untuk membandingkan isi beberapa folder sekaligus, mengidentifikasi file duplikat (secara nama maupun konten melalui _hashing_), mempertimbangkan perbedaan secara visual, dan mengeksekusi proses aksi terhadap file secara aman (seperti hapus, pindah, atau salin).

Aplikasi ini menyertakan sistem perlindungan file built-in seperti _Trash Internal_, pencegahan kesalahan hapus dengan visual interaktif, hingga _Timeline Aktivitas_ dengan fitur Undo.

---

## 📸 Tampilan Aplikasi (Snapshots)

### 1. Multi-folder Compare & Visual Diff Review

Antarmuka utama untuk menganalisis dan membandingkan _Folder A_ (Target) dengan folder pembanding lainnya. Memberikan visualisasi kode warna untuk:

- 🟢 **Hijau (Duplikat Aman)**: File identik di folder lain.
- 🔴 **Merah (Berbeda)**: Nama sama namun isi (hash/ukuran) berbeda.
- 🟠 **Oranye (Hanya di A)**: File eksklusif yang hanya ada di Folder A.

![Main UI](https://github.com/user-attachments/assets/562575c3-bd77-4ba6-a825-76f9d12f2bde)

### 2. Riwayat Aksi (Action History)

Mencatat dan memantau setiap rekam jejak operasi file di dalam aplikasi (seperti Scan, Hapus, Pindah, atau Restore). Pengguna dapat melihat detail eksekusi proses dan membatalkan aksi (Undo).

![History UI](https://github.com/user-attachments/assets/e3406637-e978-4905-90c2-8c0921790051)

### 3. Trash Internal Aplikasi (Safe Delete)

Menyediakan lapisan keamanan cadangan. File yang terhapus dapat disimpan di Trash Internal, sehingga Anda dapat memulihkannya kapan saja dan menghindar dari risiko hilangnya data secara permanen akibat kesalahan klik.

![Trash UI](https://github.com/user-attachments/assets/9627fcee-0674-4a8f-b34b-4a67d25390a0).

---

## ✨ Fitur Utama

- **Multi-Folder Compare**: Bandingkan Folder target dengan satu atau lebih folder sekaligus.
- **Smart Scanning**: Identifikasi perbandingan menggunakan nama file, ukuran, beserta metode kalkulasi SHA-256 Hash.
- **Visual Diff Review**: Tampilan tabel interaktif dengan kode warna yang memudahkan Anda mengetahui status dari setiap file.
- **Safe Delete Flow**: Opsi menghapus ke Trash Internal atau secara permanen. Adanya proteksi ekstra terhadap file _Merah_ dan _Oranye_ agar tidak terhapus tanpa izin eksplisit.
- **Export Data**: Ekspor hasil analisis ke format CSV dan Excel dengan mudah.
- **Trash & Restore System**: Manajer penyimpanan internal untuk melihat, memulihkan, dan membersihkan riwayat file Anda sendiri.
- **Timeline Aktivitas & Undo**: Lakukan Undo terhadap aksi pemulihan/pemindahan/penghapusan bila terjadi kesalahan eksekusi.

---

## � Download Aplikasi Siap Jalan (Executable)

Anda tidak perlu repot-repot menginstal Python dan _requirements_ jika hanya ingin langsung menggunakannya. Anda dapat mengunduh versi _compiled_ yang sudah siap dijalankan!

➡️ **[Download Versi Terbaru (Latest Release)](https://github.com/AlvinPradanaAntony/apps/releases/latest)**

---

## 🚀 Cara Menjalankan (Dari Source Code)

### Prasyarat

Pastikan Anda sudah menginstal **Python 3.8+**.

### 1. Clone & Setup Repositori

```bash
git clone https://github.com/AlvinPradanaAntony/apps.git
cd apps
```

### 2. Instalasi Dependensi (PySide6)

Aplikasi ini membutuhkan _PySide6_ untuk Graphical User Interface (GUI). Anda dapat memasangnya via pip:

```bash
pip install PySide6
```

_(Opsional)_ Jika menemui kebutuhan ekspor data yang mengharuskan package _pandas_ atau modul lain yang berkaitan, silakan tambahkan:

```bash
pip install pandas openpyxl
```

### 3. Jalankan Aplikasi

Jalankan file skrip utama:

```bash
python folder_compare_delete_app.py
```

---

## 📝 Catatan Penggunaan (Workflow)

1. Buka aplikasi, lalu pilih **Folder A** (Folder Utama) dan tambahkan satu atau beberapa folder pembanding.
2. Klik tombol **Scan dan Bandingkan**. Tunggu aplikasi menghitung hash dan menganalisis kesamaan.
3. Gunakan filter tampilan untuk melihat hasil mana yang berstatus Duplikat (Hijau), Berbeda (Merah), atau Hanya di A (Oranye).
4. Tandai file yang akan ditindaklanjuti, dan tentukan apakah Anda menggunakan opsi _Hapus ke Trash Internal_ agar data lebih aman, lalu klik _Hapus Terpilih_ atau ikuti alur salin/pindah.
5. Tinjau kembali dari tab **Riwayat Aksi** atau **Trash Internal**.

---

## 🛡️ Lisensi & Disclaimer

Dikembangkan oleh **Tonzdev** (v2.2.0).  
Harap gunakan aplikasi ini dengan hati-hati. Meskipun **Folder Compare Delete** dilengkapi fitur pengaman _Trash Internal_, pastikan folder target atau data sensitif lain Anda di-_backup_ secara tersendiri. Pengembang tidak bertanggung jawab atas kerugian kehilangan data akibat kelalaian operasional.
