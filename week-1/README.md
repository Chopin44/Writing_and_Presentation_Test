# Writing and Presentation Test Week 1


## HTML
HTML atau singkatan dari Hyper Text Markup Language merupakan sebuah bahasa struktural yang digunakan dalam membuat website, disebut bahasa struktural karena merupakan sebuah bahasa untuk membuat struktur-struktur dalam web atau bisa disebut sebagai kerangka web, sehingga bukan dikategorikan sebagai bahasa pemrogaman karena tidak menghasilkan sebuah fungsi.

### Struktur Dasar HTML
<p align="center" width="100%">
    <img width="60%" src="https://www.petanikode.com/img/html/dasar/struktur-html.png">
</p>
<h6 align="center">gambar di atas merupakan sebuah struktur paling dasar dalam membuat HTML</h6>
Dalam gambar dijelaskan bahwa tag yang paling penting adalah tag HTML karena merupakan tag yang mendeklarasikan bahwa sebuah file tersebut atau tag tesebut dibaca sebagai sebuah HTML. <br> <br>

Sebenarnya dalam mempelajari HTML yang terpenting adalah kita harus memahami sebuah struktur dari Tag terlebih dahulu, berikut struktur Tag dalam HTML:
<p align="center" width="100%">
    <img width="60%" src="https://www.petanikode.com/img/html/tag/element.png">
</p>
<h6 align="center">gambar di atas merupakan sebuah struktur Tag yang ada dalam HTML</h6>

Struktur paling luar adalah pembuka dan penutup tag disimbolkan dengan < dan > atau sering disebut dengan angled brackets, didalamnya bisa diisikan sebuah atribut untuk memberikan sifat dari tag tersebut. Antara kurung <> </> adalah konten dari sebuah tag yang ingin kita beri, bisa berupa text, foto, maupun video, tergangtung element tag yang kita beri.

### Jenis-Jenis Tag HTML
Dalam HTML ada 2 jenis Tag yaitu:
  <h4>
    <ol>
      <li>
      <h3>Single tag</h3>
      </li>
      Merupakan tag html yang hanya 1 kurung saja, contohnya:
        <p width="100%">
            <img width="33%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/d473b55e69f1c9db81b54bdd1484730b5c4d5c6b/Week%201./singletag.png">
        </p>
      <li>
          <h3>Double tag</h3>
      </li>
        Merupakan tag pada umumnya yang memiliki pembuka dan penutup, contohnnya:
        <p width="100%">
            <img width="33%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/d473b55e69f1c9db81b54bdd1484730b5c4d5c6b/Week%201./doubletag.png">
        </p> 
    </ol>
  </h4>

## Exercise
<ol>
    <li>Siapkan Text Editor bisa menggunakan Notepad++, Atom, Sublime, ataupun Visual Studio Code sesuai yang diinginkan</li>
    <li>Buka Text Editor dan buat sebuah file baru</li>
     <p width="100%">
        <img width="33%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/154a9169831960641e292887104b1435e8cc92a6/Week%201./1.png">
    </p>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/154a9169831960641e292887104b1435e8cc92a6/Week%201./2.png">
    </p>
    <li>Deklarasikan tag-tag yang penting dalam HTML</li>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/154a9169831960641e292887104b1435e8cc92a6/Week%201./3.png">
    </p>
    <li>Kita coba beri tag H1</li>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/154a9169831960641e292887104b1435e8cc92a6/Week%201./4.png">
    </p>
    <li>Buka File tersebut via browser</li>
    <li>Terdapat Text Hello World! di browser maka HTML berhasil dibuat</li>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/154a9169831960641e292887104b1435e8cc92a6/Week%201./5.png">
    </p>
</ol>

## CSS
CSS atau singkatan dari Cascading Style Sheets yaitu bahasa yang digunakan untuk menentukan tampilan dan format halaman website. Dengan CSS, kita bisa mengatur jenis font, warna tulisan, latar belakang halaman, dan masih banyak lagi. Dengan adanya CSS website kita akan terlihat lebih menarik, sehingga bisa juga dikatakan sebagai baju atau kosmetik yang disisi lain HTML adalah sebagai kerangkanya.

### Struktur Penulisan CSS
<p align="center" width="100%">
    <img width="60%" src="https://bilabil.com/wp-content/uploads/2019/12/struktur-css.jpg">
</p>
<h6 align="center">gambar di atas merupakan sebuah struktur penulisan dalam membuat CSS</h6>

Dalam gambar tersebut ada sebuah selector, property, dan value, nah apakah itu?
<h4>
    <ol>
      <li>
      <h3>Selector</h3>
        </li>
        Merupakan sebuah sintaks yang ditulis agar element sebuah CSS dapat ditunjuk. Seperti contoh tag-tag pada HTML seperti h1, p, div, span, img, dan masih banyak lagi.
      <li>
          <h3>Property</h3>
      </li>
        Merupakan pemberian sifat pada sebuah element. Seperti contoh ingin memberi warna text dengan color: , memberi warna background dengan background-color: , dan masih banyak lagi contohnya.
       <li>
          <h3>Value</h3>
      </li>
        Merupakan isi dari sebauh property atau sifat apa yang ingin diberikan ke dalam element tertentu. Contoh, color: red, propertynya color atau warna, warna apa yang ingin kita beri? red atau merah.
    </ol>
 </h4>


### Cara Penulisan CSS
<h4>
<ol>
  <li>
  <h3>Inline</h3>
  </li>
  Merupakan cara penulisan CSS langsung ke dalam tag HTML, berikut contohnya:
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/06ba36d85a39721d02b16ca7c01b3497dd98313f/Week%201./css%201.png">
    </p>
  <li>
      <h3>Internal</h3>
  </li>
    Merupakan penulisan CSS dalam file HTML, dengan tag Style sebagai pembuka dan penutupnya, berikut contohnya:
    <p width="100%">
         <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/0d709ab2e2c70934c59882dd84155c6c566ca6c3/Week%201./css%202.png">
    </p>
    <li>
      <h3>Eksternal</h3>
  </li>
    Merupakan penulisan CSS diluar file HTML, untuk memanggilnya bisa menggunakan tag link, berikut contohnya:
    <p width="100%">
         <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/0d709ab2e2c70934c59882dd84155c6c566ca6c3/Week%201./css%203.png">
    </p>
    <p width="100%">
         <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/06ba36d85a39721d02b16ca7c01b3497dd98313f/Week%201./css%204.png">
    </p> 
</ol>
</h4>

## Exercise
Mungkin setelah memahami struktur penulisan CSS dan cara penulisan CSS, kita masuk saja ke dalam sebuah latihan. (Disini penulis menganggap semua sudah memahami HTML)
<ol>
    <li>Seperti biasa, siapkan Text Editor bisa menggunakan Notepad++, Atom, Sublime, ataupun Visual Studio Code sesuai yang diinginkan</li>
    <li>Buka Text Editor dan buat sebuah file baru CSS (sebelumnya sudah exercise <a href="https://github.com/Chopin44/Writing-and-Presentation-Test/edit/main/Week%201./ReadMe.md#exercise">HTML</a>)</li> 
     <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/f176d0e20bf0c8d884a9754c026db4105bae289c/Week%201./css-lat1.png">
    </p>
    <li>Isikan beberapa sintaks berikut</li>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/f176d0e20bf0c8d884a9754c026db4105bae289c/Week%201./css-lat2.png">
    </p>
    <li>Panggil CSS ke dalam file Html menggunakan tag link</li>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/f176d0e20bf0c8d884a9754c026db4105bae289c/Week%201./css-lat3.png">
    </p>
    <li>Buka file html lewat browser</li>
    <li>Text dengan tag h1 yaitu Hello World akan berubah sesaui property dan value yang diberikan yaitu text yang diberi warna merah</li>
    <p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/429243a5ffcbaef073d8d154a4f14d10642b66f8/Week%201./css-lat4.png">
    </p>
</ol>

## Javascript Dasar
JavaScript adalah bahasa pemrograman yang digunakan dalam pengembangan website agar lebih dinamis dan interaktif. Kalau sebelumnya kita mengenal HTML dan CSS, yang merupakan kerangka dan komestik dari suatu website sekarang akan ada yang namanya JavaScript, Javascript dapat meningkatkan fungsionalitas pada halaman web. Bahkan dengan JavaScript ini kita bisa membuat aplikasi, tools, atau bahkan game pada web.

JavaScript atau kita singkat menjadi JS merupakan bahasa pemrograman jenis interpreter, sehingga kita tidak memerlukan compiler untuk menjalankannya. JavaScript memiliki fitur-fitur seperti berorientasi objek, client-side, high-level programming, dan loosely typed.

## Cara menjalankan Javacript
Berikut langkah menjalankannya:
1. Kita dapat menjalankan javascript langsung dengan menggunakan browser.
2. Untuk menjalankan Javascript di dalam browser tentunya kita harus memiliki file [HTML](https://github.com/Chopin44/Writing-and-Presentation-Test/edit/main/Week%201./ReadMe.md#exercise) terlebih dahulu.
3. Buatlah file baru berformat js tuliskan beberapa kode berikut:
```
console.log("Hello World")
```
<p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/a19dab8a6b383a67431e514e80880c766ad1d94a/Week%201./js-1.png">
</p>
4. Sisipkan tag script pada file HTML sepertri berikut untuk memanggil javascript
<p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/a19dab8a6b383a67431e514e80880c766ad1d94a/Week%201./js-2.png">
</p>
5. Atau kalian bisa menuliskannya langsung ke dalam file HTML menggunakan tag script
<p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/a19dab8a6b383a67431e514e80880c766ad1d94a/Week%201./js-3.png">
</p>
6. Kemudian buka file HTML lewat browser, memang tidak akan menampilkan apa-apa di dalam laman, tetapi kalian bisa melihat hasilnya di dalam console, dengan meng klik kanan mouse dan inspect element, cari bagian console.
<p width="100%">
        <img width="100%" src="https://github.com/Chopin44/Writing-and-Presentation-Test/blob/4f5d06bc036778a9924bff70aa57535697e6cd05/Week%201./js-4.png">
</p>

## Tipe Data Javascript
Tipe data dalam javascript ada 5, yaitu:
- Number
- String
- Boolean
- Array
- Objects

### 1. Number
Merupakan tipe data bilangan bulat seperti 0, 1, 2, 3, 4, dst...
Penulisannya biasanya tidak diapit apapun, contoh:
```
let a = 100
```

### 2. String
Merupakan tipe data berupa kalimat atau kata, biasanya diapit oleh tanda ' ' (petik satu) atau " " (petik dua) ataupun menggunakan (``) backtick.
contoh:
```
let a = 'Rodhi'
let b = "Andriansah"
let c = `Ganteng`
```
### 3. Boolean
Merupakan tipe data berupa dua nilai, yaitu benar (True) atau salah (False). Tipe data boolean sering digunakan untuk membuat alur logika program. Struktur logika seperti if, else, while, dan do while, membutuhkan nilai boolean sebagai ‘pengontrol’ alur program.
contoh:
```
let a = true
let b = false
```
### 4. Array
Merupakan tipe data berupa array yaitu tipe data yang dapat menyimpan banak data dalam satu variable.
contoh:
```
const arr = ['Rodhi', "Andriansah", 20]
```
### 5. Objects
Merupakan sekumpulan list dari tipe data primitif (terkadang juga tipe data reference) yang menyimpan nilai dengan konsep berpasangan name-value. Tiap item (yang lebih dikenal dengan nama variabel) disebut dengan property, dan function disebut dengan method
contoh:
```
var manusia = {
     nama : "Rodhi",
     alamat : "Pekalongan",
     umur : 20,
     pekerjaan  : "Mahasiswa"
};
```

## Looping atau Perulangan Javascript
Berikut jenis-jenis perulangan dalam javascript :
1. for

contoh:
```
for (let index = 1; index <= 5; index++) {
    console.log(index); 
} // hasil
//1
//2
//3
//4
//5
```
2. foreach

biasanya digunakan untuk mengambil data dalam array

contoh:
```
let a = [1,2,3,4,5]
a.forEach(angka => {   
    console.log(angka);
}) // hasil
//1
//2
//3
//4
//5
```
3. while

contoh:
```
let a = 0
while (a<5){
    a = a+1
    console.log(a);
}
//hasil
//1
//2
//3
//4
//5
```

4. do while

contoh :
```
let a = 0
do {
    a = a+1
    console.log(a);
} while (a<5);
//hasil
//1
//2
//3
//4
//5
```
### Function Javascript

function adalah sekumpulan kode yang digunakan untuk melakukan tugas tertentu.
```
function name(parameter1, parameter2, parameter3) {
  // kode untuk dieksekusi
}
```


## Percabangan Javascript
Ada 4 jenis yang umum digunakan dalam pemrogaman khususnya javascript yaitu:

1. if
2. if/else
3. if/else/if
4. switch/case

### 1. if
Percabangan if merupakan percabangan yang hanya memiliki satu blok pilihan saat kondisi bernilai benar.
contoh:
```
let a = true

if (a) {
    console.log("ini benar");
} // muncul ini benar

let b = false

if (b) {
    console.log("ini benar");
}// tidak muncul apa-apa karena tidak ada kondisi ketika salah
```
### 2. if/else
Percabangan if/else merupakan percabangan yang memiliki dua blok pilihan saat kondisi if bernilai benar dan kondisi else bernilai salah.
```
let a = true

if (a) {
    console.log("ini benar");
} // muncul ini benar

let b = false

if (b) {
    console.log("ini benar");
} else {
    console.log("ini salah");
}// muncul ini salah 
```
### 3. if/else/if
Percabangan if/else merupakan percabangan yang memiliki lebih dari dua blok pilihan.
contoh:
```
let nilai = "A"

if (nilai == "A") {
    console.log("Hebat");
} else if(nilai == "B") {
    console.log("Biasa");
} else {
    console.log("Jelek");
}// muncul nilai A
```
### 4. switch/case
Sama dengan if/else/if namun dengan struktur yang berbeda

contoh:
```
let jawab = "1"

switch(jawab){
    case "1":
        hadiah = "Tisu";
        break;
    case "2":
        hadiah = "1 Kotak Kopi";
        break;
    case "3":
        hadiah = "Sticker";
        break;
    case "4":
        hadiah = "Minyak Goreng";
        break;
    case "5":
        hadiah = "Uang Rp 50.000";
        break;
    default:
       hadiah = "tolong isi 1-5"
}
console.log(hadiah);
// muncul Tisu
```

## Operator Javascript
Operator merupakan karakter yang mereprentasikan sebuah operasi matematika, logika, maupun suatu proses aksi.
Ada 3 jenis operator dalam javascript yaitu:
 1. Operator Aritmatika(Arithmetic)
 2. Operator Perbandingan javascript
 3. Operator Logika Javascript
 4. Operator Penugasan(Assignment)
 5. Operator Bitwise Javascript
 6. Operator Lain(Miscellaneous Operators)

### 1. Operator Aritmetika
Operator Aritmatika digunakan untuk melakukan perhitungan Matematika seperti Operasi Penjumlahan, Perkalian, Modulus, dll.
Berikut penjelasannya:
| No | Operator       | Deskripsi                                                                        |
|----|----------------|----------------------------------------------------------------------------------|
| 1. | Penjumlahan(+) | menjumlahkan 2 operand                                                           |
| 2. | Pengurangan(-) | mengurangi suatu operand dengan operand lainnya                                  |
| 3. | Perkalian(*)   | mengalikan suatu operand dengan operand yang lainnya                             |
| 4. | Pembagian(/)   | operasi pembagian: suatu operand akan dibagi dengan operand lainnya              |
| 5. | Modulus(%)     | menghasilkan sisa bagi dari hasil pembagian suatu operand dengan operand lainnya |
| 6. | Increment(++)  | menambah 1 nilai keatas pada operand/variabel                                    |
| 7. | Decrement(--)  | mengurangi 1 nilai kebawah pada operand/variabel                                 |
### 2. Operator Perbandingan
Secara umum digunakan untuk melakukan operasi perbandingan yang akan menghasilkan nilai berupa Boolean(TRUE dan FALSE). Tipe Data Boolean yang dihasilkan diperoleh dari hasil perbandingan 2 nilai atau 2 variabel.
Berikut jenis-jenis operator perbandingan:
| No | Operator                    | Deskripsi                                                                      |
|----|-----------------------------|--------------------------------------------------------------------------------|
| 1. | Equal(==)                   | TRUE jika kedua operand nilainya sama                                          |
| 2. | Not Equal(!=)               | TRUE jika kedua operand nilainya tidak sama                                    |
| 3. | Identical(===)              | TRUE jika kedua operand nilainya sama dan dengan tipe data yang sama           |
| 4. | Not Identical(!==)          | TRUE jika ke-2 operand nilainya tidak sama serta bertipe data berbeda          |
| 5. | Lebih Besar(>)              | TRUE jika suatu operand nilainya lebih besar dari operand lainnya.             |
| 6. | Lebih Kecil(<)              | TRUE jika suatu operand nilainya lebih kecil dari operand lainnya              |
| 7. | Lebih Besar sama dengan(>=) | TRUE jika operand pertama nilainya lebih besar atau sama, dengan operand kedua |
| 8. | Lebih Kecil sama dengan(>=) | TRUE jika operand pertama nilainya lebih kecil atau sama, dengan operand kedua |
### 3. Operator Logika
Operator Logika digunakan untuk melakukan Operasi Logika, Operasi Logika juga merupakan salah satu dari beberapa operasi yang akan menghasilkan nilai dengan tipe data Boolean(TRUE dan FALSE). Sama dengan point no 2 operator ini untuk membandingkan 2 nilai.
Berikut jenis-jenis operator logika:
| No | Operator | Deskripsi                                                               |
|----|----------|-------------------------------------------------------------------------|
| 1. | AND(&&)  | TRUE jika kedua operand nilainya cocok, benar(true), misal true && true |
| 2. | OR(\|\|) | TRUE jika salah satu dari kedua operand bernilai Benar(true).           |
| 3. | NOT(!    | TRUE jika nilai dari kedua operand tidak cocok                          |
### 4. Operator Penugasan(Assignment)
Operator penugasan sebenarnya mirip dengan operator aritmetika secara fungsi, namun operator penugasan menggunakan operator = sebagai gabungan.
Berikut jenis-jenis operator penugasan:
| No | Operator | Deskripsi                |
|----|----------|--------------------------|
| 1. | =        | Assigment, memberi nilai |
| 2. | +=       | Penjumlahan              |
| 3. | -=       | Pengurangan              |
| 4. | *=       | Perkalian                |
| 5. | /=       | Pembagian                |
| 6. | %=       | Modulus                  |
### 5. Operator Bitwise
Operator Bitwise digunakan secara khusus untuk melakukan proses logika, dimana nilai atau operand yang diolah adalah bilangan biner. Bilangan Biner adalah bilangan yang hanya terdiri dari 2 angka yaitu angka 0 dan 1.
Berikut jenis-jenis operator Bitwise:
| No | Operator | Deskripsi   |
|----|----------|-------------|
| 1. | &        | AND         |
| 2. | \|       | OR          |
| 3. | ~        | NOT         |
| 4. | <<       | Shift Left  |
| 5. | >>       | Shift Right |
| 6. | ^        | XOR         |
### 6. Operator Lainnya(Miscellaneous Operators)
Operator yang termasuk dalam Misc Operators antara lain: Operator Ternary, Operator Typeof, dll. cukup berguna di lingkup javascript. Seperti:
- Ternary 
contoh:
```
function getNilai(isNilai) {
    return (isNilai ? 'A' : 'B' );
  }
  
  console.log(getNilai(1));
  //keluar A karena True

  console.log(getNilai());
  //keluar B karena False or Kosong
```

**?** sama dengan If dan **:** sama dengan else
- typeof

Merupakan Operator untuk mendefinisikan suatu tipe data
```
let a = 10
console.log(typeof(a))
//keluar number

let b = "ini String"
console.log(typeof(b))
//keluar string

let c = true
console.log(typeof(c))
//keluar boolean

```

## let, var dan const
var, let dan const merupakan sebuah keywoard untuk mendeklarasikan variabel di javascript. Berikut perbedaannya:
- var

var adalah variabel yang dapat berubah valuenya dan variabelnya dapat di dekrasikan ulang.

contoh:
```
var nama = "Rodhi"
var nama = "Andriansah"
console.log(nama);
// keluar Andriansah, value Rodhi tergantikan atau tertimpa

```
- let

Sifat let sama dengan var valuenya dapat dirubah tetapi tidak bisa di dekrasikan ulang.

contoh :
```
let nama = "Rodhi"
let nama = "Andriansah"
console.log(nama);
// error nama has been declared
```
- const

Sifanya tidak bisa dirubah valuenya dan tidak dapat juga variabelnya di deklarasikan ulang.

contoh :
```
const nama = "Rodhi"
const nama = "Andriansah"
console.log(nama)
// error variabel already declared

const nama = "Rodhi"
nama = "Andriansah"
console.log(nama)
// error variabel constant
```

## Unix Command Line

### CLI (Command Line Interface)
Command Line Interface merupakan sebuah interface yang digunakan oleh user untuk bisa mengetikkan perintah dalam bentuk teks dan memberikan instruksi pada komputer untuk mengerjakan tugas tertentu.
### Shell
Shell merupakan sebuah pondasi atau interface antara perintah yang diketikkan di CLI dengan Sistem operasi, shell lah yang nantinya akan memproses semua perintah yang diketikkan untuk diteruskan ke dalam sistem operasi.

Shell memiliki beberapa fungsi, di antaranya:
- Menangani file dan direktori
- Membuka dan menutup program
- Mengelola proses komputer
- Menjalankan task berulang

Tipe  Shell ada banyak namun yang paling terkenal adalah dari windows dan linux yaitu
- Windows Shell
Windows shell secara default biasanya menggunakan CMD(Command Prompt)
- Bash

Bash sebenarnya salah satu tipe shell dalam linux, ada banyak tipe lagi seperti zsh, ksh, tcsh.

Bash merupakan shell yang paling sering digunakan karena mudah dipahami dalam memgembangkan suatu program. Oleh karena itu untuk selanjutnya akan membahas lebih detail hanya pada Bash.

### Bash

Bash atau Bourne Again Shell adalah tipe shell yang digunakan di MacOS serta berbagai distribusi Linux, dan dikembangkan oleh Free Software Foundation. Tool ini juga bisa diinstall di Windows 10. Bash merupakan salah satu tipe shell yang bisa digunakan oleh user Linux, selain Tchs shell, Ksh shell, dan Zsh shell.

Di sebagian besar distribusi Linux, Bash ada dalam menu Utilities. Di desktop Gnome, namanya adalah Terminal, sedangkan untuk KDE, namanya adalah Konsole.
Sementara itu, di MacOS, program ini disebut Terminal.app. Untuk menjalankannya, buka Application -> Utilities -> Terminal. Atau, cukup ketikkan terminal di pencarian Spotlight.Setelah terminal terbuka, Anda bisa langsung mengetikkan perintah. Perintah biasanya terdiri dari perintah itu sendiri, argumen, dan opsi.

Perintah memuat instruksi yang akan dijalankan, argumen memberitahukan tempat perintah harus dijalankan, dan opsi meminta modifikasi hasil perintah.
Untuk menggunakan shell, kita harus tahu sintaksisnya lebih dulu. Cara ini juga dikenal sebagai shell scripting, yaitu penggunaan script di CLI untuk menjalankan task tertentu.

Meskipun ada banyak perintah yang bisa digunakan dengan CLI, semua perintah tersebut umumnya terbagi ke dalam dua kategori:

- Perintah untuk menangani atau mengelola proses
- Perintah untuk menangani atau mengelola file'

### Git dan Gitbash

Gitbash adalah shell yang diinstall dalam windows sehingga perintah-perintahnya akan sama. 
Berikut langkah awal untuk mencoba gitbash:
1. Pastikan windows anda sudah menginstallnya, petunjuk lengkap bisa cek laman [official git](https://git-scm.com/)
2. Buka gitbash atau bisa juga dengan mengklik kiri mouse dan pilih gitbash here.

![Klik gitbash here](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/420f492d593ed7baf7594b90b186e01ad24183f9/Week%201./git-1.png)

3. Berikut tampilan awal sebuah gitbash

![tampilan awal](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/420f492d593ed7baf7594b90b186e01ad24183f9/Week%201./git-2.png)

4. Ketikkan perintah, untuk mengetahui versi git kita
```
git -v
```

![cek versi](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/420f492d593ed7baf7594b90b186e01ad24183f9/Week%201./git-3.png)

5. git berhasil diinstall dan digunakan

### Perintah-perintah dalam bash

### Navigasi Directory

```bash
pwd                       # Mengetahui posisi direktori sekarang
ls                        # isi direktori
ls -a|--all               # isi direktori termasuk file yang di hidden
cd                        # pindah menuju direktori home
cd namadirektori          # pindah ke direktori yang ditulis
cd ../                    # keluar direktori satu folder
```

### Membuat folder

```bash
mkdir namadirektori                        # buat folder
mkdir nama1 nama2                          # buat folder ganda
```

### Memindahkan sebuah direktori

```bash
cp namadirektori                                             # Copy directori
mv namadirektori                                             # Memindahkan directori
```

### Deleting Directories

```bash
rmdir namadirektori                        # Hapus folder
```

### Membuat files

```bash
touch nama.txt             # buat file baru
touch nama1.txt nama2.txt  # buat file ganda 
touch {nama1,nama2}.txt        # buat file ganda
```

### Memindahkan Files

```bash
cp nama1.txt nama2.txt                                # Copy file
mv nama1.txt nama2.txt                                # Memindahkan file
```

### Menghapus sebuah file

```bash
rm nama.txt            # Hapus file
```

### membaca atau membuka file

```bash
cat foo.txt            # membuka file
less foo.txt           # membuka file satu page penuh dengan beberapa pengaturan
head foo.txt           # membuka 10 line dari atas sebuah file
tail foo.txt           # membuka 10 line dari bawah sebuah file
```

## Git Dasar

GIT adalah sebuah tools bagi para programmer dan developer yang berfungsi sebagai control system untuk menjalankan proyek pengembangan software. GIT adalah singkatan dari Group Inclusive Tour. Tujuan penggunaan GIT yakni untuk mengelola versi source code program dengan menentukan baris serta kode yang akan ditambahkan atau diganti.

### Implementasi Git
Langkah-langkah yang harus dilakukan yaitu:
1. Sudah menginstall git jika di windows namanya git bash
2. Buat sebuah folder
3. Masukkan beberapa file kodingan
4. buka gitbash here 
5. kemudian ketikkan perintah berikut
```
git init
```
![git-init](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/fc5b8f70e8d66ba2f106a37fe45118d724a36fb2/Week%201./gitbash-1.png)

6. file git berhasil dibuat di folder tersebut
7. setting username dan email dengan perintah 

```
git config --global user.name "Nama Anda"
git config --global user.email "emailAnda@email.com"
```
![git-init](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/5ca21b7e8f37a1ce40b5e6acaae915058178aa74/Week%201./gitbash-2.png)

8. jika sudah selesai dengan program yang dibuat dan ingin menyimpan prosesnya bisa menggunakan perintah

```
git add .
```
```
git commit -m "Pesan Yang ingin ditambahkan"
```
![git-init](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/fc5b8f70e8d66ba2f106a37fe45118d724a36fb2/Week%201./git-bash3.png)

9. Directory sudah terlacak dan tersimpan menggunakan git

11. jika ingin diupload ke github bisa menggunakan perintah
```
git remote add origin https://github.com/Chopin44/Contoh.git
git branch -M main
git push -u origin main
```
![git-remote](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/fc5b8f70e8d66ba2f106a37fe45118d724a36fb2/Week%201./git-bash4.png)

12. Jika berhasil akan muncul dalam github kita

![git](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/fc5b8f70e8d66ba2f106a37fe45118d724a36fb2/Week%201./git-bash5.png)

## Algoritma dan Data Struktur

Algoritma adalah suatu proses atau langkah-langkah yang terstruktur atau berurutan untuk memecahkan suatu masalah.
Seberapa penting algoritma dalam pemrogaman?

Programming itu justru identik dengan memecahkan suatu permasalahan, maka dari itu algoritma merupakan pemeran utamanya
bahasa pemrograman hanyalah pemeran pendamping
Belajar algoritma sama aja dengan mengingat kembali alur berfikir yg terstruktur

### Ciri-ciri Algoritma

| Ciri          | Deskripsi                                | Contoh         |
|---------------|------------------------------------------|----------------|
| Input         | Memiliki 0 atau lebih inputan            | Telur + Minyak |
| Output        | Memiliki min 1 buah output               | Telur          |
| Definiteness  | Instruksi jelas tidak ambigu             | Digoreng       |
| Finiteness    | Memiliki titik berhenti (stop)           | Telur Matang   |
| Effectiveness | Sebisa mungkin tepat sasaran dan efisien |                |

### Jenis Proses Algoritma

| Proses     | Deskripsi                                                           | Contoh                                              |
|------------|---------------------------------------------------------------------|-----------------------------------------------------|
| Sequence   | Instruksi yg dijalankan secara berurutan                            | Gelas diisi dengan air, lalu air siap utk diminum   |
| Selection  | Instruksi yg dijalankan jika memenuhi suatu kondisi                 | Jika lampu merah, saya akan berhenti                |
| Iteration  | Instruksi yg berulang kali dijalankan selama memenuhi suatu kondisi | Selama belum sampai rumah, saya akan terus menyetir |
| Concurrent | nstruksi yg dijalankan secara bersamaan                             | Ibu mencuci baju sambil membersihkan rumah          |

### Penyajian Algoritma
1. Deskriptif

    penyajian yang dilakukan dengan bahasa sehari-hari.
    contoh:
    saya lapar, apa yang harus saya lakukan?
    
    sudah pasti yang dilakukan adalah makan, terus bagaimana prosesnya?
    
    saya ke dapur-ambil piring di rak-ambil nasi dan lauk pauk-kemudian makan
    
2. Flowchart

    Flow chart atau diagram alir, penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual. Flow chart menggunakan simbol bangun datar sebagai representasi dari proses yg dilakukan.
    
    ![git-init](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/1ccaa02a8eb3cceb7168d6714c523d970fc21e0c/Week%201./flowchart.png)

3. Pseudo Code
    Penulisan algoritma yg hampir menyerupai penulisan pada kode pemrograman disebut dengan pseudo code.
    
    ![git-init](https://github.com/Chopin44/Writing-and-Presentation-Test/blob/1ccaa02a8eb3cceb7168d6714c523d970fc21e0c/Week%201./psuedocode.png)
    
### Data Struktur

Struktur Data adalah sebuah cara untuk mengatur data (organize data) dengan cara yang memungkinkannya diproses dalam waktu yang efektif.

Ada beberapa perintah struktur data yang dapat digunakan untuk mengatur data yaitu:

- Array
- Linked List
- Stack
- Queue
- Tree
- Hashing
- Graph, dan lain-lain.

Lalu apa bedanya Struktur Data dan Algoritma?
Algoritma adalah seperangkat aturan yang harus diikuti menyelesaikan suatu masalah. Sedangkan Struktur data adalah cara untuk menyusun data.

    









