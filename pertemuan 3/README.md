## IDEA SOLUSI BOOKING ONLINE GUNUNG CIKURAY 

## DESKRIPSI
Aplikasi ini berfokus untuk mempermudah simaksi / Booking tiket online Gunung Cikuray yang di sertakan fitur transaksi. Yang dinamakan Booking Online Gunung Cikuray. Beberapa fitur yang menjadi poin penting aplikasi in diantaranya:
- Memudahkan dalam pemesanan pada saat ingin melakukan booking Online
- Melihat Tenggat waktu yang di rencanakan apakah sedang penuh atau kosong
- Fitur slot penuh yang otomatis akan menutup laman sehingga pengguna tidak dapat membooking di hari yang sedang penuh.
- Booking Online dengan cepat langsung dari aplikasi dan melakukan transaksi saat itu juga.
 
DIAGRAM ENTITAS DAN ATRIBUT
## user (Booking)
- id_user
- email
- password
- nama_lengkap
- no_telepon
- kota_asal
- alamat
photo
## Booking
- id_Booking 
- id_user
- id_pembayaran
- tanggal Booking
- status
- kode token
- cek ulang
- transaksi
## detail_Booking Online
- id_detail_Booking
- id_pemesanan
- id_loket
- jumlah
- total_harga
## Transaksi
- ID Transaksi
- Kode transaksi
- Jenis Transaksi
- Nama Transaksi
## tiket Simaksi
- id_tiket
- id_jenis_tiket
- harga
## jenis_tiket
- id_jenis_tiket
- id_objek_pendakian
- nama pembooking
## loket
- id_loket
- nama
- lokasi
## objek_Pendakian
- ID Objek pendakian
- Nama
- Lokasi
- photto

## Erd Crow foot:
![image](https://user-images.githubusercontent.com/101303689/165088139-2db754ea-3cfe-45dc-87ad-4181de5a711f.png)
![image](https://user-images.githubusercontent.com/101303689/165088192-f71a4756-0813-42d8-972f-4eb4f9f72413.png)
