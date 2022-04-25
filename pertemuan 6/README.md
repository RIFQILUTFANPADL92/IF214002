Entity menjadi nama dari tabel
Atribute menjadi nama kolom dari tabel
Candidate key = satu atau lebih kolom unik yang akan dijadikan primary key
Primary key = satu atau lebih kolom unik yang menjadi id atau penanda dari satu record / row data
Foreign key = kolom yang digunakan atau diambil dari tabel lain
Composite key = kolom yang merupakan dua atau lebih primary key
Query = sebuah cara atau bahasa untuk membuat, mendapatkan dan memanipulasi data
DDL – Data Definition Language = membuat atau menghapus data/tabel
DQl – Data Query Language = mengambil data
DML – Data Manipulation Language = memanipulasi data
DCL – Data Control Language = menentukan siapa yang dapat mengontrol data

## Penyuaian dengan Proses Bisnis
Setelah dianalisis lebih lanjut, supaya struktur basis data sesuai dengan proses bisnis maka struktur basis data project harus dinormalisasi terlebih dahulu.
2) Normalisasi Tabel
# 🎖️ Normalisasi bentuk ke-1
- Semua tabel telah memiliki primary key (1 kolom, atau multi kolom(composite)).
- Semua tabel tidak memiliki sel yang berisi nilai lebih dari satu.
🎖️ Normalisasi bentuk ke-2
- Semua tabel telah tersertifikasi Normalisasi Bentuk ke 1
- Semua tabel tidak memiliki kolom non key yang bergantung sebagian dari composite key
# 🎖️ Normalisasi bentuk ke-3
Semua tabel telah tersertifikasi Normalisasi Bentuk ke 2
Pembuatan tabel baru :
- Menambahkan tebel kode_pos yang merupakan extend dari tabel user, supaya alamat user lebih lengkap
- Menambahkan tebel jenis_pembayaran yang merupakan extend dari tabel pembayaran, supaya pembayaran dapat dilakukan melalui berbagai jenis pembayaran
