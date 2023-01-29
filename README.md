# Tutorial

**Table of contents**
- [Dasar](#Dasar)
  - [JavaScript membuat variable](#JavaScript-membuat-variable)
  - [JavaScript output](#JavaScript-output)
  - [JavaScript function](#JavaScript-function)
  - [JavaScript type](#JavaScript-type)
- [Membuat sebuah command](#Membuat-sebuah-command)
  - [Parameter](#Parameter)

## Pendahuluan
Tutorial ini akan membantumu dalam membuat sebuah command, meskipun anda tidak pernah belajar pemograman.
Jika kamu sudah mengetahui beberapa hal tentang JavaScript, anda dapat membuka bagian [Membuat sebuah command](#Membuat-sebuah-command).

## Dasar
Berikut dasar dasar sebelum anda membuat sebuah command.

### JavaScript Basic
#### JavaScript membuat variable

Mulailah dengan mengetik berikut ini:

``` js
const age = 17
```

Ini akan membuat variabel baru bernama `age` dan memberinya nilai `17`  
Variabel digunakan untuk menyimpan data dan menggunakannya nanti dalam kode.

Sekarang simpan file tersebut agar kita dapat menjalankan kodenya. Buka terminal lagi (atau terminal baru di VSCode) dan navigasikan ke folder yang sama tempat file disimpan. Ini dapat dilakukan dengan menggunakan perintah `cd`, misalnya: `cd home/axuint/project`  
Setelah terminal Anda berada di folder yang sama dengan file Javascript Anda, Anda dapat menjalankan `node filename.js`  
Jika Anda telah melakukan semuanya dengan benar, Anda seharusnya tidak melihat apa pun.  
Pada bab selanjutnya kami akan menunjukkan kepada Anda bagaimana Anda dapat membuat sebuah 'output' ke terminal.

Secara umum, sebaiknya gunakan kata kunci `const` daripada kata kunci `let` saat mendefinisikan variabel. Variabel yang didefinisikan dengan `const` tidak dapat dimodifikasi nanti dan karenanya merupakan konstanta.  
Javascript kemudian dapat membuat kode Anda berjalan lebih efisien karena ia tahu bahwa ia tidak harus memperhitungkan perubahan nilai untuk variabel tersebut.  
Jika Anda menginginkan variabel yang dapat dimodifikasi, Anda tetap harus menggunakan `let` tentunya.

``` js
const age = 17
age = 17 // Baris ini tidak valid.
```

Baris kedua tidak valid karena Anda tidak dapat menugaskan ulang variabel `age`.

Jika Anda ingin membantu diri sendiri dan orang lain memahami kode Anda dengan lebih baik, Anda dapat menggunakan komentar.  
Komentar dapat dibuat menggunakan `//` dan semuanya setelah itu diabaikan sepenuhnya oleh Javascript.

#### JavaScript output

Sering kali Anda ingin melihat nilai variabel saat ini, untuk memastikan program Anda berjalan dengan benar.  
Anda melakukan ini dengan mencetak variabel ke terminal.  
Dalam Javascript, kita dapat melakukannya menggunakan fungsi `console.log()`.  

``` js
const age = 17

console.log(age)
```

Sekarang ketika Anda menyimpan dan menjalankan kode ini, Buka terminal dan jalankan:

``` console
axuint@localhost:~/project$ node filename.js
17
```

maka anda akan melihat output seperti diatas

#### JavaScript function

Selanjutnya anda akan belajar tentang `Function`, `Function` atau fungsi adalah bagian dari kode yang dapat digunakan berkali-kali di seluruh kode anda.
Ini sangat berguna karena anda hanya menulis kode sekali dan anda hanya memanggilnya saja untuk menggunakanya.
Contoh: 

``` js
const user = (name, age) => {
  return `Nama: ${name}, Umur: ${age}`;
}
const data = user("Axuint", 17)
console.log(data)
```

`=>` digunakan untuk mendefinisikan sebuah fungsi, yang disebut operator panah.
segala sesuatu di antara tanda kurung bulat `()` adalah parameter, dipisahkan dengan koma.
Parameter adalah sebuah variable yang dapat digunakan dalam sebuah `Function`. Kemudian ada sebuah kurawal `{}` disinilah kode kamu diletakan.
setelah `Function` selesai disini saya namai `user`

atau anda dapat melakukan:
``` js
function user(name, age){
  return `Nama: ${name}, Age: ${age}`
}
const data = user(name, age)
console.log(data)
```
Fungsinya masih sama tetapi disini tidak membutuhkan sebuah operator panah `=>`.
Lanjut, seperti yang anda lihat, kode ini mengambil parameter `name` dan `age` dan mengaplikasikannya kedalam sebuah string.
Untuk memanggilnya disini saya membuat sebuah variabe konstanta bernama `data` yang didalamnya `user("Axuint", 17)`. Anda dapat memanggil sebuah `Function` dengan menulis nama function diikuti tanda kurung bulat `()`. Untuk melihat hasilnya disini anda dapat menggunakan `console.log(nama_variable)` atau langsung memanggil sebuah function `console.log(nama_function())`.

#### JavaScript type
Sejauh ini disini hanya menggunakan sebuah `Number` dan `String`, Tetapi didalam JavaScript memiliki banyak type yang dapat digunakan.
- String adalah sebuah bagian dari teks yang dapat berisi beberapa karakter. String di definisikan dengan tanda kutip `""` atau `''` atau ``. Contoh:
``` js
const string = "Ini adalah sebuah string" // Type string
```
- Array adalah type yang dapat menampung banyak variable di didalamnya. Array didefinisikan dengan tanda kurung siku `[]`. Contoh:
``` js
const array = [1, 2, 3, 4, 5] // Type Array
```
- Object pada dasarnya adalah array tingkat lanjut. Object didefinisikan dengan tanda kurawal `{}`. Contoh:
``` js
const object = {"name": "Axuint", "age": 17} // Type Object
```
- Function
``` js
const user = (name, age) => { return `Name: ${name}, Age: ${age}` }

// Atau

function user(name, age){
  return `Name: ${name}, Age: ${age}`
}
```
- Boolean hanya memiliki nilai `true` atau `false`
``` js
const isMarry = false
const isStudent = true
```
- Jika sesuatu belum didefinisikan maka type nya adalah `undefined`
## Membuat sebuah command
#### Membuat command menyapa
Dibagian ini kita akan membuat sebuah command menyapa user, Untuk membuat command anda harus pergi ke dalam folder command dan buat sebuah file bernama `menyapa.js` extensi `.js` adalah extensi JavaScript. Untuk membuat command menyapa kita memasukan sebuah kode seperti:
``` js
export default async function({message, sender}){
  ... do something
}
```
Jika anda sudah tau fungsi sebuah `Function` maka anda dapat melihat parameter `message` dan `sender`. Parameter `message` berfungsi untuk mengirimkan pesan reply, pesan react. parameter `message` berisi biasanya object seperti:
``` konsole
{
  id: '53DCD5B314458B890297F677B7F2F6EB',
  type: 'conversation',
  fromMe: false,
  text: 'hai',
  room: '123456789@s.whatsapp.net',
  quoted: undefined,
  reacted: null,
  media: null,
  list: null,
  mentions: [],
  isViewOnce: false,
  getMessageInfo: [Function: getMessageInfo],
  reply: [Function: reply],
  react: [AsyncFunction: react],
  forward: [AsyncFunction: forward],
  delete: [Function: delete],
  waitForReply: [Function: waitForReply],
  isOffline: false
}
```
Anda dapat menggunakanya untuk mengambil object dalam sebuah pesan seperti `media`, `text`, `room`. dan parameter selanjutnya adalah `sender`, Parameter sender digunakan untuk mengambil data user seperti: nama, id. Dan biasanya `sender` memiliki object:
``` konsole
{
  id: '123456789@s.whatsapp.net',
  name: 'Axuint',
  isOwner: true,
  isAdmin: true,
  isBot: false,
  getPP: [Function: getPP]
}
```
Untuk membuat command menyapa maka kita membutuhkan parameter `message` untuk mengirimkan pesan reply dan `sender` untuk mendapatkan username user. Lanjut jika sudah masukan sebuah kode kedalam `menyapa.js`:
``` js
export default async function({message, sender}){
  const username = sender.name // Variable untuk mendapatkan username user
  return message.reply(`Hallo, ${username}!`) // Mengirimkan pesan reply menyapa
}
```