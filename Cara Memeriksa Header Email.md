
# Cara Memeriksa Header Pesan

## Melihat Header Pesan di **Google Mail (GMail) Webmail**:
Login ke akun Anda di halaman web dan buka pesannya (klik pada pesan tersebut). Klik pada "panah-ke-bawah" di pojok kanan atas pesan dan pilih "Tampilkan Asli". Sekarang Anda akan melihat sumber pesan lengkap.

## Melihat Header Pesan di **Yahoo! Mail Webmail**:
Login ke akun Anda di halaman web dan buka pesannya (klik pada pesan tersebut). Klik pada "Aksi" dan pilih "Lihat Header Lengkap".

## Melihat Header Pesan di **Hotmail Webmail**:
Login ke akun Anda di halaman web dan pergi ke daftar pesan. Klik kanan pada pesan dan pilih "Lihat Sumber Pesan".

## Melihat Header Pesan di **MS Outlook**:
Buka pesan di MS Outlook. Sekarang pergi ke "Tampilan" dan pilih "Opsi Pesan" - atau "File" -> "Info" -> "Properti". Lihat pada "Header Internet".

## Melihat Header Pesan di **Thunderbird**:
Buka pesan, kemudian klik pada "Tampilan" dan pilih "Sumber Pesan".

## Melihat Header Pesan di **MS Windows Mail (dan MS Outlook Express)**:
Pilih pesan di daftar, klik kanan pada pesan tersebut dan pilih "Properti" lalu pergi ke "Detail".

# Bidang Header Pesan Standar

- **Return Path**: Alamat email yang harus digunakan untuk pengembalian. Server mail akan mengirim pesan ke alamat email yang ditentukan jika pesan tidak dapat diantar.
- **Delivery-date**: Tanggal pesan dikirimkan.
- **Date**: Tanggal pesan dikirim.
- **Message-ID**: ID dari pesan.
- **X-Mailer**: Klien mail (program mail) yang digunakan untuk mengirim pesan.
- **From**: Pengirim pesan dalam format: "Nama Ramah" <email@alamat.tld>.
- **To**: Penerima pesan dalam format: "Nama Ramah" <email@alamat.tld>.
- **Subject**: Subjek pesan.

# Kerangka Kerja Kebijakan Pengirim (SPF)

Kerangka Kerja Kebijakan Pengirim SPF adalah kerangka kerja untuk mencegah pemalsuan alamat pengirim. Dengan kata-kata sederhana: "SPF digunakan untuk menjelaskan server mail mana yang diizinkan untuk mengirim pesan untuk suatu domain".

## Bagaimana Cara Kerja SPF?

SPF menetapkan metode bagi server mail penerima untuk memverifikasi bahwa email masuk dari suatu domain dikirim dari host yang diotorisasi oleh administrator domain tersebut. Ini menggunakan Sistem Nama Domain (DNS) yang telah mapan. Secara umum, prosesnya bekerja seperti ini:

1. Administrator domain menerbitkan kebijakan yang mendefinisikan server mail yang diotorisasi untuk mengirim email dari domain tersebut. Kebijakan ini disebut sebagai catatan SPF, dan terdaftar sebagai bagian dari catatan DNS domain secara keseluruhan.
2. Ketika server mail masuk menerima email masuk, ia mencari aturan untuk domain pengembalian (Return-Path) di DNS. Server masuk kemudian membandingkan alamat IP pengirim mail dengan alamat IP yang diotorisasi yang didefinisikan dalam catatan SPF.
3. Server mail penerima kemudian menggunakan aturan yang ditentukan dalam catatan SPF domain pengirim untuk memutuskan apakah menerima, menolak, atau memberi tanda pada pesan email.

# Mail Teridentifikasi Kunci Domain (DKIM)

"Mail Teridentifikasi Kunci Domain (DKIM) adalah metode untuk mengaitkan nama domain dengan email, sehingga memungkinkan organisasi untuk mengambil tanggung jawab atas pesan dengan cara yang dapat divalidasi oleh penerima."

## Bagaimana Cara Kerja DKIM?

DKIM memungkinkan organisasi untuk menandatangani pesan email secara digital. Prosesnya bekerja sebagai berikut:

1. Ketika mengirim email, server mail pengirim menambahkan tanda tangan digital ke header pesan. Tanda tangan ini dibuat berdasarkan isi dari pesan dan kunci privat yang hanya diketahui oleh organisasi pengirim.
2. Penerima email dapat memverifikasi tanda tangan digital dengan menggunakan kunci publik yang terkait dengan domain pengirim. Kunci publik ini dapat diakses melalui catatan DNS domain.
3. Jika tanda tangan sesuai, ini menunjukkan bahwa pesan tersebut memang berasal dari domain yang diklaim dan belum diubah selama transmisi.

# SpamAssassin's Header Lines

SpamAssassin adalah perangkat lunak anti-spam yang terpasang pada banyak server mail. Ini memberikan laporan terperinci untuk setiap pesan dengan menambahkan baris dan ringkasan ke header pesan.

- X-Spam-Score <5 berarti (pada sebagian besar sistem) bukan spam, >5 kemungkinan spam dan >15 adalah spam. Spam mungkin akan dihapus segera atau dipindahkan ke folder sampah. Beberapa sistem menambahkan [SPAM] ke subjek, sehingga pesan tersebut dapat dipindahkan ke folder sampah di klien mail menggunakan aturan.

# Unshort URL

Kirim permintaan HTTP HEAD ke URL dan lihat kode responsnya. Jika kode adalah 30x, lihat header Lokasi untuk mendapatkan URL yang tidak disingkat. Jika kode adalah 20x, maka URL tidak dialihkan.

Link ke alat:
- [https://unshorten.it/](https://unshorten.it/)
- [https://linkunshorten.com/](https://linkunshorten.com/)

Layanan Penyingkat URL Populer
- Google - [https://goo.gl/](https://goo.gl/)
- Bitly - [https://bitly.com/](https://bitly.com/)
- Bl.ink - [https://www.bl.ink/](https://www.bl.ink/)
- Polr - [https://polrproject.org/](https://polrproject.org/)
- Rebrandly - [https://www.rebrandly.com/](https://www.rebrandly.com/)
- T2M - [https://t2mio.com/](https://t2mio.com/)
- TinyURL - [https://tinyurl.com/](https://tinyurl.com/)
- URL Shortener by Zapier - [https://zapier.com/apps/url-shortener/integrations](https://zapier.com/apps/url-shortener/integrations)
- Yourls - [http://yourls.org/](http://yourls.org/)

# Cyber Threat Intelligence Open Source

- [https://openphish.com/index.html](https://openphish.com/index.html)
- [https://www.phishtank.com/index.php](https://www.phishtank.com/index.php)
- [https://apility.io/](https://apility.io/)

 ©Vinzel-2023
