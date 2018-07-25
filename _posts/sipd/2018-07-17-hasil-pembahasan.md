---
date: 2018-07-17
title: Hasil dan Pembahasan
categories:
 - sipd
description: Hasil dan Pembahasan Sistem Informasi Pemerintah Daerah Pemerintah Provinsi Banten
type: Document
---

## 3. HASIL DAN PEMBAHASAN

### 3.1 Kebutuhan Software dan Hardware

Adapun alat bantu software dan hardware dalam melakukan analisis dan perancangan adalah sebagai berikut:

#### 3.1.1 Software

* Ubuntu 17.04
* Typora (Markdown) & dillinger.io
* Gliffy Diagram

#### 3.1.2 Hardware

Laptop dengan spesifikasi sebagai berikut:

* Intel Celeron N2830 Speed 2.16 Ghz Turbo Boost 2.14 Ghz
* Memori DDR3 2GB
* Hard disk 500GB

### 3.2 Analisis Permasalahan

Permasalahan yang terjadi saat ini adalah sebagai berikut:

1. Bagi masyarakat umum merasa sulit untuk mendapatkan informasi mengenai semua hal yang berkaitan dengan hasil pembangunan di Banten alur sistem yang berjalan saat ini dirasa masih sangat minim atau kurang.
2. Bagi Oranisasi Perangkat Daerah belum adanya standar tata kelola data untuk melakukan pencatatan hasil pembangunan dan penyusunan pelaporan
3. Bagi Badan Perencanaan Pembangunan Daerah belum adanya tata kelola data yang komprehensif yang dapat mengakumulasikan seluruh data dan informasi hasil pembangunan yang dikelola oleh masing - masing Organisasi Perangkay Daerah.
4. Bagi Pemerintah Daerah belum ada pusat data yang terintegrasi yang dapat dengan cepat memberikan data dan informasi guna penyusunan laporan yang dibutuhkan oleh berbagai lembaga pemerintahan di tingkat Pusat. 

### 3.3 Solusi

Solusi yang kami tawarkan adalah pembuatan sebuah sistem informasi manajemen yang mencakup;

1. Meningkatkan mutu pencatatan data hasil pembangunan di tingkat Organisasi Perangkat Daerah,
2. Meningkatkan kualitas tata kelola data yang terintegrasi, akurat dan transparan pada Badan Perencanaan Pembangunan Daerah,
3. Menyediakan web service bagi aplikasi / sistem informasi yang terkait,
4. Menyediakan basis data hasil pembangunan yang akurat,
5. Memberi fasilitas akses informasi bagi masyarakat dengan cepat, mudah dan akurat,
6. Memberikan kemudahan bagi Pemerintah Daerah dalam hal penyusunan laporan hasil - hasil pembangunan. 

### 3.4 Perancangan Aplikasi

"Desain dan Perancangan Sistem Informasi Pembangunan Daerah Provinsi Banten" adalah sebuah sistem informasi yang memberikan informasi tentang segala kegiatan pembangunan di wilayah Provinsi Banten. Masyarakat umum dapat mengakses aplikasi ini dengan cara membuka aplikasi dari web. Semua data dan informasi dapat di input oleh pihak Organisasi Perangkat Daerah terkait, data akan tersimpan semua data kedalam pusat basisdata Bappeda Provinsi Banten.

### 3.5 Perancangan Basisdata

Pada basisdata yang digunakan oleh single user atau hanya beberapa user saja, perancangan basisdata tidak sulit. tetapi jika ukuran basisdata yang sedang atau besar (ratusan bahkan ribuan user yang berisikan jutaan bytes informasi dan melibatkan ratusan query dan program program aplikasi) perancangan basisdata menjadi sangat komplek. Oleh karena itu para pemakai mengharapkan penggunaan basisdata yang sedemikian rupa sehingga sistem harus dapat memenuhi kebutuhan-kebutuhan seluruh user tersebut.

#### 3.5.1 Tujuan perancangan basisdata:

- Untuk memenuhi informasi yang diberisikan kebutuhan-kebutuhan user secara khusus dan aplikasi - aplikasinya.
- Memudahkan pengertian struktur informasi
- Mendukung kebutuhan-kebutuhan pemrosesan dan beberapa obyek penampilan (*response time, processing time dan storage space*)

#### 3.5.2 Proses Perancangan Basisdata

Proses perancangan basisdata terdiri dari 6 tahap:

- Tahap 1, Pengumpulan data dan analisis
- Tahap 2, Perancangan basisdata secara konseptual
- tahap 3, Pemilihan DBMS
- Tahap 4, Perancangan Basisdata secara logika (*data model mapping*)
- Tahap 5, Perancangan basisdata secara fisik
- Tahap 6, Implementasi sistem basisdata

semakin banyak permintaan kepada aplikasi dapat mempengaruhi data yg terdapat di basisdata. Contoh relasi permintaan aplikasi dengan status dan log
[![Rancangan Basisdata](/document/aplikasi/sipd/images/desain-dan-perancangan/sipd_rancangan-basisdata.jpg)](/document/aplikasi/sipd/images/desain-dan-perancangan/sipd_rancangan-basisdata.jpg)

Secara khusus proses perancangan berisi 2 aktifitas paralel:

- Aktifitas yang melibatkan perancangan dari isi data dan struktur database,
- Aktifitas mengenai perancangan pemrosesan database dan aplikasi-aplikasi perangkat lunak.

Di lain pihak, kita biasanya menentukan perancangan aplikasi-aplikasi database dengan mengarah kepada konstruksi skema database yang telah ditentukan selama aktifitas yang pertama.

6 tahapan diatas tadi tidak harus diproses berurutan. Pada tahap ke 1 merupakan kumpulan informasi yang berhubungan dengan penggunaan database. Tahap 6 merupakan implementasi database-nya.

Tahap 1 dan 6 kadang-kadang bukan merupakan bagian dari perancangan database. Sedangkan yang merupakan inti dari proses perancangan database adalah pada tahap 2, 4, 5.

#### 3.5.2.1 Pengumpulan data dan analisis

Merupakan suatu tahap dimana kita melakukan proses indentifikasi dan analisa kebutuhan-kebutuhan data dan ini disebut pengumpulan data dan analisa. Untuk menentukan kebutuhan-kebutuhan suatu sistem database, kita harus mengenal terlebih dahulu bagian-bagian lain dari sistem informasi yang akan berinteraksi dengan sistem database, termasuk para user yang ada dan para useryang baru beserta aplikasi-aplikasinya. Kebutuhan-kebutuhan dari para user dan aplikasi-aplikasi inilah yang kemudian dikumpulkan dan dianalisa.

**Berikut ini adalah aktifitas-aktifitas pengumpulan data dan analisa:**

1. Menentukan kelompok pemakai dan bidang-bidang aplikasinya
2. Peninjauan dokumentasi yang ada
3. Analisa lingkungan operasi dan pemrosesan data
4. Daftar pertanyaan dan wawancara

#### 3.5.2.2 Perancangan basisdata secara konseptual

Pada tahap ini akan dihasilkan conceptual schema untuk database yang tergantung pada sebuah DBMS yang spesifik. Sering menggunakan sebuah high-level data modelseperti ER/EER modelselama tahap ini. Dalam conceptual schema, kita harus merinci aplikasi-aplikasi databaseyang diketahui dan transaksi-transaksi yang mungkin.Tahap perancangan databasesecara konseptual mempunyai 2 aktifitas pararel:

**Perancangan skema konseptual**

Menguji kebutuhan-kebutuhan data dari suatu database yang merupakan hasil dari tahap 1 dan menghasilkan sebuah conceptual database schema pada DBMS-independent model data tingkat tinggi seperti EER (Enhanced Entity Relationship) model.Untuk menghasilkan skema tersebut dapat dihasilkan dengan penggabungan bermacam-macam kebutuhan user dan secara langsung membuat skema database atau dengan merancang skema-skema yang terpisah dari kebutuhan tiap-tiap user dan kemudian menggabungkan skema-skema tersebut. Model data yang digunakan pada perancangan skema konseptual adalah DBMS-independent dan langkah selanjutnya adalah memilih DBMS untuk melakukan rancangan tersebut.

**Perancangan transaksi**

Menguji aplikasi-aplikasi databasedimana kebutuhan-kebutuhannya telah dianalisa pada fase 1, dan menghasilkan perincian transaksi-transaksi ini.Kegunaan tahap ini yang diproses secara paralel bersama tahapp perancangan skema konseptual adalah untuk merancang karakteristik dari transaksi-transaksi database yang telah diketahui pada suatu DBMS-independent. Transaksi-transaksi ini akan digunakan untuk memproses dan memanipulasi database suatu saat dimana database tersebut dilaksanakan.


#### 3.5.2.2.1 kelompok_data

Kelompok data atau lebih sering disebut dengan istilah "urusan", adalah data yang memiliki urutan tertinggi dalam sistem yang akan rancang. Tabel kelompok data adalah tabel yang dipakai untuk menyimpan data kelompok data atau urusan tersebut, didalam tabel ini terdapat beberapa field yang digunakan untuk menyimpan data dari kelompok data tersebut.

**Struktur tabel kelompok data**

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

**Referensi**

- Menggunakan referensi pada tabel :
- Digunakan sebagai referensi pada tabel : jenis_data

~~~sql
--
-- Table structure for table `kelompok_data`
--

CREATE TABLE `kelompok_data` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `name` varchar(50) DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL,
  `kode` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for kelompok_data entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `kelompok_data`
--
ALTER TABLE `kelompok_data`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `kelompok_data_field__uuid__value` (`uuid`),
  ADD KEY `kelompok_data_field__user_id__target_id` (`user_id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `kelompok_data`
--
ALTER TABLE `kelompok_data`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~sql

#### 3.5.2.2.2 Jabatan

Jabatan data adalah tabel yang menampung jabatan yang ada di lingkungan Pemerintah Provinsi Banten. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan data jabatan. Berikut adalah field yang terdapat pada tabel jabatan.

**Struktur table jabatan**

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

**Referensi**

- Menggunakan referensi pada tabel :
- Digunakan sebagai referensi pada tabel : opd

~~~sql
--
-- Table structure for table `jabatan`
--

CREATE TABLE `jabatan` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `name` varchar(50) DEFAULT NULL,
  `eselon` varchar(255) DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for jabatan entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `jabatan`
--
ALTER TABLE `jabatan`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `jabatan_field__uuid__value` (`uuid`),
  ADD KEY `jabatan_field__user_id__target_id` (`user_id`),
  ADD KEY `jabatan_field__eselon__value` (`eselon`(191));

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `jabatan`
--
ALTER TABLE `jabatan`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~

#### 3.5.2.2.3 Opd

Opd adalah singkatan dari Organisasi Perangkat Daerah, yang merupakan satuan kerja yang ada di lingkungan Pemerintah Provinsi Banten. opd disini adalah tabel yang menampung data opd yang ada di lingkungan Pemerintah Provinsi Banten, didalam tabel opd ini terdapat beberapa field yang terkait dengan opd. Berikut adalah field yang ada dalam tabel opd.

**Struktur tabel opd**

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

**Referensi**

- Menggunakan referensi pada tabel : jabatan
- Digunakan sebagai referensi pada tabel : jenis_data

~~~sql
--
-- Table structure for table `opd`
--

CREATE TABLE `opd` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `kode` varchar(128) DEFAULT NULL,
  `name` varchar(191) DEFAULT NULL,
  `induk` varchar(128) DEFAULT NULL,
  `pejabat` varchar(191) DEFAULT NULL,
  `jabatan` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `jabatan_uuid` varchar(255) DEFAULT NULL,
  `level` varchar(255) DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for opd entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `opd`
--
ALTER TABLE `opd`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `opd_field__uuid__value` (`uuid`),
  ADD KEY `opd_field__user_id__target_id` (`user_id`),
  ADD KEY `opd_field__jabatan__target_id` (`jabatan`),
  ADD KEY `opd_field__level__value` (`level`(191));

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `opd`
--
ALTER TABLE `opd`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~

#### 3.5.2.2.3 jenis_data

Jenis data atau lebih sering disebut dengan istilah "variabel" adalah tabel yang menampung data dari jenis data atau variabel tersebut. Jenis data adalah tabel yang menampung jenis data atau variabel  yang ada di lingkungan Pemerintah Provinsi Banten. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan jenis data. Berikut adalah field yang terdapat pada tabel jenis data.

**Struktur table jenis data**

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

**Referensi**

- Menggunakan referensi pada tabel : jabatan
- Digunakan sebagai referensi pada tabel : jenis_data

~~~sql
--
-- Table structure for table `jenis_data`
--

CREATE TABLE `jenis_data` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `kode` int(11) DEFAULT NULL,
  `kelompok_data` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `kelompok_data_uuid` varchar(128) DEFAULT NULL,
  `name` varchar(191) DEFAULT NULL,
  `opd` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `opd_uuid` varchar(128) DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for jenis_data entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `jenis_data`
--
ALTER TABLE `jenis_data`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `jenis_data_field__uuid__value` (`uuid`),
  ADD KEY `jenis_data_field__user_id__target_id` (`user_id`),
  ADD KEY `jenis_data_field__kelompok_data__target_id` (`kelompok_data`),
  ADD KEY `jenis_data_field__opd__target_id` (`opd`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `jenis_data`
--
ALTER TABLE `jenis_data`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~

#### 3.5.2.2.5 jenis_element

Jenis element digunakan untuk mengklasifikasikan elemen pada rancangan sistem yang akan dibuat. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan jenis element. Berikut adalah field yang terdapat pada tabel jenis element.

**Struktur tabel jenis_element**

Struktur tabel jenis elemen terdiri dari:

| Name     | Type         | Unsigned | Null     | Keterangan                                                     |
|----------|--------------|----------|----------|----------------------------------------------------------------|
| id       | int(10)      | UNSIGNED | NOT NULL | Merupakan ID dari data jenis elemen                           |
| uuid     | varchar(128) |          | NOT NULL | Merupakan Universal Unique ID dari data jenis elemen          |
| langcode | varchar(12)  |          | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam jenis elemen     |
| user_id  | int(10)      |          | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah jenis elemen |
| name     | varchar(50)  |          | NOT NULL | Merupakan nama dari jenis elemen                              |
| status   | tinyint(4)   |          | NOT NULL | Merupakan status aktif tidaknya jenis elemen                  |
| created  | int(11)      |          | NULL     | Merupakan waktu saat dibuatnya jenis elemen                   |
| changed  | int(11)      |          | NULL     | Merupakan waktu saat diubahnya jenis elemen        

**Referensi**

- Menggunakan referensi pada tabel : 
- Digunakan sebagai referensi pada tabel : element

~~~sql
--
-- Table structure for table `jenis_element`
--

CREATE TABLE `jenis_element` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `name` varchar(50) DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for jenis_element entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `jenis_element`
--
ALTER TABLE `jenis_element`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `jenis_element_field__uuid__value` (`uuid`),
  ADD KEY `jenis_element_field__user_id__target_id` (`user_id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `jenis_element`
--
ALTER TABLE `jenis_element`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~

#### 3.5.2.2.5 element

Element adalah bagian penting yang perancangan sistem ini, digunakan sebagai komponen komponen yang dipakai dalam mencatat suatu nilai atau pengukuran. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan element. Berikut adalah field yang terdapat pada tabel element.

**Struktur tabel jenis_element**

Struktur tabel jenis elemen terdiri dari:

| Name         | Type         | Unsigned | Null     | Keterangan                                           |
|--------------|--------------|----------|----------|------------------------------------------------------|
| id           | int(10)      | UNSIGNED | NOT NULL | Merupakan ID dari data elemen                           |
| uuid         | varchar(128) |          | NOT NULL | Merupakan Universal Unique ID dari data elemen          |
| langcode     | varchar(12)  |          | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam elemen     |
| user_id      | int(10)      |          | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah elemen |
| kode         | varchar(128) |          | NOT NULL | Merupakan kode elemen dari kelompok data                |
| name         | varchar(50)  |          | NOT NULL | Merupakan nama dari elemen                              |
| induk        | int(10)      | UNSIGNED | NOT NULL | Merupakan ID autoincrement dari tabel elemen            |
| induk_uuid   | varchar(128) |          | NOT NULL | Merupakan UUID induk elemena dari tabel elemen             |
| jenis_data   | int(10)      | UNSIGNED | NOT NULL | Merupakan jenis_data ID yang ada pada elemen            |
| jenis_elemen | int(10)      | UNSIGNED | NOT NULL | Merupakan jenis_elemen ID dari kolom elemen               |
| status       | tinyint(4)   |          | NOT NULL | Merupakan status aktif tidaknya elemen                  |
| created      | int(11)      |          | NULL     | Merupakan waktu saat dibuatnya elemen                   |
| changed      | int(11)      |          | NULL     | Merupakan waktu saat diubahnya elemen                   |

**Referensi**

- Menggunakan referensi pada tabel : jenis_element
- Digunakan sebagai referensi pada tabel : sipd

~~~sql
--
-- Table structure for table `element`
--

CREATE TABLE `element` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `name` varchar(50) DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL,
  `jenis_data` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `jenis_element` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `induk` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `induk_uuid` varchar(50) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for element entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `element`
--
ALTER TABLE `element`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `element_field__uuid__value` (`uuid`),
  ADD KEY `element_field__user_id__target_id` (`user_id`),
  ADD KEY `element_field__jenis_data__target_id` (`jenis_data`),
  ADD KEY `element_field__jenis_elemen__target_id` (`jenis_element`),
  ADD KEY `element_field__induk__target_id` (`induk`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `element`
--
ALTER TABLE `element`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~

#### 3.5.2.2.5 sipd

sipd adalah bagian utama yang perancangan sistem ini, digunakan sebagai komponen komponen yang dipakai dalam menampilkan nilai atau pengukuran pada tabel element. Di dalam tabel ini terdapat beberapa field yang berhubungan dengan element. Berikut adalah field yang terdapat pada tabel sipd.

| Name | Type | UNSIGNED | NULL | Comment |
| --- | --- | --- | --- | --- |
| id | int(10) | UNSIGNED | NOT NULL | Merupakan ID dari data sipd |
| uuid | varchar(128) | CHARACTER SET ascii | NOT NULL | Merupakan Universal Unique ID dari sipd |
| langcode | varchar(12) | CHARACTER SET ascii | NOT NULL | Merupakan pengenal bahasa yang dipakai dalam sipd |
| user_id | int(10) | UNSIGNED | NOT NULL | Merupakan ID dari pengguna yang membuat/mengubah sipd |
| element | int(10) | UNSIGNED | NULL | Merupakan ID dari element pada sipd |
| wilayah_banten | int(10) | UNSIGNED | NULL | Merupakan ID dari wilayah kabupaten kota  pada sipd |
| name | varchar(191) | DEFAULT | NULL | Merupakan nama dari wilayah kabupaten kota  pada sipd |
| kode_provinsi | varchar(191) | DEFAULT | NULL | Merupakan kode provinsi dari sipd |
| kode_kab_kota | varchar(191) | DEFAULT | NULL | Merupakan kode kabupaten / kota dari sipd |
| kode_kecamatan | varchar(191) | DEFAULT | NULL | Merupakan kode kecamatan dari sipd |
| kode_urusan | varchar(191) | DEFAULT | NULL | Merupakan kode urusan dari sipd |
| id_table | varchar(191) | DEFAULT | NULL | Merupakan id_table dari sipd |
| header | varchar(191) | DEFAULT | NULL | Merupakan header dari sipd |
| variable | varchar(191) | DEFAULT | NULL | Merupakan nama variabel dari sipd |
| elemen | varchar(191) | DEFAULT | NULL | Merupakan nama element dari sipd |
| s_elemen | varchar(191) | DEFAULT | NULL | Merupakan nama sub element dari sipd |
| s1_elemen | varchar(191) | DEFAULT | NULL | Merupakan nama sub sub element dari sipd |
| s2_elemen | varchar(191) | DEFAULT | NULL | Merupakan nama sub sub sub element dari sipd |
| jenis_data | varchar(191) | DEFAULT | NULL | Merupakan nama dari jenis data |
| kelompok_data | varchar(191) | DEFAULT | NULL | Merupakan nama dari kelompok data |
| pemda | varchar(191) | DEFAULT | NULL | Merupakan Nama Pemerintah Daerah dari sipd |
| opd_uuid | varchar(191) | DEFAULT | NULL | Merupakan Universal Unique ID dari Perangkat Daerah |
| opd_nama | varchar(191) | DEFAULT | NULL | Merupakan nama  dari Perangkat Daerah |
| tahun | int(11) | DEFAULT | NULL | Merupakan tahun dicatatnya sipd |
| nilai | float | DEFAULT | NULL | Merupakan nilai yang dicatat dalam sipd |
| status | tinyint(4) | |  NOT NULL | Merupakan status aktif tidaknya sipd |
| created | int(11) | DEFAULT | NULL | Merupakan waktu saat dibuatnya sipd |
| changed | int(11) | DEFAULT | NULL | Merupakan waktu saat diubahnya sipd |

~~~sql
--
-- Table structure for table `sipd`
--

CREATE TABLE `sipd` (
  `id` int(10) UNSIGNED NOT NULL,
  `uuid` varchar(128) CHARACTER SET ascii NOT NULL,
  `langcode` varchar(12) CHARACTER SET ascii NOT NULL,
  `user_id` int(10) UNSIGNED NOT NULL COMMENT 'The ID of the target entity.',
  `element` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `wilayah_banten` int(10) UNSIGNED DEFAULT NULL COMMENT 'The ID of the target entity.',
  `name` varchar(191) DEFAULT NULL,
  `kode_provinsi` varchar(191) DEFAULT NULL,
  `kode_kab_kota` varchar(191) DEFAULT NULL,
  `kode_kecamatan` varchar(191) DEFAULT NULL,
  `kode_urusan` varchar(191) DEFAULT NULL,
  `id_table` varchar(191) DEFAULT NULL,
  `header` varchar(191) DEFAULT NULL,
  `variable` varchar(191) DEFAULT NULL,
  `elemen` varchar(191) DEFAULT NULL,
  `s_elemen` varchar(191) DEFAULT NULL,
  `s1_elemen` varchar(191) DEFAULT NULL,
  `s2_elemen` varchar(191) DEFAULT NULL,
  `jenis_data` varchar(191) DEFAULT NULL,
  `kelompok_data` varchar(191) DEFAULT NULL,
  `pemda` varchar(191) DEFAULT NULL,
  `opd_uuid` varchar(191) DEFAULT NULL,
  `opd_nama` varchar(191) DEFAULT NULL,
  `tahun` int(11) DEFAULT NULL,
  `nilai` float DEFAULT NULL,
  `status` tinyint(4) NOT NULL,
  `created` int(11) DEFAULT NULL,
  `changed` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='The base table for sipd entities.';

--
-- Indexes for dumped tables
--

--
-- Indexes for table `sipd`
--
ALTER TABLE `sipd`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `sipd_field__uuid__value` (`uuid`),
  ADD KEY `sipd_field__user_id__target_id` (`user_id`),
  ADD KEY `sipd_field__element__target_id` (`element`),
  ADD KEY `sipd_field__wilayah_banten__target_id` (`wilayah_banten`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `sipd`
--
ALTER TABLE `sipd`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT;
~~~

#### 3.5.2.2.6 Hasil Restrukturisasi Data per Urusan

| NO | URUSAN                                                        | KELOMPOK DATA | JENIS DATA | HEADER | VARIABEL DATA | ELEMEN DATA | SUB ELEMEN DATA | SUB SUB ELEMEN DATA | TOTAL |
|----|---------------------------------------------------------------|---------------|------------|--------|---------------|-------------|-----------------|---------------------|-------|
| 1  | PENDIDIKAN                                                    | 1             | 1          | 13     | 62            | 49          | 0               | 0                   | 126   |
| 2  | KESEHATAN                                                     | 1             | 1          | 10     | 38            | 46          | 5               | 5                   | 106   |
| 3  | PEKERJAAN UMUM DAN PENATAAN RUANG                             | 1             | 1          | 23     | 40            | 68          | 12              | 0                   | 145   |
| 4  | PERUMAHAN DAN KAWASAN PEMUKIMAN                               | 1             | 1          | 7      | 25            | 25          | 0               | 0                   | 59    |
| 5  | KETENTRAMAN DAN KETERTIBAN UMUM SERTA PERLINDUNGAN MASYARAKAT | 1             | 1          | 13     | 47            | 69          | 12              | 0                   | 143   |
| 6  | SOSIAL                                                        | 1             | 1          | 32     | 138           | 47          | 0               | 0                   | 219   |
| 7  | TENAGA KERJA                                                  | 1             | 1          | 7      | 37            | 8           | 2               | 0                   | 56    |
| 8  | PEMBERDAYAAN PEREMPUAN DAN PERLINDUNGAN ANAK                  | 1             | 1          | 11     | 34            | 36          | 0               | 0                   | 83    |
| 9  | PANGAN                                                        | 1             | 1          | 14     | 36            | 19          | 0               | 0                   | 71    |
| 10 | PERTANAHAN                                                    | 1             | 1          | 5      | 23            | 6           | 0               | 0                   | 36    |
| 11 | LINGKUNGAN HIDUP                                              | 1             | 1          | 3      | 17            | 50          | 0               | 0                   | 72    |
| 12 | ADMINISTRASI PEMERINTAHAN DAN PENCATATAN SIPIL                | 1             | 1          | 9      | 70            | 60          | 0               | 0                   | 141   |
| 13 | PEMBERDAYAAN MASYARAKAT DAN DESA                              | 1             | 1          | 12     | 29            | 37          | 12              | 0                   | 52    |
| 14 | PENGENDALIAN PENDUDUK DAN KELUARGA BERENCANA                  | 1             | 1          | 4      | 22            | 16          | 4               | 0                   | 48    |
| 15 | PERHUBUNGAN                                                   | 1             | 1          | 8      | 32            | 41          | 38              | 0                   | 121   |
| 16 | KOMUNIKASI DAN INFORMATIKA                                    | 1             | 1          | 13     | 21            | 10          | 0               | 0                   | 46    |
| 17 | UMKM                                                          | 1             | 1          | 8      | 6             | 34          | 36              | 0                   | 86    |
| 18 | PENANAMAN MODAL                                               | 1             | 1          | 0      | 3             | 5           | 15              | 120                 | 145   |
| 19 | KEPEMUDAAN DAN OLAH RAGA                                      | 1             | 1          | 12     | 57            | 65          | 0               | 0                   | 136   |
| 20 | STATISTIK                                                     | 1             | 1          | 0      | 0             | 0           | 0               | 0                   | 2     |
| 21 | PERSANDIAN                                                    | 1             | 1          | 0      | 0             | 0           | 0               | 0                   | 2     |
| 22 | KEBUDAYAAN                                                    | 1             | 1          | 22     | 42            | 28          | 0               | 0                   | 94    |
| 23 | PERPUSTAKAAN                                                  | 1             | 1          | 2      | 13            | 48          | 53              | 0                   | 118   |
| 24 | KEARSIPAN                                                     | 1             | 1          | 12     | 27            | 4           | 0               | 0                   | 45    |
| 25 | KELAUTAN DAN PERIKANAN                                        | 1             | 1          | 34     | 90            | 34          | 6               | 0                   | 166   |
| 26 | PARIWISATA                                                    | 1             | 1          | 24     | 69            | 44          | 0               | 0                   | 139   |
| 27 | PERTANIAN                                                     | 1             | 1          | 12     | 60            | 77          | 53              | 0                   | 204   |
| 28 | KEHUTANAN                                                     | 1             | 1          | 9      | 66            | 7           | 6               | 9                   | 99    |
| 29 | ENERGI DAN SUMBERDAYA MINERAL                                 | 1             | 1          | 53     | 161           | 68          | 72              | 0                   | 356   |
| 30 | PERDAGANGAN                                                   | 1             | 1          | 3      | 11            | 50          | 9               | 0                   | 75    |
| 31 | PERINDUSTRIAN                                                 | 1             | 1          | 7      | 183           | 2           | 0               | 0                   | 244   |
| 32 | TRANSMIRASI                                                   | 1             | 1          | 19     | 68            | 28          | 0               | 0                   | 117   |
| 33 | DATA UMUM                                                     |               |            |        |               |             |                 |                     |       |
|    |                                                               |               |            |        |               |             |                 |                     |       |
|    | TOTAL                                                         | 3             | 32         | 451    | 1527          | 1801        | 335             | 134                 | 3592  |
|    | TOTAL VARIABEL S.D SUB SUB ELEMEN DATA                        |               |            |        |               |             |                 | 3077                |       |


#### 3.5.2.3 Pemilihan DBMS

Pemilihan database ditentukan oleh beberapa faktor diantaranya faktor teknik, ekonomi, dan politik organisasi.Contoh faktor teknik:

Keberadaan DBMS dalam menjalankan tugasnya seperti jenis-jenis DBMS (relational, network, hierarchical, dan lain-lain), struktur penyimpanan, dan jalur akses yang mendukung DBMS, pemakai, dan lain-lain.Faktor-faktor ekonomi dan organisasi yang mempengaruhi satu sama lain dalam pemilihan DBMS :

1. Struktur data
Jika data yang disimpan dalam database mengikuti struktur hirarki, maka suatu jenis hirarki dari DBMS harus dipikirkan.
2. Personal yang telah terbiasa dengan suatu sistem
Jika staf programmer dalam suatu organisasi sudah terbiasa dengan suatu DBMS, maka hal ini dapat mengurangi biaya latihan dan waktu belajar.
3. Tersedianya layanan penjual
Keberadaan fasilitas pelayanan penjual sangat dibutuhkan untuk membantu memecahkan beberapa masalah sistem.


#### 3.5.2.3.1 Faktor Teknik,

- Dapat bekerja di beberapa platform yang berbeda seperti LINUX, Windows, MacOS, FreeBSD, Solaris, dll.
- Mempunyai lebih banyak tipe data seperti : signed/unsigned integer yang memiliki panjang data sebesar 1,2,3,4 dan 8 byte. FLOAT, DOUBLE, CHAR, VARCHAR, TEXT, BLOB, DATE, TIME, DATETIME, TIMESTAMP, YEAR, SET, dan tipe ENUM.
- Mendukung terhadap LEFT OUTHER JOIN dengan ANSI SQL dan sintak ODBC.
- Mendukung ODBC for windows 95' (dengan source program). Semua fungsi ODBC 2.5 dan sebagainya. Sebagai contoh kita dapat menggunakan Access untuk connect ke MySQL server.
- Kita dapat menggabungkan beberapa table dari database yang berbeda dalam query yang sama. Structure table MySQL memiliki struktur tabel yang lebih fleksibel dalam menangani ALTER TABLE dibandingkan DBMS lainnya.
- Privilege (hak) dan password sangat fleksibel dan aman serta mengijinkan "Host-Based" Verifikasi. Memiliki beberapa lapisan keamanan , seperti subnet mask, nama host, dan izin akses user dengan sistem perijinan yang mendetail serta sandi/password terenkripsi.
- Program dapat running di semua OS,PHP MySQL berjalan secara web base, itu artinya semua operating system yang memiliki web browser dapat menggunakan aplikasi ini, dan semua OS tentu saja selalu memiliki web browser, Windows dengan internet explorer, Linux dengan Mozilla, Macintosh dengan safari, dan handphone dengan opera mini. Sangat mobile dan flexibel.

#### 3.5.2.3.2 Faktor Organisasi

- MySQL dapat melakukan koneksidengan komputer client menggunakan protokol TCP/IP, Unix Socket (UNIX), atau Named Pipes(Windows NT).
- MySQL memiliki antar muka/interface terhadap berbagai aplikasi dan bahasa pemrograman dengan menggunakan fungsi API (Application progamming interface).
- Command and function MySQL memiliki fungsi dan operator secara penuh yang mendukung perintah select dan where dalam query.

#### 3.5.2.3.3 Faktor Ekonomi

- Merupakan DBMS yang gratis/open source berlisensi GPL (Generic Public License).
- Cocok untuk perusahaan dengan skala yang kecil.
- Tidak membutuhkan spesifikasi hardware yang tinggi untuk bisa menjalankan MySQL ini bahkan dengan spesifikasi hardware yang minimal sekalipun.

#### 3.5.2.4 Perancangan Basisdata secara logika(data model mapping)

Tahap selanjutnya adalah membuat sebuah skema konseptual dan skema eksternal pada model data dari DBMS yang terpilih. Tahap ini dilakukan oleh pemetaan skema konseptual dan skema eksternal yang dihasilkan pada tahap 2. Pada tahap ini, skema konseptual ditransformasikan dari model data tingkat tinggi yang digunakan pada tahap 2 ke dalam model data dari model data dari DBMS yang dipilih pada tahap 3.Pemetaan tersebut dapat diproses dalam 2 tingkat:

1. Pemetaan system-independent
Pemetaan ke dalam model data DBMS dengan tidak mempertimbangkan karakteristik atau hal-hal yang khusus yang berlaku pada implementasi DBMS dari model data tersebut.
2. Penyesuain skema ke DBMS yang spesifik
Mengatur skema yang dihasilkan pada langkah 1 untuk disesuaikan pada implementasi yang khusus di masa yang akan datang dari suatu model data yang digunakan pada DBMS yang dipilih.Hasil dari tahap ini memakai perintah-perintah DDL (Data Definition Language) dalam bahasa DBMS yang dipilih yang menentukan tingkat skema konseptual dan eksternal dari sistem database. Tetapi 10 dalam beberapa hal, perintah-perintah DDL memasukkan parameter-parameter rancangan fisik sehingga DDL yang lengkap harus menunggu sampai tahap perancangan databasesecara fisik telah lengkap.Tahap ini dapat dimulai setelah pemilihan sebuah implementasi model data sambil menunggu DBMS yang spesifik yang akan dipilih. Contoh: jika memutuskan untuk menggunakan beberapa relational DBMS tetapi belum memutuskan suatu relasi yang utama. Rancangan dari skema eksternal untuk aplikasi-aplikasi yang spesifik seringkali sudah selesai selama proses ini.

#### 3.5.2.5 Perancangan basisdata secara fisik

Perancangan database secara fisik merupakan proses pemilihan struktur-struktur penyimpanan dan jalur-jalur akses pada file-file databaseuntuk mencapai penampilan yang terbaik pada bermacam-macam aplikasi.Selama fase ini, dirancang spesifikasi-spesifikasi untuk database yang disimpan yang berhubungan dengan struktur-struktur penyimpanan fisik, penempatan record dan jalur akses. Berhubungan dengan internal schema(pada istilah 3 level arsitektur DBMS).Beberapa petunjuk dalam pemilihan perancangan databasesecara fisik :

1. Response time
Waktu yang telah berlalu dari suatu transaksi database yang diajukan untuk menjalankan suatu tanggapan. Pengaruh utama pada response time adalah di bawah pengawasan DBMS yaitu : waktu akses database untuk data item yang ditunjuk oleh suatu transaksi. Response time juga dipengaruhi oleh beberapa faktor yang tidak berada di bawah pengawasan DBMS, seperti penjadwalan sistem operasi atau penundaan komunikasi.
2. Space utility
Jumlah ruang penyimpanan yang digunakan oleh file-file database dan struktur-struktur jalur akses.
3. Transaction throughput
Rata-rata jumlah transaksi yang dapat diproses per menit oleh sistem database, dan merupakan parameter kritis dari sistem transaksi (misal : digunakan pada pemesanan tempat di pesawat, bank, dll). Hasil dari fase ini adalah penentual awal dari struktur penyimpanan dan jalur akses untuk file-file database.

#### 3.5.2.6 Implementasi sistem basisdata

Setelah perancangan secara logika dan secara fisik lengkap, kita dapat melaksanakan sistem database. Perintah-perintah dalam DDL dan SDL(Storage Definition Language) dari DBMS yang dipilih, dihimpun dan digunakan untuk membuat skema database dan file-file database (yang kosong). Sekarang databasetersebut dimuat (disatukan) dengan datanya.Jika data harus dirubah dari sistem komputer sebelumnya, perubahan-perubahan yang rutin mungkin diperlukan untuk format ulang datanya yang kemudian dimasukkan ke database yang baru. Transaksi-transaksi database sekarang harus dilaksanakan oleh para programmmer aplikasi.Spesifikasi secara konseptual diuji dan dihubungkan dengan kode program dengan perintah-perintah dari embedded DML yang telah ditulis dan diuji. Suatu saat transaksi-transaksi tersebut telah siap dan data telah dimasukkan ke dalam database, maka tahap perancangan dan implementasi telah selesai, dan kemudian tahap operasional dari sistem database dimulai.

### 3.6 Perancangan Sistem

Permodelan rancangan sistem yang dgunakan adalah UML (Unified Modeling Language). Menurut Whitten dan Bentley (2007, p.381), Unified Modeling Language adalah kumpulan rancangan diagram untuk membangun sebuah sistem atau aplikasi yang dimana setiap diagram menyediakan sistem  informasi kepada tim pengembang dengan berbagai sudut pandang yang berbeda-beda. UML yang kami gunakan terdiri dari use case diagram, activity diagram, sequence diagram, state chart diagram, class diagram, technology diagram dan deployment diagram.
