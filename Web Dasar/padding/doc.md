## Padding

Padding merupakan jarak antara area konten dan border. Padding banyak diterapkan pada elemen jika elemen tersebut menerapkan warna latar atau pun border. Padding memberikan sedikit ruang sehingga konten di dalam elemen dapat lebih nyaman untuk ditampilkan. Contohnya:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Padding</title>
    <style>
        p {
            border: 4px solid #00a2c6;
            width: 275px;
        }

        p.example {
            padding: 10px;
        }
    </style>
</head>
<body>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsa mollitia quo corrupti laboriosam natus ducimus illum laudantium similique, labore quae ut laborum autem, obcaecati eius eaque sapiente, earum commodi vero!</p>
    <p class="example">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione modi eaque nemo impedit, deleniti reiciendis repellat incidunt quasi doloribus ex perspiciatis provident alias similique, tempore est corrupti, quia eveniet quam.</p>
</body>
</html>
```

Pixel merupakan satuan yang sering digunakan dalam menetapkan nilai properti ini (meskipun kita bisa juga menggunakan persentase atau ems). Jika menetapkan menggunakan persentase, maka nilai akan menjadi relatif pada elemen induk atau jendela browser (jika tidak memiliki induk elemen).

Kita dapat menentukan nilai padding yang berbeda untuk masing-masing sisi elemen dengan menggunakan:

```css
padding-top: 10px;
padding-right: 15px;
padding-bottom: 10px;
padding-left: 15px;
```

Kita bisa menggunakan shorthand seperti dibawah :

```css
padding: 10px 15px 10px 15px;
```