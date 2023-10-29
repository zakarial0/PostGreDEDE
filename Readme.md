# catatan command postgreSQL

buat user 
```
create user 'nama' password 'apaaja' role 'superuser dll';
```
liat user
```
\du
```
login psql 
```
psql --username=postgres
```

liat semua database
```psql
    \l

    \l+
    lebih detail
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

menghubungkan data tabel
```
ALTER TABLE public.provider ADD CONSTRAINT fk_user FOREIGN KEY (user_id) REFERENCES user(id);
```

mengambil data dari tabel 1 ke tabel lain
```
 SELECT <a.*, b.nama as kartu> FROM <public.user as a> LEFT JOIN <public.provider as b> ON <user_id=a.id>;
```