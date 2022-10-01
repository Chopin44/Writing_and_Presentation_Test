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

1.  Operator Aritmatika(Arithmetic)
2.  Operator Perbandingan javascript
3.  Operator Logika Javascript
4.  Operator Penugasan(Assignment)
5.  Operator Bitwise Javascript
6.  Operator Lain(Miscellaneous Operators)

### 1. Operator Aritmetika

Operator Aritmatika digunakan untuk melakukan perhitungan Matematika seperti Operasi Penjumlahan, Perkalian, Modulus, dll.
Berikut penjelasannya:
| No | Operator | Deskripsi |
|----|----------------|----------------------------------------------------------------------------------|
| 1. | Penjumlahan(+) | menjumlahkan 2 operand |
| 2. | Pengurangan(-) | mengurangi suatu operand dengan operand lainnya |
| 3. | Perkalian(\*) | mengalikan suatu operand dengan operand yang lainnya |
| 4. | Pembagian(/) | operasi pembagian: suatu operand akan dibagi dengan operand lainnya |
| 5. | Modulus(%) | menghasilkan sisa bagi dari hasil pembagian suatu operand dengan operand lainnya |
| 6. | Increment(++) | menambah 1 nilai keatas pada operand/variabel |
| 7. | Decrement(--) | mengurangi 1 nilai kebawah pada operand/variabel |

### 2. Operator Perbandingan

Secara umum digunakan untuk melakukan operasi perbandingan yang akan menghasilkan nilai berupa Boolean(TRUE dan FALSE). Tipe Data Boolean yang dihasilkan diperoleh dari hasil perbandingan 2 nilai atau 2 variabel.
Berikut jenis-jenis operator perbandingan:
| No | Operator | Deskripsi |
|----|-----------------------------|--------------------------------------------------------------------------------|
| 1. | Equal(==) | TRUE jika kedua operand nilainya sama |
| 2. | Not Equal(!=) | TRUE jika kedua operand nilainya tidak sama |
| 3. | Identical(===) | TRUE jika kedua operand nilainya sama dan dengan tipe data yang sama |
| 4. | Not Identical(!==) | TRUE jika ke-2 operand nilainya tidak sama serta bertipe data berbeda |
| 5. | Lebih Besar(>) | TRUE jika suatu operand nilainya lebih besar dari operand lainnya. |
| 6. | Lebih Kecil(<) | TRUE jika suatu operand nilainya lebih kecil dari operand lainnya |
| 7. | Lebih Besar sama dengan(>=) | TRUE jika operand pertama nilainya lebih besar atau sama, dengan operand kedua |
| 8. | Lebih Kecil sama dengan(>=) | TRUE jika operand pertama nilainya lebih kecil atau sama, dengan operand kedua |

### 3. Operator Logika

Operator Logika digunakan untuk melakukan Operasi Logika, Operasi Logika juga merupakan salah satu dari beberapa operasi yang akan menghasilkan nilai dengan tipe data Boolean(TRUE dan FALSE). Sama dengan point no 2 operator ini untuk membandingkan 2 nilai.
Berikut jenis-jenis operator logika:
| No | Operator | Deskripsi |
|----|----------|-------------------------------------------------------------------------|
| 1. | AND(&&) | TRUE jika kedua operand nilainya cocok, benar(true), misal true && true |
| 2. | OR(\|\|) | TRUE jika salah satu dari kedua operand bernilai Benar(true). |
| 3. | NOT(! | TRUE jika nilai dari kedua operand tidak cocok |

### 4. Operator Penugasan(Assignment)

Operator penugasan sebenarnya mirip dengan operator aritmetika secara fungsi, namun operator penugasan menggunakan operator = sebagai gabungan.
Berikut jenis-jenis operator penugasan:
| No | Operator | Deskripsi |
|----|----------|--------------------------|
| 1. | = | Assigment, memberi nilai |
| 2. | += | Penjumlahan |
| 3. | -= | Pengurangan |
| 4. | \*= | Perkalian |
| 5. | /= | Pembagian |
| 6. | %= | Modulus |

### 5. Operator Bitwise

Operator Bitwise digunakan secara khusus untuk melakukan proses logika, dimana nilai atau operand yang diolah adalah bilangan biner. Bilangan Biner adalah bilangan yang hanya terdiri dari 2 angka yaitu angka 0 dan 1.
Berikut jenis-jenis operator Bitwise:
| No | Operator | Deskripsi |
|----|----------|-------------|
| 1. | & | AND |
| 2. | \| | OR |
| 3. | ~ | NOT |
| 4. | << | Shift Left |
| 5. | >> | Shift Right |
| 6. | ^ | XOR |

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

let, var, dan const merupakan sebuah keyword untuk mendeklarasikan variabel di javascript. Berikut perbedaannya:

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

## Scope dan Function

Scope adalah sebuah batasan dimana sebuah variabel dapat dipanggil atau dideklarasikan. Dan ini biasanya bergantung pada block suatu fungsi.

Sedangkan fungsi atau function sendiri merupakan sebuah kumpulan kode yang dimana digunakan untuk mengatur agar kode tersebut melakukan tugas-tugas tertentu.

contoh:

```
// a dan b disini sebagai parameter
function tambah(a, b) {
    return a+b
}

// 1 dan 2 sebagai argument
console.log(tambah(1, 2))
```

Disitu dibuat sebuah fungsi bernama tambah yang menerima parameter a dan b. Kemudian mengembalikan nilainya dengan menambahkan keduanya a+b.

Lanjut kebawah, ada perintah console.log untuk menampilkannya ke dalam console dengan mengirim sebuah argument 1 dan 2 untuk diterima parameter a dan b.

Alhasil kita dapat memanggil functionnya berulang kali kemudian mengirim sebuah argument untuk menggunakan fungsi tersebut, ini mempersingkat suatu kode kita hanya perlu sebuah argumen untuk menggunakan fungsi tersebut.

Nah, disini sudah memahami tentang function kita kembali ke dalam scope, sudah dijelaskan sebelumnya bahwa scope bergantung pada block function.
Maksutnya adalah, contoh:

```
let c = 12
let d = 12

function tambah() {
    let a = 10
    let b = 12

    //ambil c dan d diluar function
    console.log(c+d)
}

// Panggil function
tambah()

// ambil a dan b di dalam function
console.log(a+b)

```

variable a dan b akan menghasilkan error not defined karena mengambil ke dalam function, function memiliki block yang menjadikan variabel di dalamnya hanya bisa diambil oleh function itu sendiri, dinamakan sebagai **local variabel**

Sedangkan c dan d merupakan variabel yang dideklarasikan diluar function dan tidak ada block yang menghalangi sehingga dapat dipanggi dimana pun, dinamakan sebagai **global variabel**

## Math dalam javascript

Math adalah sebuah built-in object dalam javascript yang memiliki properties dan method untuk keperluan perhitungan matematika. Ada banyak macam properties dan method dalam math, berikut contohnya:

### Properties Math

- Math.LN2

  Nilai desimal dari logaritma natural dari 2 dengan kira-kira nilai 0.693.

- Math.PI

  nilai pi dalam lingkaran dengan kira-kira nilai 3.14159.

- Math.SQRT1_2

  akar dari setengah dengan kira-kira nilai 0.707.

- Math.SQRT2

  akar dari 2 dengan kira-kira nilai 1.414.

  dan masih banyak lagi bisa cek ke dalam dokumen javascript di [sini](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

### Method Math

- Math.abs()

  mengembalikan nilai absolut dari nilai x.

- Math.max()

  mengambalikan nilai dari yang terbesar.

- Math.min()

  mengembalikan nilai dari yang terkecil.

- Math.sqrt()

  mengembalikan nilai akar kuadrat dari nilai x

  dan masih banyak lagi bisa cek ke dalam dokumen javascript di [sini](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

## DOM dalam javascript

### Apa itu DOM?

Document Object Model (DOM) adalah antaramuka pemrogaman untuk dokumen sebuah web. DOM merepresantasikan halaman sehingga halaman tersebut dapat diubah baik strukturnya, style, maupun kontennya. DOM mewakili document sebagai nodes maupun objek oleh karena itu bahasa pemrograman dapat berkomunikasi dengannya.

### Cara menjalankan DOM

Karena sudah berkenalan dan mengetahui fungsi dari sebuah DOM maka disini kita akan mencoba bagaimana cara menjalankan sebuah DOM menggunakan bahasa pemrogaman Javascript.

1. Ingat kita harus memiliki file HTML karena javascript dapat berjalan hanya jika menempel di dalam file HTML karena sifatnya intrepreter.
2. Buat file HTML kemudian bisa langsung dibuka melalui browser.
   ![DOM-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/734ac0ecf06369b3d4f8aeb266b433351f858e94/week-1/images/DOM-1.png)
3. Disini kita menggunakan langsung console sebagai penulisan kode-kode javascript.
   ![DOM-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/734ac0ecf06369b3d4f8aeb266b433351f858e94/week-1/images/DOM-2.png)
4. Ketikkan perintah berikut:
   ![DOM-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/734ac0ecf06369b3d4f8aeb266b433351f858e94/week-1/images/DOM-3.png)

```
//Method Write() menghapus semua element yg ada di HTML
document.write("Hello World")
```

5. DOM berhasil dimanipulasi dengan menambahkan sebuah kata Hello World.

### Manipulasi Element

Dengan adanya DOM kita dapat memanipulasi sebuah element, seperti contoh berikut:

1. Melanjutkan dari yang di [atas](https://github.com/Chopin44/Writing_and_Presentation_Test/tree/main/week-2#cara-menjalankan-dom), kita sudah mempunyai file HTML dan sebuah file JS.
2. Untuk file HTML kita buat tag div dengan Id coba

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script src="script.js" defer></script>

</head>

<body>
  // tag dan id ini yang akan dimanipulasi
  <div id="coba"></div>
</body>



</html>
```

laman sebelum dimanipulasi

![dom-element-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-element-1.png)

3. Ketikkan perintah berikut ke dalam file js

```
// variabel a sebagai penampung yang didapat dari getElement berdasar Id
let a = document.getElementById("coba")

// bagian ini mengubah isian text yang tadinya kosong
a.innerText = ("Hello World")

```

laman sesusdah dimanipulasi

![dom-element-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-element-2.png)

### Manipulasi Style

Selain element, style dari sebuah element juga dapat kita ubah, seperti contoh berikut:

1. Meneruskan contoh di [atas](https://github.com/Chopin44/Writing_and_Presentation_Test/tree/main/week-2#manipulasi-element)
2. Kita tambahkan kode berikut di file js

```
a.style.color = "blue";

```

3. Kata hello World akan berubah warna menjadi biru

![dom-element-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-element-3.png)

### Event dan Event Listener

Event adalah sesuatu kondisi untuk memberikan perintah terhadap element tertentu agar membuat web tersebut lebih interaktif. Sedangkan Event Listener adalah suatu Event yang ditembakan langsung ke dalam sebuah element tertentu lebih spesifik.

Contoh dari event sebagai berikut:

1. Kita ingin menampilkan alert ketika teks hello world diklik
2. Dengan meneruskan kode latihan di [awal](https://github.com/Chopin44/Writing_and_Presentation_Test/tree/main/week-2#manipulasi-style), tambahkan beberapa kode berikut di file js:

```
let a = document.getElementById("coba")
a.innerText = ("Hello World")

a.style.color = "blue";

// fungsi untuk menampilkan alert
function iniAlert() {
 alert("Hello World!")
}

```

3. Dengan meneruskan kode latihan di awal, tambahkan beberapa kode berikut di file HTML:

```
<body>
    // event onclick yang artinya jika diklik akan memanggil fungsi iniAlert()
    <div id="coba" onclik="iniAlert()"></div>
</body>

```

4. Jika berhasil akan tampil seperti berikut:

![dom-event-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-event-1.png)

Nah sekarang lanjut cara menggunakan event listener, sebagai berikut contohnya:

1. Seperti biasa kita akan melanjutkan latihan sebelumnya
2. hapus event onclick, berikut:

```
<body>
    <div id="coba"></div>
</body>

```

3. Tambahkan langsung ke dalam elementnya, seperti berikut:

```
let a = document.getElementById("coba")
a.innerText = ("Hello World")

a.style.color = "blue";

a.addEventListener("click", function iniAlert() {
    alert("Hello World!")
   })

```

4. Laman akan tampil sama seperti sebelumnya yaitu alert hello world jika berhasil

### Form DOM

Kita akan mencoba membuat sebuah form login menggunakan DOM sehingga nanti akan ada sebuah validasi di dalamnya.

1. Seperti biasa siapkan file HTML isikan kode berikut:

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="script.js" defer></script>

</head>

<body>
    <form id="login">
        <div>Username: </div>
        <input id="username" type="text">
        <div>Password: </div>
        <input id="password" type="password">
        <input type="submit">
    </form>
</body>
</html>
```

2. Dan file js isikan file berikut:

```
// tangkap semua element
let formSubmit = document.getElementById("login")
let inputUsername = document.getElementById("username")
let inputPassword = document.getElementById("password")

// variabel untuk validasi username dan password
let validasi = {
    username: "rodhi",
    password: "123"
}

//mengisikan formSubmit dengan sebuah event
formSubmit.addEventListener("submit", (event) => {
    event.preventDefault()

    // variabel untuk menampung username dan password ketika diinput
    let userLogin = {
        username: inputUsername.value,
        password: inputPassword.value
    }

    // cek variabel validasi dengan yang diinputkan
    login = userLogin.username == validasi.username
    && userLogin.password == validasi.password

    // memunculkan alert ketika berhasil login atau gagal
    if (login) {
        alert("Login Berhasil")
    } else {
        alert("login gagal")
    }

    // mengosongkan form ketika selesai disubmit
    loginForm.reset()

})

```

3. Buka html lewat browser, hasilnya akan seperti ini:

![dom-form-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-form-1.png)

4. Kemudian jika diisikan username dan password terserah akan muncul login gagal

![dom-form-2](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-form-2.png)

5. Sedangkan jika diisikan username rodhi dan password 123 akan muncul alert login berhasil

![dom-form-3](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/4e5e7d7ef00132c19a05c00cdfa8f52cb010a122/week-2/images/dom-form-3.png)
