# Writing Test Backend Development Week 2

## Database MYSQL

Pada minggu sebelumnya sudah memahami tentang mendesain suatu database. nah, pada tahap kita sudah masuk dalam implementasinya.

### Pengertian Database

Database adalah suatu tempat atau wadah untuk menyimpan berbagai data atau bisa disebut dengan dataset.

Sehingga cara kerja suatu database adalah untuk menyimpan dataset pada saat suatu aplikasi bekerja, dalam hal ini ketika suatu aplikasi website meminta request sebuah data ke API, API akan mengambil dari database tersebut yang isinya berbagai macam tipe data.

Database pada umumnya memiliki 2 jenis berdasarkan manajemen sistemnya yaitu Relational Database (SQL) dan Non Relational Database (NoSQL).

### Relasi-relasi pada database

1. One to One

Sebuah relasi yang menghubungkan kedua tabel dimana hanya satu baris yang berhubungan, sehingga satu baris hanya mewakili satu baris.

2. One to Many

Sebuah relasi yang menghubungkan kedua tabel dimana satu baris berhubungan dengan lebih dari 1 baris suatu tabel, sehingga satu baris bisa mewakili beberapa baris.

3. Many to Many

Sebuah relasi yang menghubungkan kedua tabel dimana lebih dari satu baris berhubungan dengan lebih dari 1 baris suatu tabel, sehingga beberapa baris bisa mewakili beberapa baris suatu tabel.

### SQL Database

Kali ini kita akan fokus terlebih dahulu ke dalam bentuk Database Relational atau biasa disebut dengan SQL, sebenarnya SQL atau singkatan dari Standard Query Language, seperti kepanjangannya, SQL sendiri merupakan sebuah bahasa (query) yang digunakan untuk mengelola suatu Relational Database.

Ada berbagai vendor atau merk yang mengeluarkan database jenis SQL, berikut contohnya yaitu :

1. MySQL
2. Oracle
3. PostgreSQL
4. Microsoft SQL Server
5. MariaDB
6. IBM Db2
7. Amazon Aurora
8. Google Cloud Spanner
9. dll.

### Cara mengelola Database

Disini kita akan menggunakan salah satu vendor database SQL yaitu MYSQL, untuk menginstall sebuah mysql di dalam komputer kita dapat menginstall langsung dengan mysql, bisa mendownload di [sini](https://dev.mysql.com/downloads/installer), lalu install seperti biasa. Namun disini saya menggunakan xampp bisa download melalui link [ini](https://www.apachefriends.org/download.html) lalu install seperti biasa.

Setelah melalui tahap di atas kita bisa melanjutkan tahap berikut:

1. Karena saya menggunakan Xampp, pertama buka XAMPP lalu aktifkan MYSQL

![database-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/database-1.png)

2. Selanjutnya buka sebuah software kelola database bisa menggunakan phpmyadmin di XAMPP namun saya akan menggunakan tableplus untuk mempermudah kelola, bisa install di [sini](https://tableplus.com/windows)

![database-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/database-2.png)

3. Membuat koneksi baru, bisa klik create new connection, dan pilih vendor yang dipakai, pilih MYSQL

![database-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/database-3.png)

4. Selanjutnya bisa mengisinya sebagai berikut untuk bisa terkoneksi dengan MYSQL

![database-4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/database-4.png)

5. Tampilan berikut jika koneksi berhasil dan masuk, klik logo database akan terlihat database yang terinstall

![database-5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/database-5.png)

6. Untuk selanjutnya kita bisa masukkan query-query SQL pada tampilan ini dengan klik logo sql

![database-6](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/database-6.png)

### Contoh Query-Query Simpel dalam MYSQL

```
-- membuat database
CREATE DATABASE <namaDatabase>
-- menggunakan database tersebut untuk dikelola
USE <namaDatabase>
```

```
-- melihat tabel di database
SHOW TABLES
```

```
-- membuat tabel
CREATE TABLE <namaTabel> (
	id int PRIMARY KEY NOT NULL auto_increment,
	nama VARCHAR(25)
);
```

```
--melihat field-field tabel
DESC <namaTabel>;
```

```
-- Mengisi record field
INSERT INTO <namaTabel> (namaField) VALUES ("Isinya");
```

```
-- menampilkan semua record tabel
SELECT * FROM <namaTabel>;
```

### Tipe data pada MYSQL

1. Tipe Data numerik

Tipe data numerik adalah tipe data yang isinya berupa angka-angka seperti Int, Float, Real, dll.

2. Tipe Data Teks

Tipe Data Teks merupakan tipe data yang menyimpan banyak karakter dengan jumlah maksimal karakter 255, seperti Char, VARCHAR, TEXT, dll.

3. Tipe Data Date

Merupakan Tipe Data yang berkaitan dengan tahun, bulan, dan hari, seperti DATE, TIME, DATETIME, dan YEAR.

4. Tipe Data Blob

Biasa untuk menyimpan gambar, musik, vide, dll. Contoh BLOB, BIT, dll.

### Manipulasi Data Menggunakan Query MYSQL

Biasanya disingkat dengan CRUD, yaitu dapat Create, Read, Update, dan Delete.

Untuk create dan read sudah dibahas di sebelumnya sehingga disini akan membahas cara untuk mengupdate dan menghapus data.

1. Mengupdate data

Contoh query:

```
-  ganti atau update isi tabel
UPDATE pelanggan set nama = "Denna" WHERE id = "2";
```

2. Menghapus data

Contoh:

```
-- hapus record nama bejo
DELETE FROM pelanggan WHERE nama="Bejo";
```

### Relasi dalam MYSQL

Ada 3 macam relasi dalam sebuah database yaitu one-to-one, one-to-many, dan many-to-many.

A. Contoh realisasi query untuk merelasikan one-to-one:

```
-- membuat tabel negara

CREATE TABLE negara (
    id int PRIMARY KEY NOT NULL auto_increment,
    nama varchar(25),
);

-- membuat tabel orang

CREATE TABLE orang (
    id int PRIMARY KEY NOT NULL auto_increment,
    nama varchar(25),
    id_negara int,
    FOREIGN KEY (id_negara) REFERENCES negara(id);
);
```

B. Contoh realisasi query untuk merelasikan one-to-many:

```
-- membuat tabel dokter
CREATE TABLE dokter (
    id int PRIMARY KEY NOT NULL auto_increment,
    nama varchar(25),
);

-- membuat tabel pasien
CREATE TABLE pasien (
    id int PRIMARY KEY NOT NULL auto_increment,
    nama varchar(25),
    id_dokter int,
    FOREIGN KEY (id_dokter) REFERENCES dokter(id);
);
```

C. Contoh realisasi query untuk merelasikan many-to-many:

```

-- membuat tabel pelanggan
CREATE TABLE pelanggan (
	id int PRIMARY KEY NOT NULL auto_increment,
	nama VARCHAR(25)
);

-- membuat tabel barang
CREATE TABLE barang (
	id int PRIMARY KEY NOT NULL auto_increment,
	nama_barang VARCHAR(25),
	harga int,
);

-- membuat tabel nota
CREATE TABLE nota (
	id int PRIMARY KEY NOT NULL auto_increment,
	pelanggan_id int,
	FOREIGN KEY (pelanggan_id) REFERENCES pelanggan(id),
	barang_id int,
	FOREIGN KEY (barang_id) REFERENCES barang(id),
	jumlah_brg int,
	tgl_pembelian date
);
```

Cntoh cara menampilkan 2 tabel berbeda:

```
--menampilkan 1 pelanggan dengan 3 barang berbeda

SELECT pelanggan.nama, barang.nama_barang, nota.jumlah_brg, nota.tgl_pembelian
FROM ((nota
INNER JOIN pelanggan ON nota.pelanggan_id = pelanggan.id)
INNER JOIN barang ON nota.barang_id = barang.id) HAVING pelanggan.nama = "Denna";
```

Contoh cara menampilkan 3 tabel berbeda:

```
--kategori yang barangnya banyak

SELECT kategori.jenis, sum(jumlah_brg) as total_brg_terjual from ((nota INNER JOIN barang ON nota.barang_id = barang.id) INNER JOIN kategori ON barang.kategori_id = kategori.id) GROUP by jenis;

```

## Autentikasi dan Otorisasi

Autentikasi merupakan sebuah fitur yang penting dalam berbagai aplikasi, dengan adanya autentikasi aplikasi dapat terjaga keamanannya, dimana ketika sebuah aplikasi dibuka mengharuskan kita untuk menginput beberapa ketentuan seperti email dan password, sehingga kita bisa masuk dan mencoba fitur-fiturnya. disisi lain dengan adanya autentikasi flow sebuah aplikasi akan jadi lebih teratur.

Otorisasi merupakan hak akses ketika kita sudah memasuki sebuah aplikasi, intinya jika autentikasi adalah cara kita masuk ke dalam aplikasi yaitu adanya beberapa peraturan seperti harus menginput email dan password dengan benar, sedangkan yang dilakukan otorisasi adalah memberikan sebuah hak apa saja yang dapat kita lakukan ketika sudah masuk dalam aplikasi.

### Variasi sebuah Autentikasi

Ada 2 jenis autentikasi yaitu:

1. Single Factor Authentication

Single Factor Authentication merupakan sebuah autentikasi yang hanya menggunakan satu lapisan keamanan, seperti contoh login dengan email dan password.

![autentikasi-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/autentikasi-1.jpg)

2. Multi Factor Authentication

Multi Factor Authentication merupakan sebuah autentikasi yang menggunakan dua lapisan keamanan, seperti contoh login dengan email dan password, namun ada lapisan keamanan lagi setelahnya yaitu mencocokkan nomor pada device yang terkait. Seperti contoh aplikasi Google Authenticator.

![autentikasi-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/autentikasi-2.png)

### Encryption dan decryption

Encryption merupakan sebuah metode untuk menyembunyikan suatu farsa-farsa tertentu sehingga tidak dapat terbaca secara bebas. Nah metode ini biasa dilakukan untuk melakukan sebuah Autentikasi.

Sedangkan Decryption merupakan sebuah cara untuk membalikkan nilai yang disembunyikan oleh metode encryption.

Salah satu library paling terkenal dalam autentikasi adalah jsonwebtoken atau bisa disingkat dengan JWT.

### JWT dalam Express

Untuk selanjutnya kita akan mencoba membuat sebuah api dengan sebuah autentikasi, disini kita menggunakan framework express dengan library JWT.

1. Install Express Seperti Biasa dan gunakan metode modular, dan library nodemon

![autentikasi-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/autentikasi-3.jpg.png)

2. Buat file auth.js didalam folder routes, isikan kode berikut:

```
const express = require('express');
const router= express.Router();
const jwt = require('jsonwebtoken');

const users = [
    {id: 1, email:"Rodhi", password: "123"},
    {id: 2, email:"Andriansah", password: "222"}
]

SECRETKEY = "asasassa"


router.post("/", (req,res) => {
    const data = req.body

    const usersData = users.find((item) => item.email === data.email && item.password === data.password)

    const token = jwt.sign(
        {
         id: usersData.id,
        },
        SECRETKEY
    )

    if (usersData) {
        res.send({
            status: "success login",
            token,
        })
    } else {
        res.status(401).send({
            status: "email or password incorrect",

        })
    }
})

router.get("/", (req, res) => {

    const header = req.headers.authorization
    const token = header.split(" ")[1]
    decode = jwt.verify(token, SECRETKEY)
    res.send({
        token,
        decode,
    })
})


module.exports = router
```

3. Jalankan api dengan perintah

```
npm run dev
```

4. post data di endpoint auth

![autentikasi-4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/autentikasi-4.png)

5. kita akan mendapatkan sebuah token acak, ini bisa dilakukan untuk mendapatkan id dari login, coba mendapatkan id dengan cara berikut:

![autentikasi-5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/autentikasi-5.jpg.png)
masukkan token di kolom auth -> bearer -> dan isikan pada kotak bearer token

## Sequileze

Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server.

Dengan fitur fitur di Sequelize, kita bisa mengelola dan mengatur data di database kita dengan cepat, dan efisien.

sedangkan untuk ORM adalah sebuah cara atau metode untuk menggabungkan antara database dengan OOP sehingga keduanya dapat digunakan, dimana database menggunakan SQL sedangkan dengan adanya ORM SQL dapat diubah menjadi bahasa pemrogaman dengan berbasis OOP.

untuk lebih jelasnya mungkin kita akan mencoba sedikit fitur sequileze, berikut tahap-tahapnya:

1. Install sequileze dan cli nya :

```
// install sequelize cli globally
npm i -g sequelize-cli

// install in local project
npm install sequelize

// install driver vendor database
npm i mysql2

// init sequelize in local project
npx sequelize-cli init

```

2. Ketika sudah terinstall dan sudah di inisiasi kita dapat mengatur config.json sesuaikan dengan database kita

![sequileze-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/sequileze-1.png)

3. Selanjutnya kita bisa menjalankan sequelize-cli di terminal untuk membuat database dengan perintah berikut:

```
npx sequileze-cli db:migrate
```

4. Kita bisa mengisi field database dengan perintah

```
npx sequelize-cli model:generate --name User --attributes email:string,password:string
```

5. Cek database apakah sesuai

![sequileze-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/e29c2f45a2fc192d8f3037d663059ca9df3ef298/week-6/images/sequileze-2.png)

6. Mengisi database dengan method post

```
//panggil models User
const modelUsers = require('../models/').Users;
```

```
// Mencoba registers
router.post("/register", async (req, res) => {
    try {
        await modelUsers.create({
            email: req.body.email,
            password: req.body.password

        });
        res.send({
            message: "register success"
        })
    } catch (error) {
        res.status(500).send({
                error: "Ada yang error"
        })
    }
})
```
