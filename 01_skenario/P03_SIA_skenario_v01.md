<!-- deskripsi skenario -->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

<!-- tabel kebutuhan -->
|  ID   |                        Kebutuhan tugas                         |
|-------|----------------------------------------------------------------|
|SIA-R01|             Mahasiswa dapat melihat jadwal kuliah              |
|SIA-R02|          Admin akademik dapat mengelola jadwal kuliah          |
|SIA-R03|                 Mahasiswa dapat mengajukan KRS                 |
|SIA-R04|        Sistem memvalidasi KRS sebagai bagian pengajuan         |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi |
|       |                          pengajuan                             |
|SIA-R06|   Dosen wali dapat memproses persetujuan atau penolakan KRS    |

<!-- batas sistem dan aturan -->
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar
tugas.

<!-- tabel identifikasi aktor  -->
|  Aktor       |                 Tujuan terhadap sistem             |
|--------------|----------------------------------------------------|
|Mahasiswa     | Mengajukan KRS dan mengunduh bukti pengajuan       |
|Dosen wali    | Memproses persetujuan atau penolakan KRS           |

<!-- katalog use case -->
|   ID   |  Nama  |   use   |          case Peran dalam model            |
|--------|--------|---------|--------------------------------------------|
|SIA-UC01| Lihat  | jadwal  |       kuliah Fungsi utama mahasiswa        |
|SIA-UC02| Kelola | jadwal  |    kuliah Fungsi utama admin akademik      |
|SIA-UC03| Ajukan |   KRS   |          Fungsi utama mahasiswa            |
|SIA-UC04|Validasi|   KRS   |       Perilaku yang disertakan UC03        |
|SIA-UC05| Unduh  |  bukti  |pengajuan KRS Tambahan bersyarat pada UC03  |
|SIA-UC06| Proses |keputusan|        KRS Fungsi utama dosen wali         |

<!-- relasi include -->
SIA-UC03 «include» SIA-UC04
Alasan: Validasi KRS menjadi bagian wajib yang harus dilalui pada saat pengajuan KRS.

<!-- relasi extend -->
SIA-UC05 «extend» SIA-UC03
Extension point: Konfirmasi penyimpanan tersedia.
Kondisi: [mahasiswa memilih mengunduh bukti].
Alasan: Pengajuan KRS tetap berhasil tersimpan meskipun mahasiswa tidak mengunduh bukti.