# LAPORAN PRAKTIKUM ADBO
## PERTEMUAN 3: USE CASE DIAGRAM DAN USE CASE DESCRIPTION

- **Nama:** Andika Rahman
- **NIM:** 2406044
- **Mata Kuliah:** Praktikum Analisis dan Desain Berorientasi Objek (ADBO)
- **Program Studi:** S1 Teknik Informatika (Semester 5)

---

## A. TUJUAN PRAKTIKUM

Berdasarkan Jobsheet Praktikum Pertemuan 3, tujuan dari praktikum ini adalah agar mahasiswa mampu:

1. Menuliskan batas sistem, aktor, kebutuhan, aturan bisnis, dan asumsi dari skenario yang diberikan.
2. Menentukan use case berdasarkan tujuan aktor, bukan berdasarkan nama tombol, tabel, atau langkah teknis.
3. Membuat Use Case Diagram yang konsisten dengan daftar kebutuhan dan hubungan aktor–fungsi.
4. Menyusun Use Case Description yang memuat pemicu, prasyarat, alur utama, alur alternatif atau pengecualian, dan pascakondisi.
5. Menunjukkan keterlacakan setiap use case ke kebutuhan yang mendasarinya.
6. Memperbaiki model berdasarkan review dan mendokumentasikan perubahan pada versi berikutnya.

---

## B. DASAR TEORI

### 1. Pengertian Use Case Diagram

Use Case Diagram merupakan salah satu diagram dalam UML yang digunakan untuk menggambarkan fungsi-fungsi suatu sistem serta interaksi antara sistem dengan pihak luar. Diagram ini membantu menjelaskan layanan apa saja yang disediakan oleh sistem dan siapa saja aktor yang dapat menggunakan layanan tersebut.

Use Case Diagram memberikan gambaran umum mengenai hubungan antara aktor dan fungsi sistem. Diagram ini tidak menjelaskan secara terperinci urutan tindakan atau respons sistem, melainkan menunjukkan fungsi yang tersedia dan hubungan interaksinya.

### 2. Komponen Use Case Diagram

Terdapat beberapa komponen yang digunakan dalam pembuatan Use Case Diagram, yaitu:

1. **Actor**, merupakan orang, sistem, atau proses yang berinteraksi dengan sistem yang sedang dikembangkan.
2. **Use Case**, merupakan fungsi atau layanan yang disediakan oleh sistem untuk mencapai tujuan tertentu.
3. **Association**, merupakan hubungan yang menunjukkan interaksi antara aktor dengan use case.
4. **System Boundary**, merupakan batas yang menunjukkan ruang lingkup sistem yang sedang dibahas.
5. **Collaboration**, merupakan kerja sama beberapa elemen untuk menghasilkan perilaku yang lebih besar.
6. **Include**, merupakan hubungan yang menunjukkan bahwa suatu use case menyertakan perilaku dari use case lainnya.
7. **Extend**, merupakan hubungan yang menambahkan perilaku tertentu pada use case dasar berdasarkan kondisi tertentu.
8. **Generalization**, merupakan hubungan antara elemen umum dengan elemen khusus.

### 3. Relasi Include

Relasi `<<include>>` digunakan ketika suatu use case membutuhkan perilaku dari use case lain sebagai bagian dari pelaksanaannya. Arah panah berasal dari use case yang menyertakan menuju use case yang disertakan.

Pada studi kasus laboratorium, proses Ajukan Peminjaman selalu menjalankan pemeriksaan ketersediaan peralatan. Oleh karena itu, hubungan antara LAB-UC03 Ajukan Peminjaman dengan LAB-UC04 Periksa Ketersediaan menggunakan relasi `<<include>>`.

### 4. Relasi Extend

Relasi `<<extend>>` digunakan untuk menggambarkan perilaku tambahan yang hanya dijalankan apabila kondisi tertentu terpenuhi. Use case dasar tetap dapat berjalan meskipun perilaku tambahan tersebut tidak dilakukan.

Pada studi kasus laboratorium, Cetak Bukti Pengajuan menjadi perilaku tambahan ketika mahasiswa memilih untuk mencetak bukti pada halaman konfirmasi. Dengan demikian, LAB-UC05 Cetak Bukti Pengajuan menggunakan relasi `<<extend>>` terhadap LAB-UC03 Ajukan Peminjaman.

### 5. Use Case Description

Use Case Description merupakan dokumentasi yang menjelaskan secara terperinci bagaimana suatu fungsi sistem dijalankan melalui interaksi antara aktor dengan sistem. Dokumentasi ini digunakan untuk menjelaskan proses yang tidak dapat ditampilkan secara lengkap hanya melalui diagram.

Bagian-bagian yang terdapat dalam Use Case Description meliputi:

1. **ID dan Nama**, sebagai identitas use case yang sesuai dengan diagram.
2. **Sumber Kebutuhan**, menunjukkan kebutuhan yang mendasari fungsi tersebut.
3. **Tujuan**, menjelaskan hasil yang ingin dicapai oleh aktor.
4. **Aktor Utama**, merupakan pihak yang memulai proses untuk mencapai tujuan.
5. **Aktor Pendukung**, merupakan pihak lain yang ikut berinteraksi jika ada.
6. **Pemicu**, menjelaskan kejadian yang memulai proses.
7. **Prasyarat**, merupakan kondisi yang harus terpenuhi sebelum proses dimulai.
8. **Alur Utama**, menjelaskan langkah-langkah ketika proses berjalan dengan normal.
9. **Alur Alternatif atau Pengecualian**, menjelaskan kondisi lain atau kegagalan yang mungkin terjadi.
10. **Pascakondisi**, menjelaskan keadaan sistem setelah proses berhasil atau gagal.
11. **Aturan Bisnis dan Asumsi**, menjelaskan ketentuan yang memengaruhi jalannya proses.

---

## C. HASIL PRAKTIKUM

### 1. Studi Kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus

Pada latihan pertama, digunakan studi kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus. Sistem ini menggambarkan proses pengelolaan informasi peralatan, pengajuan peminjaman, pemeriksaan ketersediaan, keputusan peminjaman, serta laporan peminjaman.

Berdasarkan skenario yang diberikan, terdapat enam kebutuhan utama yang digunakan sebagai dasar pembuatan model, yaitu:

| ID Kebutuhan | Kebutuhan Sistem |
|---|---|
| LAB-R01 | Mahasiswa dapat melihat ketersediaan peralatan. |
| LAB-R02 | Petugas dapat mengelola data peralatan. |
| LAB-R03 | Mahasiswa dapat mengajukan peminjaman dan sistem memeriksa ketersediaan sebelum menyimpan pengajuan. |
| LAB-R04 | Mahasiswa dapat mencetak bukti pada konfirmasi pengajuan jika memilihnya. |
| LAB-R05 | Petugas dapat menetapkan persetujuan atau penolakan pengajuan. |
| LAB-R06 | Kepala laboratorium dapat melihat laporan peminjaman. |

Berdasarkan kebutuhan tersebut, terdapat tiga aktor yang berinteraksi dengan sistem, yaitu:

| Aktor | Tujuan terhadap Sistem |
|---|---|
| Mahasiswa | Melihat ketersediaan, mengajukan peminjaman, dan mencetak bukti. |
| Petugas Laboratorium | Mengelola peralatan dan memproses keputusan peminjaman. |
| Kepala Laboratorium | Melihat laporan peminjaman. |

Selanjutnya, kebutuhan tersebut diterjemahkan menjadi tujuh use case sebagai berikut:

| ID Use Case | Nama Use Case |
|---|---|
| LAB-UC01 | Lihat Ketersediaan Peralatan |
| LAB-UC02 | Kelola Data Peralatan |
| LAB-UC03 | Ajukan Peminjaman |
| LAB-UC04 | Periksa Ketersediaan |
| LAB-UC05 | Cetak Bukti Pengajuan |
| LAB-UC06 | Proses Keputusan Peminjaman |
| LAB-UC07 | Lihat Laporan Peminjaman |

### 2. Penentuan Relasi Include dan Extend pada Kasus LAB

Dalam proses pemodelan, terdapat dua hubungan utama yang digunakan untuk menjelaskan keterkaitan antaruse case.

**Relasi Include**

LAB-UC03 Ajukan Peminjaman memiliki hubungan `<<include>>` dengan LAB-UC04 Periksa Ketersediaan. Hubungan ini digunakan karena pemeriksaan ketersediaan merupakan bagian dari proses validasi pengajuan dan harus dilakukan sebelum pengajuan disimpan.

**Relasi Extend**

LAB-UC05 Cetak Bukti Pengajuan memiliki hubungan `<<extend>>` dengan LAB-UC03 Ajukan Peminjaman. Hubungan ini digunakan karena pencetakan bukti hanya dilakukan apabila mahasiswa memilih untuk mencetaknya pada halaman konfirmasi. Pengajuan tetap dapat berhasil meskipun mahasiswa tidak mencetak bukti.

Pada relasi extend terdapat ketentuan sebagai berikut:

- **Use Case Dasar:** LAB-UC03 Ajukan Peminjaman.
- **Use Case Tambahan:** LAB-UC05 Cetak Bukti Pengajuan.
- **Extension Point:** Bukti pengajuan tersedia.
- **Kondisi:** Mahasiswa memilih cetak.

### 3. Penyusunan Use Case Description LAB-UC03

Salah satu use case yang dijelaskan dalam jobsheet adalah LAB-UC03 Ajukan Peminjaman. Use case ini bertujuan menghasilkan pengajuan peminjaman yang tersimpan di dalam sistem.

Informasi utama use case tersebut adalah:

| Elemen | Keterangan |
|---|---|
| ID dan Nama | LAB-UC03 Ajukan Peminjaman |
| Tujuan | Menghasilkan pengajuan peminjaman yang tersimpan. |
| Aktor Utama | Mahasiswa |
| Sumber Kebutuhan | LAB-R03 dan LAB-R04 |
| Pemicu | Mahasiswa memilih fungsi pengajuan peminjaman. |
| Prasyarat | Mahasiswa telah terautentikasi dan data peralatan tersedia. |
| Pascakondisi Berhasil | Pengajuan tersimpan dengan nomor dan status Menunggu Keputusan. |
| Pascakondisi Gagal | Tidak ada pengajuan baru yang berhasil tersimpan. |
| Include | LAB-UC04 Periksa Ketersediaan. |
| Extend | LAB-UC05 Cetak Bukti Pengajuan. |

Alur utama dimulai ketika mahasiswa membuka halaman pengajuan, kemudian memilih peralatan, jumlah, rentang waktu, dan tujuan peminjaman. Setelah mahasiswa mengirim pengajuan, sistem memeriksa kelengkapan data dan menjalankan proses pemeriksaan ketersediaan. Jika peralatan tersedia, sistem menyimpan pengajuan dan memberikan nomor pengajuan. Selanjutnya, sistem menampilkan halaman konfirmasi yang berisi nomor dan status pengajuan.

Apabila mahasiswa memilih untuk mencetak bukti, sistem menjalankan perilaku tambahan berupa pencetakan bukti pengajuan. Namun, apabila mahasiswa tidak memilih pencetakan, pengajuan tetap dianggap berhasil selama seluruh proses validasi terpenuhi.

### 4. Tugas Sistem Informasi Akademik (SIA)

Pada latihan kedua, digunakan studi kasus Sistem Informasi Akademik dengan fokus pada proses pengajuan Kartu Rencana Studi (KRS). Mahasiswa dapat memilih mata kuliah dan mengajukan KRS melalui sistem. Sistem kemudian melakukan validasi terhadap kelengkapan, prasyarat mata kuliah, dan benturan jadwal.

Apabila validasi berhasil, sistem menyimpan pengajuan dengan status Menunggu Persetujuan Dosen Wali. Pada halaman konfirmasi, mahasiswa dapat memilih untuk mengunduh bukti pengajuan. Selanjutnya, dosen wali dapat menyetujui atau menolak KRS serta memberikan catatan keputusan.

Kebutuhan yang digunakan dalam tugas SIA adalah:

| ID Kebutuhan | Kebutuhan Sistem |
|---|---|
| SIA-R01 | Mahasiswa dapat melihat jadwal kuliah. |
| SIA-R02 | Admin akademik dapat mengelola jadwal kuliah. |
| SIA-R03 | Mahasiswa dapat mengajukan KRS. |
| SIA-R04 | Sistem memvalidasi KRS sebagai bagian dari pengajuan. |
| SIA-R05 | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan. |
| SIA-R06 | Dosen wali dapat memproses persetujuan atau penolakan KRS. |

Pada tugas ini, kebutuhan SIA-R01 dan SIA-R02 tetap mempertahankan identitas dari Pertemuan 2. Sementara itu, kebutuhan SIA-R03 sampai SIA-R06 digunakan untuk menambahkan fungsi pengajuan KRS.

### 5. Penyusunan Use Case Description SIA

Berdasarkan skenario tugas, terdapat empat use case yang perlu dibuatkan deskripsi, yaitu:

1. **Ajukan KRS**, menjelaskan proses mahasiswa memilih mata kuliah dan mengirim pengajuan KRS.
2. **Validasi KRS**, menjelaskan proses pemeriksaan kelengkapan, prasyarat mata kuliah, dan benturan jadwal.
3. **Unduh Bukti Pengajuan KRS**, menjelaskan proses pengunduhan bukti apabila mahasiswa memilihnya pada halaman konfirmasi.
4. **Proses Keputusan KRS**, menjelaskan proses dosen wali memberikan persetujuan atau penolakan terhadap pengajuan KRS.

Dalam proses pengajuan KRS, validasi merupakan bagian yang harus dijalankan. Oleh karena itu, hubungan antara Ajukan KRS dengan Validasi KRS menggunakan `<<include>>`. Sementara itu, Unduh Bukti Pengajuan KRS merupakan perilaku tambahan yang tidak menentukan keberhasilan pengajuan sehingga menggunakan relasi `<<extend>>`.

### 6. Pengujian Konsistensi Model SIA

Setelah diagram dan deskripsi use case disusun, dilakukan pemeriksaan terhadap tiga kondisi yang ditentukan dalam jobsheet.

| No. | Kondisi Pengujian | Hasil yang Diharapkan |
|---|---|---|
| 1 | Validasi berhasil dan mahasiswa tidak mengunduh bukti. | Pengajuan KRS tetap tersimpan dengan status Menunggu Persetujuan Dosen Wali. |
| 2 | Validasi gagal. | Pengajuan belum berhasil tersimpan. |
| 3 | Validasi berhasil dan mahasiswa memilih mengunduh bukti. | Pengajuan tersimpan dan mahasiswa dapat mengunduh bukti pengajuan. |

Ketiga kondisi tersebut digunakan untuk memastikan bahwa hubungan include dan extend sudah sesuai dengan perilaku sistem yang dijelaskan dalam skenario dan Use Case Description.

### 7. Pemeriksaan dan Dokumentasi Artefak

Setelah diagram dan deskripsi use case dibuat, dilakukan pemeriksaan terhadap kesesuaian antara kebutuhan, katalog use case, diagram, dan deskripsi. Pemeriksaan juga mencakup arah panah include dan extend, penempatan extension point, kondisi tambahan, serta pascakondisi ketika proses berhasil maupun gagal.

Berkas sumber diagram disimpan menggunakan format `.drawio`, sedangkan hasil ekspor disimpan dalam format `.png`. Penamaan berkas mengikuti pola `P03_<NIM>_<KASUS>_<ARTEFAK>_v<NN>` agar hasil praktikum LAB dan SIA dapat dibedakan. Apabila terdapat perubahan setelah review, versi berikutnya digunakan tanpa menimpa berkas sebelumnya.

---

## D. ANALISIS

Berdasarkan praktikum yang dilakukan, Use Case Diagram memiliki peran penting dalam menggambarkan fungsi-fungsi yang tersedia di dalam suatu sistem serta hubungan antara aktor dengan fungsi tersebut. Pada studi kasus laboratorium, terdapat tiga aktor yang memiliki tujuan berbeda, yaitu Mahasiswa, Petugas Laboratorium, dan Kepala Laboratorium. Setiap aktor dihubungkan dengan use case sesuai kebutuhan yang telah ditentukan sehingga fungsi sistem dapat digambarkan secara lebih terstruktur.

Penggunaan relasi include dan extend menjadi salah satu bagian penting dalam pemodelan. Relasi include digunakan pada proses pengajuan peminjaman karena pemeriksaan ketersediaan harus selalu dilakukan sebelum pengajuan disimpan. Sementara itu, relasi extend digunakan pada pencetakan bukti karena aktivitas tersebut hanya dilakukan jika mahasiswa memilihnya. Dari kedua relasi tersebut dapat dipahami bahwa include menggambarkan perilaku yang menjadi bagian dari proses utama, sedangkan extend menggambarkan perilaku tambahan yang bersifat bersyarat.

Pada tugas Sistem Informasi Akademik, proses pengajuan KRS memiliki beberapa kondisi yang harus diperhatikan, terutama ketika validasi berhasil, validasi gagal, maupun ketika mahasiswa memilih mengunduh bukti pengajuan. Hasil pengujian terhadap ketiga kondisi tersebut membantu memastikan bahwa diagram dan Use Case Description memberikan gambaran yang konsisten. Selain itu, status KRS yang tersimpan tetap Menunggu Persetujuan Dosen Wali dan tidak secara otomatis dianggap telah disetujui.

Melalui praktikum ini juga dapat dipahami bahwa Use Case Diagram dan Use Case Description memiliki fungsi yang saling melengkapi. Diagram memberikan gambaran hubungan aktor dengan fungsi sistem, sedangkan deskripsi menjelaskan proses, respons sistem, kondisi alternatif, serta hasil akhir dari setiap fungsi. Oleh karena itu, keduanya harus memiliki nama, ID, dan kebutuhan yang konsisten agar model yang dihasilkan mudah dipahami dan dapat diperiksa kembali.

---

## E. KESIMPULAN

Berdasarkan praktikum Analisis dan Desain Berorientasi Objek pada Pertemuan 3, dapat disimpulkan bahwa Use Case Diagram digunakan untuk menggambarkan fungsi sistem dan hubungan interaksi antara aktor dengan sistem. Dalam pembuatannya, setiap aktor dan use case harus disesuaikan dengan kebutuhan serta tujuan yang terdapat pada skenario.

Praktikum ini memberikan pemahaman mengenai penggunaan relasi include dan extend dalam menggambarkan hubungan antaruse case. Include digunakan untuk menunjukkan perilaku yang menjadi bagian dari proses utama, sedangkan extend digunakan untuk menunjukkan perilaku tambahan yang dijalankan berdasarkan kondisi tertentu. Selain itu, Use Case Description digunakan untuk menjelaskan proses secara lebih terperinci melalui pemicu, prasyarat, alur utama, alur alternatif, dan pascakondisi.

Dengan adanya praktikum ini, mahasiswa dapat memahami bahwa pemodelan sistem tidak hanya dilakukan melalui diagram, tetapi juga membutuhkan dokumentasi yang jelas dan konsisten. Kesesuaian antara kebutuhan, diagram, deskripsi, serta hasil pemeriksaan menjadi hal penting agar model sistem dapat dipahami dan dikembangkan dengan lebih baik.

---

## F. REFERENSI

1. Institut Teknologi Garut. (2026). Jobsheet Praktikum Analisis dan Desain Berorientasi Objek (ADBO) Pertemuan 3: Use Case Diagram dan Use Case Description.
2. Object Management Group. (2017). *OMG Unified Modeling Language (UML), Version 2.5.1*.
3. Dokumentasi draw.io. *An Introduction to UML Diagrams, Save a Diagram in Various Formats, dan Supported Export Formats*.
4. Repository Praktikum ADBO: https://github.com/andika282006/IFRWP5149_2406044_LabAlat