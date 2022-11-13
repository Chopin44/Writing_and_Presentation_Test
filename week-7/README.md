# Writing Test Backend Development Week 3

## In Deepth with sequileze

Sebelumya kita sudah memahami tentang cara menginstall dan cara menjalankan sebuah sequileze dengan menggunakan CLI, dan juga mencoba untuk mengoneksikan database mysql dengan metode sequileze.

Ketika sebuah sequileze di inisiasi menggunakan perintah `npx sequileze-cli init`
perintah tersebut akan mengotomasi pembuatan folder-folder yang diperlukan untuk development sebuah aplikasi dengan menggunakan sequileze.

Foldernya yaitu :

- **config** : didalamnya ada file config.json Digunakan untuk mengatur koneksi sebuah database
- **migrations** : Isinya biasanya untuk memerintah atau menginisiasi model tersebut ke dalam database (pembuatan tabel)
- **models** : Digunakan untuk menggenerate sebuah field-field dalam database.
- **seeder** : Otomasi untuk mengisi record dalam database.

Nah, setelah langkah inisiasi dilakukan biasanya kita langsung mengubah dan mengatur file config.json untuk disesuaikan ke dalam database yang kita punya. untuk langkah-langkah awal ini kita bisa cek minggu sebelumnya di [sini](https://github.com/Chopin44/Writing_and_Presentation_Test/tree/main/week-6)

### Models dan Migrations

Models adalah sesuatu yang merepresentasikan field-field dalam database. Ketika sebuah models dibuat folder `migrations` pun akan terbuat, karena sebuah migrations biasanya mencontoh models yang disediakan.

contoh perintah:

```
npx sequelize-cli init
npx sequelize-cli model:generate --name User --attributes firstName:string,lastName:string,email:string
```

Folder yang terbuat :

![sequileze - 1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/sequileze%20-%201.png)

Dan isi models dan migrations:

![sequileze - 2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/sequileze%20-%202.png)

![sequileze - 3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/sequileze%20-%203.png)

dengan perintah `db:migrate` akan menjalankan sebuah file di dalam migrations yang didalamnya lagi ada kode berakhiran dengan `up` sedangkan perintah `db:undo` akan menjalankan perintah code yang berakhiran down.

Sebuah migrations dapat diatur dan disesuaikan perintah di dalamnya, bisa cek lebih dalam di [sini](https://sequelize.org/docs/v6/other-topics/migrations/)

### Seeder

Seeder adalah sebuah metode untuk menyimpan perintah-perintah insert. Sehingga di dalamnya mengandung record-record yang akan di isikan ke dalam sebuah database.

Berikut contoh perintah untuk menginisiasi sebuah seed:

```
npx sequelize-cli seed:generate --name demo-user
```

File baru akan tampil di dalam folder seeder:

![sequileze - 4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/sequileze%20-%204.png)

Selanjutnya kita isikan record apa saja sesuai field-field yang kita buat contoh:

![sequileze - 5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/sequileze%20-%205.png)

Dan jalankan perintah `npx sequelize-cli db:seed:all` maka record pun terisi otomatis.

### Simple Query dalam sequileze

Setelah tahap-tahap di atas sudah memahami dan sudah mencoba mengimplementasikan, langkah selanjutnya bisa mencoba query-query sequileze.

#### INSERT

perintah memasukkan sebuah record ke dalam field tabel, contoh :

```
// Create a new user
const jane = await User.create({ firstName: "Jane", lastName: "Doe" });
```

#### SELECT

perintah menseleksi dan biasanya untuk melakukan pencarian dalam tabel, contoh:

```
const users = await User.findAll();
```

#### UPDATE

Untuk mengubah record di dalam sebauh tabel database, contoh:

```
await User.update({ lastName: "Doe" }, {
  where: {
    lastName: null
  }
});
```

#### DELETE

Menghapus record dalam tabel database, contoh :

```
// Delete everyone named "Jane"
await User.destroy({
  where: {
    firstName: "Jane"
  }
});
```

Cek lebih dalam tentang query bisa di [sini](https://sequelize.org/docs/v6/core-concepts/model-querying-basics/)

## MongoDB

MongoDb adalah salah satu Database yang bertipe database NoSQL atau singkatan dari not only SQL. Dan pengertian dari NoSQL sendiri adalah sebuah database yang tidak mengandalkan suatu relasi di dalamnya. ada banyak sekali database yang bertipe NoSQL selain MongoDB, seperti Cassandra, Redis, CouchDB, dan masih banyak lagi.

Nah, dikarenakan MongoDB adalah sebuah database yang NoSQL sehingga database yang di simpan berbentuk dokumen yang berformat JSON.

### Cara Kerja MongoDB

Kita sudah berkenalan dengan MongoDB lebih baiknya kita juga berkenalan bagaimana cara kerja MongoDB apakah memiliki perbedaan dengan Database SQL.

Untuk lebih jelasnya kita masuk ke dalam implementasi langsung, sebelumnya install terlebih dahulu mongoDB dapat mendownloadnya di [sini](https://repo.mongodb.org/yum/amazon/2/mongodb-org/6.0/x86_64/RPMS/mongodb-org-server-6.0.2-1.amzn2.x86_64.rpm)

1. Jika sudah menginstall mongoDB dengan benar, bisa mengeceknya dengan CLI ketikkan perintah `mongosh`

![mongo - 1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongo%20-%201.png)

2. Untuk mengecek database yang ada di dalamnya bisa mengetikkan perintah `show databases;`

![mongo - 2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongo%20-%202.png)

3. Berikutnya coba masukkan sebuah dokumen ke dalam database, sebelumnya gunakan perintah `use <database>` untuk memilih database yang ingin dikelola, kemudian ketikkan perintah sebagai berikut:

```
db.inventory.insertMany([
   {item: "granat", jumlah: 5},
   {item: "handgun", jumlah: 3},
   {item: "sniper", jumlah: 1},
])
```

![mongo - 3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongo%20-%203.png)

4. Untuk memastikan record sudah masuk bisa menggunakan perintah

```
db.inventory.find({})
```

![mongo - 4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongo%20-%204.png)

5. Untuk lebih jelas lagi dalam memonitor mongoDB bisa menggunakan sebuah GUI untuk mongoDB yaitu mongoDB compass, bisa di install di [sini](https://downloads.mongodb.com/compass/mongodb-compass-1.33.1-darwin-x64.dmg)

6. Setelah menginstall bisa mengoneksikannya dengan database mongo kita, URL default mongo biasanya adalah `mongodb://localhost:27017`

![mongo - 5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongo%20-%205.png)

7. kemudian klik konek dan hasilnya akan seperti ini, kita bisa melihat database dan collection-collection yang ada:

![mongo - 6](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongo%20-%206.png)

Nah dapat dilihat pada struktur data pertama dan kedua yang ada, mongoDB atau NOSQL membolehkan suatu record diisi fleksibel dan bebas tanpa suatu field-field yang sama. Itulah yang menjadi perbedaan SQL dan NoSQL.

## Mongoose

Mongoose adalah sebuah library yang khusus digunakan untuk mongoDB, mongoose adalah ODM sama seperti ORM SQL yaitu sequelize. Sehingga sebagai Object Modelling antara database dan codingan, maksutnya adalah kita dapat mengelola database dengan OOP atau coding.

### Cara Kerja Mongoose

Mongoose menerjemahkan antara objek dalam kode dan representasi objek tersebut di mongoDB.

Untuk lebih jelasnya langsung saja masuk ke dalam implementasi :

1. Install Mongoose menggunakan perintah seperti biasa :

```
npm install mongoose
```

2. Nah setelah berhasil di install kita dapat menggunakan mongoose untuk mengoneksikan ke mongoDB database, berikut contoh codingannya :

- config.js

```
const mongoose = require('mongoose');
const db = async() => {
    try {
        await mongoose.connect('mongodb://localhost:1212/ToDoApp');
        console.log("Database terkoneksi!");
      } catch (error) {
        console.log(error);
      }

}

// module ini dapat dipanggil ke dalam app.js
module.exports = db
```

- app.js (harap install express !)

```
const express = require("express");
const app = express();
const allRouter = require("./routes");
const db = require("./config/config");

app.use(express.json());

//koneksi ke mongodb
db();

app.use(allRouter);
app.listen(1212, (err) => {
  console.log("Server running on Port " + 1212);
});

```

Jika berhasil akan muncul log koneksi berhasil seperti ini :

![mongoose - 1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongoose%20-%201.png)

3. Setelah terkoneksi kita coba membuat models. contoh codingan:

```
const mongoose = require('mongoose');
const { Schema } = mongoose

const userSchema = new Schema({
    name:  String,
    class: String,
    email: String,
    password: String,
  });

const User = mongoose.model('users', userSchema)

module.exports = User

```

4. Models sudah dibuat kita bisa mencoba memasukkan beberapa codingan ke dalam method endpoint kita, contoh codingan:

- Mendapatkan data user sesuai nama

```
router.get("/", async (req, res) => {
    try {
      const dataUser = await user.find({}, "name");
      res.json({
        message: "get Data success",
        data: dataUser,
      });
    } catch (error) {
      res.status(500).send({
        message: "opps something error!",
        error: error.message,
      });
    } )
```

Berikut hasil API-nya :

![mongoose - 2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/mongoose%20-%202.png)

## Docker

Docker adalah sebuah software yang digunakan untuk menjalankan software-software menggunakan sebuah konsep container.

Docker berfungsi sebagai penyedia layanan virtual bagi aplikasi yg di install pada sebuah host.

Docker akan menyediakan hal-hal yang diperlukan untuk aplikasi mulai dari akses file, koneksi internet, hingga port agar aplikasi dapat berjalan dengan mulus.

### Docker vs Virtual Machine

Cara kerja sebuah docker memang mirip sekali dengan sebuah Virtual Machine, yang membedakannya adalah pada saat berjalannya suatu docker tidak butuh sebuah OS standalone untuk berjalan. Sedangkan VM membutuhkan OS di setiap VM nya.

![docker - 1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/docker%20-%201.png)

Ketika kita ingin menjalankan 3 VM, setiap VM harus menginstall sebuah OS di masing-masing VM, ini membutuhkan resource yang lebih banyak dan sudah pasti waktu dalam pembuatannya pun akan lebih lama.

Berbeda dengan Docker, ketika kita ingin membuat 3 aplikasi, atau 3 ekosistem, docker hanya memperlukan sebuah Lib/Bins dari software yang ingin dibuat dan tidak perlu menginstall OS terlebih dahulu, 3 aplikasi ini berjalan di dalam sebuah container engine, sehingga pembuatannya pun cepat dan efisien.

### Cara Menggunakan Docker

1. Install docker sesuai OS kita, bisa cek ke situs [official](https://docs.docker.com/engine/install/) nya
2. Ketika docker sudah berhasil di install, kita bisa coba cek untuk memastikannya dengan perintah `docker run hello-world` di CLI.

   ![docker - 2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/docker%20-%202.png)

   Sebenarnya pada log di atas ada sebuah tulisan mengenai pull, nah disitu dijelaskan bahwa image local kita belum ada image hello-world. Sehingga terjadilah pull atau yang artinya mendownload image yang ada di dalam cloud docker, ada dalam docker hub.

3. Docker ternyata benar-benar berhasil di install, kita bisa coba buka docker desktop, disitu ada beberapa image yang sudah saya install

   ![docker - 3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/docker%20-%203.png)

   sudah dijelaskan diatas ketika kita menjalankan perintah `docker run hello-world` berguna untuk menjalankan image hello-world sekaligus menge pull atau mendownload image dari cloud ketika kita tidak mempunyai img di dalam local.

4. kita bisa jalankan ulang dalam tab container, setiap container membutuhkan image untuk menjalankan container, dan setiap image di jalankan akan membuat sebuah container baru, berikut contohnya :

   ![docker - 4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/docker%20-%204.png)

   terlihat ada 3 container

   ![docker - 5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/docker%20-%205.png)

   kita coba jalankan image mongo dan buat container baru dengan klik run berikut

   ![docker - 6](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/c3d2742f1f3217c9e8971591f1e32f117ad9e646/week-7/images/docker%20-%206.png)

   terilhat container baru berhasil ditambahkan dan dalam keadaan aktif, kita bisa matikan kembali dengan pencet simbol kotak.
