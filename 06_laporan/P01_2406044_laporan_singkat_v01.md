# LAPORAN PRAKTIKUM ADBO
## PERTEMUAN 1: PENGENALAN LINGKUNGAN PRAKTIKUM DAN KAKAS PEMODELAN UML

- **Nama:** Andika Rahman
- **NIM:** 2406044
- **Mata Kuliah:** Praktikum Analisis dan Desain Berorientasi Objek (ADBO)
- **Program Studi:** S1 Teknik Informatika (Semester 5)

---

### A. TUJUAN PRAKTIKUM
Berdasarkan ketentuan praktikum (Sub-CPMK terkait), tujuan dari Pertemuan 1 adalah agar mahasiswa mampu:
1. Menyiapkan workspace dan struktur direktori proyek repository sesuai Standar Operasional Prosedur (SOP) yang ditetapkan
2. Menggunakan fitur dasar kakas pemodelan UML (seperti *draw.io*) untuk membuat kanvas baru, menempatkan elemen latihan, menghubungkannya, serta menyimpan berkas sumber
3. Membuka kembali berkas sumber (`.drawio`) untuk membuktikan bahwa diagram tetap dapat disunting (*reopen test*)
4. Mengisi logbook singkat dan template metadata artefak yang merekam prosedur, hasil pemeriksaan, kendala, serta tindak lanjut individu

---

### B. DASAR TEORI
1. **Pengenalan Lingkungan & Workspace UML**
   Praktikum Analisis dan Desain Berorientasi Objek (ADBO) menggunakan studi kasus utama berupa *Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus*. Pada tahap awal (Pertemuan 1), fokus diarahkan pada pengenalan lingkungan kerja, pengelolaan struktur folder proyek agar tertib, serta pengoperasian kakas editor diagram Diagram yang dibuat pada pertemuan ini merupakan **uji operasional kakas** (*tool training*), dan belum menjadi spesifikasi analisis kebutuhan final
2. **Standard Operating Procedure (SOP) Penataan Direktori**
   Untuk menjaga kerapian dan keterlacakan artefak, workspace wajib diinisialisasi dalam folder induk berpola `IFRWP5149_<NIM>_LabAlat` yang mencakup subfolder:
   - `00_administrasi/` (Logbook kegiatan)
   - `01_skenario/` (Skenario orientasi `S-ORI-01`
   - `02_template/` (Template metadata artefak)c
   - `03_latihan_tools/` (Tempat penyimpanan berkas uji coba/latihan kakas)
   - `04_model_analisis/` & `05_model_desain/` (Disiapkan kosong untuk pertemuan selanjutnya)
   - `06_laporan/` (Laporan singkat progres)
3. **Aturan Penomoran Versi Artefak**
   Format penamaan berkas mengikuti aturan baku `P<dua_digit>_<NIM>_<jenis_artefak>_v<dua_digit>.<ekstensi>` (dimulai dari versi `v01`), di mana nomor versi pada berkas sumber (`.drawio`) dan hasil ekspor gambar (`.png`) harus selalu konsisten/sama

---

### C. HASIL PRAKTIKUM
1. **Setup Workspace & Berkas Administrasi**
   - Berhasil membangun struktur direktori repository lokal `IFRWP5149_2406044_LabAlat` lengkap dengan berkas `README.md` yang memuat identitas, rincian kakas, dan status pekerjaan.
   - Berhasil menyusun logbook kegiatan awal pada `00_administrasi/P01_2406044_logbook_v01.md` dan template metadata pada folder `02_template/`.
2. **Skenario Orientasi (`S-ORI-01`)**
   - Menyimpan draf skenario orientasi awal pada `01_skenario/S-ORI-01_orientasi_kasus_v01.md` yang mencatat konteks peminjaman alat serta batas sistem informasi laboratorium.
3. **Latihan Diagram Aktivitas Sederhana**
   - Membuat diagram aktivitas uji operasional kakas di folder `03_latihan_tools/` dengan nama berkas sumber **`P01_2406044_latihan_activity_v01.drawio`** dan hasil ekspor **`P01_2406044_latihan_activity_v01.png`**.
   - Diagram tersebut memuat tepat **4 elemen berurutan** sesuai instruksi jobsheet:
     1. *Initial Node* (Node awal)
     2. Aktivitas: *"Buka daftar peralatan"*
     3. Aktivitas: *"Lihat informasi ketersediaan"*
     4. *Activity Final Node* (Node akhir)

---

### D. ANALISIS
1. **Analisis Struktur Workspace:** Pemisahan folder antara area latihan (`03_latihan_tools`) dan area model analisis tervalidasi (`04_model_analisis`) terbukti sangat efektif untuk mencegah tercampurnya berkas uji coba kakas dengan artefak perancangan sistem yang sesungguhnya di pertemuan-pertemuan berikutnya.
2. **Analisis Pengoperasian Kakas & Konsistensi Versi:** Pengujian buka ulang (*reopen test*) pada berkas `.drawio` menunjukkan bahwa format sumber dapat dimuat kembali, disunting posisinya, dan diekspor ulang ke format PNG tanpa mengalami kerusakan data. Hal ini memastikan bahwa dokumentasi proyek memenuhi standar kelayakan pengerjaan jangka panjang.
3. **Keterbatasan Tahap Awal:** Diagram aktivitas latihan yang dibuat pada pertemuan ini murni berfungsi sebagai pengujian fitur dasar editor (pembuatan bentuk, penambahan label, dan penghubung garis) sehingga belum merepresentasikan aturan bisnis secara mendalam—yang baru akan mulai dimodelkan secara bertahap pada modul-modul analisis berikutnya.

---

### E. KESIMPULAN
1. Praktikum Pertemuan 1 telah berhasil diselesaikan dengan tercapainya seluruh indikator Sub-CPMK terkait ketepatan penyiapan workspace proyek dan pengoperasian fitur dasar kakas UML.
2. Seluruh artefak pendukung seperti *README.md*, logbook, template metadata, skenario orientasi `S-ORI-01`, hingga berkas latihan diagram aktivitas (`.drawio` dan `.png`) telah tertata rapi sesuai SOP penamaan versi `v01` di dalam repository GitHub pribadi **`andika282006/IFRWP5149_2406044_LabAlat`**.