## Soal
1. Basis data relasional dapat langsung dibangun menggunakan perintah SQL di sistem basis data seperti MySQL, dsb tanpa ada perancangan terlebih dahulu. Jelaskan apa keuntungan melakukan perancangan basis data terlebih dahulu (menggunakan ERD ataupun Class Diagram) !
2. Jelaskan bagaimana cara mentransformasikan proses bisnis sebuah organisasi menjadi struktur data di basis data !
3. Rancang solusi digital dari satu permasalahan yang ada di sekitar Anda.
A. Deskripsikan solusi digital tersebut dalam satu paragraf
B. Buat list fitur-fitur yang ada pada solusi digital tersebut
C. Buat ERD notasi Chen dari struktur data yang mewakili fitur2 di solusi digital tersebut
D. Buat ERD notasi Crow Foot dari struktur data logical yang mewakili fitur2 di solusi digital tersebut, lengkap dengan keys, tipe data, dan normalisasi hingga bentuk ke 3
## Jawaban
1) Keuntungan merancang basis data menggunakan ERD atau Class Diagram
Keuntungan menggunakan ERD
- Membantu menganalisis suatu database dengan cara yang lebih cepat dan juga lebih murah.
- Mampu menjalankan relasi antar setiap data yang mempunyai keterkaitan dengan berdasarkan objek yang dihubungkan dengan suatu relasi khusus.
- Membantu menjalankan dokumentasi data yang terdapat dalam suatu database dengan cara melakukan analisis dan identifikasi pada setiap objek ataupun entitas serta relasinya.
- Melakukan suatu pengujian model yang sebelumnya sudah dibuat.
# Keuntungan menggunakan Class Diagram
- Mampu mengilustrasikan model data untuk sistem informasi, terlepas dari apakah model data tersebut rumit atau sederhana.
- Memberikan gambaran umum mengenai skema aplikasi dengan lebih baik.
- Membantumu menyampaikan secara visual kebutuhan spesifik apa pun dari suatu sistem dan menyebarkan informasi tersebut ke bisnis.
- Terdapat bagan terperinci yang menyoroti kode spesifik yang perlu diprogram dan diterapkan ke struktur yang sesuai.
- Menyediakan deskripsi implementasi independen dari tipe yang digunakan dalam sistem untuk kemudian diteruskan di antara komponen-komponennya.
2) Cara mentransformasikan proses bisnis menjadi struktur data
1. Analisa Kebutuhan dan Pengumpulan Data
- Menentukan siapa yang akan memakai dan batas-batas bagaimana aplikasi akan bekerja
- Melakukan pengumpulan informasi dari dokumentasi yang pernah ada
- Menganalisa proses di organisasi dan bagaimana data akan di proses
- Membuat daftar pertanyaan dan melakukan wawancara
- Mendeskripsikan ide solusi bisis & fitur-fitur dari aplikasi
2. Perancangan basis data secara Konseptual
- Merancang/mengkonsep bagaimana database akan dibuat
- Membuat skema alur database, Menentukan entitas & atribut dari aplikasi, perancangan alur transaksi yang nantinya akan dilakukan di database. (Pembuatan Flowchart atau ERD)
3. Perancangan Database secara Logical
- Pemetaan (Transformasi data) Pemetaan ke dalam model data DBMS dengan tidak mempertimbangkan karakteristik atau hal-hal yang khusus yang berlaku pada implementasi DBMS dari model data tsb.
- Penyesuaian Skema ke DBMS Mengatur skema yang dihasilkan dari tahap Pemetaan untuk disesuaikan pada implementasi yang khusus di masa yang akan datang dari suatu model data yang digunakan pada DBMS yang dipilih.
- Menambahkan Primary key, Composite key & Foreign key dari setiap Entitas / Tabel dan menambahkan tipe data untuk setiap atribut.
- Menambahkan cardinality dan optionality untuk setiap Entitas / Tabel dan menerapkan aturan normalisasi.
4. Perancangan Database secara Fisikal
Beberapa hal yang bisa dipertimbangkan dalam pemilihan perancangan basis data secara fisik :
- Response time, waktu akses basis data untuk data item yang ditunjuk oleh suatu transaksi. -Space utility, jumlah ruang penyimpanan yang digunakan oleh file-file basis data dan struktur jalur akses.
- Transaction throughput, rata-rata jumlah transaksi yang dapat diproses per menit oleh sistem basis data dan merupakan parameter kritis dari sistem transaksi (misal : digunakan pada pemesanan tempat di pesawat, bank, dll).
5. Pemilihan DBMS
Beberapa faktor yang bisa dijadikan pertimbangan saat memilih DBMS :
- Faktor Teknik Keberadaan DBMS dalam menjalankan tugasnya seperti jenis-jenis DBMS (relational, network, hierarchical), struktur penyimpanan, dan jalur akses yang mendukung DBMS, pemakai, dll.
- Faktor Ekonomi dan Organisasi Struktur Data, personal yang telah terbiasa menggunakan sistem (programmer), dan tersedianya layananan purna jual.
6. Implementasi Setelah menganalisa permasalahan, mengkonsep proses bisnis, mendesain database, yang terakhir adalah menggabungkan atau mengimplementasikan database yang telah dirancang untuk kemudian mulai dibentuk sebuah aplikasi (dilakukan oleh programmer). Selesainya proses implementasi ini adalah apabila sebuah aplikasi telah selesai dan bisa memproses data sesuai dengan konsep.
3. IDEA SOLUSI BOOKING ONLINE GUNUNG CIKURAY 

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
## ERD Crow's Foot Database
# Setelah Normalisasi:
![image](https://user-images.githubusercontent.com/101303689/165091413-c909bcdd-e592-46b0-95de-38322f071851.png)
