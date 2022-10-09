# Writing Week 3

## In deep with Javascript Array

Array adalah sebuah tipe data yang dapat menyimpan berbagai tipe data yang berbeda.
Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.

Contoh array :

```
let arr = ["satu", 2, True]
console.log(arr)

```

Di atas variabel arr menampung 3 tipe data yang berbeda yaitu ada satu sebagai String, 2 sebagai Number, dan True sebagai boolean.

### Terus fungsi array untuk apa?

Dalam sebuah programming, mengorganisasi data dan menyimpan data adalah konsep penting dari programming. Dengan adanya array kita dapat mengelola data lebih baik, mengingat sifatnya yang dapat menyimpan banyak tipe data yang berbeda.

### Konsep Array

Dalam array kita dapat banyak menyimpan tipe data yang berbeda. Disitu sebenarnya ada sebuah aturan, bahwa index array atau nilai array itu dimulai dari angka 0.

![array-1](https://github.com/Chopin44/Writing_and_Presentation_Test/blob/1de4c49ea951e7019868ca8ff5f1909dd6ca849b/week-3/images/array-1.png)

### Cara Memanggil Data dalam Array

Seperti yang dijelaskan dalam konsep di atas, array memiliki index yang dimulai dari nol, sehingga jika ingin memanggil sebuah nilai yang pertama kita harus memulainya dari nol(0), dan berlaku untuk seterusnya.

```
let arr = ["Jeruk","Mangga","Semangka", "Melon"]

//Tampil data array
console.log(arr)

//Tampil Jeruk
console.log(arr[0])

//Tampil Melon
console.log(arr[3])
```

### Update Array

Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array.
Contoh:

```
let arr = [1,2,3,4,5]
arr[0] = 0
console.log(arr)
//tampil [0,2,3,4,5]

```

### const pada array

- Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
- Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
- Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const

##### Const tidak dapat diubah ke array baru

```
const arr = [1,2,3,4,5]
arr = [0]
console.log(arr)
// Output error Assignment to constant variable
```

##### Let dapat diubah ke array baru

```
let arr = [1,2,3,4,5]
arr = [0]
console.log(arr)
//tampil [0]

```

##### const tetap bisa mengubah isi array

```
const arr = [1,2,3,4,5]
arr[0] = 0
console.log(arr)
//tampil [0,2,3,4,5]

```

### Properties dalam Array

Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.

Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.
Kita hanya membahas length. Untuk yang lainnya bisa cek di link
[ini](https://www.w3schools.com/jsref/jsref_obj_array.asp).

1. .length
   length akan mengembalikan nilai dari jumlah panjang data suatu array.

```
let arr = [1,2,3,4,5,6]
console.log(arr.length)
//tampil 6
```

### Method Array

Array memiliki method atau biasa disebut built-in methods.

Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.

Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.

Sama halnya dengan Array properti. Kita bisa cek dokumentasi untuk melihat method yang sudah tersedia pada link [ini](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

1. push()
   Digunakan untuk memasukkan data urutan terakhir dalam array

```
let arr = ["kerbau", "babi", "anjing"]
arr.push("monyet")
console.log(arr)
//tampil ["kerbau", "babi", "anjing", "monyet"]
```

2. pop()
   Adalah method yang menghapus item array index terakhir.

```
let arr = ["kerbau","babi", "anjing"]
arr.pop()
console.log(arr)
//tampil ["kerbau","babi"]
```

3. shift()
   Method yang menghapus item array index pertama.

```
let arr = ["kerbau","babi", "anjing"]
arr.shift()
console.log(arr)
//tampil ["babi", "anjing"]
```

4. unshift()
   Method yang menambahkan item arrya index pertama.

```
let arr = ["kerbau","babi", "anjing"]
arr.unshift("monyet")
//tampil ["monyet","kerbau","babi", "anjing"]
```

5. sort()
   Method yang digunakan untuk mengurutkan secara Ascending atau Descending Alphanumeric

```
const num = [1,4,6,7,3,2]
num.sort()
console.log(num)
// tampil [1, 2, 3, 4, 6, 7]
```

### Looping pada Array

Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()

1. forEach()
   forEach() adalah method untuk melakukan looping pada setiap elemen array

```
const merkMinuman = ["Starbuck","Milo", "Dancow", "Janji Jiwa"]
merkMinuman.forEach(e => {
    console.log(e)
})
//tampil Starbuck, Milo, Dancow, Janji Jiwa
```

2. Map()
   melakukan perulangan/looping dengan membuat array baru

```
const arr = [1,2,3,4,5]

let angka = arr.map(num => {
    return num*2
})

console.log(angka)
//tampil [2,4,6,8,10]
```

### MultiDimensional Array

Multidimensional Array bisa dianalogikan dengan array of array.

Ada array didalam array
Contoh:

```
let inventory = [
    ['Kaos', 10],
    ['Jaket', 1],
    ['Celana' 2]
]
console.log(inventory)
// tampil [Array(2), Array(2), Array(2)]
```

#### Memanggil array multidimensi

```
let inventory = [
    ['Kaos', 10],
    ['Jaket', 1],
    ['Celana' 2]
]
console.log(inventory[0],[0])
// tampil Kaos
console.log(inventory[2],[1])
// tampil 2
```

## In Deep with Javascript Object

Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)

Properti adalah data lengkap dari sebuah object.

Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.

### Membuat Object

Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel.

```
let object = {}

//kita isikan properti
let object = {
    property1: 1,
    property2: 2
}
console.log(object)
```

Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

### Mengakses Object dan Property Object

```
let game = {
    title: "Death Stranding",
    genre: "Action-Adventure",
    rating: "Mature",
    physical: true,
}
console.log(game)
// Mengakses seluruh objek
console.log(game.title)
// tampil Death Stranding
```

#### Bracket Notation

```
let game = {
    title: "Death Stranding",
    genre: "Action-Adventure",
    rating: "Mature",
    physical: true,
}
console.log(game['genre'])
//tampil Action-Adventure
console.log(game['physical'])
//tampil true
```

### Update Object

Kita dapat melakukan update pada variabel dengan tipe data Object.

- Object dapat mengupdate value dari key yang sudah tersedia
- Object dapat menambahkan key dan value baru

```
const game = {
    title: "Death Stranding",
    genre: "Action-Adventure",
    rating: "Mature",
    physical: true,
}
// mengubah value title
game.title = "Resident Evil 4 Remake"
// menambahkan property baru
game.console = "PS4, PS5, Steam"

console.log(game)
```

### Delete Object

Kita dapat menghapus properti dari object menggunakan delete operator.

```
const game = {
    title: "Death Stranding",
    genre: "Action-Adventure",
    rating: "Mature",
    physical: true,
}
delete game.rating
console.log(game)
// Output
// title: "Death Stranding",
// genre: "Action-Adventure",
// physical: true,
```

#### Penting

Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru.

```
const game = {
    title: "Death Stranding",
    genre: "Action-Adventure",
    rating: "Mature",
    physical: true,
}
game = {
    sub-title = "Death Stranding"
}
console.log(game)
// error Assigment to constamt variable.
```

Jadi jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.

```
let game = {
    title: "Death Stranding",
    genre: "Action-Adventure",
    rating: "Mature",
    physical: true,
}
game = {
    subtitle : "Death Stranding"
}
console.log(game)
// {title: "Death-Stranding"}
```

### Method dalam Object

Jika value yang kita masukkan pada property berupa function.

Maka itu disebut method.

Contoh:

```
const kenalan = {
    baru: function() {
        return "Hai Nama saya Rodhi"
    },
    sudahKenal: function() {
        return "Hai senang berkenalan denganmu"
    }
}
console.log(kenalan.baru())
//tampil Hai Nama saya Rodhi
```

### Nested Object

Pada kasus Aplikasi-aplikasi yang kompleks aakan ada data yang kompleks juga seperti object yang bersarang, ini asalnya dari turuna object lainnya.

Contoh:

```
const movie = {
    page: 1,
    result: {
        title: "Marvel Avengers",
        genre: "Superheroes",
        rating: "Teen",
    }
}
console.log("Halaman ke-", movie.page)
console.log(movie.result.title)
// tampil
//Halaman ke- 1
//Marvel Avengers
```

### Pass by Reference

Kita bisa mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.

Ini biasa disebut passed by reference.

```
let num = {
    angka1: 1,
    angka2: 2
}

function ubah(obj) {
    obj.angka1= 5,
    obj.angka2= 8
};

ubah(num)
console.log(num.angka1)
console.log(num.angka2)
// angka dalam object num berubah
// 1 jadi 5 dan 2 jadi 8
```

### Looping Object

Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.

Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.

```
const movie = {
    page: 1,
    result: {
        title: "Marvel Avengers",
        genre: "Superheroes",
        rating: "Teen",
    }
}
for (let data in movie) {
    console.log(data)
}
// tampil page dan result

for (let data in movie.result) {
    console.log(data)
}
// tampil title,genre,rating

```

### Array of Object

Apakah object hanya menyimpan 1 data?
Tidak.
Object sama seperti Array yang bisa menyimpan banyak data.
Kita dapat menggunakan array of object untuk data yang lebih dari satu.

```
const movies = [
    {
        title: "Marvel Avengers",
        genre: "Superheroes",
        rating: "Teen",
    },
    {
        title: "Spiderman III",
        genre: "Superheroes",
        rating: "Teen",
    },
    {
        title: "Sherlock Holmes",
        genre: "Crime, Mystery",
        rating: "Teen",
    }
]

movies.forEach((e) => {
    console.log(e)
})
//output
//{title: 'Marvel Avengers', genre: 'Superheroes', rating: 'Teen'}
//{title: 'Spiderman III', genre: 'Superheroes', rating: 'Teen'}
//{title: 'Sherlock Holmes', genre: 'Crime, Mystery', rating: 'Teen'}
```

## Javascript Recursive

Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.

### Konsep Penulisan

```
function recursive() {
    //..
    recursive()
    //..
}
```

```
function recursive() {

    if(kondisi) {
        // Stop panggil recursive
    } else {
        recursive()
    }

}
```

### Ciri-ciri Recursive

- Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
- Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

contoh kasus recursive:

1. Menghitung Mundur Angka

```
function hitungMundur(angkaDepan) {
    console.log(angkaDepan)

    let nextAngka = angkaDepan - 1;

    //jika kondisi ini bernilai flase maka recursive berhenti
    if(nextAngka > 0) {
        hitungMundur(nextAngka);
    }
}
hitungMundur(10)
```

2. Mencari x pangkat n

```
function pow (x, n) {
if (n = 1) {
return x
} else {
return x \*pow(x, n -1)
}
}

console.log(pow(2,4))

```

## Asynchronous JavaScript

Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous.
Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous.

Kita bisa membuat asynchronous secara simulasi artinya tidak murni asynchronous dengan beberapa cara:

1. Callback
2. Promises
3. Async/Await

### 1. Callback function

Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.

Contoh:

```
const undangan = (nama1, nama2, undang) => {
    console.log(`Ini Nama saya ${nama1} dan ini nama teman saya ${nama2}`)
    undang()
}

const undang = () => {
 console.log("Iya diundang")
}

undangan("Rodhi", "Yukino", undang)
// Ini Nama saya Rodhi dan ini nama
// teman saya Yukino
// Iya diundang
```

2. Promise

Promise adalah Sebuah mekanisme baru pada fitur javascript / ES6 yang merepresentasikan sebuah object request pengolahan data yang dilakukan secara asynchronous seperti ajax, dan promise ini mewakili sebuah operasi yang belum selesai, tetapi diharapkan di masa mendatang.

Dalam pengambilan data, promise memiliki 3 kemungkinan state.

1. Pending(sedang dalam proses)
2. Fulfilled (berhasil)
3. Rejected (gagal)

```
let promise = true;

const Promises = new Promise((resolve, reject) => {
	if(promise){
		resolve('janji ditepati')
	}else{
		reject('janji tidak ditepati')
	}
})

Promises
.then(res => console.log(`Ok ${res} !`))
.catch(res => console.log(`Its Ok ! ${res}`))

// Ok janji ditepati

```
