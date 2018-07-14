---
date: 2018-07-16
title: perancangan-database
categories:
  - sipd
description: Perancangan database Sistem Informasi Pemerintah Daerah Pemerintah Provinsi Banten
type: Document
---

## kelompok_data

Kelompok data atau lebih sering disebut dengan istilah "urusan", adalah data yang memiliki urutan tertinggi dalam sistem yang akan rancang. Tabel kelompok data adalah tabel yang dipakai untuk menyimpan data kelompok data atau urusan tersebut, didalam tabel ini terdapat beberapa field yang digunakan untuk menyimpan data dari kelompok data tersebut.

### Struktur tabel kelompok data

Struktur tabel kelompok data terdiri dari:

| Name     | Type         | Unsigned | Null     | Keterangan                                                     |
|----------|--------------|----------|----------|----------------------------------------------------------------|
| id       | int(10)      | UNSIGNED | NOT NULL | Merupakan ID dari data kelompok data                           |
| uuid     | varchar(128) |          | NOT NULL | Merupakan Universal Unique ID dari data kelompok data          |
| langcode | varchar(12)  |          | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam kelompok data     |
| user_id  | int(10)      |          | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah kelompok data |
| name     | varchar(50)  |          | NOT NULL | Merupakan nama dari kelompok data                              |
| status   | tinyint(4)   |          | NOT NULL | Merupakan status aktif tidaknya kelompok data                  |
| created  | int(11)      |          | NULL     | Merupakan waktu saat dibuatnya kelompok data                   |
| changed  | int(11)      |          | NULL     | Merupakan waktu saat diubahnya kelompok data                   |

### Referensi

- Menggunakan referensi pada tabel :
- Digunakan sebagai referensi pada tabel : jenis_data

## Jabatan

Jabatan data adalah tabel yang menampung jabatan yang ada di lingkungan Pemerintah Provinsi Banten. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan data jabatan. Berikut adalah field yang terdapat pada tabel jabatan.

### Struktur table jabatan

| Name     | Type         | Unsigned | Null     | Keterangan                                               |
|----------|--------------|----------|----------|----------------------------------------------------------|
| id       | int(10)      | UNSIGNED | NOT NULL | Merupakan ID dari data jabatan                           |
| uuid     | varchar(128) |          | NOT NULL | Merupakan Universal Unique ID dari data jabatan          |
| langcode | varchar(12)  |          | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam jabatan     |
| user_id  | int(10)      |          | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah jabatan |
| name     | varchar(50)  |          | NOT NULL | Merupakan nama dari jabatan                              |
| eselon   | varchar(255) |          | NOT NULL | Merupakan tingkat eselon dari jabatan terkait            |
| status   | tinyint(4)   |          | NOT NULL | Merupakan status aktif tidaknya jabatan                  |
| created  | int(11)      |          | NULL     | Merupakan waktu saat dibuatnya jabatan                   |
| changed  | int(11)      |          | NULL     | Merupakan waktu saat diubahnya jabatan                   |

### Referensi

- Menggunakan referensi pada tabel :
- Digunakan sebagai referensi pada tabel : opd
