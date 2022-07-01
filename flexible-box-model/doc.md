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

### Flex Grow

Properti flex-grow ini digunakan untuk memberitahu berapa banyak ukuran yang harus ditetapkan oleh flex-item. **Nilai dari properti ini bukan nilai dari dimensi asli pada flex item, melainkan nilai yang relatif terhadap ruang kosong pada flex container.**

Jika kita menetapkan nilai **flex-grow** yang sama pada seluruh flex item, maka dimensi dari tiap flex item akan sama rata dan memenuhi ruang kosong yang ada pada container. Namun jika kita memberikan nilai yang berbeda dari salah satu item-nya, contohnya nilai yang lebih besar, maka flex item tersebut akan mencakup ukuran yang lebih besar. Flex item yang lain akan menyusut menyesuaikan agar tetap masuk pada ruang flex container.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex Grow</title>
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
            background-color: #FBDD1C;
            margin: 5px;
            border: 2px solid black;
            border-radius: 10px;
        }

        .fisrt {
            flex-grow: 1;
        }

        .second {
            flex-grow: 2;
        }

        .third {
            flex-grow: 1;
        }


    </style>
</head>
<body>
    <div class="container">
        <div class="box first"></div>
        <div class="box second"></div>
        <div class="box third"></div>
    </div>
</body>
</html>
```

Cara kerja flex-grow mirip seperti potongan kue. Ruang kosong pada elemen akan dibagi-bagi sesuai besaran nilainya. Contoh di atas memberi kita gambaran seperti sebuah kue dengan luas total 4, kemudian kue tersebut dipotong menjadi 3 potong. Potongan yang tengah mendapatkan 2 bagian dan potongan yang lainnya masing - masing mendapatkan 1 bagian. Maka potongan yang tengah akan lebih besar dari potongan yang lain.

### Flex Direction

Seperti yang sudah kita ketahui sebelumnya, flexbox merupakan *directional agnostic*, di mana kita dapat mengubah arah munculnya flex-item yang berada di flex container. Secara default deretan flex-item ditampilkan secara **horizontal**, namun kita dapat mengubahnya dengan menetapkan properti **flex-direction** pada *flex container*-nya.