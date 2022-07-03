## Operator Komparasi

Terdapat serangkaian karakter khusus yang disebut dengan operator pembanding/komparasi yang dapat mengevaluasi dan membandingkan dua nilai. Berikut daftar operator dan fungsinya:

| Operator | Fungsi |
| -------- | ------ |
| == | Membandingkan kedua nilai **apakah sama**. (Tidak Identik) |
| != | Membandingkan kedua nilai **apakah tidak sama**. (Tidak Identik) |
| === | Membandingkan kedua nilai **apakah identik**. |
| !== | Membandingkan kedua nilai **apakah tidak identik**. |
| > | Membandingkan dua nilai **apakah nilai pertama lebih besar dari nilai kedua**. |
| >= | Membandingkan dua nilai **apakah nilai pertama lebih besar atau sama dengan dari nilai kedua**. |
| < | Membandingkan dua nilai apakah nilai pertama **lebih kecil dari nilai kedua**. |
| <= | Membandingkan dua nilai **apakah nilai pertama lebih kecil dari atau sama dengan nilai kedua**. |

Ketika kita melakukan perbandingan antara dua nilai, JavaScript akan mengevaluasi kedua nilai tersebut dan akan mengembalikan boolean dengan nilai hasil perbandingan tersebut, baik `false`, atau `true`. Berikut contohnya:

```javascript
let a = 10;
let b = 12;

console.log(a < b);
console.log(a > b);

/* output
true
false
*/
```

### Perbedaan "sama" dan "identik"

Dalam operator komparasi di JavaScript, hal yang menjadi sedikit “*tricky*” adalah membedakan antara “sama” (`==`) dan “identik” (`===`).

Kita sudah mengetahui bahwa setiap nilai pasti memiliki tipe data baik itu number, string atau boolean. Contohnya sebuah string “10” dan number 10 merupakan hal yang serupa, tetapi keduanya tidak benar-benar sama.

Hal inilah yang membedakan antara sama dan identik pada JavaScript. Jika kita ingin membandingkan hanya dari kesamaan nilainya kita bisa gunakan `==` tapi jika kita ingin membandingkan dengan memperhatikan tipe datanya kita gunakan `===`.

```javascript
const aString = '10';
const aNumber = 10

console.log(aString == aNumber) // true, karena nilainya sama-sama 10
console.log(aString === aNumber) // false, karena walaupun nilainya sama, tetapi tipe datanya berbeda

/* output
true
false
*/
```

### Logical Operators

Terdapat beberapa operator lain yang dapat kita gunakan untuk menetapkan logika yang lebih kompleks, yakni dengan *logical operators*. Dengan *logical operator* kita dapat menggunakan kombinasi dari dua nilai boolean atau bahkan lebih dalam menetapkan logika.

Pada JavaScript terdapat tiga buah karakter khusus yang berfungsi sebagai *logical operator*, berikut macam-macam *logical operator* dan fungsinya:

| Operator | Deskripsi |
| -------- | --------- |
| && | Operator dan *(and)*, logika akan menghasilkan **true apabila semua kondisi terpenuhi** (bernilai true). |
| &#x7c; &#x7c;  | Operator atau *(or)*, logika akan menghasilkan **true apabila ada salah satu kondisi terpenuhi** (bernilai true). |
| ! | Operator tidak (not), digunakan untuk membalikan suatu kondisi. |

Contoh :

```javascript
let a = 10;
let b = 12;

/* AND operator */
console.log(a < 15 && b > 10); // (true && true) -> true
console.log(a > 15 && b > 10); // (false && true) -> false

/* OR operator */
console.log(a < 15 || b > 10); // (true || true) -> true
console.log(a > 15 || b > 10); // (false || true) -> true

/* NOT operator */
console.log(!(a < 15)); // !(true) -> false
console.log(!(a < 15 && b > 10)); // !(true && true) -> !(true) -> false

/* output
true
false
true
true
false
false
*/
```



