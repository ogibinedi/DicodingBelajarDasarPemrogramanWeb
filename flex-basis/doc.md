## Flex Basis

Selain menggunakan `flex-grow`, untuk menentukan ukuran flex item, kita bisa gunakan properti flex-basis. Properti ini mirip seperti width dalam menentukan dimensi box. Kita bisa menggunakan nilai satuan tetap seperti px, pt, pc, cm dll. Selain itu, kita juga bisa menggunakan satuan persentase (%).

Properti `flex-basis` ini digunakan ketika kita ingin menetapkan ukuran awal pada sebuah flex-item. Alhasil, kita dapat mengatur ukuran dengan lebih leluasa. `flex-basis` biasa digunakan ketika kita menerapkan nested flex-container dan terdapat perbedaan jumlah child pada container-nya. Untuk lebih mudah menggambarkannya, perhatikan contoh berikut:

Sebabnya, `flex-grow` akan mencari nilai yang sesuai yang dapat dibagi pada flex-items. Agak terdengar aneh, bukan? Nah, temukan artikel yang cukup menarik yang membahas permasalahan ini pada tautan berikut.

Sebenarnya bisa saja kita menggunakan `flex-grow` untuk mendapatkan hasil yang diinginkan namun kita harus mencari nilai yang pas secara manual. Ini tentunya akan memakan waktu lebih.

Pada kasus seperti ini, solusinya adalah menggunakan properti flex-basis. Dengan properti ini kita dapat asumsikan bahwa total ruang kosong pada flex-container adalah 100%. Jika dibagi rata terhadap empat buah flex-item, maka tiap itemnya harus memiliki nilai 25%.

Sebabnya, `flex-grow` akan mencari nilai yang sesuai yang dapat dibagi pada flex-items. Agak terdengar aneh, bukan? Nah, temukan artikel yang cukup menarik yang membahas permasalahan ini pada tautan berikut.

Sebenarnya bisa saja kita menggunakan `flex-grow` untuk mendapatkan hasil yang diinginkan namun kita harus mencari nilai yang pas secara manual. Ini tentunya akan memakan waktu lebih.

Pada kasus seperti ini, solusinya adalah menggunakan properti `flex-basis`. Dengan properti ini kita dapat asumsikan bahwa total ruang kosong pada flex-container adalah 100%. Jika dibagi rata terhadap empat buah `flex-item`, maka tiap itemnya harus memiliki nilai 25%.