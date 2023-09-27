# catatan command postgreSQL

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
```CREATE TABLE public.nama_table (
    id SERIAL PRIMARY KEY,
    nama VARCHAR(100),
    saldo INT );
```