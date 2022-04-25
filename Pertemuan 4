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

## Relationship
- user (1 , 1) ----- (0 , N) Booking
- Booking (1 , N) ----- (1 , 1) detail_Booking
- Booking (1 , 1) ----- (0 , 1) Transaksi
- detail_Booking (0 , 1) ----- (1 , N) tiket
- detail_Booking (0 , N) ----- (1 , N) loket
- tiket (1 , N) ----- (1 , 1) jenis_tiket
- jenis_tiket (1 , N) ----- (1 , N) objek_Pendakian
## ERDish
- Each user may order zero or more Booking
- Each Booking must have one and only one detail_Booking
- Each Booking may be paid zero or one Transaksi
- Each detail_Booking must have one or more tiket
- Each detail_Booking must have one or more loket
- Each tiket must have one and only one jenis_tiket
- Each jenis_tiket must have one or more objek_pendakian

## ERD Crow Foot:
