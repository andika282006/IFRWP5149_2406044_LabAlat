# LAPORAN PRAKTIKUM ADBO
## PERTEMUAN 5: SKENARIO USE CASE - DARI DIAGRAM KE LANGKAH KEGIATAN

- **Nama:** Andika Rahman
- **NIM:** 2406044
- **Mata Kuliah:** Praktikum Analisis dan Desain Berorientasi Objek (ADBO)
- **Program Studi:** S1 Teknik Informatika (Semester 5)

---

## A. TUJUAN PRAKTIKUM

Berdasarkan Jobsheet Praktikum Pertemuan 5, tujuan dari praktikum ini adalah agar mahasiswa mampu:

1. Menyusun tabel skenario untuk satu use case dengan struktur lengkap, mulai dari nama use case, aktor, tujuan, deskripsi, kegiatan, respons sistem, skenario normal, skenario alternatif, hingga skenario akhir.
2. Menulis langkah skenario secara berurutan dengan satu aksi pada setiap langkah.
3. Memisahkan aktivitas aktor pada kolom Kegiatan dan tanggapan sistem pada kolom Respon Sistem.
4. Memetakan relasi include menjadi langkah wajib pada skenario normal dan relasi extend menjadi cabang bersyarat pada skenario alternatif.
5. Menerapkan generalization aktor dan generalization use case dalam penyusunan tabel skenario.
6. Memeriksa kesesuaian tabel skenario dengan diagram kumulatif Pertemuan 4, termasuk nama, ID, aktor, dan hubungan antaruse case.

---

## B. DASAR TEORI

### 1. Pengertian Skenario Use Case

Skenario use case merupakan uraian langkah demi langkah mengenai interaksi antara aktor dengan sistem dalam menjalankan suatu fungsi. Skenario menjelaskan apa yang dilakukan aktor, bagaimana sistem memberikan respons, kapan proses dapat mengalami kondisi alternatif, dan bagaimana suatu proses dinyatakan selesai.

Skenario use case disusun dalam bentuk tabel yang memiliki dua kolom utama, yaitu Kegiatan dan Respon Sistem. Kolom Kegiatan berisi tindakan yang dilakukan oleh aktor, sedangkan kolom Respon Sistem berisi tanggapan yang diberikan oleh sistem terhadap tindakan tersebut.

### 2. Perbedaan Use Case Diagram, Use Case Description, dan Skenario Use Case

Ketiga bentuk dokumentasi tersebut memiliki fungsi yang saling berkaitan, tetapi berbeda dalam penyajiannya.

1. **Use Case Diagram**, digunakan untuk menggambarkan fungsi yang tersedia pada sistem serta hubungan antara aktor dengan use case.
2. **Use Case Description**, digunakan untuk menjelaskan tujuan, pemicu, prasyarat, alur utama, alur alternatif, dan pascakondisi dari suatu use case.
3. **Skenario Use Case**, digunakan untuk menjabarkan proses interaksi aktor dan sistem secara lebih terperinci melalui langkah-langkah kegiatan dan respons sistem.

Dengan demikian, skenario use case merupakan pengembangan dari use case description yang disusun berdasarkan diagram sebagai acuan. Ketiganya harus memiliki informasi yang konsisten agar tidak terjadi perbedaan antara fungsi yang dimodelkan dengan proses yang dijelaskan.

### 3. Struktur Tabel Skenario Use Case

Dalam penyusunan tabel skenario, terdapat beberapa bagian yang harus dicantumkan, yaitu:

1. **Nama Use Case**, berisi nama fungsi yang sedang dijelaskan.
2. **Aktor**, menunjukkan pihak yang menjalankan fungsi tersebut.
3. **Tujuan**, menjelaskan hasil yang ingin dicapai oleh aktor.
4. **Deskripsi**, memberikan gambaran singkat mengenai proses yang dilakukan.
5. **Kegiatan**, berisi tindakan yang dilakukan oleh aktor.
6. **Respon Sistem**, berisi tanggapan sistem terhadap tindakan aktor.
7. **Skenario Normal**, menjelaskan langkah-langkah utama ketika proses berjalan sesuai kondisi yang diharapkan.
8. **Skenario Alternatif**, menjelaskan kondisi lain yang dapat terjadi apabila terdapat penyimpangan dari alur normal.
9. **Skenario Akhir**, menjelaskan kondisi akhir ketika proses berhasil maupun gagal.

### 4. Kaidah Penulisan Langkah Skenario

Dalam menulis skenario use case, setiap langkah harus memiliki satu tindakan yang jelas agar mudah dipahami dan diperiksa. Kolom Kegiatan hanya berisi aktivitas aktor, sedangkan kolom Respon Sistem hanya berisi tanggapan sistem.

Penulisan langkah menggunakan kalimat aktif dan kata kerja yang jelas, seperti memilih, mengisi, mengirim, menampilkan, memeriksa, menyimpan, dan menolak. Data yang dimasukkan atau ditampilkan juga harus disebutkan secara spesifik, termasuk nama field, nilai, maupun status.

Penomoran pada skenario alternatif harus melanjutkan nomor dari skenario normal dan tidak dimulai kembali dari angka satu. Setiap cabang alternatif juga harus menjelaskan langkah asal terjadinya kondisi tersebut.

### 5. Pemetaan Relasi Include

Relasi `<<include>>` pada Use Case Diagram diterjemahkan menjadi langkah wajib dalam bagian Skenario Normal. Hal ini karena use case yang disertakan selalu dijalankan sebagai bagian dari proses utama.

Pada studi kasus laboratorium, LAB-UC03 Ajukan Peminjaman memiliki relasi include dengan LAB-UC04 Periksa Ketersediaan. Oleh karena itu, pemeriksaan ketersediaan harus dicantumkan sebagai langkah dalam skenario normal pengajuan peminjaman.

Langkah tersebut cukup ditulis sebagai rujukan menuju tabel skenario LAB-UC04 tanpa menyalin seluruh langkah yang ada di dalamnya.

### 6. Pemetaan Relasi Extend

Relasi `<<extend>>` diterjemahkan menjadi cabang bersyarat pada bagian Skenario Alternatif. Relasi ini digunakan ketika suatu aktivitas hanya dijalankan apabila kondisi tertentu terpenuhi.

Contohnya pada LAB-UC03 Ajukan Peminjaman, aktivitas Cetak Bukti Pengajuan hanya dilakukan apabila mahasiswa memilih untuk mencetak bukti. Oleh karena itu, langkah tersebut ditulis sebagai cabang alternatif dengan mencantumkan condition dan extension point sesuai diagram P04.

### 7. Penerapan Generalization Aktor

Generalization aktor digunakan ketika beberapa aktor khusus memiliki fungsi yang sama karena mewarisi fungsi dari aktor umum.

Dalam penyusunan skenario, aktivitas yang dimiliki bersama cukup ditulis satu kali menggunakan nama aktor umum. Apabila terdapat perbedaan perilaku pada aktor khusus, perbedaan tersebut ditambahkan sebagai catatan atau cabang pada tabel yang sama.

Contohnya adalah aktor Peminjam yang berlaku untuk Mahasiswa dan Dosen pada sistem peminjaman peralatan laboratorium.

### 8. Penerapan Generalization Use Case

Generalization use case digunakan ketika beberapa use case khusus memiliki perilaku dasar yang sama dengan use case umum.

Skenario untuk use case umum berisi langkah-langkah bersama, sedangkan setiap use case khusus memiliki tabel tersendiri yang hanya menjelaskan perilaku pembeda. Langkah yang sama cukup dirujuk ke tabel skenario use case umum.

### 9. Collaboration dan Realization

Collaboration merupakan elemen yang digunakan untuk menunjukkan realisasi suatu use case. Dalam penyusunan tabel skenario, collaboration tidak dibuatkan tabel tersendiri dan tidak diberikan langkah kegiatan.

Collaboration hanya dicantumkan pada bagian keterangan tabel use case yang direalisasikannya. Langkah kegiatan dan pertukaran pesan dalam collaboration akan dibahas pada diagram interaksi di pertemuan berikutnya.

---

## C. HASIL PRAKTIKUM

### 1. Studi Kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus

Pada latihan pertama, digunakan studi kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus. Studi kasus ini menggunakan diagram kumulatif Pertemuan 4 sebagai acuan utama.

Pada bagian ini, tidak terdapat kebutuhan atau use case baru. Kebutuhan LAB-R01 sampai LAB-R11 serta hubungan antaruse case tetap mengacu pada Jobsheet Pertemuan 4. Tugas praktikum adalah memeriksa dan menelaah 12 tabel skenario yang telah disediakan dalam Jobsheet Pertemuan 5.

Adapun 12 use case yang diperiksa adalah:

| No. | ID Use Case | Nama Use Case |
|---|---|---|
| 1 | LAB-UC01 | Lihat Ketersediaan Peralatan |
| 2 | LAB-UC02 | Kelola Data Peralatan |
| 3 | LAB-UC03 | Ajukan Peminjaman |
| 4 | LAB-UC04 | Periksa Ketersediaan |
| 5 | LAB-UC05 | Cetak Bukti Pengajuan |
| 6 | LAB-UC06 | Proses Keputusan Peminjaman |
| 7 | LAB-UC07 | Lihat Laporan Peminjaman |
| 8 | LAB-UC08 | Tambah Data Peralatan |
| 9 | LAB-UC09 | Ubah Data Peralatan |
| 10 | LAB-UC10 | Hapus Data Peralatan |
| 11 | LAB-UC11 | Catat Pengembalian Peralatan |
| 12 | LAB-UC12 | Periksa Kondisi Peralatan |

### 2. Pemeriksaan Skenario LAB

Pemeriksaan dilakukan dengan mencocokkan setiap tabel skenario terhadap diagram kumulatif P04. Hal-hal yang diperiksa meliputi kesesuaian nama use case, ID, aktor, tujuan, serta hubungan antaruse case.

Beberapa hubungan penting yang diperiksa adalah:

**a. Relasi Include**

Pada proses Ajukan Peminjaman, pemeriksaan ketersediaan merupakan langkah wajib yang harus dilakukan sebelum pengajuan disimpan. Hal yang sama berlaku pada proses Catat Pengembalian Peralatan, yaitu sistem harus menjalankan pemeriksaan kondisi peralatan.

Hubungan tersebut dapat dilihat pada:

- LAB-UC03 Ajukan Peminjaman dengan LAB-UC04 Periksa Ketersediaan.
- LAB-UC11 Catat Pengembalian Peralatan dengan LAB-UC12 Periksa Kondisi Peralatan.

**b. Relasi Extend**

Pada proses pengajuan peminjaman, mahasiswa dapat memilih untuk mencetak bukti pengajuan. Aktivitas tersebut hanya dilakukan apabila kondisi pencetakan terpenuhi.

Hubungan tersebut terdapat pada LAB-UC03 Ajukan Peminjaman dengan LAB-UC05 Cetak Bukti Pengajuan.

**c. Generalization Aktor**

Aktor Peminjam merupakan aktor umum yang berlaku untuk Mahasiswa dan Dosen. Oleh karena itu, skenario pengajuan peminjaman ditulis satu kali atas nama Peminjam, sedangkan perbedaan perilaku aktor khusus dicantumkan sebagai catatan atau cabang.

**d. Generalization Use Case**

Pengelolaan data peralatan terdiri dari satu use case umum dan tiga use case khusus, yaitu:

- LAB-UC02 Kelola Data Peralatan.
- LAB-UC08 Tambah Data Peralatan.
- LAB-UC09 Ubah Data Peralatan.
- LAB-UC10 Hapus Data Peralatan.

Skenario LAB-UC02 berisi langkah pengelolaan secara umum, sedangkan ketiga use case khusus menjelaskan perilaku yang membedakan proses tambah, ubah, dan hapus data.

**e. Collaboration**

Collaboration tidak dibuatkan tabel skenario tersendiri. Collaboration hanya dicantumkan pada keterangan tabel use case yang direalisasikannya.

Contohnya:

- LAB-CO01 Ajukan Peminjaman merealisasikan LAB-UC03.
- LAB-CO02 Catat Pengembalian Peralatan merealisasikan LAB-UC11.

### 3. Penelusuran Hasil Pemeriksaan Skenario LAB

Pemeriksaan terhadap tabel skenario LAB dapat didokumentasikan menggunakan tabel penelusuran berikut.

| ID Use Case | Relasi yang Ditelusuri | Hasil Pencocokan |
|---|---|---|
| LAB-UC01 | Asosiasi aktor | Dicocokkan dengan aktor Mahasiswa. |
| LAB-UC02 | Generalization use case | Dicocokkan dengan LAB-UC08, LAB-UC09, dan LAB-UC10. |
| LAB-UC03 | Include, extend, generalization aktor, collaboration | Dicocokkan dengan LAB-UC04, LAB-UC05, Peminjam, dan LAB-CO01. |
| LAB-UC04 | Include | Dicocokkan dengan LAB-UC03. |
| LAB-UC05 | Extend | Dicocokkan dengan LAB-UC03. |
| LAB-UC06 | Asosiasi aktor | Dicocokkan dengan Petugas Laboratorium. |
| LAB-UC07 | Asosiasi aktor | Dicocokkan dengan Kepala Laboratorium. |
| LAB-UC08 | Generalization use case | Dicocokkan dengan LAB-UC02. |
| LAB-UC09 | Generalization use case | Dicocokkan dengan LAB-UC02. |
| LAB-UC10 | Generalization use case | Dicocokkan dengan LAB-UC02. |
| LAB-UC11 | Include dan collaboration | Dicocokkan dengan LAB-UC12 dan LAB-CO02. |
| LAB-UC12 | Include | Dicocokkan dengan LAB-UC11. |

Catatan: Hasil pada tabel tersebut merupakan panduan penelusuran berdasarkan hubungan dalam jobsheet. Kolom hasil pemeriksaan akhir perlu disesuaikan dengan pencocokan yang benar-benar dilakukan terhadap diagram P04.

### 4. Tugas Sistem Informasi Akademik, Layanan Hasil Studi

Pada tugas kedua, digunakan studi kasus Sistem Informasi Akademik dengan fokus pada layanan hasil studi. Tugas ini merupakan kelanjutan dari diagram SIA Pertemuan 4, bukan membuat sistem atau diagram baru.

Kebutuhan yang digunakan adalah SIA-R07 sampai SIA-R12. Seluruh nama aktor, ID use case, dan hubungan harus tetap mengikuti diagram kumulatif P04.

Berdasarkan indeks tugas pada Jobsheet Pertemuan 5, terdapat tujuh use case yang harus dibuatkan tabel skenario, yaitu:

| No. | ID Use Case | Nama Use Case | Aktor |
|---|---|---|---|
| 1 | SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika |
| 2 | SIA-UC08 | Input Nilai Mata Kuliah | Dosen |
| 3 | SIA-UC09 | Lihat KHS | Mahasiswa |
| 4 | SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik |
| 5 | SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik |
| 6 | SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik |
| 7 | SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik |

### 5. Penyusunan Skenario SIA

Penyusunan skenario dilakukan dengan mengikuti struktur tabel yang sama seperti contoh LAB-UC03 pada Jobsheet Pertemuan 5.

Setiap tabel harus memiliki nama use case, aktor, tujuan, deskripsi, kolom Kegiatan, kolom Respon Sistem, Skenario Normal, Skenario Alternatif, dan Skenario Akhir.

Berikut penjelasan masing-masing use case:

**a. SIA-UC07 Lihat Kalender Akademik**

Skenario ditulis satu kali atas nama Civitas Akademika dan berlaku untuk Mahasiswa serta Dosen. Hal ini karena kedua aktor tersebut mewarisi fungsi melihat kalender akademik dari aktor umum Civitas Akademika.

**b. SIA-UC08 Input Nilai Mata Kuliah**

Skenario menjelaskan proses dosen dalam memasukkan nilai mata kuliah yang diampunya. Prasyaratnya adalah dosen harus merupakan pengampu mata kuliah tersebut. Apabila nilai yang dimasukkan berada di luar rentang yang sah, sistem harus menolak proses penyimpanan nilai.

Collaboration yang merealisasikan use case ini adalah SIA-CO01 Input Nilai Mata Kuliah.

**c. SIA-UC09 Lihat KHS**

Skenario menjelaskan proses mahasiswa dalam melihat Kartu Hasil Studi. Sistem hanya menampilkan nilai yang sudah dipublikasikan sehingga nilai yang belum dipublikasikan tidak ditampilkan dalam KHS.

Collaboration yang merealisasikan use case ini adalah SIA-CO02 Lihat KHS.

**d. SIA-UC10 Kelola Data Mahasiswa**

Skenario ini merupakan use case umum yang menjelaskan proses pengelolaan data mahasiswa. Langkah-langkah umum digunakan sebagai acuan bagi tiga use case khusus, yaitu Tambah Data Mahasiswa, Ubah Data Mahasiswa, dan Hapus Data Mahasiswa.

**e. SIA-UC11 Tambah Data Mahasiswa**

Skenario ini menjelaskan perilaku khusus berupa penambahan data mahasiswa baru. Langkah yang bersifat umum tetap merujuk pada skenario SIA-UC10.

**f. SIA-UC12 Ubah Data Mahasiswa**

Skenario ini menjelaskan proses perubahan data mahasiswa yang sudah tersimpan. Perilaku khususnya adalah data mahasiswa berhasil diperbarui, sedangkan langkah umum mengikuti SIA-UC10.

**g. SIA-UC13 Hapus Data Mahasiswa**

Skenario ini menjelaskan proses penghapusan data mahasiswa. Penghapusan hanya dapat dilakukan apabila mahasiswa tidak memiliki data akademik aktif. Jika masih terdapat data akademik aktif, sistem harus menolak penghapusan.

### 6. Penerapan Generalization pada SIA

Dalam penyusunan skenario SIA, terdapat dua penerapan generalization yang harus diperhatikan.

**Generalization Aktor**

Mahasiswa dan Dosen merupakan aktor khusus dari Civitas Akademika. Keduanya mewarisi fungsi Lihat Kalender Akademik sehingga skenario hanya ditulis satu kali atas nama Civitas Akademika.

**Generalization Use Case**

SIA-UC10 Kelola Data Mahasiswa merupakan use case umum yang memiliki tiga use case khusus, yaitu:

- SIA-UC11 Tambah Data Mahasiswa.
- SIA-UC12 Ubah Data Mahasiswa.
- SIA-UC13 Hapus Data Mahasiswa.

Skenario umum menjelaskan langkah pengelolaan bersama, sedangkan skenario khusus menjelaskan perilaku pembeda dari masing-masing fungsi.

### 7. Pemeriksaan Konsistensi Skenario SIA

Setelah ketujuh tabel skenario dibuat, dilakukan pemeriksaan untuk memastikan bahwa seluruh informasi telah sesuai dengan diagram P04.

Beberapa aturan khusus yang harus diperhatikan adalah:

1. Mahasiswa dan Dosen mewarisi fungsi Lihat Kalender Akademik dari Civitas Akademika.
2. Input Nilai Mata Kuliah hanya dapat dilakukan oleh dosen pengampu mata kuliah tersebut.
3. KHS hanya menampilkan nilai yang sudah dipublikasikan.
4. Hapus Data Mahasiswa hanya dapat dilakukan apabila mahasiswa tidak memiliki data akademik aktif.
5. Collaboration hanya dicantumkan pada keterangan tabel yang direalisasikannya dan tidak memiliki langkah kegiatan sendiri.
6. Diagram SIA Pertemuan 4 tidak diubah karena produk P05 berupa dokumen skenario, bukan diagram baru.

### 8. Pemeriksaan Struktur dan Penamaan Dokumen

Dokumen praktikum disimpan pada folder `01_skenario` dengan mengikuti pola penamaan yang ditentukan dalam jobsheet.

Berkas yang menjadi deliverable adalah:

- `P05_2406044_LAB_skenario_v01.md`
- `P05_2406044_SIA_skenario_v01.drawio`

Berkas LAB berisi hasil penelaahan terhadap 12 tabel skenario studi kasus, sedangkan berkas SIA berisi tujuh tabel skenario tugas akademik.

Diagram P04 tetap digunakan sebagai acuan dan tidak boleh ditimpa atau diubah. Selain itu, logbook singkat perlu dibuat untuk mencatat tabel LAB yang sudah diperiksa dan perkembangan penyusunan tabel skenario SIA.

---

## D. ANALISIS

Berdasarkan materi praktikum Pertemuan 5, skenario use case merupakan bagian penting dalam proses analisis sistem karena dapat menjelaskan interaksi antara aktor dan sistem secara lebih terperinci. Jika Use Case Diagram hanya menunjukkan fungsi dan hubungan antaraktor, maka skenario use case menjelaskan bagaimana fungsi tersebut dijalankan melalui urutan kegiatan dan respons sistem. Dengan adanya skenario, setiap proses dapat dipahami secara lebih jelas dan dapat diperiksa berdasarkan langkah-langkah yang telah ditentukan.

Pada studi kasus laboratorium, pemeriksaan terhadap 12 tabel skenario memberikan pemahaman mengenai hubungan antara diagram kumulatif P04 dengan penjabaran langkah kegiatan. Relasi include harus menjadi bagian dari skenario normal karena merupakan proses wajib, sedangkan relasi extend menjadi bagian dari skenario alternatif karena hanya dijalankan apabila kondisi tertentu terpenuhi. Generalization aktor juga membuat penyusunan skenario lebih sederhana karena perilaku yang sama cukup ditulis satu kali menggunakan aktor umum.

Pada tugas Sistem Informasi Akademik, penerapan generalization aktor dan generalization use case menjadi bagian yang perlu diperhatikan. Civitas Akademika digunakan sebagai aktor umum untuk Mahasiswa dan Dosen dalam melihat kalender akademik. Sementara itu, Kelola Data Mahasiswa menjadi use case umum yang memiliki tiga fungsi khusus, yaitu tambah, ubah, dan hapus. Setiap skenario khusus hanya menjelaskan perilaku yang membedakannya dari skenario umum sehingga tidak terjadi pengulangan langkah yang sama.

Selain itu, penyusunan skenario harus memperhatikan penomoran yang berlanjut dari skenario normal ke skenario alternatif. Pemisahan antara kegiatan aktor dan respons sistem juga penting agar alur interaksi tidak membingungkan. Setiap kondisi alternatif harus memiliki keterangan mengenai langkah asalnya, sedangkan skenario akhir harus menjelaskan kondisi ketika proses berhasil maupun gagal. Dengan demikian, hasil skenario dapat digunakan sebagai dokumentasi yang lebih jelas dan menjadi dasar untuk proses pemodelan berikutnya.

---

## E. KESIMPULAN

Berdasarkan praktikum Analisis dan Desain Berorientasi Objek pada Pertemuan 5, dapat disimpulkan bahwa skenario use case digunakan untuk menjelaskan urutan interaksi antara aktor dengan sistem secara lebih terperinci. Penyusunan skenario dilakukan berdasarkan diagram kumulatif Pertemuan 4 sehingga nama use case, ID, aktor, serta hubungan antaruse case harus tetap konsisten.

Praktikum ini memberikan pemahaman mengenai struktur tabel skenario yang terdiri dari nama use case, aktor, tujuan, deskripsi, kegiatan, respons sistem, skenario normal, skenario alternatif, dan skenario akhir. Selain itu, relasi include, extend, generalization aktor, generalization use case, serta collaboration harus diterapkan sesuai aturan pemetaan yang telah ditentukan dalam jobsheet.

Melalui praktikum ini, mahasiswa dapat memahami bahwa dokumentasi skenario sangat membantu dalam menjelaskan proses yang tidak dapat ditampilkan hanya melalui diagram. Penyusunan langkah yang terstruktur, penggunaan penomoran yang benar, serta kesesuaian antara skenario dan diagram menjadi hal penting agar hasil analisis sistem lebih mudah dipahami, diperiksa, dan dikembangkan pada pertemuan selanjutnya.

---

## F. REFERENSI

1. Institut Teknologi Garut. (2026). Jobsheet Praktikum Analisis dan Desain Berorientasi Objek (ADBO) Pertemuan 5: Skenario Use Case - Dari Diagram ke Langkah Kegiatan.
2. Object Management Group. (2017). *OMG Unified Modeling Language (UML), Version 2.5.1*.
3. Jobsheet Praktikum ADBO Pertemuan 3. Sumber use case description dan kebutuhan awal sistem.
4. Jobsheet Praktikum ADBO Pertemuan 4. Sumber diagram kumulatif, katalog use case, generalization, collaboration, dan kebutuhan sistem.
5. Repository Praktikum ADBO: https://github.com/andika282006/IFRWP5149_2406044_LabAlat