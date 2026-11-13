# LAPORAN PRAKTIKUM ADBO
## PERTEMUAN 4: USE CASE DIAGRAM LANJUTAN - GENERALIZATION DAN COLLABORATION

- **Nama:** Andika Rahman
- **NIM:** 2406044
- **Mata Kuliah:** Praktikum Analisis dan Desain Berorientasi Objek (ADBO)
- **Program Studi:** S1 Teknik Informatika (Semester 5)

---

## A. TUJUAN PRAKTIKUM

Berdasarkan Jobsheet Praktikum Pertemuan 4, tujuan dari praktikum ini adalah agar mahasiswa mampu:

1. Mengidentifikasi aktor umum dan aktor khusus berdasarkan skenario, kemudian menyusun hubungan generalization aktor dengan arah panah yang benar.
2. Menyusun generalization use case yang terdiri dari use case umum dan beberapa use case khusus serta menjelaskan perilaku yang diwariskan.
3. Menggunakan collaboration untuk menggambarkan realisasi suatu use case dan menghubungkannya menggunakan relasi realization.
4. Membuat Use Case Diagram kumulatif dengan mempertahankan seluruh elemen dari Pertemuan 3 serta menambahkan elemen baru pada Pertemuan 4.
5. Menyusun Use Case Description baru yang memuat pemicu, prasyarat, alur utama, alur alternatif, dan pascakondisi.
6. Menunjukkan keterlacakan elemen baru terhadap kebutuhan sistem serta melakukan pemeriksaan dan perbaikan model berdasarkan hasil review.

---

## B. DASAR TEORI

### 1. Pengertian Use Case Diagram Lanjutan

Use Case Diagram merupakan diagram UML yang digunakan untuk menggambarkan fungsi sistem dan hubungan antara aktor dengan sistem. Pada Pertemuan 4, materi ini dikembangkan dengan menambahkan konsep generalization dan collaboration.

Pertemuan 4 merupakan kelanjutan dari pemodelan pada Pertemuan 3. Oleh karena itu, diagram sebelumnya tidak dibuat ulang dari awal, melainkan dipertahankan dan ditambahkan elemen baru sesuai kebutuhan skenario. Pengembangan ini bertujuan agar model sistem menjadi lebih lengkap tanpa mengubah fungsi yang sudah ditentukan sebelumnya.

### 2. Generalization Aktor

Generalization aktor merupakan hubungan antara aktor umum dengan aktor khusus. Aktor khusus mewarisi seluruh hubungan atau fungsi yang dimiliki oleh aktor umum, sehingga tidak perlu menggambar ulang asosiasi yang sama.

Sebagai contoh, pada sistem peminjaman peralatan laboratorium terdapat aktor Peminjam sebagai aktor umum. Aktor Mahasiswa dan Dosen merupakan aktor khusus yang mewarisi fungsi dari Peminjam. Keduanya dapat melihat ketersediaan peralatan dan mengajukan peminjaman.

Arah panah generalization menggunakan garis utuh dengan ujung segitiga kosong yang mengarah kepada aktor umum. Apabila aktor khusus memiliki fungsi tambahan yang tidak dimiliki aktor lainnya, hubungan tersebut tetap digambarkan secara langsung dari aktor khusus.

### 3. Generalization Use Case

Generalization use case merupakan hubungan antara use case umum dengan use case khusus. Use case khusus mewarisi tujuan dan perilaku dasar dari use case umum, kemudian memiliki perilaku tambahan yang membedakannya.

Contohnya adalah Kelola Data Peralatan sebagai use case umum yang memiliki tiga bentuk khusus, yaitu Tambah Data Peralatan, Ubah Data Peralatan, dan Hapus Data Peralatan.

Ketiga use case tersebut mempunyai tujuan umum yang sama, yaitu mengelola data peralatan, tetapi masing-masing memiliki hasil yang berbeda. Tambah digunakan untuk menyimpan data baru, Ubah digunakan untuk memperbarui data, sedangkan Hapus digunakan untuk menghapus data sesuai ketentuan yang berlaku.

Arah panah generalization berasal dari use case khusus menuju use case umum dengan menggunakan garis utuh dan ujung segitiga kosong.

### 4. Collaboration

Collaboration merupakan elemen UML yang menggambarkan sekumpulan elemen dan peran yang bekerja sama untuk menyediakan suatu perilaku sistem. Collaboration menjelaskan bagaimana beberapa bagian di dalam sistem bekerja sama dalam mewujudkan fungsi tertentu.

Dalam diagram, collaboration digambarkan menggunakan bentuk elips dengan garis putus-putus. Nama collaboration harus sama persis dengan nama use case yang direalisasikannya.

Collaboration bukan merupakan use case tambahan dan tidak dihubungkan langsung dengan aktor. Pada praktikum ini, collaboration digunakan untuk menunjukkan realisasi dari use case utama yang telah ditentukan dalam skenario.

### 5. Relasi Realization

Realization merupakan hubungan yang menunjukkan bahwa suatu elemen mewujudkan atau merealisasikan elemen lainnya. Pada praktikum ini, collaboration berperan sebagai realisasi dari use case.

Relasi realization digambarkan menggunakan garis putus-putus dengan ujung segitiga kosong. Arah panah berasal dari collaboration menuju use case yang direalisasikan.

Sebagai contoh, collaboration Ajukan Peminjaman merealisasikan use case Ajukan Peminjaman. Keduanya memiliki nama yang sama, tetapi memiliki fungsi pemodelan yang berbeda.

### 6. Perbedaan Include, Extend, Generalization, dan Realization

Keempat relasi tersebut memiliki fungsi yang berbeda dalam pemodelan UML.

1. **Include**, menunjukkan perilaku suatu use case yang selalu disertakan dalam pelaksanaan use case lainnya.
2. **Extend**, menunjukkan perilaku tambahan yang dijalankan apabila kondisi tertentu terpenuhi.
3. **Generalization**, menunjukkan hubungan antara elemen khusus dengan elemen umum yang mewarisi perilakunya.
4. **Realization**, menunjukkan hubungan antara elemen yang merealisasikan dengan elemen yang direalisasikan.

Pemahaman terhadap perbedaan tersebut penting agar penggunaan relasi dalam diagram tidak tertukar dan tetap sesuai dengan tujuan pemodelan.

### 7. Use Case Description Lanjutan

Use Case Description merupakan dokumentasi yang menjelaskan proses pelaksanaan suatu fungsi sistem secara lebih terperinci. Pada Pertemuan 4, format Use Case Description masih menggunakan format dari Pertemuan 3, tetapi ditambahkan dua bagian baru, yaitu Generalization dan Collaboration.

Bagian yang terdapat dalam Use Case Description meliputi ID dan nama, sumber kebutuhan, tujuan, aktor utama, aktor pendukung, pemicu, prasyarat, alur utama, alur alternatif atau pengecualian, pascakondisi berhasil, pascakondisi gagal, aturan bisnis atau asumsi, generalization, dan collaboration.

---

## C. HASIL PRAKTIKUM

### 1. Studi Kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus

Pada latihan pertama, digunakan studi kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus. Studi kasus ini merupakan pengembangan dari model yang telah dibuat pada Pertemuan 3.

Pada Pertemuan 4, terdapat penambahan fungsi yang berkaitan dengan peminjaman oleh dosen, pengelolaan data peralatan, serta pencatatan pengembalian peralatan. Selain itu, digunakan konsep generalization untuk menggambarkan hubungan aktor dan use case yang memiliki fungsi umum.

Kebutuhan baru yang digunakan pada studi kasus LAB adalah:

| ID Kebutuhan | Kebutuhan Sistem |
|---|---|
| LAB-R07 | Mahasiswa dan Dosen sebagai Peminjam dapat melihat ketersediaan peralatan dan mengajukan peminjaman. |
| LAB-R08 | Petugas laboratorium dapat mengelola data peralatan dalam bentuk tambah, ubah, dan hapus. |
| LAB-R09 | Petugas laboratorium dapat mencatat pengembalian peralatan untuk peminjaman yang berstatus Dipinjam. |
| LAB-R10 | Sistem memeriksa dan mencatat kondisi peralatan sebagai bagian dari pencatatan pengembalian. |
| LAB-R11 | Model menunjukkan collaboration yang merealisasikan Ajukan Peminjaman dan Catat Pengembalian Peralatan. |

Kebutuhan LAB-R01 sampai LAB-R06 dari Pertemuan 3 tetap dipertahankan dan tidak diubah.

### 2. Generalization Aktor pada Kasus LAB

Pada studi kasus laboratorium, terdapat lima aktor yang digunakan dalam diagram kumulatif, yaitu:

| Aktor | Kedudukan | Tujuan terhadap Sistem |
|---|---|---|
| Peminjam | Aktor umum | Mewakili peran umum pengguna yang meminjam peralatan. |
| Mahasiswa | Aktor khusus | Melihat ketersediaan, mengajukan peminjaman, dan mencetak bukti pengajuan. |
| Dosen | Aktor khusus | Melihat ketersediaan dan mengajukan peminjaman. |
| Petugas Laboratorium | Aktor tetap | Mengelola data peralatan, memproses keputusan, dan mencatat pengembalian. |
| Kepala Laboratorium | Aktor tetap | Melihat laporan peminjaman. |

Aktor Peminjam menjadi aktor umum bagi Mahasiswa dan Dosen karena keduanya mempunyai fungsi yang sama, yaitu melihat ketersediaan peralatan dan mengajukan peminjaman.

Dengan menggunakan generalization, hubungan terhadap fungsi tersebut cukup digambarkan satu kali dari aktor Peminjam. Mahasiswa tetap memiliki hubungan langsung dengan fungsi Cetak Bukti Pengajuan karena fungsi tersebut hanya dilakukan oleh mahasiswa.

### 3. Generalization Use Case pada Kasus LAB

Pada bagian pengelolaan data peralatan, terdapat satu use case umum dan tiga use case khusus.

| ID Use Case | Nama Use Case | Kedudukan |
|---|---|---|
| LAB-UC02 | Kelola Data Peralatan | Use case umum |
| LAB-UC08 | Tambah Data Peralatan | Use case khusus |
| LAB-UC09 | Ubah Data Peralatan | Use case khusus |
| LAB-UC10 | Hapus Data Peralatan | Use case khusus |

Ketiga use case khusus tersebut merupakan bentuk pengembangan dari Kelola Data Peralatan. Masing-masing mempunyai perilaku yang berbeda, yaitu menambahkan data baru, memperbarui data yang sudah tersedia, dan menghapus data peralatan yang memenuhi ketentuan.

Pada hubungan ini, arah panah generalization berasal dari LAB-UC08, LAB-UC09, dan LAB-UC10 menuju LAB-UC02 sebagai use case umum.

### 4. Penambahan Use Case Pengembalian Peralatan

Selain pengelolaan data peralatan, terdapat penambahan proses pencatatan pengembalian peralatan.

| ID Use Case | Nama Use Case | Peran dalam Model |
|---|---|---|
| LAB-UC11 | Catat Pengembalian Peralatan | Fungsi utama petugas laboratorium. |
| LAB-UC12 | Periksa Kondisi Peralatan | Perilaku yang disertakan dalam pencatatan pengembalian. |

LAB-UC11 digunakan untuk mencatat pengembalian peralatan yang sebelumnya telah dipinjam. Dalam proses tersebut, sistem juga menjalankan LAB-UC12 untuk memeriksa dan mencatat kondisi peralatan.

Oleh karena itu, hubungan antara LAB-UC11 Catat Pengembalian Peralatan dengan LAB-UC12 Periksa Kondisi Peralatan menggunakan relasi `<<include>>`.

### 5. Collaboration dan Realization pada Kasus LAB

Pada studi kasus laboratorium, terdapat dua collaboration yang digunakan untuk menunjukkan realisasi dari use case utama.

| ID Collaboration | Nama Collaboration | Use Case yang Direalisasikan |
|---|---|---|
| LAB-CO01 | Ajukan Peminjaman | LAB-UC03 Ajukan Peminjaman |
| LAB-CO02 | Catat Pengembalian Peralatan | LAB-UC11 Catat Pengembalian Peralatan |

Collaboration LAB-CO01 merealisasikan proses Ajukan Peminjaman, sedangkan LAB-CO02 merealisasikan proses Catat Pengembalian Peralatan.

Kedua collaboration digambarkan menggunakan elips bergaris putus-putus dan dihubungkan dengan use case menggunakan relasi realization. Arah panah realization berasal dari collaboration menuju use case yang direalisasikan.

### 6. Penyusunan Use Case Description LAB-UC11

Salah satu dokumentasi baru yang disusun pada Pertemuan 4 adalah Use Case Description LAB-UC11 Catat Pengembalian Peralatan.

Informasi utama dari use case tersebut adalah:

| Elemen | Keterangan |
|---|---|
| ID dan Nama | LAB-UC11 Catat Pengembalian Peralatan |
| Sumber Kebutuhan | LAB-R09 dan LAB-R10 |
| Tujuan | Pengembalian tercatat dan status peminjaman serta kondisi peralatan terbarui. |
| Aktor Utama | Petugas Laboratorium |
| Pemicu | Petugas memilih fungsi pencatatan pengembalian dan menentukan peminjaman yang akan dikembalikan. |
| Prasyarat | Petugas telah terautentikasi dan peminjaman terpilih berstatus Dipinjam. |
| Pascakondisi Berhasil | Pengembalian tercatat dengan tanggal kembali dan kondisi peralatan; status peminjaman menjadi Selesai. |
| Pascakondisi Gagal | Tidak ada pengembalian baru yang tercatat dan status peminjaman tidak berubah. |
| Include | LAB-UC12 Periksa Kondisi Peralatan |
| Collaboration | LAB-CO02 Catat Pengembalian Peralatan |

Alur utama dimulai ketika petugas memilih peminjaman yang akan dikembalikan. Sistem kemudian menampilkan data peminjaman dan statusnya. Petugas mengonfirmasi alat serta jumlah yang dikembalikan. Selanjutnya, sistem memeriksa apakah status peminjaman masih Dipinjam dan menjalankan proses pemeriksaan kondisi peralatan.

Setelah seluruh pemeriksaan terpenuhi, sistem menyimpan tanggal pengembalian dan kondisi peralatan, kemudian mengubah status peminjaman menjadi Selesai. Sistem selanjutnya menampilkan ringkasan pengembalian sebagai konfirmasi kepada petugas.

Pada alur alternatif, apabila status peminjaman bukan Dipinjam, sistem menolak pencatatan pengembalian. Jika kondisi peralatan Rusak Ringan atau Rusak Berat, sistem tetap mencatat pengembalian dan menandai kondisi tersebut pada data peralatan. Apabila jumlah alat yang dikembalikan tidak sesuai, sistem meminta petugas memeriksa kembali data sebelum penyimpanan dilakukan.

### 7. Tugas Sistem Informasi Akademik (SIA), Layanan Hasil Studi

Pada tugas kedua, digunakan studi kasus Sistem Informasi Akademik dengan fokus pada layanan hasil studi. Tugas ini berbeda dari Pertemuan 2 yang membahas jadwal kuliah dan Pertemuan 3 yang membahas pengajuan KRS.

Skenario pada Pertemuan 4 membahas Mahasiswa dan Dosen yang termasuk dalam kelompok Civitas Akademika dan dapat melihat kalender akademik. Dosen dapat menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa dapat melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya telah dipublikasikan. Sementara itu, Admin Akademik bertugas mengelola data mahasiswa.

Kebutuhan baru pada tugas SIA adalah:

| ID Kebutuhan | Kebutuhan Sistem |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen sebagai Civitas Akademika dapat melihat kalender akademik. |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya. |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan. |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus, yaitu tambah, ubah, dan hapus data mahasiswa. |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |

Kebutuhan SIA-R01 sampai SIA-R06 dari pertemuan sebelumnya tetap dipertahankan. Dengan demikian, diagram SIA pada Pertemuan 4 merupakan diagram kumulatif yang mencakup fungsi jadwal kuliah, pengajuan KRS, dan layanan hasil studi.

### 8. Generalization Aktor pada Tugas SIA

Pada tugas SIA, terdapat aktor umum Civitas Akademika yang memiliki dua aktor khusus, yaitu Mahasiswa dan Dosen.

| Aktor | Kedudukan | Tujuan terhadap Sistem |
|---|---|---|
| Civitas Akademika | Aktor umum | Melihat kalender akademik. |
| Mahasiswa | Aktor khusus | Melihat kalender akademik dan KHS. |
| Dosen | Aktor khusus | Melihat kalender akademik dan menginput nilai mata kuliah yang diampunya. |
| Admin Akademik | Aktor tetap | Mengelola data mahasiswa. |
| Dosen Wali | Aktor tetap | Memproses keputusan KRS sesuai fungsi dari pertemuan sebelumnya. |

Mahasiswa dan Dosen mewarisi fungsi melihat kalender akademik dari aktor umum Civitas Akademika. Oleh karena itu, asosiasi terhadap fungsi tersebut cukup digambarkan satu kali dari Civitas Akademika.

Sementara itu, fungsi melihat KHS tetap menjadi fungsi khusus Mahasiswa dan fungsi menginput nilai mata kuliah menjadi fungsi khusus Dosen.

### 9. Generalization Use Case pada Tugas SIA

Pada pengelolaan data mahasiswa, terdapat satu use case umum dan tiga use case khusus.

| ID Use Case | Nama Use Case | Kedudukan |
|---|---|---|
| SIA-UC10 | Kelola Data Mahasiswa | Use case umum |
| SIA-UC11 | Tambah Data Mahasiswa | Use case khusus |
| SIA-UC12 | Ubah Data Mahasiswa | Use case khusus |
| SIA-UC13 | Hapus Data Mahasiswa | Use case khusus |

Ketiga use case khusus tersebut merupakan bentuk pengembangan dari Kelola Data Mahasiswa. Tambah Data Mahasiswa digunakan untuk memasukkan data mahasiswa baru, Ubah Data Mahasiswa digunakan untuk memperbarui data yang tersedia, sedangkan Hapus Data Mahasiswa digunakan untuk menghapus data mahasiswa sesuai ketentuan yang telah ditentukan.

Hubungan generalization digambarkan dari masing-masing use case khusus menuju SIA-UC10 Kelola Data Mahasiswa sebagai use case umum.

### 10. Collaboration dan Realization pada Tugas SIA

Pada tugas SIA, terdapat dua collaboration yang digunakan untuk menunjukkan realisasi dari fungsi utama layanan hasil studi.

| ID Collaboration | Nama Collaboration | Use Case yang Direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09 Lihat KHS |

Collaboration Input Nilai Mata Kuliah digunakan untuk merealisasikan fungsi dosen dalam memasukkan nilai mata kuliah yang diampunya. Sementara itu, collaboration Lihat KHS digunakan untuk merealisasikan fungsi mahasiswa dalam melihat hasil studi.

Kedua collaboration dihubungkan dengan use case masing-masing menggunakan relasi realization. Nama collaboration dibuat sama persis dengan nama use case yang direalisasikannya.

### 11. Use Case Description pada Tugas SIA

Pada tugas SIA, dokumentasi use case dibuat untuk Input Nilai Mata Kuliah dan Lihat KHS.

**Input Nilai Mata Kuliah**

Use case ini menjelaskan proses dosen dalam memasukkan nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Prasyaratnya adalah dosen telah terautentikasi dan merupakan dosen pengampu mata kuliah tersebut.

Apabila dosen memasukkan nilai yang berada di luar rentang nilai yang sah, sistem harus menolak data tersebut. Jika nilai berhasil dimasukkan sesuai ketentuan, sistem menyimpan nilai sebagai data yang belum dipublikasikan sampai dinyatakan resmi sesuai aturan tugas.

Collaboration yang merealisasikan use case ini adalah SIA-CO01 Input Nilai Mata Kuliah.

**Lihat KHS**

Use case ini menjelaskan proses mahasiswa dalam melihat Kartu Hasil Studi untuk semester yang telah dipublikasikan nilainya. Sistem hanya menampilkan nilai yang sudah dipublikasikan sehingga nilai yang belum resmi tidak ditampilkan pada KHS.

Collaboration yang merealisasikan use case ini adalah SIA-CO02 Lihat KHS.

### 12. Pengujian Konsistensi Model SIA

Setelah diagram dan deskripsi disusun, dilakukan pemeriksaan terhadap tiga kondisi yang ditentukan dalam jobsheet.

| No. | Kondisi Pengujian | Hasil yang Diharapkan |
|---|---|---|
| 1 | Mahasiswa melihat kalender akademik tanpa asosiasi langsung dari Mahasiswa. | Tetap diperbolehkan karena Mahasiswa mewarisi fungsi dari Civitas Akademika. |
| 2 | Dosen yang bukan pengampu mencoba menginput nilai. | Sistem menolak proses karena dosen tersebut tidak memenuhi prasyarat sebagai pengampu mata kuliah. |
| 3 | Admin Akademik menghapus data mahasiswa yang masih memiliki data akademik aktif. | Penghapusan ditolak karena tidak sesuai dengan aturan tugas. |

Ketiga kondisi tersebut digunakan untuk memeriksa kesesuaian antara hubungan generalization, hak akses aktor, aturan sistem, dan Use Case Description.

### 13. Pemeriksaan dan Dokumentasi Artefak

Pada tahap akhir, diagram kumulatif LAB dan SIA diperiksa berdasarkan kesesuaian antara kebutuhan, katalog use case, hubungan generalization, collaboration, realization, serta deskripsi use case.

Berkas diagram disimpan menggunakan format `.drawio` sebagai sumber yang dapat diedit kembali dan format `.png` sebagai hasil ekspor. Penamaan berkas mengikuti pola P04 dengan identitas NIM dan kasus yang digunakan.

Berkas P03 tetap dipertahankan dan tidak ditimpa. Apabila terdapat perubahan setelah proses review, perubahan disimpan menggunakan versi berikutnya, yaitu v02, serta dicatat pada metadata dan logbook.

---

## D. ANALISIS

Berdasarkan materi dan kegiatan praktikum Pertemuan 4, penggunaan generalization membantu menyederhanakan diagram dengan mengelompokkan aktor atau use case yang mempunyai fungsi umum. Pada studi kasus laboratorium, Mahasiswa dan Dosen memiliki fungsi yang sama dalam melihat ketersediaan peralatan dan mengajukan peminjaman. Oleh karena itu, keduanya dapat dihubungkan melalui aktor umum Peminjam. Dengan cara tersebut, asosiasi yang sama tidak perlu digambarkan berulang kali sehingga diagram menjadi lebih sederhana dan mudah dipahami.

Generalization juga diterapkan pada pengelolaan data peralatan. Fungsi Kelola Data Peralatan menjadi use case umum yang memiliki tiga fungsi khusus, yaitu Tambah Data Peralatan, Ubah Data Peralatan, dan Hapus Data Peralatan. Ketiga fungsi tersebut memiliki tujuan umum yang sama, tetapi menghasilkan tindakan yang berbeda. Hal ini menunjukkan bahwa generalization dapat digunakan untuk menggambarkan hubungan antara fungsi umum dan bentuk pelaksanaannya yang lebih khusus.

Selain generalization, penggunaan collaboration dan realization memberikan pemahaman mengenai hubungan antara fungsi yang terlihat oleh aktor dengan elemen yang bekerja sama untuk mewujudkan fungsi tersebut. Pada kasus laboratorium, collaboration digunakan untuk merealisasikan Ajukan Peminjaman dan Catat Pengembalian Peralatan. Sementara itu, pada tugas SIA, collaboration digunakan untuk merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. Arah realization harus berasal dari collaboration menuju use case, sehingga tidak tertukar dengan relasi include maupun extend.

Pada tugas Sistem Informasi Akademik, generalization aktor Civitas Akademika menunjukkan bahwa Mahasiswa dan Dosen memiliki fungsi bersama dalam melihat kalender akademik. Selain itu, pengelolaan data mahasiswa menggunakan generalization use case karena terdapat fungsi umum yang memiliki tiga bentuk khusus. Pengujian terhadap dosen yang bukan pengampu dan penghapusan data mahasiswa yang masih memiliki data akademik aktif juga menunjukkan pentingnya memperhatikan prasyarat dan aturan bisnis dalam penyusunan deskripsi use case.

Secara keseluruhan, praktikum Pertemuan 4 memperlihatkan bahwa pengembangan diagram harus dilakukan secara bertahap dan konsisten dengan model sebelumnya. Elemen yang sudah dibuat pada Pertemuan 3 tetap dipertahankan, sedangkan elemen baru ditambahkan berdasarkan kebutuhan yang tersedia. Dengan demikian, diagram kumulatif dapat menggambarkan sistem secara lebih lengkap tanpa mengubah arti kebutuhan yang telah ditentukan sebelumnya.

---

## E. KESIMPULAN

Berdasarkan praktikum Analisis dan Desain Berorientasi Objek pada Pertemuan 4, dapat disimpulkan bahwa generalization dan collaboration merupakan konsep penting dalam pengembangan Use Case Diagram lanjutan. Generalization digunakan untuk menunjukkan hubungan antara aktor atau use case umum dengan elemen khusus yang mewarisi fungsi atau perilaku dasarnya.

Selain itu, collaboration dan realization digunakan untuk menggambarkan bagaimana suatu use case direalisasikan oleh sekumpulan elemen yang bekerja sama. Penggunaan kedua konsep tersebut harus memperhatikan arah panah, bentuk notasi, serta kesesuaian nama antara collaboration dengan use case yang direalisasikannya.

Praktikum ini juga memberikan pemahaman mengenai pentingnya mempertahankan konsistensi diagram dari pertemuan sebelumnya. Diagram P04 harus memuat seluruh fungsi lama dan penambahan fungsi baru sesuai kebutuhan sistem. Dengan adanya dokumentasi kebutuhan, katalog use case, Use Case Description, serta pemeriksaan hasil model, proses analisis sistem dapat dilakukan secara lebih terstruktur dan mudah ditelusuri.

---

## F. REFERENSI

1. Institut Teknologi Garut. (2026). Jobsheet Praktikum Analisis dan Desain Berorientasi Objek (ADBO) Pertemuan 4: Use Case Diagram Lanjutan - Generalization dan Collaboration.
2. Object Management Group. (2017). *OMG Unified Modeling Language (UML), Version 2.5.1*.
3. Tegarden, D. P., Samuel, B., Lukyanenko, R., Dennis, A., dan Wixom, B. H. *Systems Analysis and Design: An Object-Oriented Approach with UML*. Wiley.
4. Fowler, M. *UML Distilled: A Brief Guide to the Standard Object Modeling Language*. Addison-Wesley.
5. Dokumentasi draw.io. *An Introduction to UML Diagrams, Save a Diagram in Various Formats, dan Supported Export Formats*.
6. Repository Praktikum ADBO: https://github.com/andika282006/IFRWP5149_2406044_LabAlat