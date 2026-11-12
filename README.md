# 📸 Batch Photo TimeStamp & Kompresor

Aplikasi web berbasis satu file (*single-file HTML/JS*) yang dirancang khusus untuk membubuhkan cap waktu (*timestamp*) otomatis, membaca metadata **EXIF** (termasuk koordinat GPS dan konversi lokasi otomatis), melakukan kompresi fleksibel, serta mendukung pemrosesan banyak foto sekaligus (*batch processing*).

---

## ✨ Fitur Utama

1. **Smart EXIF & GPS Extraction:**
   - Secara otomatis mendeteksi tanggal dan waktu asli pengambilan foto (`DateTimeOriginal` / `DateTime`) dari metadata EXIF kamera.
   - Mendeteksi koordinat GPS Latitude & Longitude dan secara otomatis mengonversikannya menjadi nama wilayah/lokasi yang mudah dibaca menggunakan *Reverse Geocoding* (OpenStreetMap / Nominatim).
   - Menyediakan mode *fallback* (waktu sistem) jika foto tidak memiliki metadata EXIF.

2. **Pemrosesan Massal (Batch Processing):**
   - Mendukung unggah satu foto atau banyak foto sekaligus (*multi-upload*) melalui tombol klik atau fitur *drag & drop*.
   - Pratinjau langsung (*live preview*) pada kanvas dengan pilihan penyesuaian sudut posisi cap waktu (Kiri Atas, Kanan Atas, Kiri Bawah, Kanan Bawah).

3. **Mekanisme Unduh Cerdas (Smart Download):**
   - **1 Foto:** Langsung diunduh dalam format `.JPG` tunggal dengan nama file asli yang bersih.
   - **>1 Foto (Batch):** Dikemas secara otomatis ke dalam arsip `.ZIP` menggunakan *JSZip* atau dapat diunduh per foto satuan.

4. **Kompresi & Ukuran File Fleksibel:**
   - Pengaturan persentase kualitas JPEG (*slider* 20% - 100%).
   - Pembatasan resolusi maksimal (*Resize* ke 2K, Full HD, HD, dll.).
   - Target batas ukuran file maksimal (dalam KB) untuk keperluan unggah dokumen instansi.

5. **Mode Edit Manual Timestamp:**
   - Memungkinkan pengguna untuk menyesuaikan jam, hari, tanggal, atau teks lokasi secara manual (dapat diterapkan untuk foto aktif saja atau seluruh foto dalam antrean *batch*).

---

## 🛠️ Teknologi yang Digunakan

- **HTML5 & Tailwind CSS:** Antarmuka pengguna modern, responsif, dan elegan dengan tema gelap (*dark mode*).
- **EXIF.js:** Pustaka JavaScript untuk membaca metadata EXIF dari file foto JPG/JPEG.
- **JSZip & FileSaver.js:** Pustaka untuk mengepak dan mengunduh banyak file langsung di browser sebagai arsip ZIP.
- **Google Fonts (Oswald & Inter):** Kombinasi tipografi profesional untuk tampilan cap waktu yang estetis.

---

## 🚀 Cara Menjalankan Aplikasi

1. Simpan kode sumber aplikasi ke dalam satu file bernama `index.html`.
2. Buka file `index.html` tersebut menggunakan browser web apa saja (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari, dll.) tanpa memerlukan instalasi peladen (*server*) atau perangkat lunak tambahan.

---

## 📋 Panduan Penggunaan Singkat

1. **Unggah Foto:** Klik area kotak unggah atau seret (*drag & drop*) foto berformat `.jpg`, `.jpeg`, `.png`, atau `.webp` ke dalam zona unggah.
2. **Atur Cap Waktu:** Sesuaikan ukuran cap waktu melalui *slider* dan pilih sudut posisi yang diinginkan (default: Kiri Bawah).
3. **Atur Kompresi (Opsional):** Ubah tingkat kualitas gambar atau pilih batas maksimal resolusi serta ukuran file sesuai kebutuhan laporan.
4. **Edit Manual (Opsional):** Centang opsi *"Aktifkan Edit Timestamp & Lokasi Manual"* jika Anda ingin mengubah informasi waktu atau lokasi secara spesifik.
5. **Unduh Hasil:** Klik tombol unduh utama untuk menyimpan foto (.JPG untuk satu foto, atau .ZIP untuk banyak foto).
