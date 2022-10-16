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

## Responsive Web Design

Responsive Web Design adalah suatu keadaan sebuah halaman web dimana tampilannya akan cocok, rapi dan tetap enak dilihat jika diakses dari perangkat apapun dengan resolusi layar yang berbeda. Secara umum, sebuah halaman web tidak bisa menyesuaikan tampilannya sendiri dengan resolusi layar perangkat yang mengaksesnya.

### Tools Untuk Mengembangkan Responsive Web

Tools atau alat yang biasa digunakan oleh seorang developer biasanya terdapat pada bawaan browser, misal pada browser chrome disebut Chrome Dev Tools. Untuk mengaksesnya kita bisa mengikuti langkah berikut :

1. Buka web browser dan buka laman yang ingin kita cek

![responsive-1]()

2. Klik kanan dan klik inspect

![responsive-2]()

3. Klik logo device sebelah elements

![responsive-3]()

4. Nah disini kita bisa pilih dimensi atau ukuran sesuai yang kita inginkan, jika layout web menyesuaikan dengan yang dipilih dan masih rapi berarti web kita responsive

![responsive-4]()

### Viewport

Viewport adalah istilah untuk area tampilan halaman pada device atau perangkat tampilan. Tag meta ini membuat dimensi konten yang ditampilkan sedemikian rupa sehingga ukuran layar dapat digunakan secara efektif. Dalam hal ini, fungsinya memastikan bahwa semua konten ditampilkan dalam keterbacaan dan akurasi yang sama pada layar dengan ukuran berbeda.Meta tag viewport menyesuaikan halaman web dengan panjang dan lebar layar sehingga browser seluler dapat menampilkan semua konten dengan benar.

Cara menambahkan tag meta viewport pada HTML :

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Web Design</title>
</head>

<body>

</body>

</html>
```

### CSS Relative Units

CSS unit adalah satuan untuk menentukan ukuran dari suatu elemen atau kontennya. Misal, jika ingin menentukan margin dari sebuah paragraf, kita bisa memberikan nilai tertentu. Nilai ini akan diikuti oleh satuan (CSS unit).

Dalam CSS ada yang namanya absolut units dan relative units, keduanya berbeda secara sifatnya. Absolut akan selalu tetap dalam ukuran layar apapun, sedangkan relative akan menyesuaikan.

Contoh-contoh relative units:

- **%:** Ukurannya relatif terhadap parent element
- **em:** Ukurannya relatif terhadap font-size dari elemen saat ini
- **rem:** Ukurannya relatif terhadap font-size root elemen (<html>). "rem" = "root em"
- **ch:** Ukurannya mengikuti jumlah karakter (1 karakter sama dengan lebar dari karakter 0/nol font yang sedang aktif)
- **vh:** Ukurannya relatif terhadap tinggi viewport (ukuran jendela tau aplikasi), 1vh = 1/100 dari tinggi viewport
- **vw:** Ukurannya relatif terhadap lebar dari viewport. 1vw = 1/100 lebar viewport
- **vmin:** Ukurannya relatif terhadap ukuran viewport yang lebih kecil (misalnya diorientasi portrait, lebar akan lebih kecil daripada tinggi). 1vmin = 1/100 dari ukuran viewport yang lebih kecil.
- **vmax:** Sama dengan vmin, dia akan melihat ukuran viewport yang lebih besar
- **ex:** Ukurannya relatif terhadap tinggi dari karakter "x" kecil font yang sedang aktif.

### Contoh Implementasi Relative CSS Units:

1. Masukkan kode- kode berikut:

HTML code:

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Responisve Web Design</title>
</head>

<body>
    <div class="box1">
        This box has padding set to 1em, and has a font-size of 20px.
    </div>
    <div class="box2">
        This box also has padding set to 1em, and has a font-size of 40px.
    </div>
</body>

</html>
```

CSS code :

```
.box1 {
    width: 300px;
    font-size: 10px;
    padding: 2em;
    border: 4px solid #ccc;
    margin-bottom: 20px;
  }

  .box2 {
    width: 300px;
    font-size: 20px;
    padding: 1em;
    border: 4px solid #ccc;
  }
```

2. Hasilnya akan seperti ini:

![responsive-5]()

Dari implementasi di atas bisa disimpulkan bahwa units em adalah units relative karena mengikuti ukuran dari suatu font-size. misal font-sizenya 10px dengan padding 2em, ukuran 10px akan dikali 2 sehingga 2em sama dengan 20px. Sedangkan di box-2 padding 1 em menyesuaikan juga dengan font-sizenya yaitu 20px karena hanya 1em, 20 dikalikan 1 hasilnya akan sama yaitu 20px.

### Media-Query

Media query merupakan modul CSS3 yang berguna membuat layout kita responsive dengan menyesuaikan tampilan berdasarkan ukuran layar perangkat.

Terkadang tampilan yang sudah kita desain dengan sedemikian rupa bisa kacau jika ditampilkan pada tampilan mobile. Dengan media query kita dapat menyelesaikan masalah ini dengan menentukan aturan ukuran dan tata letak elemen dengan kondisi-kondisi tertentu

Media query juga disebut dengan Breakpoint, karena cara kerja media query yakni dengan cara mengecheck ukuran viewport(layar/area dimana konten terlihat) apakah sesuai dengan kondisi yang kita deklarasikan, jika benar maka kode dalam kondisi tersebut yang akan dieksekusi. Dengan kata lain media query memberikan kemampuan menggunakan kode css yang sesuai dengan kondisi yang ditentukan.

Contoh implementasi :

- Code HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Responisve Web Design</title>
</head>

<body>
    <div>
        <h1>Latihan Media Query</h1>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTUKiCsH1MQag8ItwI6a65oorHPgtIZxUOR4g&usqp=CAU"
            alt="nanas">
        </div>

</body>


</html>
```

- Code CSS

```
@media only screen and (min-width: 1200px) {
    div {
        display: flex;
    }
    img {
        margin: 0px 20px;
    }
  }
```

Hasilnya :

Jika kurang dari 1200px:

![responsive-6]()

Jika lebih dari 1200px

![responsive-7]()

Image akan berada di kanan atau displaynya flex

### Flexbox dan Grid

Flexbox dan Grids sama-sama berfungsi untuk mengatur tampilan sebuah halaman web menjadi lebih terstruktur dan rapi. Perbedaannya hanya terletak pada arah pembagian dimensinya saja.

Flexbox hanya dapat mengatur arah pembagian dimensi tampilan hanya secara horizontal saja atau secara vertikal saja.

Sebagai contoh, pada flexbox, jika kita atur arahnya menjadi "kolom", maka tampilannya hanya terbagi rata secara vertikal. Begitu juga dengan arah "baris" yang akan secara horizontal.

Contoh Implementasi flexbox :

- Code HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Responsive Web Design</title>
</head>

<body>
    <div id="flex">
        <div>
            BOX 1
        </div>
        <div>
            BOX 2
        </div>
        <div>
            BOX 3
        </div>
        <div>
            BOX 4
        </div>
    </div>
</body>

</html>
```

- Code Css

```
#flex {
    display: flex;
}

#flex div {
    background-color: blue;
    padding: 20px;
    margin: 10px;
    border: 1px;
    border-color: black;
    border-style: solid;
}
```

Hasilnya:

![flebox]()

Contoh Implementasi Grid :

- Code HTML :

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Responsive Web Design</title>
</head>

<body>
    <div id="grid">
        <div class="box-1">
            BOX 1
        </div>
        <div class="box-2">
            BOX 2
        </div>
        <div class="box-3">
            BOX 3
        </div>
        <div class="box-4">
            BOX 4
        </div>
    </div>
</body>

</html>
```

- Code CSS

```
#grid {
    display: grid;
    grid-template-areas:
    'header header header header'
    'left left right right'
    'footer footer footer footer';
}

#grid div {
    background-color: blue;
    padding: 20px;
    margin: 1px;
    border: 2px;
}

.box-1 {
    grid-area: header;
}

.box-2 {
    grid-area: left;
}

.box-3 {
    grid-area: right;
}

.box-4 {
    grid-area: footer;
}
```

Hasilnya :

![grid]()

## Bootstrap

Bootstrap adalah sebuah framework css yang fungsinya untuk memudahkan kita dalam melakukan styling pada web dan memudahkan kita untuk membuat web yang responsive.

Untuk lebih jelasnya kita langsung saja masuk ke dalam implementasi:

1. Untuk memasukkan Bootstrap secara online bisa menggunakan cdn

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    /// Memasukkan Bootstrap secara online
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <title>Responsive Web Design</title>
</head>

<body>
</body>

</html>
```

2. Kita coba menggunakan class-class dalam bootstrap seperti berikut:

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <title>Responsive Web Design</title>
</head>

<body>
    <h1 class="container bg-primary">Hello World!</h1>

    </div>

</body>

</html>
```

Hasilnya:

![Bootstrap-1]()

### Layout dalam Bootstrap

Layout dalam bootstrap menggunakan row dan col seperti grid pada css, dan class container sebagai penampung utamanya.

Berikut Contoh Penerapanya:

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <title>Responsive Web Design</title>
</head>

<body>
    <div class="container p-5">
        <div class="row gy-6">
            <div class="col-6">
                <div class="p-3 border bg-primary">BOX 1</div>
            </div>
            <div class="col-6">
                <div class="p-3 border bg-primary">BOX 2</div>
            </div>
            <div class="col-6">
                <div class="p-3 border bg-primary">BOX 3</div>
            </div>
            <div class="col-6">
                <div class="p-3 border bg-primary">BOX 4</div>
            </div>
        </div>

    </div>

</body>

</html>
```

Hasilnya :

![Bootstrap-2]()

### Component Bootstrap

Ada banyak sekali component-component pada bootstrap yang memudahkan dan mempercepat development pada suatu web, contoh component bootstraps :

- Alert
- Carousel
- Card
- Button
- Modal
- Dan masih banyak lagi kita bisa cek di official [bootstrap](https://getbootstrap.com/docs/5.0/components)

berikut contoh salah satu penggunaan component bootstrap yaitu component Card

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <title>Responsive Web Design</title>
</head>

<body>
    <div class="row row-cols-1 row-cols-6">
        <div class="col">
            <div class="card h-100">
                <img src="https://images.unsplash.com/photo-1665856314098-4aa9ff7a3d76?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80"
                    alt="" class="card-img-top">
                <div class="card-body">
                    <h5 class="card-title">Special title treatment</h5>
                    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div>
        <div class="col">
            <div class="card h-100">
                <img src="https://images.unsplash.com/photo-1665807897792-86ece12fd7e5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw0fHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60"
                    alt="" class="card-img-top">
                <div class="card-body">
                    <h5 class="card-title">Special title treatment</h5>
                    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div>
        <div class="col">
            <div class="card h-100">
                <img src="https://images.unsplash.com/photo-1665683607528-f1bed144ce6e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxN3x8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60"
                    alt="" class="card-img-top">
                <div class="card-body">
                    <h5 class="card-title">Special title treatment</h5>
                    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div>
    </div>

    </div>

</body>

</html>
```

Hasilnya :

![Bootstrap-3]()
