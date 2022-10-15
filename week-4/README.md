# Writing Test

## Fetch

Pada minggu lalu sudah memahami tentang asynchronous, yaitu sebuah metode eksekusi kode dimana kode tersebut dijalankan secara langsung tidak menunggu antrian.

Fetch adalah salah satu method javascript untuk mengambil data yang hanya bisa dijalankan secara asynchronous.

**Kenapa?**

karena memerlukan waktu untuk mengeksekusi kodenya, di sisi lain fetch adalah method yang biasanya mengambil data dari data eksternal bukan lokal.

Minggu lalu juga sudah menyinggung tentang Async - Await yaitu salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise, sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil. Fitur tersebut digunakan bersamaan dengan method .fetch().

**Contoh penulisan async - await bersamaan dengan fetch :**

- Code untuk HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="script.js" defer></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM"
        crossorigin="anonymous"></script>
    <title>Manga</title>
</head>

<body>
    <div class="container">

        <h1 style="text-align: center;">List Popular Anime</h1>

        <div id="tampil" class="row row-cols-1 row-cols-md-6 g-3">
        </div>
    </div>


</body>

</html>
```

- Code untuk Javascript

```
//link Api
let url = "https://raznime.herokuapp.com/popular"

let tampil = document.getElementById("tampil")


let getData = async() => {
    // fetching api menggunakan http request
    let getManga= await fetch(url)
    // mengubah data api menjadi json()
    let dataManga = await getManga.json()
    // Melakukan perulangan untuk mendapatkan data dalam array
    dataManga.forEach(e => {
        // menampilkan data menggunakan DOM
        tampil.innerHTML += `
        <div class="col">
        <div class="card h-100">
          <img src="${e.animeImg}" class="card-img-top" alt="...">
          <div class="card-body">
            <h6 class="card-title">${e.animeId}</h6>
          </div>
        </div>
      </div>
        `
    });
    console.log(tampil);

}
getData()
```

### HTTP Request

Seperti penjelasan di atas method fetch pada javascript menggunakan http request,

**Apa itu http request?**

HTTP adalah protokol untuk mengambil sumber data seperti dokumen HTML. Tujuannya adalah untuk pertukaran data di Web dan merupakan protokol client-server, yang berarti permintaan sesuai dengan apa yang diminta oleh peminta (requester), biasanya browser Web. Dokumen lengkap direkonstruksi kembali dari sub-dokumen berbeda yang diambil, misalnya, teks, deskripsi layout, gambar, video, skrip, dan banyak lagi.

### JSON

HTTP adalah sebuah protokol pertukaran data, nah dalam bentuk apa data tersebut dipertukarkan? ada yang namanya JSON, adalah data Object yang sering digunakan dalam pertukaran data karena sifatnya yang fleksibel dan dapat diambil dalam bahasa pemrogaman apapun.

### API

API adalah singkatan dari Application Programming Interface. API sendiri merupakan interface yang dapat menghubungkan satu aplikasi dengan aplikasi lainnya.

Dengan kata lain, peran API adalah sebagai perantara antar berbagai aplikasi berbeda, baik dalam satu platform yang sama atau pun lintas platform.

**URL yang kita dapatkan dengan method Fetch adalah sebuah API yang di dalamnya ada banyak sumber data.**

## Git & Github Lanjutan

Mengingat kembali tentang GIT, GIT adalah sebuah tools bagi para programmer dan developer yang berfungsi sebagai control system untuk menjalankan proyek pengembangan software. GIT adalah singkatan dari Group Inclusive Tour. Tujuan penggunaan GIT yakni untuk mengelola versi source code program dengan menentukan baris serta kode yang akan ditambahkan atau diganti.

**Sehingga Kenapa git penting bagi programmer?**

Dengan adanya git programmer dapat mengelola source kodenya lebih baik, misalkan suatu kode disimpan pada saat sekarang namun ada kesalahan, dengan demikian ingin kembali lagi ke versi lebih awal lagi yang tanpa adanya masalah(bug), dengan git programmer bisa kembali ke versi awal.

**Terus apa itu github?**

Sudah dibahas diminggu pertama writing, bahwa github merupakan suatu merk, atau sebuah perusahaan yang menyediakan layanan internet dengan menggunakan tools git, sehingga layanan git tersebut berbasis nantinya akan berbasis cloud. Ada merk lain seperti Gitlab dan bitbucket yang fungsinya sama dengan github.

karena implementasi git sudah dibahas di week 1,
untuk Selanjutnya akan fokus membahas tentang git lanjutan dimana kita bisa menggunakan github untuk berkolaborasi.

### Github Collab

Dalam github kita dapat berkolaborasi dengan sesama programmer lainnya dengan membentuk organisasi, berikut contoh implementasinya.

1.  Membuat Organisasi

![git-collab-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-1.png)

2.  Klik yang free karena disini kita hanya sebagai latihan

![git-collab-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-2.png)

3.  Isi form sesuai petunjuk

![git-collab-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-3.png)

4.  Setelah melakukan langkah-langkah isi form, maka akan muncul seperti ini, artinya akun organisasi berhasil dibuat kita dapat melakukan beberapa perubahan seperti membuat repository, menambahkan anggota, pull request, dll

![git-collab-4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-4.png)

### Git Merge

GIT merge adalah perintah untuk menggabungkan kedua cabang atau branch pada suatu repository, untuk lebih jelasnya langsung masuk ke dalam implementasi saja:

1. Siapkan sebuah repository dengan cara create repository di github

![git-collab-5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-5.png)

2. Berikut jika repository berhasil dibuat

![git-collab-6](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-6.png)

3. Tambahkan branch baru

![git-collab-7](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-7.png)

4. Branch baru berhasil dibuat

![git-collab-8](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-8.png)

5. Kita coba git clone repository tersebut ke dalam local

![git-collab-9](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-9.png)

6. Kita lakukan beberapa perubahan file readme pada branch dev, gunakan perintah `git switch <nama branch>` untuk berganti cabang

![git-collab-10](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-10.png)

7. kita coba lakukan merge pada branch main, lalu coba kita git push

![git-collab-11](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-collab-11.png)

8. hasilnya akan sama antara 2 cabang

### Git pull Request

1. lakukan langkah-langkah sperti sebelumnya

![git-pull-request-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-pull-request-1.png)

2. Disini akan muncul notifikasi pull request, artinya kita bisa melakukan sebuah
   request ke dalam branch main, coba kita klik

![git-pull-request-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-pull-request-2.png)

3. akan masuk ke halaman ini, kita coba create request

![git-pull-request-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-pull-request-3.png)

4. Kita coba konfirmasi request

![git-pull-request-4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-pull-request-4.png)

5. Request berhasil terpenuhi dan tidak ada konflik, merge atau penggabungan berhasil

![git-pull-request-5](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-pull-request-5.png)

6. Hasilnya kan sama seperti git merge di atas, keduanya akan sama antara branch nya

### Cara mengatasi konflik

Ketika kita melakukan merge pada suatu merge namun branch tersebut memiliki suatu error seperti ada letak kode yang sama maka akan timbul sebuah conflict seperti berikut:

![git-conflict-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-conflict-1.png)

1. Cukup klik sesuai yang kita inginkan, kode mana yang sesuai maka git akan otomatis menyesuaikan

![git-conflict-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-conflict-2.png)

2. Seperti berikut hasilnya, kita coba simpan dan push

![git-conflict-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-conflict-3.png)

3. branch main akan berisi sesuai yang kita pilih

![git-conflict-4](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/a64e5773d249563c48215344fb1e45993feaf6c3/week-4/images/git-conflict-4.png)
