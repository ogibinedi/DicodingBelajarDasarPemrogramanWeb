## Display Roles  (Properti `display`)

Display roles dibagi kedalam dua bagian yaitu:

1. inline element
2. block element

### inline element:

- Elemen HTML yang secara default tidak menambahkan baris baru ketika dibuat.
- Nilai lebar dan tinggi elemen inline sebesar konten di dalamnya, dan tidak dapat diubah.
- Margin dan padding hanya mempengaruhi elemen secara horizontal, tidak vertikal.

### block element:

- Elemen HTML secara default menambahkan baris baru ketika dibuat.
- Jika tidak diatur lebarnya, lebar dari elemen block akan memenuhi lebar dari browser atau elemen yang menaunginya.
- Kita dapat mengatur dimensi dari elemen block.
- Di dalam elemen block, kita dapat menyimpan tag elemen HTML lainnya.

Nilai dari properti `display` diantaranya :

- inline : digunakan untuk mengubah elemen block berperilaku seperti elemen inline.
- block : digunakan untuk mengubah elemen inline berperilaku seperti elemen block.
- inline-block : membuat elemen block tidak menambahkan baris baru ketika dibuat, namun tetap mempertahankan sifat lain dari elemen block.
- none : digunakan untuk menyembunyikan elemen dari halaman.

Properti `display` banyak digunakan dalam kasus pembuatan navigasi. Navigasi biasanya menggunakan element list yang sifatnya block yang selalu ditampilkan dalam baris baru. Dengan menggunakan properti `display` list tersebut bisa diubah kedalam bentuk horizontal (inline).

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Display Roles</title>
    <style>
        li {
            display: inline;

            margin-left: 5px;
        }
    </style>
</head>
<body>
    <ul>
        <li>Home</li>
        <li>Product</li>
        <li>About</li>
        <li>Contact</li>
    </ul>
</body>
</html>
```
