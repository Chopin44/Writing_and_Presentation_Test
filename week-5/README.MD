# Writing Test Backend Development Week 1

## Web Sever & Restful API

### Apa itu Web server?

Web Server adalah sebuah software yang memberikan layanan berupa data. Sebuah web server mengandung beberapa bagian yang dapat mengontrol bagaimana user megakses sebauh file yang sudah dihosting. Ini menggunakan sebuah protokol yang bernama HTTP server. HTTP adalah sebuah protokol yang dapat memahami URL suatu web.

### Jenis-jenis Web Server

#### 1. Static Web Server

Static Web Server adalah sebuah web server yang konten-kontennya statis tidak berubah-ubah. Sehingga ketika ingin mengubah suatu konten didalamnya membutuhkan kita untuk mengoding ulang di dalam filenya. Contoh static web server adalah seperti company profile, yang isi didalamnya tidak berubah-ubah.

#### 2. Dynamic Web Server

Dynamic Web Server adalah sebuah web server yang kontennya berubah-ubah setiap waktu, karena sifatnya yang berubah-ubah sehingga biasanya membutuhkan beberapa bantuan seperti API dan sebuah Database dalam pembuatannya, alhasil ketika ada data yang berubah kita tidak perlu mengubah kodaingan di dalamnya, hanya mengubah Database.

### Arsitektur Static/Dynamic Web Server

![web-server-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/web-server-1.png)

Dapat dilihat pada gambar tersebut ada tambahan database dan templating engine jika dalam Dynamic Web Server, seperti penjelasan sebelumnya dynamic web server membutuhkan sebuah database untuk mengubah data di dalam web namun tidak mengubah codingan yang ada dalam file HTMLnya misal.

### Apa saja yang dapat kita lakukan dalam sisi server?

#### 1. Efficient storage and delivery of information

Sudah pasti pembuatan aplikasi pada sisi server lebih efisien baik dalam urusan penyimpanan dan proses pengiriman, karena pembuatan per halamannya yang dipisah.

#### 2. Customised user experience

Server dapat menyimpan sebuah informasi dari usernya sehingga ketika user tersebut katakanlah mencoba membuka sebuah web kembali tidak usah melakukan pencarian kembali karena ada data yang disimpan.

#### 3. Controlled access to content

Server-side programming memungkinkan kita untuk membatasi sebuah website untuk otrisasi user dan membatasi informasi pada user tersebut untuk melihat informasi website yang ada di didalamnya.

### Restful API

Restful API merupakan sebuah gaya arsitektur sebuah API, yang didalamnya mengandung beberapa aturan.

Berikut beberapa aturan yang harus ada dalam sebuah API jika ingin menmgusung gaya arsitektur RESTful API:

1. Uniform interface
2. Client-server
3. Stateless
4. Cacheable
5. Layered System
6. Code on demand (optional)

#### Method Dalam sebuah REST API

1. GET: Memungkinkan kita untuk membuat sebuah request dan mendapatkan sebuah data dalam server.
2. PUT: Update entrian sebuah Database
3. POST: Membuat sebuah data baru dalam database
4. DELETE: Menghapus sebuah data dalam database

## Berkenalan dengan Node JS

Node JS adalah runtime environment untuk JavaScript yang bersifat open-source dan cross-platform. Dengan Node.js kita dapat menjalankan kode JavaScript di mana pun, tidak hanya terbatas pada lingkungan browser.

Node.js menjalankan V8 JavaScript engine (yang juga merupakan inti dari Google Chrome) di luar browser. Ini memungkinkan Node.js memiliki performa yang tinggi.

beberapa fitur penting dari Node.js yang menjadikannya pilihan utama dalam pengembangan aplikasi:

#### - Asynchronous & Event-driven

Semua API dari Node.js bersifat asynchronous, artinya tidak memblokir proses lain sembari menunggu satu proses selesai. Server Node.js akan melanjutkan ke ke pemanggilan API berikutnya lalu memanfaatkan mekanisme event notification untuk mendapatkan respon dari panggilan API sebelumnya.

#### - Very Fast

Eksekusi kode dengan Node.js sangat cepat karena berjalan pada V8 JavaScript Engine dari Google Chrome.

#### - Single Threaded but Highly Scalable

Node.js menggunakan model single thread dengan event looping. Mekanisme ini membantu server untuk merespon secara asynchronous dan menjadikan server lebih scalable dibandingkan server tradisional yang menggunakan banyak thread untuk menangani permintaan.

### Cara Install Node JS

Kita bisa mendownload nya pada link [ini](https://nodejs.org/en/), setelah mendownloadnya bisa di install seperti software-software pada umumnya.

Kita bisa cek apakah node js berhasil diinstall dengan mengetik
`node -v` pada CLI kita.

![node-js-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/node-js-1.png)

### Built-in Modul pada Node JS

#### 1. Console

Modul ini sama dengan modul yang ada dijavascript yang gunanya untuk mendebug sebuah code.

```
console.log("Hello World!")
```

#### 2. Process

Digunakan untuk menampilkan dan mengontrol sebuah proses yang sedang berjalan.

```
// Menampilkan file config env yang sedang berjalan didalam file system
const process = require('process')
const env = process.env
console.log(env);
```

#### 3. OS

Sebuah method yang berhubunbgan dengan sistem operasi.

```
// Menampilkan informasi cpu
const os = require('os');
console.log(os.cpus());
```

#### 4. FS

Method yang berfungsi untuk menampilkan maupun mengontrol sebauh file system

```
// Membaca file yang sudah kita buat yaitu os.js
const fs = require('fs');
read = fs.readFileSync('./os.js')
console.log(read.toString());
```

#### 5. Event

Method untuk membuat sebuah event dan menangkapnya

```
const eventEmitter = require('events')

class MyEmitter extends eventEmitter {}

const myEventEmitter = new eventEmitter()

//Buat event
myEventEmitter.on("sapa", () => {
    console.log("Haiiii");
})

//tangkap event
myEventEmitter.emit("sapa")

```

### Berkenalan dengan Express JS

Express JS adalah salah satu framework javascripts yang didesain khusus untuk membuat aplikasi backend yaitu untuk membuat API. Express Js bersifat open source dengan lisensinya dipegang oleh MIT.

#### Apa itu backend application?

![backend-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/backend-1.png)

Back end app adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app. Umumnya server-side app membuat REST API

Kelebihan dari framework ini terletak pada fitur caching, support dengan Google V8 Engine, JavaScript, serta didukung oleh komunitas dan skalabilitas aplikasi yang baik.

#### Cara install express js

Karena expressJS adalah sebuat modules atau package yang dikembangkan menggunakan bahasa javascript, maka kita bisa menggunakan NPM untuk menginstall express JS

```
npm i express save
```

#### Persiapan Development

Terdapat beberapa module yang perlu diinstal untuk mempermudah develop server side application, seperti nodemon (agar dapat restart application otomatis selama proses development)

```
npm i -d nodemon
```

#### Develop menggunakan Express Js

Basic syntax pada Express JS

```
const express = require('express')
const app = express()
const port = 3000

//Parameter req adalah dari client
//Parameter res adalah dari server
app.get('/', => (req, res) {
    console.log("hello world!)
})

app.listen(port, => () {
    console.log(`example listening port at http://localhost:${port}`)
})

```

#### Method-method dalam express:

1. get:

```
app.get('/', => (req, res) {
    console.log("hello world!)
})
```

2. Post:

```
app.Post('/users/:id', => (req, res) {
    res.send("Posting success")
})
```

3. Deleting:

```
app.Post('/users/:id', => (req, res) {
    res.send("Deleting success...")
})
```

#### Middleware dalam Express JS

Middleware function adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle.
Fungsi next biasanya di berikan nama variable next.

```
const express = require("express")
const app = new express()

const middle = (req, res, next) => {
    console.log("Ada middleware")
    next()
}

app.use(middle)

app.get('/', (req,res,next) => {
    console.log("iya ada");
})

app.listen(3000)

```

### Desain Database

Sebelum membuat sebuah aplikasi backend yang sangat terikat dengan yang namanya database, alangkah baiknya kita membuat sebuah desain suatu database. Mendesain suatu database memudahkan kita untuk mengembangkan suatu aplikasi backend dengan adanya desain kita tidak kebingungan dalam menentukan relasi antar entitasnya, dan akan mengurangi terjadinya sebuah anomali data.

#### Entitas Relationship Models

ERM atau Entitas Relationship Models adalah sebuah pendekatan dimana kita membuat sebuah model antar entitas agar memudahkan dalam menentukan antar relasinya.

Contoh ERM :

![erm-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/erm-1.png)

Setelah membuat ERM, kita bisa mengubahnya ke dalam bentuk ERD yaitu Entity Relationship Digram, berikut contohnya:

![erm-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/erm-2.png)

#### normalisasi

Adalah tahap dimana mengorganisaksikan sebuah data ke dalam tabel agar data tersebut:

1. Tidak redundant
2. mudah dicari
3. tidak terjadi anomali

Ada 3 tahap leve; dalam melakukan normalisasi yaitu:

- 1NF
  - Tidak ada urutan dalam penyimpanan data
  - harus menggunakan tipe data yang sama pada 1 kolom
  - harus ada primary key
  - tiap kolom harus berisi nilai tunggal
- 2NF
  - harus dalam bentuk 1NF
  - tidak ada partial depedenct (atribut yang tidak ada hubungan dengan primary key akan dipisah)
- 3nf

  - harus dalam bentuk 3NF
  - tidak ada transitif dependecy (setiap atribut harus bergantung pada primary key supaya tidak terjadi transiitif depedency)

  Berikut contoh dalam melakukan normalisasi:

1. Data ini belum dinormalisasi

![unf](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/unf.png)

2. Tahap 1NF

![1NF](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/1NF.png)

3. Tahap 2NF

![2NF](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/2392593b8853f7d2387a88e937796e148fd1aae8/week-5/images/2NF.png)

Data tersebut sudah tidak ada anomali sehingga tidak perlu lanjut ke dalam tahap 3NF
