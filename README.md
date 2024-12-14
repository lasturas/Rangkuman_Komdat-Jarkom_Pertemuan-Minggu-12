# Rangkuman_Komdat-Jarkom_Pertemuan-Minggu-12

# Network Security: NAT, Tunneling, VPN

## Pendahuluan
Keamanan jaringan (Network Security) adalah praktik melindungi jaringan komputer dari ancaman internal maupun eksternal. Beberapa teknologi utama yang digunakan adalah NAT, Tunneling, dan VPN.

---

## Network Address Translation (NAT)

![image](https://github.com/user-attachments/assets/a7b9d369-487b-415f-b83d-4eb2071c4fe9)

### Pengertian
NAT mengubah alamat IP pada header paket data saat melewati router, memungkinkan beberapa perangkat di jaringan lokal menggunakan satu alamat IP publik untuk mengakses internet.

### Jenis-Jenis NAT
- **Static NAT**: Memetakan satu alamat IP lokal ke satu alamat IP publik.
  - *Contoh*: Server lokal dengan IP 192.168.1.100 dipetakan ke IP publik 203.0.113.1.
- **Dynamic NAT**: Memetakan alamat IP lokal ke IP publik secara dinamis dari pool.
  - *Contoh*: Pool IP publik 203.0.113.2-203.0.113.10.
- **PAT (Port Address Translation)**: Berbagi satu alamat IP publik dengan membedakan nomor port.
  - *Contoh*: Dua perangkat lokal menggunakan IP publik 203.0.113.11 dengan port berbeda.

### Keuntungan
- Mengurangi kebutuhan alamat IP publik.
- Menyembunyikan jaringan internal.

### Keterbatasan
- Menambah latensi.
- Tidak mendukung beberapa protokol tertentu.

---

## Tunneling

![image](https://github.com/user-attachments/assets/18020056-69fc-4d93-bae3-441e1fd062ed)

### Pengertian
Tunneling mengenkapsulasi paket data dalam protokol lain untuk melewati jaringan yang tidak mendukung protokol asli.

### Cara Kerja
1. Data asli dikemas dalam protokol tambahan.
2. Paket data dienkripsi (opsional).
3. Data dikirim melalui "terowongan" menuju tujuan.

### Jenis Protokol Tunneling
- **GRE (Generic Routing Encapsulation)**: Untuk berbagai payload.
- **IPsec**: Untuk data terenkripsi.
- **L2TP**: Digunakan bersama IPsec.

### Kelebihan
- Mendukung protokol yang tidak didukung jaringan.
- Menambah keamanan dengan enkripsi.

### Kekurangan
- Meningkatkan overhead jaringan.
- Membutuhkan konfigurasi tambahan.

---

## Virtual Private Network (VPN)

### Pengertian
VPN memungkinkan koneksi aman antara perangkat dan jaringan lain melalui internet menggunakan tunneling dan enkripsi.

### Cara Kerja
1. Klien VPN memulai koneksi ke server VPN.
2. Data dienkripsi di perangkat lokal.
3. Data terenkripsi dikirim ke server VPN.
4. Server VPN meneruskan data ke tujuan dengan IP server.

### Jenis VPN
- **Remote Access VPN**: Menghubungkan individu ke jaringan perusahaan.
- **Site-to-Site VPN**: Menghubungkan dua jaringan berbeda.
- **Client-Based VPN**: Koneksi perangkat ke server VPN.

### Keuntungan
- Menyembunyikan alamat IP.
- Melindungi data dengan enkripsi.
- Akses konten yang dibatasi geografis.

### Kekurangan
- Memperlambat koneksi internet.
- Bergantung pada penyedia VPN.

---

## Perbandingan NAT, Tunneling, dan VPN

| **Aspek**             | **NAT**                     | **Tunneling**                 | **VPN**                      |
|-----------------------|----------------------------|------------------------------|-----------------------------|
| **Fungsi Utama**      | Mengelola alamat IP        | Enkapsulasi data             | Keamanan & privasi          |
| **Keamanan**          | Minimal                   | Sedang (dengan enkripsi)     | Tinggi (dengan enkripsi)    |
| **Penggunaan**        | Jaringan lokal            | Protokol lintas jaringan     | Koneksi aman                |
| **Kompleksitas**      | Rendah                    | Sedang                       | Tinggi                      |

---

## Kesimpulan
NAT, Tunneling, dan VPN memiliki peran penting dalam keamanan jaringan. NAT digunakan untuk mengelola alamat IP dan memungkinkan perangkat dalam jaringan lokal menggunakan satu alamat IP publik. Tunneling memungkinkan data melewati jaringan yang tidak mendukung protokol tertentu dengan enkapsulasi data, serta memberikan keamanan tambahan dengan enkripsi. VPN merupakan solusi yang lebih lengkap untuk melindungi privasi dan keamanan data dengan mengenkripsi komunikasi antar perangkat dan jaringan. Memahami peran dan penerapan masing-masing teknologi membantu memilih solusi terbaik untuk kebutuhan jaringan.
