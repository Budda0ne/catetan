---
title: "JavaScript: Mengenal Perulangan (Loop)"
categories: [javascript]
tags: [mengenal javascript, mengenal perulangan nila, javascript loop]
excerpt: "Mengetahui cara melakukan perulangan objek dalam bahasa JavaScript"
header:
 teaser: "https://cdn.statically.io/img/www.boleh.id/bolehtau/wp-content/uploads/2019/09/js.jpg?w=420px"
 og_image: "https://cdn.statically.io/img/www.boleh.id/bolehtau/wp-content/uploads/2019/09/js.jpg"
---
Sejauh ini kita sudah [mengenal array](https://www.catetan.pw/javascript/javascript-arrays-dan-objek/) sebagai tempat untuk menyimpan banyak data. Ada beberapa kasus dimana kita ingin memeriksa setiap item dalam sebuah array dan melakukan sesuatu dengannya, tetapi kita tidak ingin menuliskan seluruh daftar nilai pada array secara manual, dan menyibukkan diri untuk melakukan hal yang berulang. Maka dari itu kita perlu mempelajari teknik yang dapat mengatasi permasalahan tersebut, teknik ini disebut dengan **loops**.

## For loop

Terdapat beberapa cara dalam melakukan proses `loop` pada JavaScript, namun “for” merupakan salah satu **cara yang banyak digunakan**. Struktur dasar dari for tampak seperti berikut:

```javascript
for(inisialisasi variabel; test kondisi; perubahan nilai variabel) {
    // do something
}
```

Dan berikut contoh penerapan for secara nyata:

```javascript
for(let i = 0; i < 5; i++) {
    console.log(i);
}
/* output
0
1
2
3
4
*/
```

Mungkin kode tersebut sulit dipahami jadi mari kita bahas sedikit demi sedikit.

Yang pertama adalah `for()`, kita memanggil for statement di mana kita memerintahkan JavaScript seperti ini: “Hai JavaScript! Lakukan perulangan jika kondisi ini benar”, selanjutnya tentu kita membutuhkan sebuah kondisi untuk dievaluasi.

Namun sebelum memberikan kondisi, kita dapat membuat sebuah variabel `i` sebagai index iterasi dengan memberikan nilai 0 `(let i = 0;)`. Mengapa kita memberikan nilai **0** pada variabel `i`? Karena ini merupakan sebuah habit dimana perhitungan perulangan dimulai dari 0, begitu juga dengan indexing pada array.

Lalu `i < 5;` merupakan sebuah kondisi dimana jika kondisinya terpenuhi proses looping akan dijalankan. Jadi jika kita memberikan kondisi seperti ini: `i < 5;` maka proses looping akan terjadi sebanyak 5 kali.

Dan terakhir `i++``; menunjukan perubahan nilai variabel `i` di setiap proses perulangan terjadi. Biasanya perubahan merupakan _increment_ ataupun _decrement_ dari variabel yang kita tetapkan sebelumnya (variabel i). Jika kita tidak menetapkan perubahan nilai, proses perulangan dapat berjalan selamanya! Karena kondisi akan terus terpenuhi.

Lalu `{ console.log(i); }` merupakan statement yang akan dieksekusi pada **setiap proses loop**. Kita dapat menuliskan banyak statement di sini selama berada di dalam tanda `{ }`. Pada kode tersebut kita memerintahkan JavaScript untuk menampilkan nilai `i` pada setiap proses perulangan. Sehingga _output_ akan menghasilkan deretan angka dari **0** hingga **4**.

Huft, cukup panjang untuk memahami for loops, mari kita kembali ke tujuan awal, lantas bagaimana **cara memeriksa item** dalam array dengan menggunakan _for loop_? Kita dapat melakukannya dengan seperti ini:

```javascript
const myArray = ["Harry", "Ron", "Hermione", "Tom"];
for(let i = 0; i < myArray.length; i++) {
    console.log(myArray[i]);
}
/* output
Harry
Ron
Hermione
Tom
*/
```

Mudah kan? Kita gunakan `i < myArray.length` sebagai **batasan** pada proses looping, sehingga proses looping **tidak lebih dari panjang array**. Kemudian untuk mengakses index array kita manfaatkan nilai variabel `i`, dimana variabel `i` ini terus bertambah nilainya pada tiap proses loop, sehingga kita bisa mengakses tiap index pada array secara otomatis.

## For of loop

Cara lain dalam melakukan looping adalah menggunakan **for..of**. For of mulai hadir pada _ECMAScript 2015 (ES6)_. Cara ini jauh lebih sederhana dan modern dibanding [for loop biasa](#for-loop). Struktur dasar dari for of loop nampak seperti ini:

```javascript
for(arrayItem of myArray) {
    // do something
}
```

Yups, `for of` tidak membutuhkan banyak statement untuk melakukan proses looping pada array. Dengan for..of, nilai tiap array akan diinisialisasi pada variabel baru yang kita tentukan pada tiap proses looping-nya. Jumlah proses looping nya pun akan menyesuaikan dengan ukuran dari array. Sederhananya seperti kita melakukan perintah “Hei JavaScript! Lakukan perulangan pada myArray, akses tiap nilainya dan simpan pada variabel arrayItem”. Pada proses looping kita gunakan variabel `arrayItem` untuk mengakses tiap nilai dari item `myArray`.

Agak sulit memang menjelaskan dengan kata-kata, mari kita terjemahkan dalam kode secara langsung.

```javascript
let myArray = ["Harry", "Ron", "Hermione", "Tom"];
for(const arrayItem of myArray) {
    console.log(arrayItem)
}
/* output
Harry
Ron
Hermione
Tom
*/
```

Lebih mudah dan simpel bukan?

Berikut snippet code dari contoh kode yang digunakan pada materi di atas, Anda bisa mencobanya sendiri, dan pahami cara penggunaan dari for loop dan for of loop.

https://glot.io/snippets/fi7iwiumv8
