# Meta Data
## EXIFTOOL - Alat Analisis Meta Data

EXIFTOOL merupakan sebuah alat yang digunakan untuk mengekstrak dan menampilkan informasi meta data dari berbagai jenis file. Alat ini sangat berguna dalam bidang forensik digital dan analisis keamanan informasi.

### Instalasi EXIFTOOL
EXIFTOOL tidak termasuk dalam paket alat default Kali Linux. Untuk menginstalnya, Anda dapat menggunakan perintah `apt-get`:

```bash
apt-get install exiftool
```

### Penggunaan EXIFTOOL
Setelah terinstal, EXIFTOOL dapat digunakan untuk mengekstrak informasi meta data dari berkas. Misalnya, untuk menganalisis file bernama `Dokumen.docx` yang berada di desktop, gunakan perintah berikut:

```bash
exiftool /root/Desktop/Dokumen.docx
```

### Jenis Informasi yang Ditampilkan
EXIFTOOL akan menampilkan berbagai informasi meta data yang terkandung dalam file, seperti:

- Pembuat Berkas (Creator)
- Nama Perusahaan (Company)
- Tanggal Pembuatan dan Modifikasi
- Hak Akses dan Izin Berkas (Permissions)
- Aplikasi yang Digunakan untuk Membuat atau Mengedit
- dan informasi lainnya tergantung pada jenis dan isi dari file tersebut.

Informasi ini sangat berguna dalam investigasi forensik digital, di mana detail-detail seperti pembuat berkas, tanggal modifikasi, dan perangkat lunak yang digunakan dapat memberikan petunjuk penting dalam suatu penyelidikan.

Vinzel - 2023
