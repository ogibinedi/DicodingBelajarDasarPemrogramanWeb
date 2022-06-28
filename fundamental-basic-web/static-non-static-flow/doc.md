## Beda Static Flow dan Non Static FLow

CSS memiliki dua buah *flow* yang bisa digunakan untuk menampilkan elemen, yakni *static* dan *non-static*

Misalkan kita memiliki tiga buah elemen `<div>` yang berukuran 200px kali 200px (width dan height), berikut contohnya:

```css
.box {
    width: 200px;
    height: 200px;
}

.first {
   background-color: #60d0a8;
}
 
.second {
   background-color: #6495ed;
}
 
.third {
   background-color: #ffa500;
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Static Non Static Flow</title>
    <style>
        .box {
            width: 200px;
            height: 200px;
        }

        .first {
            background-color: #60d0a8;;
        }

        .second {
            background-color: #6495ed;
        }

        .third {
            background-color: #ffa500;
        }
    </style>
</head>
<body>
    <div class="box first"></div>
    <div class="box second"></div>
    <div class="box third"></div>
</body>
</html>
```

Karena kita tidak mengatur properti position dari ketiga elemen tersebut, maka tiap elemen akan ditampilkan dengan static flow seperti ini:

![Ilustrasi 1](sc/image1.jpeg)

Ketika kita menambahkan pembatas pada kotak nomor dua dengan menambah properti `margin-top: 20px` akan mempengaruhi kotak nomor tiga

```css
.second {
    background-color: #6495ed;
    margin-top: 20px;
}
```

![Ilustrasi 2](sc/image2.png)

Pada ilustrasi di atas kita bisa lihat bahwa kotak yang berwarna oranye ikut bergeser ke bawah. Berbeda ketika kita menerapkan properti position yang dapat membuat elemen keluar dari static flow. Contohnya kita menerapkan properti position dengan nilai relatif.

```css
.second {
    background-color: #6495ed;
    position: relative;
}
```

![Ilustrasi 3](sc/image3.png)

Pada tampilan browser mungkin tidak terdapat perbedaan apapun setelah menerapkan nilai `relative` pada atribut `position`. Namun sebenarnya elemen yang menerapkannya akan diangkat dari luar *static flow* seperti yang ditampilkan pada ilustrasi 3D. Sehingga elemen tersebut dapat leluasa berpindah posisi tanpa mempengaruhi elemen yang berada pada *static flow*.

Untuk mengubah posisi elemen yang berada di *non-static flow*, kita dapat menggunakan properti `top`, `right`, `bottom`, maupun `left`.

```css
.second {
    background-color: #6495ed;
    position: relative;
    top: 30px;
    left: 10px;
}
```

![Ilustrasi 4](sc/image4.png)

>Note: properti `top`, `left`, `right`, dan `bottom` pada CSS hanya akan berpengaruh pada elemen yang menerapkan non-static flow (elemen yang menerapkan nilai `relative`, `absolute`, dan `fixed` pada *properti position*).

### Normal Flow

Dalam flow normal, setiap elemen block ditempatkan di bawah elemen sebelumnya. Karena ini merupakan cara standar browser memperlakukan elemen HTML, kita tidak perlu menetapkan nilai properti position ketika ingin membuat perilaku seperti ini tetapi secara sintaks perilaku ini ditetapkan dengan nilai static.

### Relative Flow

Seperti yang kita ketahui sebelumnya, dengan menetapkan `relative` pada properti `position`, kita dapat melakukan perpindahan posisi elemen ke atas, kanan, bawah, maupun kiri. Perpindahan posisi yang dilakukan tidak akan berpengaruh terhadap posisi elemen di sekitarnya karena dengan  *relative positioning*, elemen tersebut akan dipindahkan dari normal flow.

### Absolute Flow

Ketika properti position diberikan nilai absolute, akan berperilaku sama dengan relative. Elemen akan dikeluarkan dari normal flow sehingga jika elemen dipindahkan posisinya tidak akan berpengaruh pada elemen lain di sekitarnya. 

Namun yang membedakannya adalah elemen ini benar-benar tidak dianggap ada oleh elemen pada normal flow. Akibatnya, lokasi awal elemen yang diberikan nilai absolute akan ditempati oleh elemen di bawahnya.

### Fixed Flow

*Fixed positioning* merupakan *absolute position* namun posisinya selalu relatif pada jendela browser (meskipun diletakan di dalam induk elemen diluar dari *flow normal*). Bahkan ketika pengguna melakukan *scrolling* posisinya akan tetap nampak pada posisinya di layar.





