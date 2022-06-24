## Text dan Background Color

Implementasi mengganti warna dibagi kedalam dua bagian yaitu :

### Foreground Color ( Pewarnaan Pada Teks)

Nilai dari properti color dapat berupa *predefined color name* atau sebuah *numeric value* dengan menggunakan RGB, RGBA, HEX, HSL, ataupun HSLA. Berikut sebagai contoh, seluruh elemen `<p>` akan diberi warna abu-abu (gray) dengan menggunakan beberapa cara yang ada:

```css
p { color: gray; }
p { color: #666666; }
p { color: #666; }
p { color: rgb(102,102,102); }
```

>**Catatan**: Terdapat dua cara dalam penetapan nilai color menggunakan format **hexadecimal**, yaitu dengan menyebutkan digit hexadecimal secara lengkap (6 digit) dan menyebutkan tiga digit (paling sedikit) hexadecimal. Pada contoh diatas, nilai #666666 dan #666 memiliki hasil yang sama. Artinya setiap digit dari #666 akan melakukan duplikasi dari digit pertama ke digit kedua, digit ketiga ke digit keempat dan digit kelima ke digit keenam, sesuai urutan pendefinisiannya.

Properti `color` dapat diaplikasikan ke seluruh elemen yang ada pada HTML dan nilainya dapat diturunkan pada elemen turunannya. Jadi kita bisa mengubah warna teks pada seluruh dokumen HTML dengan menerapkan properti `color` pada elemen` <body>`, seperti ini:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Foreground Color</title>
    <style>
        body {
            color: steelblue; /* warna ini akan berlaku terhadap elemen yang ada dalam elemen body*/
        }
    </style>
</head>
<body>
<h1>Bandung</h1>
<P>Kota metropolitan terbesar di Provinsi Jawa Barat, sekaligus menjadi ibu kota provinsi tersebut.</p>
 
 
<h2>Sejarah</h2>
<p>Kata Bandung berasal dari kata bendung atau bendungan karena terbendungnya sungai Citarum oleh lava Gunung Tangkuban Parahu yang lalu membentuk telaga. Legenda yang diceritakan oleh orang-orang tua di Bandung mengatakan bahwa nama Bandung diambil dari sebuah kendaraan air yang terdiri dari dua perahu yang diikat berdampingan yang disebut perahu bandung yang digunakan oleh Bupati Bandung, R.A. Wiranatakusumah II, untuk melayari Ci Tarum dalam mencari tempat kedudukan kabupaten yang baru untuk menggantikan ibu kota yang lama di Dayeuhkolot.</p>
 
 
<p>Berdasarkan filosofi Sunda, kata Bandung juga berasal dari kalimat Nga-Bandung-an Banda Indung, yang merupakan kalimat sakral dan luhur karena mengandung nilai ajaran Sunda. Nga-Bandung-an artinya menyaksikan atau bersaksi. Banda adalah segala sesuatu yang berada di alam hidup yaitu di bumi dan atmosfer, baik makhluk hidup maupun benda mati. Sinonim dari banda adalah harta. Indung berarti Ibu atau Bumi, disebut juga sebagai Ibu Pertiwi tempat Banda berada.</p>
 
 
<h2>Geografis</h2>
<p>Kota Bandung dikelilingi oleh pegunungan, sehingga bentuk morfologi wilayahnya bagaikan sebuah mangkok raksasa, secara geografis kota ini terletak di tengah-tengah provinsi Jawa Barat, serta berada pada ketinggian ±768 m di atas permukaan laut, dengan titik tertinggi di berada di sebelah utara dengan ketinggian 1.050 meter di atas permukaan laut dan sebelah selatan merupakan kawasan rendah dengan ketinggian 675 meter di atas permukaan laut.</p>
 
 
<p>Kota Bandung dialiri dua sungai utama, yaitu Sungai Cikapundung dan Sungai Citarum beserta anak-anak sungainya yang pada umumnya mengalir ke arah selatan dan bertemu di Sungai Citarum. Dengan kondisi yang demikian, Bandung selatan sangat rentan terhadap masalah banjir terutama pada musim hujan.</p>
 
 
<h2>Wisata</h2>
<p>Sejak dibukanya Jalan Tol Cipularang, kota Bandung telah menjadi tujuan utama dalam menikmati liburan akhir pekan terutama dari masyarakat yang berasal dari Jakarta sekitarnya. Selain menjadi kota wisata belanja, kota Bandung juga dikenal dengan sejumlah besar bangunan lama berarsitektur peninggalan Belanda.</p>
 
 
<h3>Farm House Lembang</h3>
<p>Berada di jalur utama Bandung-Lembang, Farm House menjadi objek wisata yang tidak pernah sepi pengunjung. Selain karena letaknya strategis, kawasan ini juga menghadirkan nuansa wisata khas Eropa. Semua itu diterapkan dalam bentuk spot swafoto Instagramable.</p>
 
 
<h3>Observatorium Bosscha</h3>
<p>Memiliki beberapa teleskop, antara lain, Refraktor Ganda Zeiss, Schmidt Bimasakti, Refraktor Bamberg, Cassegrain GOTO, dan Teleskop Surya. Refraktor Ganda Zeiss adalah jenis teleskop terbesar untuk meneropong bintang. Benda ini diletakkan pada atap kubah sehingga saat teropong digunakan, atap tersebut harus dibuka. Observatorium Bosscha boleh dikunjungi oleh siapa pun, tanpa tiket. Namun, bagi yang ingin menggunakan teleskop Zeiss, wajib mendaftarkan diri. Untuk instansi atau lembaga pendidikan, diberikan jadwal hari Selasa sampai Jumat. Sementara itu, kunjungan individu dibuka setiap hari Sabtu.</p>
</body>
</html>

```

### Background Color

CSS memperlakukan setiap elemen HTML seperti berada pada sebuah kotak (kita akan mempelajari ini pada pembahasan *box model*). Properti `background-color` dapat mengatur warna latar belakang dari kotak tersebut. 

Sama seperti text color, kita dapat menspesifikasikan warna yang dipilih dengan numeric values atau dengan predefined color name. Properti `background-color` akan bernilai transparan jika tidak kita tetapkan (default).

Kebanyakan browser menetapkan nilai putih sebagai standar untuk nilai `background-color`, tetapi nilai standar tersebut dapat pengguna ubah menggunakan pemilihan mode cerah atau mode gelap pada pengaturan browser-nya. Maka untuk memastikan website kita memiliki tampilan background color putih, kita dapat terapkan nilai `background-color: white;` pada elemen `<body>`.

Biasanya kita juga menerapkan `padding` saat menetapkan `background-color` guna memberi jarak antara konten dan tepi kotak elemen.


