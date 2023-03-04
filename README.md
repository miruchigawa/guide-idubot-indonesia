# Tutorial

**Table of contents**
- [Dasar](#Dasar)
  - [JavaScript variable](#JavaScript-variable)
  - [JavaScript output](#JavaScript-output)
  - [JavaScript function](#JavaScript-function)
  - [JavaScript type](#JavaScript-type)
- [Membuat sebuah command](#Membuat-sebuah-command)
  - [Membuat command menyapa](#Membuat-command-menyapa)
  - [Bermain main dengan variable](#Bermain-main-dengen-variable)
- [Penutup](#Penutup)
  - [Penulis](#Penulis)

## Pendahuluan
Tutorial ini akan membantumu dalam membuat sebuah command, meskipun anda tidak pernah belajar pemograman.
Jika kamu sudah mengetahui beberapa hal tentang JavaScript, anda dapat membuka bagian [Membuat sebuah command](#Membuat-sebuah-command).

> **Warning**
> 
> Package ini dalam tahap pembaruan mungkin terdapat kata yang belum lengkap

## Dasar
Berikut dasar dasar sebelum anda membuat sebuah command.

### JavaScript Basic
#### JavaScript variable

Variabel di JavaScript adalah tempat untuk menyimpan nilai, seperti angka atau teks, yang dapat digunakan dalam program. Variabel digunakan untuk menyimpan data yang diperlukan dan dapat digunakan berulang kali di seluruh program.

Dalam JavaScript, variabel dapat dideklarasikan menggunakan kata kunci var, let, atau const. Deklarasi variabel dengan var digunakan untuk variabel global atau variabel lokal yang dapat diubah nilainya. Deklarasi variabel dengan let digunakan untuk variabel lokal yang nilainya dapat diubah. Sedangkan, deklarasi variabel dengan const digunakan untuk variabel konstan yang nilainya tidak dapat diubah.

Contoh:
``` js
var name = "Miru"; // Deklarasi variabel dengan var
let age = 30; // Deklarasi variabel dengan let
const PI = 3.14; // Deklarasi variabel dengan const
```
Variabel juga dapat diinisialisasi dengan nilai default atau tanpa nilai. Nilai variabel dapat diubah dengan memberikan nilai baru.

Contoh:
``` js
let message; // Inisialisasi variabel tanpa nilai
message = "Hello, world!"; // Mengubah nilai variabel
console.log(message); // Output: Hello, world!
```
JavaScript juga mendukung tipe data yang berbeda, seperti string, angka, boolean, array, objek, dan lainnya. Variabel dapat menampung nilai dari tipe data apa pun.

Contoh:
``` js
let name = "Miru"; // Tipe data string
let age = 30; // Tipe data angka
let isStudent = true; // Tipe data boolean
let numbers = [1, 2, 3, 4]; // Tipe data array
let person = { name: "Miru", age: 30 }; // Tipe data objek
```

Variabel JavaScript dapat digunakan untuk menyimpan dan memanipulasi data dalam program. Dengan menggunakan variabel, programmer dapat membuat program yang lebih fleksibel dan dinamis.

#### JavaScript output

Output JavaScript adalah hasil yang dihasilkan oleh kode JavaScript yang dijalankan di lingkungan runtime Node.js. Output dapat berupa teks, angka, boolean (true/false), array, objek, atau nilai lainnya, tergantung pada jenis kode yang dieksekusi. 

Beberapa cara umum untuk menghasilkan output JavaScript adalah sebagai berikut:

Menggunakan perintah console.log(): Ini adalah cara yang umum digunakan untuk menghasilkan output di konsol Node.js. Contoh: console.log("Hello, world!");

Menggunakan modul fs: Modul ini dapat digunakan untuk menulis atau membaca dari file. Contoh:

``` js
const fs = require('fs');
fs.writeFileSync('output.txt', 'Hello, world!');
```
Menggunakan modul http: Modul ini dapat digunakan untuk membuat server web dan menghasilkan output sebagai respons terhadap permintaan HTTP. Contoh:

``` js

const http = require('http');
http.createServer(function(req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello, world!');
}).listen(8080);

```
Menghasilkan output ke variabel: Output dapat disimpan ke dalam variabel untuk digunakan nanti dalam program. Contoh: var message = "Hello, world!";

#### JavaScript function

Selanjutnya anda akan belajar tentang `Function`, `Function` atau fungsi adalah sebuah blok kode yang dapat dipanggil atau dijalankan kembali dengan cara memanggil namanya. 
Function dapat digunakan untuk mengelompokkan kode, melakukan tugas yang berulang, atau memecah kode program menjadi bagian-bagian yang lebih kecil dan mudah diatur. Setiap function dapat memiliki satu atau lebih parameter, yang digunakan untuk memasukkan nilai atau data ke dalam function tersebut, dan setiap function dapat mengembalikan sebuah nilai atau hasil yang dihasilkan dari proses di dalam function. 
Function dianggap sebagai salah satu konsep paling fundamental dalam JavaScript, dan sangat penting dalam pembuatan program JavaScript yang efisien dan mudah dipahami.

Contoh 1: Function dengan satu parameter
``` js
function greeting(name) {
  console.log("Hello, " + name + "!");
}

greeting("Axuint"); // output: Hello, Axuint!
greeting("Miru"); // output: Hello, Miru!
```
Contoh di atas adalah function yang bernama "greeting", yang memiliki satu parameter "name". Function ini akan mencetak pesan "Hello, [name]!" ke dalam konsol, di mana [name] adalah nilai yang diberikan ke parameter "name". Function ini dipanggil dua kali dengan nilai parameter yang berbeda, yaitu "Axuint" dan "Miru".

Contoh 2: Function dengan dua parameter dan nilai kembali


``` js
function calculateArea(width, height) {
  var area = width * height;
  return area;
}

var rectangleArea = calculateArea(5, 10);
console.log(rectangleArea); // output: 50
```
Contoh di atas adalah function yang bernama "calculateArea", yang memiliki dua parameter "width" dan "height". Function ini akan menghitung luas persegi panjang berdasarkan nilai parameter "width" dan "height", kemudian mengembalikan hasil perhitungan dengan kata kunci "return". Function ini dipanggil dengan nilai parameter "5" dan "10", dan hasil perhitungan di simpan ke dalam variabel "rectangleArea". Hasil perhitungan tersebut kemudian dicetak ke dalam konsol menggunakan fungsi "console.log".
#### JavaScript type

JavaScript memiliki beberapa tipe data, yang dapat dibagi menjadi dua kategori: primitif dan objek.

Tipe data primitif adalah tipe data yang sederhana dan tidak berubah. Ada lima tipe data primitif di JavaScript, yaitu:

- Number: Tipe data ini digunakan untuk merepresentasikan angka, baik itu bilangan bulat atau desimal.

- String: Tipe data ini digunakan untuk merepresentasikan teks atau karakter.

- Boolean: Tipe data ini hanya memiliki dua nilai, yaitu true dan false, yang digunakan untuk merepresentasikan nilai benar atau salah.

- Null: Tipe data ini merepresentasikan nilai kosong atau non-eksisten.

- Undefined: Tipe data ini digunakan untuk merepresentasikan nilai yang belum ditentukan atau tidak terdefinisi.

Tipe data objek adalah tipe data yang kompleks dan bisa berubah. Objek digunakan untuk merepresentasikan struktur data yang lebih kompleks, seperti array, fungsi, dan objek itul sendiri. Objek memiliki properti dan metode yang dapat diakses melalui notasi titik atau tanda kurung siku.

JavaScript juga memiliki dua tipe data khusus, yaitu:

- Symbol: Tipe data ini diperkenalkan pada ECMAScript 6 dan digunakan untuk merepresentasikan nilai unik yang digunakan sebagai properti objek.

- BigInt: Tipe data ini diperkenalkan pada ECMAScript 2020 dan digunakan untuk merepresentasikan angka yang lebih besar dari 2^53 - 1, yang merupakan batas maksimal untuk tipe data Number.

Dalam JavaScript, tipe data diidentifikasi secara dinamis saat variabel atau nilai dideklarasikan dan dapat diubah selama program dijalankan. Oleh karena itu, sangat penting untuk memahami tipe data JavaScript dan bagaimana mereka berperilaku dalam program.

Berikut adalah contoh penggunaan tipe data di JavaScript:

- Number:
``` js
let x = 10;
let y = 3.14;
let z = x + y;
console.log(z); // Output: 13.14
```
- String:
``` js
let firstName = "Miru";
let lastName = 'Ichigawa';
let fullName = firstName + " " + lastName;
console.log(fullName); // Output: Miru Ichigawa
```
- Boolean:
``` js
let isStudent = true;
if (isStudent) {
  console.log("You are a student");
} else {
  console.log("You are not a student");
}
```
- Null:
``` js
let person = null;
console.log(person); // Output: null
```
- Undefined:
``` js
let age;
console.log(age); // Output: undefined
```
- Objek:
``` js
let car = { brand: "Toyota", model: "Camry", year: 2022 };
console.log(car.brand); // Output: Toyota
```
- Array:
``` js
let fruits = ["apple", "banana", "orange"];
console.log(fruits[1]); // Output: banana
```
- Function:
``` js
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("John"); // Output: Hello, John!
```
- Symbol:
``` js
let sym1 = Symbol();
let sym2 = Symbol("key");
let obj = {
  [sym1]: "value1",
  [sym2]: "value2"
};
console.log(obj[sym1]); // Output: value1
```
- BigInt:
``` js
let bigNumber = 123456789012345678901234567890n;
console.log(bigNumber); // Output: 123456789012345678901234567890n
```

## Membuat sebuah command
#### Membuat command menyapa
Dibagian ini kita akan membuat sebuah command menyapa user, Untuk membuat command anda harus pergi ke dalam folder `commands` dan buat sebuah file bernama `menyapa.js` seperti ini:
```
├── commands 
│   └── menyapa.js
```

Untuk membuat command kita memasukan sebuah kode seperti
``` js
export default async function({message, sender}){
  ... do something
}
```
**Q & A**
``` txt
Q: Apa itu export kegunaanya?
A: export digunakan untuk mengekspor nilai dari module yang mana file ini akan di import kedalam command manager dan akan digunakan jika ada yang menggunakanya
```
``` txt
Q: Apa itu async dan await?
A: Async dan Await adalah fitur yang tersedia di Node.js untuk menangani operasi asynchronous atau operasi non-blokir.
```

Jika anda sudah tau fungsi sebuah `Function` maka anda dapat melihat parameter `message` dan `sender`. Parameter `message` berfungsi untuk mengirimkan pesan reply, pesan react. parameter `message` berisi biasanya object seperti
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
Anda dapat menggunakanya untuk mengambil object dalam sebuah pesan seperti `media`, `text`, `room`. dan parameter selanjutnya adalah `sender`, Parameter sender digunakan untuk mengambil data user seperti username dan id dan biasanya `sender` memiliki object seperti
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
Untuk membuat command menyapa maka kita membutuhkan parameter `message` untuk mengirimkan pesan reply dan `sender` untuk mendapatkan username user. 
Lanjut jika sudah, masukan sebuah kode kedalam `menyapa.js`:
``` js
export default async function({message, sender}){
  const username = sender.name // Variable untuk mendapatkan username user
  return message.reply(`Hallo, ${username}!`) // Mengirimkan pesan reply menyapa
}
```
#### Bermain main dengen variable
Jika kamu sudah mengetahui apa itu `function` dalam JavaScript maka kalian pasi mengetahui jika dalam `function` ada sebuah `parameter` nah di dalam `parameter` tersebut kita bisa menyimpan banyak sekali `variable` untuk kita gunakan. pada kali ini saya akan mencontohkan bagaimana sih cara menggunakan dan mengaplikasikannya ke kode kita. Sebelum itu mari kita bikin terlebih dalulu file commands nya disini saya akan namakan `info.js` untuk menampilkan data user yang kita tag atau mentions.
```
├── commands 
│   └── menyapa.js
│   └── info.js
```
Nah untuk memulai mari kita buka terlebih dahulu teks editor kalian kalian bisa pakai `vscode` , `sublime text` atau `notepad` kalau disini saya menggunakan `sublime text`. Ok selanjutnya kita buka file info.js dan tulis sebuah export function sebagai berikut:

``` js
export default async function({bot, sender, message, parameters}){
  return message.reply("Hai"); // mengirimkan pesan balasan ke pengirim pesan
}

```
Nah selanjutnya kita klik `ctrl + s` secara bersamaan untuk mensave file info.js. Selanjutnya kita open terminal dan kita kill terlebih dahulu proses kodenya dengan klik tombol `ctrl + c`. Jika sudah kita run kembali kodenya dengan mengetik `node index` di dalam terminal, Tunggu kode berjalan dan selanjutnya kita cek apakah kode kita berhasil buka WhatsApp dan chat bot dengan mengetik `!info`.

jika bot kalian seperti di atas maka selamat kamu berhasil membuat sebuah commands.
Next kita buka kembali file `info.js` dan kita ubah kembali kode yang kita ketik tadi.
``` js
export default async function({bot, sender, message, parameters}){
  return message.reply("Hai " + sender.name + "!"); // mengirimkan pesan balasan ke pengirim pesan dengan menyebut nama pengirim pesan
}
```
mari kita ubah kembali untuk mengecek apakah user mentag seseorang atau tidak.
``` js
export default async function({ bot, sender, message, parameters }) {
  const mentioned = message.mentions.length > 0; // Cek jumlah mentions 
  const replyMessage = `Hai ${sender.name}!\nKamu ${mentioned ? "telah" : "tidak"} men-tag seseorang.`; // Mengirim pesan balasan
  return message.reply(replyMessage);
}
```

Penjelasan:
- `const mentioned = message.mentions.length > 0;` digunakan untuk memeriksa apakah ada mention pada pesan. Jika ada, nilai variabel mentioned akan menjadi true, jika tidak, nilai variabel mentioned akan menjadi false.
- `const replyMessage = Hai ${sender.name}!\nKamu ${mentioned ? "telah" : "tidak"} men-tag seseorang.;` digunakan untuk membuat pesan balasan. Pesan balasan akan berisi informasi bahwa pengirim telah men-tag seseorang jika mentioned bernilai true, atau informasi bahwa pengirim tidak men-tag siapa pun jika mentioned bernilai false.
- `return message.reply(replyMessage);` digunakan untuk membalas pesan dengan isi variabel replyMessage menggunakan metode reply pada objek message.
### Penutup
Terimakasih kepada para `contributor` dan teman teman semua yang sudah membaca tutorial ini semoga bermanfaat.
#### Penulis
- [Miftah Fauzan (Axuint)](https://miftahfauzan.netlify.app)