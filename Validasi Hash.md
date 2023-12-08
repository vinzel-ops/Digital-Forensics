# Alat Validasi Hash
Berikut adalah daftar alat validasi hash yang umum digunakan:
- HashCalc: Sebuah alat yang efisien untuk menghitung nilai hash file dan teks.
- MD5 Calculator: Alat sederhana untuk menghasilkan nilai hash MD5 dari file.
- HashMyFiles: Aplikasi yang memungkinkan pengguna untuk menghitung nilai hash untuk file dan direktori.
- Md5sum: Utilitas standar untuk menghasilkan nilai hash MD5.
- Chaosmd5: Alat yang menghasilkan nilai hash MD5 dengan cara yang unik dan berbeda.
- Autopsy: Alat forensik digital yang juga menyediakan fungsionalitas penghitungan hash.
- dc3dd: Sebuah alat yang dirancang untuk memfasilitasi penciptaan nilai hash pada saat proses duplikasi data.

## Tipe Hash MD5
- MD5 menghasilkan nilai hash 128-bit.
- Sangat jarang, namun ada kemungkinan dua file berbeda menghasilkan nilai hash MD5 yang sama.

## Tipe Hash Secure Hash Algorithm (SHA)
- Variasi SHA termasuk SHA-1, SHA-224, SHA-256, SHA-384, dan SHA-512.
- SHA-1 menghasilkan ringkasan pesan sepanjang 160-bit.
- SHA-224 menghasilkan ringkasan sepanjang 224-bit, dengan variasi lainnya sesuai dengan angka yang direpresentasikan.

## md5deep
- Perintah `md5deep file_name` digunakan untuk menghitung nilai hash MD5 dari sebuah file.
- Perintah `md5deep -wM file_name_1 file_name_2` digunakan untuk membandingkan hash dari dua file.

## Alat Sederhana
- Perintah `sha256sum file_name` digunakan untuk menghitung nilai hash SHA-256 dari sebuah file.
- Perintah `md5sum file_name` digunakan untuk menghitung nilai hash MD5 dari sebuah file.

## Cara Memeriksa Hash

### hashdeep
```
root@kali:~/hash_test# hashdeep hash.txt 
%%%% HASHDEEP-1.0
%%%% size,md5,sha256,filename
## Invoked from: /root/hash_test
## # hashdeep hash.txt
## 
18,ed650c02bd24a50eeef0b7b4a7a444f8,1b84e07e77fab43901d7701eb1468e4074c642175b987078eebf231cea913b38,/root/hash_test/hash.txt
```

### split
```
root@kali:~/hash_test# split -n 5 hash.txt hash_parts
root@kali:~/hash_test# ls
hash_partsaa  hash_partsab  hash_partsac  hash_partsad  hash_partsae  hash.txt
```

### combine
```
root@kali:~/hash_test# cat hash_partsa* > hash_1.txt
```

### Akhirnya Memeriksa
```
root@kali:~/hash_test# hashdeep hash.txt | egrep ^[0-9].*,.* && hashdeep hash_1.txt | egrep ^[0-9].*,.*
18,ed650c02bd24a50eeef0b7b4a7a444f8,1b84e07e77fab43901d7701eb1468e4074c642175b987078eebf231cea913b38,/root/hash_test/hash.txt
18,ed650c02bd24a50eeef0b7b4a7a444f8,1b84e07e77fab43901d7701eb1468e4074c642175b987078eebf231cea913b38,/root/hash_test/hash_1.txt
```
