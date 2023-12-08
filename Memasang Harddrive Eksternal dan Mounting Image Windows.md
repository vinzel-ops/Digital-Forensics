
# Memasang Harddrive Eksternal dan Mounting Image Windows

## Memasang Harddrive Eksternal
Langkah-langkah untuk memasang harddrive eksternal di sistem operasi Linux adalah sebagai berikut:

1. Identifikasi perangkat:
   - Gunakan perintah `fdisk -l` untuk mengidentifikasi harddrive eksternal.

2. Membuat folder:
   - Buat folder untuk mount point dengan perintah `sudo mkdir /media/name_of_device`.

3. Mengedit file /etc/fstab:
   - Tambahkan baris seperti `/dev/sdb1 /mnt/sdb1 vfat defaults 0 0` ke dalam file `/etc/fstab`.

4. Memasang perangkat:
   - Gunakan perintah `mount -a` untuk memasang perangkat.

Beberapa alat forensik akan memasang perangkat eksternal secara otomatis, termasuk:
- EnCase
- C.A.IN.E
- Ewfmount
- Xmount

## Mounting Image Windows
Berikut adalah alat-alat yang dapat digunakan untuk memasang image Windows:

1. Arsenal Image Mounter (AIM):
   - Alat gratis yang dapat memasang berbagai format termasuk file terpisah dan file Encase.

2. FTK Imager:
   - Menawarkan kemampuan mounting image, namun tidak mendukung file Encase versi terbaru.

3. OSFMount

4. P2-eXplorer

Alat-alat ini sangat penting dalam konteks forensik digital, memungkinkan para profesional untuk menganalisis data dari image sistem tanpa harus mengakses fisiknya secara langsung.

---------------
### HANYA UNTUK PEMBELAJARAN
 ©Vinzel-2023
