## Box Dimensions

Secara standar sebuah box yang dihasilkan tiap elemen selalu cukup untuk menampung konten. Tetapi kita dapat mengatur nilai dimensi dari box tersebut dengan properti `width` dan `height`. 

Cara yang paling banyak digunakan dalam menentukan dimensi kotak adalah dengan menggunakan *pixel*, persentase, atau *ems*. Secara tradisional, pixel merupakan cara yang paling populer karena kita dapat merancang dan mengontrol ukuran secara akurat. 

Berbeda ketika kita menggunakan persentase, ukuran kotak akan relative atau menyesuaikan dari ukuran lain, seperti ukuran jendela browser atau ukuran induk yang menaunginya. Sedangkan ketika menggunakan ems, nilai dimensi kotak akan menyesuaikan berdasarkan ukuran teks yang ditampilkan pada konten elemen tersebut. 

Pada saat ini banyak developer mulai merancang menggunakan persentase dan ems untuk menetapkan ukuran *box* agar dapat menyesuaikan dengan berbagai macam ukuran layar.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box</title>
    <style>
        .box {
           height: 300px;
           width: 300px;
           background-color: #11C5C6;
       }
       p {
           height: 75%;
           width: 75%;
           background-color: #FBDD1C;
       }
    </style>
</head>
<body>
    <div class="box">
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officiis labore repudiandae dolore harum eum, praesentium deserunt, nostrum iste adipisci ipsa blanditiis inventore beatae omnis delectus provident quaerat facilis unde sapiente.</p>
    </div>
</body>
</html>
```

Pada contoh di atas kita dapat melihat elemen `<div>` memiliki dimensi elemen dengan lebar **300px** dan tinggi **300px**. Di dalamnya terdapat elemen `<p>` yang memiliki ukuran elemen 75% dari lebar dan tinggi elemen induknya. Dengan begitu berarti elemen `<p>` memiliki ukuran **225px** untuk panjang dan lebarnya.

### Limiting Dimension

Beberapa website yang ada sekarang menampilkan layout yang dapat melebar dan menyempit mengikuti ukuran layar pengguna. Pada prinsip tampilan tersebut mungkin kita memerlukan sebuah limitasi ukuran yang harus ditampilkan agar konten selalu dapat ditampilkan secara proporsional. Untuk melakukannya kita manfaatkan properti `min-width` dan `max-width`.

- min-width : merupakan properti yang digunakan untuk menetapkan nilai lebar minimal yang harus dimiliki elemen.
- max-width : merupakan properti yang digunakan untuk menetapkan nilai lebar maksimal yang harus dimiliki elemen.

Keduanya merupakan properti yang sangat membantu untuk memastikan konten halaman dapat terbaca oleh pengguna (terutama ketika pengguna menggunakan ponsel). Misalnya, kita dapat menggunakan properti `max-width` untuk memastikan bahwa baris teks yang muncul tidak terlalu lebar.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Limiting Dimension</title>
    <style>
       .content {
           max-width: 800px;
           height: 400px;
           margin: 0 auto;
           background-color: deeppink;
       }

       p {
           font-size: 1.5em;
           font-weight: bold;
       }
    </style>
</head>
<body>
    <div class="content">
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officiis labore repudiandae dolore harum eum, praesentium deserunt, nostrum iste adipisci ipsa blanditiis inventore beatae omnis delectus provident quaerat facilis unde sapiente.</p>
    </div>
</body>
</html>
```

Dengan cara yang sama, mungkin kita juga perlu membatasi ukuran panjang. Kita bisa gunakan `min-height` dan `max-height`.

### Overflowing Content

Dimensi box yang dihasilkan elemen selalu cukup untuk menampung konten tetapi hal ini tidak berlaku jika kita tetapkan secara manual panjang dan lebarnya. Tak jarang terjadi *overflow* ketika kita menerapkan ukuran pada elemen tetapi konten di dalamnya begitu banyak. Contohnya seperti berikut:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Overflowing Content</title>
    <style>
       div {
           height: 200px;
           width: 200px;
           background-color: lightgreen;
       }
    </style>
</head>
<body>
    <div>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officiis labore repudiandae dolore harum eum, praesentium deserunt, nostrum iste adipisci ipsa blanditiis inventore beatae omnis delectus provident quaerat facilis unde sapiente.</p>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Officiis labore repudiandae dolore harum eum, praesentium deserunt, nostrum iste adipisci ipsa blanditiis inventore beatae omnis delectus provident quaerat facilis unde sapiente.</p>
    </div>
</body>
</html>
```

### Box Sizing

Pada CSS2 ukuran lebar dan panjang elemen mengacu pada konten elemen (*content-box*). Itu berarti ukuran elemen seluruhnya merupakan nilai panjang dan lebar yang kita spesifikasikan ditambah dengan nilai *padding* dan *border* yang diterapkan pada elemen. Hal tersebut membuat sebagian developer menjadi sulit menetapkan ukuran dimensi.

Setelah CSS3 kita dapat memilih tipe pengukuran lain dalam menentukan dimensi elemen. Dengan menggunakan properti `box-sizing` kita dapat menentukannya berdasarkan border box, di mana ukuran elemen sudah termasuk content, padding dan border. Dengan metode ini, hasil elemen yang ditampilkan (termasuk *padding* dan *border*) akan memiliki dimensi yang sama persis seperti yang kita tentukan.

```html
<!doctype html>
<html lang="en">
<head>
   <style>
       div {
           height: 200px;
           width: 200px;
           background-color: lightgreen;
           border: 10px solid cornflowerblue;
           padding: 20px;
       }
 
       .content {
           box-sizing: content-box;
       }
 
       .box {
           box-sizing: border-box;
       }
   </style>
</head>
<body>
<div class="content">
</div>
<p>Elemen menerapkan <code>box-sizing: content-box;</code> Ukuran box secara keseluruhan akan menjadi 260px lebar, 260px tinggi; 260 = 200 + 20 + 20 + 10 + 10</p>
<br>
<div class="box">
</div>
<p>Elemen menerapkan <code>box-sizing: border-box;</code> Ukuran box akan tetap 200px lebar, 200px tinggi meskipun menerapkan padding dan border</p>
</body>
</html>
```