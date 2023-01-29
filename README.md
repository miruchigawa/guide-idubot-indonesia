# Tutorial

**Table of contents**
- [Basic](#Basic)
  - [JavaScript membuat variable](#JavaScript-variable)
  - [JavaScript output](#show-output)
  - [JavaScript function](#JavaScript-function)
  - [JavaScript type](#JavaScript-type)
- [Membuat sebuah command](#create-a-command)
  - [Parameter](#parameter)

## Pembukaan
Tutorial ini akan membantumu dalam membuat sebuah command, meskipun anda tidak pernah belajar pemograman.
Jika kamu sudah mengetahui beberapa hal tentang JavaScript, anda dapat membuka bagian [Membuat sebuah command](#create-a-command).

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
axuint@localhost ~$ node filename.js
17
```

maka anda akan melihat output seperti diatas