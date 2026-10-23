<!-- SKENARIO -->
Skenario berikut merupakan bahan latihan yang ditetapkan untuk 
jobsheet, bukan hasil pengumpulan kebutuhan laboratorium nyata. 
Skenario ini melanjutkan potongan model Pertemuan 3. 
Selain mahasiswa, dosen juga meminjam peralatan laboratorium untuk 
kegiatan praktikum dan penelitian. Mahasiswa dan dosen sama-sama 
dapat melihat ketersediaan peralatan dan mengajukan peminjaman. 
Petugas laboratorium mengelola data peralatan: menambah peralatan 
baru, mengubah data peralatan, dan menghapus data peralatan yang 
tidak lagi dipakai. Setelah peminjaman disetujui dan alat diambil, petugas 
mencatat pengembalian peralatan. Pada saat mencatat pengembalian, 
petugas memeriksa dan mencatat kondisi peralatan. Dua use case utama 
pada potongan model ini, Ajukan Peminjaman dan Catat Pengembalian 
Peralatan, ditunjukkan realisasinya oleh collaboration yang bersesuaian. 
Seluruh fungsi Pertemuan 3 tetap berlaku dan tetap digambar: 
pemeriksaan ketersediaan di dalam pengajuan, pencetakan bukti 
pengajuan oleh mahasiswa, proses keputusan peminjaman oleh petugas, 
dan laporan peminjaman untuk kepala laboratorium. Diagram Pertemuan 
4 adalah diagram Pertemuan 3 yang ditambah, bukan diagram baru yang 
menggantikannya.

<!-- TABEL KEBUTUHAN -->
| ID | Kebutuhan |
| :--- | :--- |
| LAB-R01 | Mahasiswa dapat melihat ketersediaan peralatan |
| LAB-R02 | Petugas dapat mengelola data peralatan |
| LAB-R03 | Mahasiswa dapat mengajukan peminjaman; sistem memeriksa ketersediaan sebelum menyimpan |
| LAB-R04 | Mahasiswa dapat mencetak bukti pada konfirmasi pengajuan jika memilihnya |
| LAB-R05 | Petugas dapat menetapkan persetujuan atau penolakan pengajuan |
| LAB-R06 | Kepala laboratorium dapat melihat laporan peminjaman |
| LAB-R07 | Mahasiswa dan Dosen, sebagai Peminjam, dapat melihat ketersediaan peralatan dan mengajukan peminjaman. |
| LAB-R08 | Petugas laboratorium mengelola data peralatan dalam tiga bentuk khusus: tambah, ubah, dan hapus data peralatan. |
| LAB-R09 | Petugas laboratorium dapat mencatat pengembalian peralatan untuk peminjaman yang berstatus Dipinjam. |
| LAB-R10 | Sistem memeriksa dan mencatat kondisi peralatan sebagai bagian dari pencatatan pengembalian. |
| LAB-R11 | Model menunjukkan collaboration yang merealisasikan Ajukan Peminjaman dan Catat Pengembalian Peralatan. |

<!-- BATAS SISTEM DAN ATURAN -->
Batas sistem dan aturan 
• Sistem mencatat dan menyediakan informasi; perpindahan fisik alat tidak 
terjadi di dalam perangkat lunak (tetap dari Pertemuan 3). 
• Pengguna telah terautentikasi dan memiliki hak akses sesuai peran (tetap 
dari Pertemuan 3). 
• Pengembalian hanya dapat dicatat untuk peminjaman berstatus Dipinjam. 
Peminjaman yang masih Menunggu Keputusan atau Ditolak tidak dapat 
dicatat pengembaliannya. 
• Kondisi peralatan pada pengembalian dicatat dengan salah satu nilai: Baik, 
Rusak Ringan, atau Rusak Berat. 
• Hapus Data Peralatan hanya untuk peralatan yang tidak sedang dipinjam 
dan tidak memiliki pengajuan aktif. 
• Keterlambatan dan denda belum dimodelkan pada pertemuan ini. Tuliskan 
sebagai pertanyaan terbuka pada berkas kebutuhan, jangan mengarang 
aturan denda. 
• Kriteria penerimaan model: semua kebutuhan LAB-R01 sampai LAB-R11 
mempunyai representasi pada diagram kumulatif, arah generalization dan 
realization benar, dan diagram konsisten dengan deskripsinya.

<!-- aktor umum dan aktor khusus  -->
| Aktor | Kedudukan | Tujuan terhadap sistem |
| :--- | :--- | :--- |
| **Peminjam** | Umum (*general*), baru pada Pertemuan 4 | Peran umum bagi peminjam peralatan. Mewariskan fungsinya kepada Mahasiswa dan Dosen. |
| **Mahasiswa** | Khusus dari Peminjam, tetap dari Pertemuan 3 | Melihat ketersediaan dan mengajukan peminjaman (diwarisi dari Peminjam), ditambah mencetak bukti pengajuan sebagai asosiasi khususnya sendiri. |
| **Dosen** | Khusus dari Peminjam, baru pada Pertemuan 4 | Melihat ketersediaan dan mengajukan peminjaman (diwarisi dari Peminjam). |
| **Petugas Laboratorium** | Tetap dari Pertemuan 3 | Mengelola data peralatan, memproses keputusan peminjaman, dan mencatat pengembalian peralatan. |
| **Kepala Laboratorium** | Tetap dari Pertemuan 3 | Melihat laporan peminjaman. |

<!-- TABEL KATALOG USE CASE -->
| ID | Nama use case | Peran dalam model | Sumber Kebutuhan |
|---|---|---|---|
| LAB-UC01 | Lihat ketersediaan peralatan | Fungsi aktor umum Peminjam | LAB-R01, LAB-R07 |
| LAB-UC02 | Kelola data peralatan | Use case UMUM bagi LAB-UC08, LAB-UC09, LAB-UC10 | LAB-R02, LAB-R08 |
| LAB-UC03 | Ajukan peminjaman | Fungsi aktor umum Peminjam; direalisasikan LAB-CO01 | LAB-R03, LAB-R07 |
| LAB-UC04 | Periksa ketersediaan | Perilaku yang disertakan (include) pada LAB-UC03 | LAB-R03 |
| LAB-UC05 | Cetak bukti pengajuan | Tambahan bersyarat pada LAB-UC03 melalui extend | LAB-R04 |
| LAB-UC06 | Proses keputusan peminjaman | Fungsi utama petugas | LAB-R05 |
| LAB-UC07 | Lihat laporan peminjaman | Fungsi utama kepala laboratorium | LAB-R06 |
| LAB-UC08 | Tambah data peralatan | Use case KHUSUS (generalization) dari LAB-UC02 | LAB-R08 |
| LAB-UC09 | Ubah data peralatan | Use case KHUSUS (generalization) dari LAB-UC02 | LAB-R08 |
| LAB-UC10 | Hapus data peralatan | Use case KHUSUS (generalization) dari LAB-UC02 | LAB-R08 |
| LAB-UC11 | Catat pengembalian peralatan | Fungsi utama petugas; direalisasikan LAB-CO02 | LAB-R09 |
| LAB-UC12 | Periksa kondisi peralatan | Perilaku yang disertakan (include) pada LAB-UC11 | LAB-R10 |

<!-- RELASI INCLUDE -->
- LAB-UC03 «include» LAB-UC04
  Alasan: pemeriksaan ketersediaan menjadi bagian validasi saat pengajuan peminjaman.
- LAB-UC11 «include» LAB-UC12
  Alasan: pemeriksaan kondisi peralatan selalu disertakan di dalam proses pencatatan pengembalian.

<!-- RELASI EXTEND -->
- LAB-UC05 «extend» LAB-UC03
  Extension point: Bukti pengajuan tersedia.
  Kondisi: [mahasiswa memilih cetak].
  Alasan: pengajuan tetap berhasil dan sah tanpa harus mencetak bukti.

<!-- RELASI GENERALIZATION -->
- Mahasiswa «generalization» Peminjam
  Alasan: Mahasiswa mewarisi fungsi umum Peminjam (melihat ketersediaan & mengajukan peminjaman) serta memiliki asosiasi khusus mencetak bukti.
- Dosen «generalization» Peminjam
  Alasan: Dosen mewarisi fungsi umum Peminjam dari aktor Peminjam.
- LAB-UC08 «generalization» LAB-UC02 (Tambah Data Peralatan adalah bentuk khusus dari Kelola Data Peralatan)
- LAB-UC09 «generalization» LAB-UC02 (Ubah Data Peralatan adalah bentuk khusus dari Kelola Data Peralatan)
- LAB-UC10 «generalization» LAB-UC02 (Hapus Data Peralatan adalah bentuk khusus dari Kelola Data Peralatan)

<!-- RELASI REALIZATION -->
- LAB-CO01 (Collaboration: Ajukan Peminjaman) «realization» LAB-UC03
  Alasan: collaboration LAB-CO01 mewujudkan perilaku use case Ajukan Peminjaman.
- LAB-CO02 (Collaboration: Catat Pengembalian Peralatan) «realization» LAB-UC11
  Alasan: collaboration LAB-CO02 mewujudkan perilaku use case Catat Pengembalian Peralatan.