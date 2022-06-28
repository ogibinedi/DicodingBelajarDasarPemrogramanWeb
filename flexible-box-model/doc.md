## Flexible Box Model

Berikut beberapa konsep dari flexbox yang perlu kita ketahui:

- Dapat mengubah ukuran dimensi elemen dengan menyesuaikan ukuran yang cocok bagi ruang kosong yang ada pada container-nya.
- Flexbox *is directional agnostic*. ini berbeda dengan konsep block model di mana elemen selalu ditampilkan secara vertikal dengan membuat baris baru. Ini berbeda pula dengan konsep *inline* model di mana elemen selalu ditampilkan secara *horizontal*. Dengan flexbox kita dapat melakukan kedua hal tersebut dengan mudah.
- Dibuat untuk menyusun layout yang mobile friendly.

### Flex Container

Secara default deretan flex-item pada container ditampilkan secara horizontal. Ketika menggunakan flex, kita tidak perlu mengatur dimensi dari tiap flex item secara manual untuk mengisi ruang kosong pada container. Sebelum ada flexbox, hal ini jadi kendala umum. Alih-alih, kita harus melakukan perhitungan yang tepat agar tak terjadi overflow pada layout yang ditampilkan.

Untuk membuat sebuah flex container kita gunakan properti **display** dengan nilai **flex**. Dengan demikian seluruh anak dari container tersebut akan menjadi flex item.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex Container</title>
    <style>
        .container {
            display: flex;

            /* properti lainnya */
            width: 800px;
            height: 250px;
            background-color: #11C5C6;
            border: 2px solid black;
            padding: 20px;
            border-radius: 10px;
            margin: 0 auto;
        }

        .box {
            flex-grow: 1;

            /* properti lainnya */
            background-color: #FBDD1C;
            margin: 5px;
            border: 2px solid black;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Flex Container -->
        <div class="box">
            <!-- Flex Item -->
            <p style="font-size: 18px; text-align:center;">Flex item</p>
        </div>
        <div class="box">
            <!-- Flex Item -->
            <p style="font-size: 18px; text-align:center;">Flex item</p>
        </div>
        <div class="box">
            <!-- Flex Item -->
            <p style="font-size: 18px; text-align:center;">Flex item</p>
        </div>
    </div>
</body>
</html>
```

