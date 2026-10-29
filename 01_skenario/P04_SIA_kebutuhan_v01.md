# Dokumen Kebutuhan dan Skenario Sistem Informasi Akademik: Layanan Hasil Studi (Versi 01)

## 1. Deskripsi Skenario Tugas
Tugas ini berbeda dari tugas pertemuan sebelumnya. Tugas Pertemuan 2
adalah jadwal kuliah dan tugas Pertemuan 3 adalah pengajuan KRS. Tugas
Pertemuan 4 adalah layanan hasil studi, dengan teknik generalization dan
collaboration yang sama seperti studi kasus, tetapi diterapkan pada skenario
baru tanpa contoh jawaban.
Skenario tugas berikut fiktif untuk praktikum dan berbeda dari tugas
Pertemuan 2 (jadwal kuliah) dan Pertemuan 3 (pengajuan KRS).
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang
dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang
diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu
Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin
Akademik mengelola data mahasiswa: menambah data mahasiswa baru,
mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case
utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh
collaboration yang bersesuaian

---

## 2. Tabel Kebutuhan Tugas (SIA-R07 s.d. SIA-R12)
| ID | Kebutuhan tugas |
| :--- | :--- |
| SIA-R01 s.d. SIA-R02 | Kebutuhan Pertemuan 2 tetap berlaku (Jadwal Kuliah dan Kelola Jadwal Kuliah) |
| SIA-R03 s.d. SIA-R06 | Kebutuhan Pertemuan 3 tetap berlaku (Pengajuan KRS, Validasi KRS, Unduh Bukti, Proses Keputusan KRS) |
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS |

---

## 3. Batas dan Asumsi Sistem
•Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02
(Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap
mempunyai identitas berbeda.
• Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
• Kalender akademik pada tugas ini adalah agenda resmi institusi (awal
semester, batas KRS, masa ujian, dan sejenisnya); jangan
menyamakannya dengan jadwal kuliah pada Pertemuan 2.
• Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai
yang diinput belum terpublikasi sebelum dinyatakan resmi oleh ketentuan
tugas ini: KHS hanya menampilkan nilai yang sudah dipublikasikan.
• Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data
akademik aktif. Ketentuan ini fiktif untuk latihan.
• Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari
Pertemuan 3. Pembayaran dan perancangan basis data berada di luar
tugas ini.

---

## 4. Identifikasi Aktor (Generalization Aktor)
| Aktor | Kedudukan | Tujuan terhadap sistem |
| :--- | :--- | :--- |
| **Civitas Akademika** | Umum (*general*), baru di Pertemuan 4 | Peran umum bagi civitas akademika; mewariskan fungsi melihat kalender akademik kepada Mahasiswa dan Dosen. |
| **Mahasiswa** | Khusus dari Civitas Akademika, tetap dari P2 & P3 | Mengajukan KRS, melihat jadwal, mengunduh bukti KRS, serta melihat kalender akademik (diwarisi) dan melihat KHS. |
| **Dosen** | Khusus dari Civitas Akademika, baru di P4 | Melihat kalender akademik (diwarisi dari Civitas Akademika) serta menginput nilai mata kuliah. |
| **Admin Akademik** | Tetap dari pertemuan sebelumnya | Mengelola data mahasiswa (tambah, ubah, hapus). |

---

## 5. Katalog Use Case Gabungan SIA
| ID | Nama use case | Peran dalam model | Sumber kebutuhan |
| :--- | :--- | :--- | :--- |
| SIA-UC01 | Lihat Jadwal Kuliah | Tetap dari Pertemuan 2; fungsi mahasiswa | SIA-R01 |
| SIA-UC02 | Kelola Jadwal Kuliah | Tetap dari Pertemuan 2; fungsi admin | SIA-R02 |
| SIA-UC03 | Ajukan KRS | Tetap dari Pertemuan 3; fungsi mahasiswa | SIA-R03 |
| SIA-UC04 | Validasi KRS | Tetap dari Pertemuan 3; disertakan (*include*) SIA-UC03 | SIA-R04 |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Tetap dari Pertemuan 3; tambahan bersyarat (*extend*) SIA-UC03 | SIA-R05 |
| SIA-UC06 | Proses Keputusan KRS | Tetap dari Pertemuan 3; fungsi dosen wali | SIA-R06|
| SIA-UC07 | Lihat Kalender Akademik | Baru di P4; fungsi aktor umum Civitas Akademika | SIA-R07 |
| SIA-UC08 | Input Nilai Mata Kuliah | Baru di P4; fungsi dosen; direalisasikan SIA-CO01 | SIA-R08 |
| SIA-UC09 | Lihat KHS | Baru di P4; fungsi mahasiswa; direalisasikan SIA-CO02 | SIA-R09 |
| SIA-UC10 | Kelola Data Mahasiswa | Baru di P4; use case UMUM bagi SIA-UC11, SIA-UC12, SIA-UC13 | SIA-R10, SIA-R11 |
| SIA-UC11 | Tambah Data Mahasiswa | Baru di P4; use case KHUSUS dari SIA-UC10 | SIA-R11 |
| SIA-UC12 | Ubah Data Mahasiswa | Baru di P4; use case KHUSUS dari SIA-UC10 | SIA-R11|
| SIA-UC13 | Hapus Data Mahasiswa | Baru di P4; use case KHUSUS dari SIA-UC10 | SIA-R11 |

---

## 6. Uji Konsistensi (Analisis Situasi A, B, dan C)[cite: 22]
- **Situasi A:** Mahasiswa melihat kalender akademik tanpa garis asosiasi langsung dari Mahasiswa tetap benar menurut diagram karena Mahasiswa berkedudukan sebagai aktor khusus yang mewarisi fungsi tersebut dari aktor umum *Civitas Akademika* (*generalization*).
- **Situasi B:** Dosen yang bukan pengampu mencoba menginput nilai akan ditolak oleh sistem karena prasyarat use case mengharuskan dosen tersebut adalah pengampu sah mata kuliah terkait.
- **Situasi C:** Admin Akademik menghapus data mahasiswa yang masih memiliki data akademik aktif akan ditolak oleh sistem sesuai aturan pembatasan penghapusan data.