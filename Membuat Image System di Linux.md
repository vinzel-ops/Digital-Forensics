
# Cara Membuat Image System pada Linux

## 1. Disk ke Disk dengan `dd`
Perintah `dd` digunakan untuk menciptakan citra disk secara langsung dari satu disk ke disk lain. Contohnya:
```bash
dd if=/dev/sda2 of=/dev/sdb2 bs=512 noerror
```
- `if=/dev/sda2` merupakan sumber disk.
- `of=/dev/sdb2` menentukan disk tujuan.
- `bs=512` menetapkan ukuran blok data yang ditransfer adalah 512 byte.
- `noerror` menginstruksikan agar proses terus berlangsung meskipun terjadi error, dengan menulis nol di bagian yang error.

## 2. Membuat Citra dengan `DCFLDD`
`DCFLDD` adalah versi lanjutan dari `dd`, dikembangkan oleh Defense Computer Forensics Lab. Contoh penggunaannya:
```bash
dcfldd if=/dev/sda hash=md5 of=/media/diskimage.dd bs=512 noerror
```
- `if=/dev/sda` sebagai perangkat input.
- `hash=md5` untuk menghitung hash MD5 dari citra, memverifikasi integritas citra.
- `of=/media/diskimage.dd` menentukan lokasi file citra.
- `bs=512` untuk transfer data 512 byte setiap kali.
- `noerror` untuk melanjutkan transfer data meski ada error.

## 3. `Dc3DD`
Dikembangkan oleh Defense Cyber Crime Center, `Dc3DD` menawarkan kecepatan yang lebih tinggi dan fitur tambahan dibanding `dd`.

## 4. `Guymager`
`Guymager` adalah alat GUI gratis untuk Linux yang memudahkan pembuatan citra disk.

## 5. `ddrescue`
Digunakan khusus untuk kasus-kasus dengan kluster yang rusak.
```bash
ddrescue -r1 -v /dev/sdb1 /dev/sdc1 ddrescue1.log
```
- `-r1` untuk melakukan percobaan pemulihan.
- `-v` untuk output yang lebih verbose.

## 6. `DD` Melalui Jaringan dengan `Netcat`
- Sumber: 
  ```bash
  dd if=/dev/had bs=16065b | netcat targethost_IP target_port
  ```
- Target: 
  ```bash
  Netcat -l -p target_port | dd of=/dev/hdc bs=16065b
  ```

## 7. `FTK Imager`
Untuk mengunduh FTK Imager, kunjungi: [FTK Imager Version 3.4.3](https://accessdata.com/product-download/ftk-imager-version-3.4.3)

# Panduan Membuat Citra Sistem pada Windows

- `EnCase Forensic`
- `dd.exe`
- `FTK Imager`
- `dc3dd`

# Cara Menyalin Perangkat Seluler

## MOBILedit
Alat khusus untuk perangkat seluler. Kunjungi: [MOBILedit](http://www.mobiledit.com/)

## Android SDK
Alat khusus untuk perangkat Android.

# Menangani Kondisi Perangkat: Menyala dan Mati

## Saat Perangkat Menyala
- Kumpulkan informasi RAM.
- Data terenkripsi mungkin tidak terenkripsi di RAM.
- Identifikasi proses yang sedang berjalan.

## Saat Perangkat Mati
- Biarkan dalam keadaan mati.
- Buat dua salinan bit secara lengkap.

---------------
### HANYA UNTUK PEMBELAJARAN
 ©Vinzel-2023
