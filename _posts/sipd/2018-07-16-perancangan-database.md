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

## Opd

Opd adalah singkatan dari Organisasi Perangkat Daerah, yang merupakan satuan kerja yang ada di lingkungan Pemerintah Provinsi Banten. opd disini adalah tabel yang menampung data opd yang ada di lingkungan Pemerintah Provinsi Banten, didalam tabel opd ini terdapat beberapa field yang terkait dengan opd. Berikut adalah field yang ada dalam tabel opd.

### Struktur tabel opd

| Name         | Type         | Unsigned | Null     | Keterangan                                                                             |
|--------------|--------------|----------|----------|----------------------------------------------------------------------------------------|
| id           | int(10)      | UNSIGNED | NOT NULL | Merupakan ID dari data opd                                                             |
| uuid         | varchar(128) |          | NOT NULL | Merupakan Universal Unique ID dari data opd                                            |
| langcode     | varchar(12)  |          | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam opd                                       |
| user_id      | int(10)      |          | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah opd                                   |
| kode         | varchar(128) |          | NOT NULL | Merupakan kode opd dari kelompok data, saatini digunakan kode opd dari aplikasi simpeg |
| name         | varchar(50)  |          | NOT NULL | Merupakan nama dari opd                                                                |
| induk        | int(10)      | UNSIGNED | NOT NULL | Merupakan ID autoincrement dari tabel opd                                              |
| induk_uuid   | varchar(128) |          | NOT NULL | Merupakan UUID induk opda dari tabel opd                                               |
| pejabat      | varchar(191) |          | NULL     | Perupakan Pejabat yang terkait dengan jabatan pada opd                                 |
| jabatan      | int(10)      | UNSIGNED | NOT NULL | Merupakan jabatan ID yang ada pada opd                                                 |
| jabatan_uuid | varchar(128) |          | NOT NULL | Merupak UUID dari kolom opd                                                            |
| status       | tinyint(4)   |          | NOT NULL | Merupakan status aktif tidaknya opd                                                    |
| created      | int(11)      |          | NULL     | Merupakan waktu saat dibuatnya opd                                                     |
| changed      | int(11)      |          | NULL     | Merupakan waktu saat diubahnya opd                                                     |

### Referensi

- Menggunakan referensi pada tabel : jabatan
- Digunakan sebagai referensi pada tabel : jenis_data

## jenis_data

Jenis data atau lebih sering disebut dengan istilah "variabel" adalah tabel yang menampung data dari jenis data atau variabel tersebut. Jenis data adalah tabel yang menampung jenis data atau variabel  yang ada di lingkungan Pemerintah Provinsi Banten. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan jenis data. Berikut adalah field yang terdapat pada tabel jenis data.

### Struktur table jenis data

| Name               | Type         | Unsigned | Null     | Keterangan                                               |
|--------------------|--------------|----------|----------|----------------------------------------------------------|
| id                 | int(10)      | UNSIGNED | NOT NULL | Merupakan ID dari data jabatan                           |
| uuid               | varchar(128) |          | NOT NULL | Merupakan Universal Unique ID dari data jabatan          |
| langcode           | varchar(12)  |          | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam jabatan     |
| user_id            | int(10)      |          | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah jabatan |
| kelompok_data      | int(10)      | UNSIGNED | NOT NULL | Merupakan ID autoincrement dari kelompok data            |
| kelompok_data_uuid | varchar(128) |          | NOT NULL | Merupakan UUID dari kelompok data                        |
| name               | varchar(50)  |          | NOT NULL | Merupakan nama dari jabatan                              |
| opd                | int(10)      | UNSIGNED | NOT NULL | Merupakan ID autoincrement dari tabel opd                |
| opd_uuid           | varchar(128) |          | NOT NULL | Merupakan UUID dari tabel opd                            |
| status             | tinyint(4)   |          | NOT NULL | Merupakan status aktif tidaknya jabatan                  |
| created            | int(11)      |          | NULL     | Merupakan waktu saat dibuatnya jabatan                   |
| changed            | int(11)      |          | NULL     | Merupakan waktu saat diubahnya jabatan                   |


### Referensi

- Menggunakan referensi pada tabel : jabatan
- Digunakan sebagai referensi pada tabel : jenis_data
