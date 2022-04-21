Jawaban
1) Keuntungan merancang basis data menggunakan ERD atau Class Diagram
Keuntungan menggunakan ERD
Membantu menganalisis suatu database dengan cara yang lebih cepat dan juga lebih murah.
Mampu menjalankan relasi antar setiap data yang mempunyai keterkaitan dengan berdasarkan objek yang dihubungkan dengan suatu relasi khusus.
Membantu menjalankan dokumentasi data yang terdapat dalam suatu database dengan cara melakukan analisis dan identifikasi pada setiap objek ataupun entitas serta relasinya.
Melakukan suatu pengujian model yang sebelumnya sudah dibuat.
Keuntungan menggunakan Class Diagram
Mampu mengilustrasikan model data untuk sistem informasi, terlepas dari apakah model data tersebut rumit atau sederhana.
Memberikan gambaran umum mengenai skema aplikasi dengan lebih baik.
Membantumu menyampaikan secara visual kebutuhan spesifik apa pun dari suatu sistem dan menyebarkan informasi tersebut ke bisnis.
Terdapat bagan terperinci yang menyoroti kode spesifik yang perlu diprogram dan diterapkan ke struktur yang sesuai.
Menyediakan deskripsi implementasi independen dari tipe yang digunakan dalam sistem untuk kemudian diteruskan di antara komponen-komponennya.
2) Cara mentransformasikan proses bisnis menjadi struktur data
Analisa Kebutuhan dan Pengumpulan Data

Menentukan siapa yang akan memakai dan batas-batas bagaimana aplikasi akan bekerja
Melakukan pengumpulan informasi dari dokumentasi yang pernah ada
Menganalisa proses di organisasi dan bagaimana data akan di proses
Membuat daftar pertanyaan dan melakukan wawancara
Mendeskripsikan ide solusi bisis & fitur-fitur dari aplikasi
Perancangan basis data secara Konseptual

Merancang/mengkonsep bagaimana database akan dibuat
Membuat skema alur database, Menentukan entitas & atribut dari aplikasi, perancangan alur transaksi yang nantinya akan dilakukan di database. (Pembuatan Flowchart atau ERD)
Perancangan Database secara Logical

Pemetaan (Transformasi data) Pemetaan ke dalam model data DBMS dengan tidak mempertimbangkan karakteristik atau hal-hal yang khusus yang berlaku pada implementasi DBMS dari model data tsb.
Penyesuaian Skema ke DBMS Mengatur skema yang dihasilkan dari tahap Pemetaan untuk disesuaikan pada implementasi yang khusus di masa yang akan datang dari suatu model data yang digunakan pada DBMS yang dipilih.
Menambahkan Primary key, Composite key & Foreign key dari setiap Entitas / Tabel dan menambahkan tipe data untuk setiap atribut.
Menambahkan cardinality dan optionality untuk setiap Entitas / Tabel dan menerapkan aturan normalisasi.
Perancangan Database secara Fisikal

Beberapa hal yang bisa dipertimbangkan dalam pemilihan perancangan basis data secara fisik :

Response time, waktu akses basis data untuk data item yang ditunjuk oleh suatu transaksi. -Space utility, jumlah ruang penyimpanan yang digunakan oleh file-file basis data dan struktur jalur akses.
Transaction throughput, rata-rata jumlah transaksi yang dapat diproses per menit oleh sistem basis data dan merupakan parameter kritis dari sistem transaksi (misal : digunakan pada pemesanan tempat di pesawat, bank, dll).
Pemilihan DBMS

Beberapa faktor yang bisa dijadikan pertimbangan saat memilih DBMS :

Faktor Teknik Keberadaan DBMS dalam menjalankan tugasnya seperti jenis-jenis DBMS (relational, network, hierarchical), struktur penyimpanan, dan jalur akses yang mendukung DBMS, pemakai, dll.
Faktor Ekonomi dan Organisasi Struktur Data, personal yang telah terbiasa menggunakan sistem (programmer), dan tersedianya layananan purna jual.
Implementasi Setelah menganalisa permasalahan, mengkonsep proses bisnis, mendesain database, yang terakhir adalah menggabungkan atau mengimplementasikan database yang telah dirancang untuk kemudian mulai dibentuk sebuah aplikasi (dilakukan oleh programmer). Selesainya proses implementasi ini adalah apabila sebuah aplikasi telah selesai dan bisa memproses data sesuai dengan konsep.
