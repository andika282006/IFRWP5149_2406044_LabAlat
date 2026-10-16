<!-- Tulis use case description utama -->

|        Elemen         |                           SIA-UC03 — Ajukan KRS                         |
|-----------------------|-------------------------------------------------------------------------|
| Tujuan                |Menghasilkan pengajuan KRS yang tersimpan menunggu persetujuan dosenwali |
| Aktor utama           | Mahasiswa                                                               |
| Sumber kebutuhan      | SIA-R03, SIA-R04, dan SIA-R05                                           |
| Pemicu                | Mahasiswa memilih fungsi pengajuan KRS                                  |
| Prasyarat             | Mahasiswa telah terautentikasi;datamata kuliah,prasyarat,jadwalperubahan|
| Pascakondisi berhasil | Pengajuan KRS tersimpan dengan status Menunggu persetujuan              |
| Pascakondisi gagal    | Tidak ada pengajuan KRS yang berhasil tersimpan                         |
| Include               | SIA-UC04 — Validasi KRS                                                 |
| Extension point       | Konfirmasi penyimpanan tersedia, pada langkah 5                         |
| Extend                | SIA-UC05 jika [mahasiswa memilih mengunduh bukti]                       |

**Alur utama:**

| Langkah | Tindakan mahasiswa | Respons sistem |
|---------|---|---|
| 1       | Membuka pengajuan KRS | Menampilkan formulir pemilihan mata kuliah |
| 2       | Memilih mata kuliah | Menampung isian mata kuliah yang dipilih |
| 3       | Mengirim pengajuan KRS | Menjalankan SIA-UC04 Validasi KRS (memeriksa kelengkapan, prasyarat, dan benturan jadwal) |
| 4       | | Jika validasi berhasil, menyimpan pengajuan dengan status Menunggu persetujuan |
| 5       | Melihat konfirmasi penyimpanan | Menampilkan status pengajuan; mencapai *extension point* |
| 6       | Mengakhiri pengajuan | Menutup proses pengajuan KRS |