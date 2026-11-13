# LAPORAN PRAKTIKUM ADBO
## PERTEMUAN 2: UNIFIED MODELLING LANGUAGE (UML)

- **Nama:** Andika Rahman
- **NIM:** 2406044
- **Mata Kuliah:** Praktikum Analisis dan Desain Berorientasi Objek (ADBO)
- **Program Studi:** S1 Teknik Informatika (Semester 5)

---

## A. TUJUAN PRAKTIKUM

Berdasarkan Jobsheet Praktikum Pertemuan 2, tujuan dari praktikum ini adalah:

1. Memahami penggunaan notasi dasar UML, khususnya pada Use Case Diagram.
2. Menempatkan aktor, use case, asosiasi, dan batas sistem sesuai dengan aturan pemodelan UML.
3. Membuat diagram berdasarkan kebutuhan dan skenario yang telah ditentukan.
4. Mengisi metadata artefak menggunakan template yang telah disediakan.
5. Melakukan pemeriksaan dan perbaikan terhadap kesalahan notasi serta dokumentasi diagram.

---

## B. DASAR TEORI

### 1. Pengertian UML

Unified Modelling Language (UML) merupakan bahasa pemodelan visual yang digunakan untuk menggambarkan, merancang, dan mendokumentasikan suatu sistem. UML membantu pengembang dalam memahami struktur serta perilaku sistem melalui berbagai jenis diagram. Dengan adanya UML, kebutuhan sistem dapat disampaikan secara lebih jelas sehingga memudahkan proses analisis dan perancangan perangkat lunak.

### 2. Konsep Dasar UML

Dalam UML terdapat beberapa konsep dasar yang digunakan untuk membentuk suatu model, yaitu:

1. **Things**, merupakan elemen dasar yang digunakan dalam pemodelan UML.
2. **Relationships**, merupakan hubungan yang menghubungkan satu elemen dengan elemen lainnya.
3. **Diagrams**, merupakan gambaran visual yang disusun dari elemen dan hubungan untuk menjelaskan suatu sistem.

### 3. Jenis Hubungan dalam UML

Beberapa jenis hubungan yang terdapat dalam UML antara lain:

1. **Dependency**, menunjukkan hubungan ketergantungan antara satu elemen dengan elemen lainnya.
2. **Association**, menunjukkan hubungan komunikasi antara aktor dengan fungsi atau use case.
3. **Generalization**, menunjukkan hubungan pewarisan atau hubungan umum dan khusus.
4. **Realization**, menunjukkan hubungan implementasi antara suatu elemen dengan elemen lainnya.

### 4. Notasi Use Case Diagram

Pada praktikum pertemuan 2, notasi yang digunakan difokuskan pada empat elemen utama, yaitu:

1. **Actor**, menggambarkan pihak yang berinteraksi dengan sistem dan ditempatkan di luar batas sistem.
2. **Use Case**, menggambarkan fungsi atau layanan yang disediakan oleh sistem dan digambarkan menggunakan bentuk elips.
3. **Association**, merupakan garis lurus yang menghubungkan aktor dengan use case untuk menunjukkan adanya interaksi.
4. **System Boundary**, merupakan persegi panjang yang menunjukkan batas ruang lingkup sistem.

### 5. Prinsip Penyusunan Use Case Diagram

Dalam membuat Use Case Diagram, terdapat beberapa aturan yang harus diperhatikan. Aktor harus ditempatkan di luar batas sistem, sedangkan use case harus berada di dalam batas sistem. Nama sistem pada diagram harus sesuai dengan skenario yang digunakan. Hubungan antara aktor dan use case juga harus sesuai dengan fungsi yang disebutkan dalam skenario.

Selain itu, garis asosiasi hanya digunakan untuk menunjukkan hubungan interaksi antara aktor dan fungsi sistem, bukan untuk menunjukkan urutan proses. Pada latihan ini tidak digunakan hubungan include, extend, maupun generalization.

---

## C. HASIL PRAKTIKUM

### 1. Latihan Notasi Use Case Diagram LAB

Pada latihan pertama, praktikum menggunakan studi kasus Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus. Sistem ini digunakan sebagai contoh untuk memahami hubungan antara aktor dengan fungsi yang tersedia di dalam sistem.

Berdasarkan skenario yang diberikan, terdapat dua kebutuhan utama, yaitu:

| ID Kebutuhan | Aktor | Fungsi Sistem |
|---|---|---|
| LAB-R01 | Mahasiswa | Lihat ketersediaan peralatan |
| LAB-R02 | Petugas laboratorium | Kelola data peralatan |

Dari kebutuhan tersebut, diagram dibuat dengan menempatkan aktor Mahasiswa dan Petugas Laboratorium di luar batas sistem. Sementara itu, fungsi Lihat Ketersediaan Peralatan dan Kelola Data Peralatan ditempatkan di dalam batas sistem.

**Nama sistem:** Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus.

**File yang digunakan:**
- `01_skenario/P02_LAB_skenario_v01.md`
- `03_latihan_tools/P02/LAB/P02_2406044_LAB_notasi_usecase_v01.drawio`
- `03_latihan_tools/P02/LAB/P02_2406044_LAB_notasi_usecase_v01.png`

**Metadata artefak:**
- ID Artefak: LAB-P02-UC
- Judul: Latihan Notasi Fungsi Laboratorium
- Pertemuan: 02
- Sumber Kebutuhan: LAB-R01 dan LAB-R02
- Jenis Artefak: Use Case Diagram
- Status: LATIHAN NOTASI

### 2. Latihan Perbaikan Notasi Use Case Diagram SIA

Pada latihan kedua, digunakan studi kasus Sistem Informasi Akademik (SIA). Pada bagian ini diberikan sebuah diagram awal yang masih memiliki beberapa kesalahan notasi. Tugas praktikum adalah mengidentifikasi dan memperbaiki kesalahan tersebut agar sesuai dengan aturan dasar Use Case Diagram.

Kebutuhan sistem yang digunakan adalah:

| ID Kebutuhan | Aktor | Fungsi Sistem |
|---|---|---|
| SIA-R01 | Mahasiswa | Lihat jadwal kuliah |
| SIA-R02 | Admin akademik | Kelola jadwal kuliah |

**Kesalahan pada diagram awal dan perbaikannya:**

| No. | Kesalahan | Perbaikan |
|---|---|---|
| 1 | Aktor Mahasiswa ditempatkan di dalam batas sistem. | Aktor Mahasiswa dipindahkan ke luar batas sistem. |
| 2 | Fungsi Lihat Jadwal Kuliah digambarkan menggunakan persegi panjang. | Bentuknya diubah menjadi elips sesuai notasi Use Case. |
| 3 | Aktor Mahasiswa dihubungkan dengan fungsi Kelola Jadwal Kuliah. | Hubungan tersebut dihapus dan disesuaikan dengan kebutuhan sistem. |
| 4 | Judul diagram menggunakan nama sistem laboratorium. | Judul diganti menjadi Sistem Informasi Akademik. |

Setelah dilakukan perbaikan, diagram memiliki dua aktor dan dua fungsi utama. Aktor Mahasiswa dihubungkan dengan fungsi Lihat Jadwal Kuliah, sedangkan Admin Akademik dihubungkan dengan fungsi Kelola Jadwal Kuliah. Kedua fungsi tersebut berada di dalam batas sistem Sistem Informasi Akademik.

**File yang digunakan:**
- `01_skenario/P02_SIA_skenario_v01.md`
- `03_latihan_tools/P02/SIA/P02_2406044_SIA_perbaikan_notasi_v01.drawio`
- `03_latihan_tools/P02/SIA/P02_2406044_SIA_notasi_v01.drawio`
- `03_latihan_tools/P02/SIA/P02_2406044_SIA_notasi_v01.png`

### 3. Pemeriksaan Hasil Praktikum

Pemeriksaan dilakukan untuk memastikan bahwa diagram yang dibuat telah sesuai dengan ketentuan pada jobsheet. Beberapa hal yang diperiksa meliputi kesesuaian judul sistem, posisi aktor, bentuk use case, hubungan asosiasi, serta kesesuaian nama fungsi dengan kebutuhan yang diberikan.

Selain itu, dilakukan pemeriksaan terhadap file sumber diagram agar dapat dibuka dan diedit kembali menggunakan draw.io. Hasil ekspor PNG juga perlu disesuaikan dengan diagram sumber agar tidak terdapat perbedaan antara keduanya.

---

## D. ANALISIS

Berdasarkan praktikum yang telah dilakukan, penggunaan UML khususnya Use Case Diagram membantu menggambarkan hubungan antara pengguna dengan fungsi yang tersedia di dalam sebuah sistem. Melalui latihan LAB, dapat dipahami bahwa setiap aktor harus memiliki hubungan dengan fungsi yang sesuai berdasarkan kebutuhan sistem. Mahasiswa hanya berhubungan dengan fungsi melihat ketersediaan peralatan, sedangkan Petugas Laboratorium berhubungan dengan fungsi mengelola data peralatan.

Pada latihan SIA, ditemukan beberapa kesalahan dalam diagram awal, seperti posisi aktor yang berada di dalam batas sistem, penggunaan bentuk persegi panjang untuk menggambarkan use case, hubungan aktor yang tidak sesuai, serta judul sistem yang keliru. Kesalahan tersebut diperbaiki berdasarkan aturan dasar notasi UML. Perbaikan ini menunjukkan bahwa setiap elemen dalam Use Case Diagram memiliki aturan penempatan dan bentuk yang harus diperhatikan agar informasi yang disampaikan tidak menimbulkan kesalahpahaman.

Dari kedua latihan tersebut, dapat dipahami bahwa garis asosiasi pada Use Case Diagram tidak menunjukkan urutan atau alur proses, melainkan hanya menunjukkan hubungan interaksi antara aktor dan fungsi sistem. Oleh karena itu, hubungan antaraktor dan use case harus dibuat berdasarkan kebutuhan yang telah ditentukan, bukan berdasarkan perkiraan atau penambahan fungsi sendiri. Pengelolaan nama file, metadata, serta penyimpanan diagram dalam format draw.io dan PNG juga penting untuk menjaga kerapian dan konsistensi dokumentasi hasil praktikum.

---

## E. KESIMPULAN

Berdasarkan praktikum Analisis dan Desain Berorientasi Objek pada Pertemuan 2, dapat disimpulkan bahwa UML merupakan salah satu bahasa pemodelan yang digunakan untuk menggambarkan kebutuhan dan interaksi dalam suatu sistem. Melalui Use Case Diagram, hubungan antara aktor dengan fungsi sistem dapat divisualisasikan menggunakan empat notasi dasar, yaitu Actor, Use Case, Association, dan System Boundary.

Praktikum ini juga memberikan pemahaman mengenai pentingnya mengikuti aturan penggunaan notasi UML. Kesalahan pada posisi aktor, bentuk use case, hubungan asosiasi, dan penamaan sistem dapat memengaruhi kejelasan diagram. Oleh karena itu, setiap elemen harus disusun sesuai dengan skenario dan kebutuhan yang telah ditentukan.

Selain memahami notasi UML, praktikum ini melatih ketelitian dalam membuat, memperbaiki, menyimpan, serta mendokumentasikan artefak menggunakan draw.io dan format Markdown. Dengan demikian, hasil pemodelan dapat tersusun lebih rapi, konsisten, dan mudah diperiksa kembali.

---

## F. REFERENSI

1. Institut Teknologi Garut. Jobsheet Praktikum Analisis dan Desain Berorientasi Objek (ADBO) Pertemuan 2.
2. Object Management Group (OMG). Unified Modeling Language (UML) Version 2.5.1.
3. diagrams.net. Dokumentasi Penggunaan draw.io. https://www.drawio.com/
4. Repository Praktikum ADBO: https://github.com/andika282006/IFRWP5149_2406044_LabAlat