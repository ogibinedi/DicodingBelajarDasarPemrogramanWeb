## JavaScript

JavaScript merupakan bahasa pemrograman client-side sehingga seluruh prosesnya berjalan pada sisi pengguna bukan server. JavaScript diperlukan pada pengembangan website ketika kita membutuhkan suatu interaksi dari pengguna. Sesungguhnya website hanya menampilkan konten yang statis jika hanya menggunakan HTML dan CSS.

Karena diolah pada sisi client, JavaScript sangat bergantung pada pengaturan dan kemampuan browser ketika melakukan sebuah proses (compiling atau rendering pada DOM). Bahkan pengguna dapat sepenuhnya tidak mengizinkan JavaScript berjalan pada browser dengan menonaktifkan dukungan JavaScript pada browser.

Sama seperti styling, untuk menggunakan JavaScript pada website kita bisa menerapkannya melalui atribut HTML, embed script, atau menggunakan file external.

### Atribut HTML

Untuk menuliskan JavaScript menggunakan atribut, kita bisa menerapkannya pada atribut event seperti “onclick”, sehingga JavaScript akan dieksekusi ketika elemen tersebut ditekan oleh kursor. Contohnya sebagai berikut:

```html
<button onclick="alert('Anda menekan elemen button')">Click disini!</button>
```

Ada banyak sekali atribut event yang dapat digunakan untuk menuliskan script di dalamnya. Kita bisa lihat apa saja atributnya pada tautan berikut: [Event Attribut](https://www.w3schools.com/tags/ref_eventattributes.asp)

Tentunya atribut tersebut kita gunakan sesuai dengan kebutuhan kita. `onclick` merupakan salah satu atribut yang common atau banyak digunakan karena interaksi tersebut sering pengguna lakukan.

### Embeded Script

JavaScript juga dapat dituliskan dengan menanamnya (embedding) pada berkas HTML dengan menggunakan elemen `<script>`.

```html
<script>
    // JavaScript dituliskan disini.
</script>
```

Elemen `<script>` dapat diletakan di dalam elemen `<head>` atau `<body>`. Akan tetapi jika kita menerapkan banyak script pada elemen `<head>` proses memuat halaman akan menjadi lambat, karena HTML akan membaca kode dari atas ke bawah.

### External Script

Metode lainnya yaitu dengan menggunakan berkas external yang berekstensi **.js**. Di dalam berkas tersebutlah seluruh JavaScript dituliskan. Keuntungan menggunakan metode ini adalah script dapat diterapkan pada berbagai berkas HTML tanpa menuliskan ulang scriptnya (keuntungan yang sama juga ketika kita menggunakan external css).

Untuk menghubungkan external script dengan berkas HTML, kita gunakan elemen `<script>` lalu tambahkan atribut `src` dengan nilai alamat berkas **.js** yang digunakan.

```html
<script src="berkas-javascript.js"></script>
```

Sama seperti Embedded Script, kita bisa tuliskan tag `<script>` tersebut di dalam elemen `<head>`. Namun, direkomendasikan untuk disimpan di dalam elemen `<body>` sebelum tag penutup `</body>`.

### Console Log

Script yang kita tuliskan sebelumnya berfungsi untuk menampilkan sebuah data baik itu teks (string) atau variabel, objek, fungsi dsb. Pada console website  console.log() biasanya digunakan sebagai sarana debugging sederhana untuk mengetahui nilai dari suatu variabel.

### Statement

Sebuah *script* dibangun dari serangkaian *statement*. *Statement* merupakan sebuah perintah yang bertujuan untuk memberitahu apa yang harus dilakukan browser. Contohnya kode berikut merupakan *statement* yang menyatakan bahwa browser harus menampilkan pesan (*alert*) dengan kalimat “Terima kasih”.

```javascript
alert("Terimakasih");
```

