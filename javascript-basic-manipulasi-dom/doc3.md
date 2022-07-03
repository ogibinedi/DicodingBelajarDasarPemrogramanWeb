## Array dan Object

Array merupakan tipe data yang dapat mengelompokkan lebih dari satu nilai dari tipe data lain dengan menempatkannya pada satu variabel. Contoh:

```javascript
let myArray = ["Coklat", 42.5, 22, true, "Programming"];
console.log(myArray);

/* output:
[ 'Coklat', 42.5, 22, true, 'Programming' ]
*/
```

Nilai - nilai yang berada pada array disusun dan diakses secara *indexing*. Pengurutan nilai jika ingin mengaksesnya di mulai dari angka 0,1,2,3... dan seterusnya.

Untuk mengakses nilai di dalam array kita gunakan tanda kurung siku [] yang di dalamnya berupa angka yang merupakan posisi nilai yang ingin diakses.

```javascript
let myArray = ["Coklat", 42.5, 22, true, "Programming"];
console.log(myArray[1]);

/* output:
42.5
*/
```

 Jika kita mengakses nilai array lebih dari index-nya maka hasilnya akan `undefined`. Index terakhir array selalu jumlah nilai array - 1.
 Contoh lebih detail sbb:

 ```javascript
 let myArray = ["Coklat", 42.5, 22, true, "Programming"];
console.log(myArray[0]);
console.log(myArray[1]);
console.log(myArray[2]);
console.log(myArray[3]);
console.log(myArray[4]);
console.log(myArray[5]);
console.log("Panjang nilai myArray adalah " + myArray.length + ".");

/* output:
Coklat
42.5
22
true
Programming
undefined
Panjang nilai myArray adalah 5.
*/
```

### Objek

Objek serupa dengan array yang dapat menampung banyak nilai dengan tipe data yang beragam. Untuk mengelola data menggunakan objek, bedanya objek diakses tidak melalui *indexing*,  melainkan menggunakan pendekatan *key-value*. Untuk mengakses nilainya kita gunakan key. Key juga biasa disebut dengan properti.

Untuk menetapkan objek pada variabel gunakan tanda kurung kurawal { } dalam menginisialisasinya. Kemudian di dalamnya kita tetapkan **key: value**.

```javascript
let object = {key1: "value1", key2: "value2", key3: "value3"}
```

Dalam menentukan nama key, gunakanlah nama yang dapat mendeskripsikan dari value-nya. Pada value, kita dapat mengisikan nilai dengan tipe data apapun, termasuk array. Contoh:

```javascript
let user = {
    firstName: "Harry",
    lastName: "Potter", 
    age: 20, 
    isMuggle: false,
    stuff: ["Magic Wind", "Flying Car", "Owl"]
};

console.log("Nama: " + user.firstName + " " + user.lastName);
console.log("Jenis Sihir: " + user.stuff[0]);
console.log("Burung Kesayangan: " + user.stuff[2]);

/*output:
Nama: Harry Potter
Jenis Sihir: Magic Wind
Burung Kesayangan
*/
```

Banyak hal sebenarnya yang dapat diceritakan tentang dua hal ini, terutama untuk objek. Jika Kita ingin tahu lebih dalam, Kita bisa baca dokumentasinya pada tautan yang disediakan oleh MDN:

- [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [Objek](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)