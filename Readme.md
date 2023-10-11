# catatan command postgreSQL

login psql 
```
psql --username=postgres
```

liat semua database
```psql
    \l
```
clear terminal
```psql
    \! clear
```

create database
```psql
    CREATE DATABASE nama_database;
```

pindah ke database
```psql
    /c nama_database
```

hapus database
```psql
    DROP DATABASE nama_database;
```

membuat table (pulsa)
```
    CREATE TABLE public.nama_table (
    id SERIAL PRIMARY KEY,
    nama VARCHAR(100),
    saldo INT );
```

melihat semua table
```
    \dt
```

melihat isi table
```
\d <nama_tabel>;
```

mengambil data tabel
```
SELECT * FROM <public.user>;
```

menambahkan data ke tabel
```
INSERT INTO <public.user> (nama, saldo) VALUES ('Dede','0');
```

update data pada tabel
```
UPDATE <public.user> SET <saldo=10000> WHERE <id=1>;
```

menghapus data di tabel
```
DELETE FROM <public.user> WHERE <id=2>;
```