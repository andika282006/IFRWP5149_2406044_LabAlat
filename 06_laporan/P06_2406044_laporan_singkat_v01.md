# LAPORAN PRAKTIKUM ADBO
## PERTEMUAN 6: ACTIVITY DIAGRAM – DARI SKENARIO KE ALUR AKTIVITAS

- **Nama:** Andika Rahman
- **NIM:** 2406044
- **Mata Kuliah:** Praktikum Analisis dan Desain Berorientasi Objek (ADBO)
- **Program Studi:** S1 Teknik Informatika (Semester 5)

---

### A. TUJUAN PRAKTIKUM

Berdasarkan Jobsheet Praktikum Pertemuan 6, tujuan dari praktikum ini adalah agar mahasiswa mampu:

1. Menyusun alur utama activity diagram berdasarkan Skenario Normal pada tabel skenario Pertemuan 5.
2. Mengubah Skenario Alternative menjadi percabangan decision dengan guard yang sesuai.
3. Menggunakan fork dan join sebagai pasangan untuk menggambarkan proses yang berjalan secara paralel.
4. Mengelompokkan setiap action ke dalam swimlane sesuai dengan aktor yang menjalankan aktivitas tersebut.
5. Menelusuri setiap action pada activity diagram ke langkah tabel skenario Pertemuan 5.
6. Memeriksa kelengkapan dan kesesuaian diagram menggunakan checklist sebelum berkas dikumpulkan.

### B. DASAR TEORI

1. **Pengertian Activity Diagram**

   Activity diagram merupakan salah satu diagram UML yang digunakan untuk menggambarkan alur aktivitas dalam suatu proses. Diagram ini menunjukkan urutan kegiatan, percabangan keputusan, proses yang berjalan secara paralel, serta pembagian tanggung jawab setiap pelaku dalam sistem. Pada praktikum ini, activity diagram dibuat berdasarkan tabel skenario use case yang telah disusun pada Pertemuan 5.

2. **Unsur-Unsur Activity Diagram**

   Dalam pembuatan activity diagram terdapat beberapa unsur utama yang digunakan, yaitu:

   - **Initial Node:** Menunjukkan titik awal suatu aktivitas. Setiap diagram memiliki tepat satu initial node.
   - **Action:** Menggambarkan langkah atau kegiatan yang dilakukan oleh aktor maupun sistem.
   - **Control Flow:** Menunjukkan arah dan urutan perpindahan dari satu action ke action berikutnya.
   - **Decision:** Digunakan untuk membagi alur berdasarkan kondisi tertentu.
   - **Guard:** Kondisi yang ditulis dalam tanda kurung siku untuk menjelaskan setiap jalur keluar dari decision.
   - **Merge:** Menggabungkan kembali beberapa jalur percabangan ke dalam satu alur.
   - **Fork:** Membagi satu alur menjadi dua atau lebih proses yang berjalan secara paralel.
   - **Join:** Menggabungkan kembali proses paralel setelah seluruh proses selesai.
   - **Activity Final Node:** Menunjukkan akhir dari seluruh aktivitas.
   - **Swimlane:** Membagi aktivitas berdasarkan pihak yang bertanggung jawab dalam menjalankan action.

3. **Pemetaan Skenario ke Activity Diagram**

   Pembuatan activity diagram dilakukan dengan mengubah isi tabel skenario menjadi bentuk visual. Skenario Normal digunakan sebagai alur utama, sedangkan Skenario Alternative digunakan sebagai percabangan decision. Langkah include digambarkan sebagai action wajib dalam alur utama, sementara langkah extend digambarkan sebagai cabang bersyarat. Setiap kegiatan aktor ditempatkan pada swimlane aktor yang bersangkutan, sedangkan respon sistem ditempatkan pada swimlane Sistem.

4. **Aturan Penggunaan Decision, Fork, dan Join**

   Setiap jalur keluar dari decision harus memiliki guard yang jelas dan mencakup seluruh kemungkinan kondisi. Cabang yang kembali ke alur utama harus disatukan menggunakan merge. Sementara itu, proses paralel yang dimulai melalui fork harus diakhiri dengan join sebelum alur dilanjutkan. Penggunaan kedua unsur tersebut harus sesuai dengan kebutuhan proses yang digambarkan.

### C. HASIL PRAKTIKUM

Pada Pertemuan 6, praktikum berfokus pada pembuatan activity diagram berdasarkan tabel skenario yang telah disusun pada Pertemuan 5. Studi kasus yang digunakan adalah Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus serta Sistem Informasi Akademik (SIA).

**1. Activity Diagram Sistem Laboratorium (LAB)**

Berdasarkan jobsheet, terdapat tujuh activity diagram utama yang harus dibuat, yaitu:

1. **LAB-UC01 – Lihat Ketersediaan Peralatan:** Menggambarkan proses peminjam membuka fungsi ketersediaan peralatan, kemudian sistem menampilkan daftar peralatan beserta status ketersediaannya.
2. **LAB-UC02 – Kelola Data Peralatan:** Menggambarkan proses pengelolaan data peralatan dengan tiga pilihan, yaitu tambah, ubah, dan hapus data.
3. **LAB-UC03 – Ajukan Peminjaman:** Menggambarkan proses pengajuan peminjaman mulai dari pengisian formulir, penyimpanan data, pemeriksaan ketersediaan peralatan, hingga proses keputusan peminjaman.
4. **LAB-UC05 – Cetak Bukti Pengajuan:** Menggambarkan proses pencetakan bukti pengajuan apabila mahasiswa memilih untuk mencetak bukti tersebut.
5. **LAB-UC06 – Proses Keputusan Peminjaman:** Menggambarkan proses petugas laboratorium dalam memeriksa dan menetapkan keputusan pengajuan peminjaman, baik disetujui maupun ditolak.
6. **LAB-UC11 – Catat Pengembalian Peralatan:** Menggambarkan proses pengembalian peralatan, pemeriksaan kondisi, serta pembaruan status peralatan.
7. **LAB-UC07 – Lihat Laporan Peminjaman:** Menggambarkan proses kepala laboratorium memilih periode dan melihat laporan peminjaman sesuai periode tersebut.

Dalam pembuatan diagram LAB, terdapat beberapa use case yang tidak dibuatkan diagram tersendiri. LAB-UC04 dan LAB-UC12 dimasukkan sebagai action include pada diagram induknya, sedangkan LAB-UC08, LAB-UC09, dan LAB-UC10 dimasukkan sebagai cabang tambah, ubah, dan hapus pada Activity Kelola Data Peralatan.

**2. Activity Diagram Sistem Informasi Akademik (SIA)**

Pada bagian SIA, tugas praktikum adalah membuat satu activity diagram yang menggambarkan proses Input Nilai Mata Kuliah sampai Lihat KHS. Diagram ini menggunakan empat swimlane, yaitu Dosen, Sistem, Admin Akademik, dan Mahasiswa.

Alur utama dimulai ketika dosen memasukkan nilai mata kuliah, kemudian sistem menyimpan nilai tersebut. Setelah itu, dilakukan pemeriksaan kelengkapan nilai menggunakan decision. Apabila nilai belum lengkap, dosen harus melengkapi nilai terlebih dahulu. Apabila sudah lengkap, proses dilanjutkan ke pemeriksaan dan pengesahan oleh Admin Akademik.

Setelah nilai disahkan, sistem menyiapkan publikasi hasil studi. Selanjutnya, proses dibagi menggunakan fork menjadi dua aktivitas yang berjalan secara paralel, yaitu menerbitkan KHS pada portal akademik dan mengirim pemberitahuan hasil studi kepada mahasiswa. Kedua proses tersebut kemudian disatukan menggunakan join sebelum mahasiswa melihat KHS.

**3. Struktur Penyimpanan Hasil Praktikum**

Berkas hasil praktikum disimpan pada folder `04_model_analisis/P06/` dengan pembagian folder LAB dan SIA. Setiap diagram disimpan dalam format `.drawio` sebagai berkas sumber dan `.png` sebagai hasil ekspor.

Nama berkas mengikuti pola penamaan yang ditetapkan dalam jobsheet, menggunakan NIM 2406044 dan versi `v01`.

### D. ANALISIS

Berdasarkan materi Pertemuan 6, activity diagram merupakan pengembangan dari tabel skenario use case yang telah dibuat pada Pertemuan 5. Setiap langkah kegiatan dan respon sistem harus diterjemahkan menjadi action yang saling terhubung sehingga alur proses dapat dipahami dengan lebih mudah. Dengan demikian, diagram yang dihasilkan tidak boleh dibuat berdasarkan perkiraan sendiri, tetapi harus mengikuti urutan dan ketentuan pada tabel skenario sumber.

Penggunaan decision dan guard menjadi bagian penting dalam menggambarkan kondisi yang memungkinkan terjadinya percabangan. Setiap kondisi harus memiliki jalur yang jelas agar tidak terdapat alur yang menggantung. Apabila beberapa jalur kembali ke proses utama, digunakan merge untuk menyatukannya. Sementara itu, fork dan join digunakan ketika terdapat beberapa aktivitas yang dapat berjalan secara bersamaan. Kedua unsur tersebut tidak dapat saling menggantikan karena memiliki fungsi yang berbeda.

Pembagian swimlane juga membantu memperjelas tanggung jawab setiap pihak dalam sistem. Aktivitas yang dilakukan oleh mahasiswa, petugas laboratorium, dosen, admin akademik, maupun sistem harus ditempatkan pada swimlane yang sesuai. Melalui pembuatan diagram LAB dan SIA, hubungan antara skenario use case dengan alur aktivitas sistem dapat digambarkan secara lebih terstruktur. Pemeriksaan akhir perlu memastikan bahwa seluruh action memiliki sumber langkah yang jelas, setiap decision memiliki guard, fork berpasangan dengan join, serta tidak ada aktivitas yang terputus.

### E. KESIMPULAN

Berdasarkan praktikum Pertemuan 6, dapat disimpulkan bahwa activity diagram digunakan untuk menggambarkan alur aktivitas suatu proses berdasarkan skenario use case. Pembuatan diagram dilakukan dengan mengubah Skenario Normal menjadi alur utama, Skenario Alternative menjadi percabangan, serta menggunakan fork dan join untuk menggambarkan proses paralel.

Melalui praktikum ini, mahasiswa mempelajari penggunaan initial node, action, control flow, decision, merge, fork, join, activity final node, dan swimlane dalam pemodelan UML. Selain itu, setiap aktivitas harus memiliki keterkaitan dengan tabel skenario Pertemuan 5 agar diagram yang dibuat tetap sesuai dengan kebutuhan sistem. Hasil akhir praktikum berupa tujuh activity diagram LAB dan satu activity diagram SIA dalam format draw.io beserta ekspor PNG.

### F. REFERENSI

1. Object Management Group. (2017). *OMG Unified Modeling Language (OMG UML), Version 2.5.1*.
2. Institut Teknologi Garut. (2026). *Jobsheet Praktikum Analisis dan Desain Berorientasi Objek Pertemuan 4*. Institut Teknologi Garut.
3. Institut Teknologi Garut. (2026). *Jobsheet Praktikum Analisis dan Desain Berorientasi Objek Pertemuan 5*. Institut Teknologi Garut.
4. Institut Teknologi Garut. (2026). *Jobsheet Praktikum Analisis dan Desain Berorientasi Objek Pertemuan 6: Activity Diagram – Dari Skenario ke Alur Aktivitas*. Institut Teknologi Garut.
5. Fowler, M. *UML Distilled: A Brief Guide to the Standard Object Modeling Language*. Addison-Wesley.
6. draw.io. *An Introduction to UML Diagrams, Save a Diagram in Various Formats, dan Supported Export Formats*.