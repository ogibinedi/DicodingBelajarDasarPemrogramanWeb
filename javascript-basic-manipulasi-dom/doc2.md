## Tipe Data

 Tipe data merupakan pengklasifikasian data berdasarkan jenis data tersebut. Pada JavaScript terdapat beberapa tipe data sebagai berikut:

 ### Undefined

 Tipe data ini terbentuk ketika sebuah variabel tidak memiliki nilai, dalam arti lain ketika kita mendeklarasikan variabel tanpa menginisialisasikan nilainya, maka variabel tersebut menjadi `undefined`. 

 Contoh :

 ```javascript
 let x;
 console.log("Tipe data variable x: " + typeof(x));

//  output: Tipe data variable x: undefined
```
>Fungsi `typeof()` digunakan untuk memastikan tipe data pada variabel dengan mengembalikan tipe data tersebut dalam bentuk teks

### Numbers

Nilai dari tipe data number adalah angka. JavaScript variabel bertipe data number dituliskan seperti ini:

```javascript
let x = 10;
```

Jika angka tersebut merupakan sebuah bilangan desimal, maka kita bisa gunakan tanda titik pada pecahan bilangannya.

```javascript
let x = 10;
console.log(typeof(x))

/* output: number */

let y = 17.25;
console.log(typeof(y))

/* output: number */
```

Pada tipe data number kita juga dapat melakukan perhitungan aritmatika seperti penambahan, pengurangan, perkalian, dll. Berikut operator yang dapat kita gunakan dalam melakukan perhitungan aritmatika pada tipe data number:

| Operator | Fungsi | Contoh |
| -------- | ------ | ------ |
| + | Penambahan | 10 + 10 = 20 |
| - | Pengurangan | 15 - 7 = 8 |
| / | Pembagian | 21 / 7 = 3 |
| * | Perkalian | 9 * 9 = 81 |
| % | Sisa Hasil Bagi | 5 % 2 = 1 |

```javascript
let a = 12;
let b = 9;

console.log(a + b)
console.log(a - b)
console.log(a * b)
console.log(a / b)
console.log(a % b)

/* output:
21
3
108
1.3333333333333333
3
*/
```

Pada operator aritmatika juga terdapat operator increment (++) dan decrement (--). Operator increment dan decrement digunakan untuk menambahkan atau mengurangi nilai 1 pada nilai variabel yang ada sekarang.

Operator ini dapat dituliskan sebelum atau sesudah variabel, tetapi hal tersebut bukan berarti sama. Berikut ketentuannya:

- Jika dituliskan setelah variabel (x++), statement akan menghasilkan nilai variabel sebelum ditingkatkan nilainya.
- Jika dituliskan sebelum variabel (++x), statement akan menghasilkan nilai variabel setelah ditingkatkan nilainya.

Lebih jelasnya berikut contoh kode dalam penerapan operator tersebut, perhatikan hasil yang di dapat.

```javascript
/* Increment dan Decrement */

let postfix = 5;
console.log(postfix++);
/* output: 5 */

let prefix = 5;
console.log(++prefix);
/* output: 6 */
```

### Strings

Tipe data selanjutnya adalah strings, String ini dasarnya adalah sebuah teks. Pada JavaScript untuk menetapkan nilai string pada variabel, gunakan tanda single (‘) atau double quote (“) di antara teksnya. Contohnya:

```javascript
let greet = "Hello";
console.log(typeof(greet));

// output: string
```

Apa pun yang berada di antara tanda double quote atau single quote merupakan sebuah string, baik itu angka, huruf maupun karakter spesial. 

Pada string juga kita dapat menggunakan operator plus (+). Operator tersebut pada string berfungsi untuk menggabungkan dua teks yang terpisah menjadi satu buah teks. Contohnya seperti ini:

```javascript
let greet = "Hello";
let moreGreet = greet + greet;

console.log(moreGreet);

// output: HelloHello
```

### boolean

Boolean hanya dapat memiliki dua nilai, yakni `true` atau `false`. Tipe data ini menjadi kunci utama dalam penentuan logika, kita akan memahaminya nanti ketika pembahasan *if/else statement*. Untuk menetapkan nilai `boolean` pada variabel kita bisa menggunakan keyword `true` atau `false`.

```javascript
let x = true;
let y = false;

console.log(typeof(x))
console.log(typeof(y))

/* output: 
boolean
boolean
*/
```

Atau kita bisa gunakan operator komparasi seperti lebih dari `(>)` atau kurang dari `(<)`. Contohnya:

```javascript
const a = 10;
const b = 12;

let isGreater = a > b;
let isLess = a < b;

console.log(isGreater);
console.log(isLess);

/* output:
false
true
*/
```

### Null

Serupa dengan undefined, namun null perlu diinisialisasikan pada variabel. null biasa digunakan sebagai nilai sementara pada variabel, tapi sebenarnya nilai tersebut “tidak ada”.

Contoh:

```javascript
let someLaterData = null;
console.log(someLaterData);

/* output:
null
*/
```

Meskipun terdapat beberapa tipe data dalam JavaScript, tetapi variabel pada JavaScript memiliki sifat tipe data yang dinamis. Artinya, kita dapat memberikan tipe data yang berubah-ubah pada satu variabel yang sama. Contohnya:

```javascript
let x; // x merupakan undefined
x = 1 // sekarang x merupakan number
x = true // sekarang x merupakan boolean
x = "Harry" // sekarang x merupakan string
```




