
# Lateral Movement (Gerakan Lateral)
## Akses Desktop Jarak Jauh (RDP)

### Catatan Event Log
- `security.evtx`
  - 4648 – Logon dengan kredensial alternatif - jika NLA diaktifkan pada tujuan
    * Nama Pengguna yang Sedang Login
    * Nama Pengguna Alternatif
    * Nama Host Tujuan/IP
    * Nama Proses
  
- `Microsoft-WindowsTerminalServicesRDPClient%4Operational.evtx`
  - 1024 - Nama Host Tujuan
  - 1102 - Alamat IP Tujuan

### Registry
- Tujuan desktop jarak jauh dilacak per pengguna
  - `NTUSER\Software\Microsoft\TerminalServer Client\Servers`

- ShimCache – **SYSTEM**
  - `mstsc.exe` - Klien Desktop Jarak Jauh
  
- BAM/DAM – **SYSTEM** – Waktu Terakhir Dieksekusi
  - `mstsc.exe` Klien Desktop Jarak Jauh

- **AmCache.hve** – Waktu Pertama Dieksekusi
   - `mstsc.exe`

- UserAssist – **NTUSER.DAT**
   - Eksekusi klien `mstsc.exe` Desktop Jarak Jauh
   - Waktu Terakhir Dieksekusi
   - Jumlah Kali Dieksekusi
   
- RecentApps – **NTUSER.DAT**
   - Eksekusi klien `mstsc.exe` Desktop Jarak Jauh
   - Waktu Terakhir Dieksekusi
   - Jumlah Kali Dieksekusi
   - Subkey `RecentItems` melacak tujuan dan waktu koneksi

### Sistem Berkas
- Jumplist – `C:\Users\<Username>\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations\`
   - `{MSTSC-APPID}-automaticDestinations-ms`
   - Melacak tujuan dan waktu koneksi Desktop Jarak Jauh
- Prefetch – `C:\Windows\Prefetch\`
   - `mstsc.exe-{hash}.pf`
- Bitmap Cache – `C:\USERS\<USERNAME>\AppData\Local\Microsoft\TerminalServer Client\Cache`
   - `bcache##.bmc`
   - `cache####.bin`

### Memetakan Penyebaran Jaringan - `net.exe` ke C$ atau Admin$
### Catatan Event Log
### Registry
### Sistem Berkas

---------------
### HANYA UNTUK PEMBELAJARAN
 ©Vinzel-2023
