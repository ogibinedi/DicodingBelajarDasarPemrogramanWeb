## Border

Border merupakan sebuah garis yang mengelilingi area konten dan padding (opsional). Kita bisa mengatur tipe, ketebalan, serta warna garis yang ditampilkan sesuai dengan yang kita inginkan. Kita juga bisa mengatur dalam menampilkan sebagian atau keseluruhan garis pada elemen. Mari kita eksplorasi apa saja properties yang dapat mengatur border.

### Border Width

Properti `border-width` digunakan untuk mengatur ketebalan dari border. Nilai dari properti ini dapat berupa pixel atau menggunakan predefined names value seperti `thin`, `medium`, dan `thick`. Kita tidak bisa menggunakan nilai persentase (%) pada properti ini.

Kita dapat mengatur ukuran garis secara individual dengan menggunakan empat properti terpisah seperti ini:

```css
.box {
   border-top-width: 2px;
   border-right-width: 1px;
   border-bottom-width: 1px;
   border-left-width: 2px;
}
```

Tetapi kita juga dapat menetapkan nilai keempatnya sekaligus dalam satu properti seperti ini

```css
.box {
  border-width: 2px 1px 1px 2px; /*top right bottom left*/
}
```

Properti `border-width` dapat ditentukan dengan menggunakan satu, dua, tiga, atau empat nilai. Berikut penjelasannya: 

- Ketika satu nilai ditentukan, maka nilai berlaku untuk empat sisi.
- Ketika dua nilai ditentukan, nilai pertama berlaku untuk sisi atas dan bawah, nilai kedua untuk sisi kiri dan kanan.
- Ketika tiga nilai ditentukan, nilai pertama berlaku untuk sisi atas, nilai yang kedua untuk sisi kiri dan kanan, nilai ketiga untuk sisi bawah.
- Ketika empat nilai ditentukan, nilai pertama berlaku untuk sisi atas, nilai yang kedua untuk sisi kanan, nilai yang ketiga untuk sisi bawah, dan nilai yang keempat untuk sisi kiri. Urutan tersebut berdasarkan arah jarum jam (clockwise).

### Border Style

Kita bisa menetapkan tipe border dengan menggunakan properti border-style. Berikut nilai - nilai yang dapat digunakan pada properti ini:

| Nilai Properti | Penjelasan |
| -------------- | ---------- |
| Solid | Tipe garis padat (tidak terputus - putus) |
| dotted | Garis yang dibentuk dari serangkaian titik-titik (jika ketebalan garis 2px, maka titik-titik akan berukuran 2px dan memiliki jarak 2px antar titiknya). |
| dashed | Garis yang dibentuk dari serangkaian garis pendek. |
| double | Garis yang dibentuk dari dua buah garis padat. |
| groove | Tipe garis yang berbentuk seperti frame |
| hidden | Digunakan untuk menyembunyikan garis pada elemen. |

Untuk lebih jelas mengenai macam-macam CSS Border Style bisa di klik tautan berikut ini : [CSS Border Style](https://www.w3schools.com/css/css_border.asp)

Kita juga bisa menetapkan tipe garis secara individual pada sisi elemen dengan menggunakan empat properti terpisah. Contohnya seperti ini:

```css
.box {
   border-top-style: solid;
   border-right-style: dotted;
   border-bottom-style: groove;
   border-left-style: double;
 
   border-width: 4px;
   border-color: red;
   width: 200px;
   height: 50px;
}
```

### Border Color

Properti terakhir adalah `border-color`. Properti ini digunakan untuk menentukan warna pada garis dengan menggunakan nilai RGB, Hex, atau nama warna pada CSS.

```css
/* menggunakan rgb format */
border-color: rgb(80, 138, 212);
 
/* menggunakan format hex */
border-color: #4ee717;
 
/* menggunakan nama warna */
border-color: red;
```

Sama seperti properti border yang lain, kita dapat menentukan warna pada individual sisi pada elemen dengan menggunakan properti yang terpisah.

```css
border-top-color: #919191;
border-right-color: #111111;
border-bottom-color: #4ee717;
border-left-color: #00c8eb;
```

Tetapi kita juga dapat menetapkan nilai keempatnya sekaligus dalam satu properti seperti ini:

```css
border-color: #919191 #111111 #4ee717 #00c8eb;
```

### Shorthand

Untuk menerapkan border pada elemen kita harus mendefinisikan seluruh properti border yang ada. Dimulai dari menetapkan ketebalan (`border-width`), tipe (`border-style`), dan warna (`border-color`). Jika kita lupa menetapkan salah satu properti tersebut, maka garis tidak akan nampak pada elemen.

Dengan begitu tentu untuk menetapkan border pada elemen, kita perlu menuliskan properti yang banyak bukan? Ya memang, tetapi CSS menyediakan jalan pintas (*shorthand*) untuk membuat border dengan satu properti saja. Properti `border` memiliki tiga buah nilai yang digunakan untuk menentukan ketebalan, tipe dan warna pada border. Berikut contoh penerapannya:

```css
.box {
   border: 4px dashed #00a2c6;
   width: 200px;
}
```

Perlu kita perhatikan bahwa penulisan urutan harus benar. Nilai pertama digunakan untuk ketebalan, yang kedua untuk tipe, dan yang ketiga untuk warna garis.

```css
div { border: width style color }
```

