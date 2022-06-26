## Proyek Aplikasi 'Tiketku'
### DDL
```sql
CREATE TABLE IF NOT EXISTS public.booking
(
    id_booking integer NOT NULL,
    id_user integer NOT NULL,
    tanggal_booking date NOT NULL,
    status status_booking NOT NULL,
    total_harga integer NOT NULL,
    id_transaksi integer NOT NULL,
    CONSTRAINT booking_pkey PRIMARY KEY (id_booking),
    CONSTRAINT id_transaksi FOREIGN KEY (id_transaksi)
        REFERENCES public.transaksi (id_transaksi) MATCH SIMPLE
        ON UPDATE NO ACTION
        ON DELETE NO ACTION
        NOT VALID,
    CONSTRAINT id_user FOREIGN KEY (id_user)
        REFERENCES public.users (id_user) MATCH SIMPLE
        ON UPDATE NO ACTION
        ON DELETE NO ACTION
        NOT VALID
)

TABLESPACE pg_default;
```
```sql
```
```sql
CREATE TABLE IF NOT EXISTS public.detail_booking
(
    id_detail_pem integer NOT NULL,
    id_booking integer NOT NULL,
    id_tiket integer NOT NULL,
    id_loket integer NOT NULL,
    tanggal_pendakian date NOT NULL,
    jumlah_tiket integer NOT NULL,
    total_harga integer NOT NULL,
    CONSTRAINT detail_booking_pkey PRIMARY KEY (id_detail_pem)
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.jenis_tiket
(
    id_jenis_tiket integer NOT NULL,
    id_obj_pendakian integer NOT NULL,
    nama character varying(24) COLLATE pg_catalog."default" NOT NULL,
    harga integer NOT NULL,
    CONSTRAINT jenis_tiket_pkey PRIMARY KEY (id_jenis_tiket),
    CONSTRAINT id_obj_wisata FOREIGN KEY (id_obj_pendakian)
        REFERENCES public.objek_pendakian (id_obj_pendakian) MATCH SIMPLE
        ON UPDATE NO ACTION
        ON DELETE NO ACTION
        NOT VALID
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.jenis_transaksi
(
    id_jenis_pemb integer NOT NULL,
    nama_pemb character varying(24) COLLATE pg_catalog."default" NOT NULL,
    metode_pemb character varying(24) COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT jenis_transaksi_pkey PRIMARY KEY (id_jenis_pemb)
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.kode_pos
(
    kode_pos integer NOT NULL,
    provinsi character varying(50) COLLATE pg_catalog."default" NOT NULL,
    kota character varying(50) COLLATE pg_catalog."default" NOT NULL,
    kecamatan character varying(50) COLLATE pg_catalog."default" NOT NULL,
    desa character varying(50) COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT kode_pos_pkey PRIMARY KEY (kode_pos)
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.loket
(
    id_loket integer NOT NULL,
    nama character varying(50) COLLATE pg_catalog."default" NOT NULL,
    lokasi character varying(50) COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT loket_pkey PRIMARY KEY (id_loket)
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.objek_pendakian
(
    id_obj_pendakian integer NOT NULL,
    nama character varying(50) COLLATE pg_catalog."default" NOT NULL,
    lokasi character varying(50) COLLATE pg_catalog."default" NOT NULL,
    photo character varying(256) COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT objek_pendakian_pkey PRIMARY KEY (id_obj_pendakian)
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.tiket
(
    id_tiket integer NOT NULL,
    id_jenis_tiket integer NOT NULL,
    stok integer NOT NULL,
    CONSTRAINT id_tiket PRIMARY KEY (id_tiket)
        INCLUDE(id_jenis_tiket)
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.transaksi
(
    id_transaksi integer NOT NULL,
    id_jenis_pemb integer NOT NULL,
    kode_transaksi integer NOT NULL,
    tanggal_transaksi date NOT NULL,
    img_barcode character varying(256) COLLATE pg_catalog."default" NOT NULL,
    status status_bayar NOT NULL,
    CONSTRAINT transaksi_pkey PRIMARY KEY (id_transaksi),
    CONSTRAINT kode_transaksi UNIQUE (kode_transaksi)
        INCLUDE(img_barcode),
    CONSTRAINT id_jenis_pemb FOREIGN KEY (id_jenis_pemb)
        REFERENCES public.jenis_transaksi (id_jenis_pemb) MATCH SIMPLE
        ON UPDATE NO ACTION
        ON DELETE NO ACTION
        NOT VALID
)

TABLESPACE pg_default;
```
```sql
CREATE TABLE IF NOT EXISTS public.users
(
    id_user integer NOT NULL,
    kode_pos integer NOT NULL,
    email character varying(50) COLLATE pg_catalog."default" NOT NULL,
    pass_user character varying(256) COLLATE pg_catalog."default" NOT NULL,
    is_admin integer NOT NULL,
    nama_lengkap character varying(50) COLLATE pg_catalog."default" NOT NULL,
    no_telp character varying(24) COLLATE pg_catalog."default" NOT NULL,
    alamat character varying(256) COLLATE pg_catalog."default" NOT NULL,
    photo character varying(256) COLLATE pg_catalog."default" NOT NULL,
    CONSTRAINT users_pkey PRIMARY KEY (id_user),
    CONSTRAINT email UNIQUE (email)
        INCLUDE(email),
    CONSTRAINT kode_pos FOREIGN KEY (kode_pos)
        REFERENCES public.kode_pos (kode_pos) MATCH SIMPLE
        ON UPDATE NO ACTION
        ON DELETE NO ACTION
        NOT VALID
)

TABLESPACE pg_default;

```

### DML
