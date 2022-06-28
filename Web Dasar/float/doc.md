## Floating

Sederhananya properti float dapat membuat elemen berada pada sebelah kanan atau kiri. Saat diterapkan pada elemen inline, properti float juga memungkinkan elemen di sekitarnya mengelilingi elemen tersebut (wrap). 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Floating</title>
    <style>
        .container {
            width: 800px;
            border: 4px solid #000;
            padding: 10px;
        }

        img {
            float: left;
            margin: 10px;
        }

        
    </style>
</head>
<body>
    <div class="container">
        <img src="https://i.imgur.com/cs2BJzw.jpg" width="200px" alt="dicoding">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis dolor odio incidunt inventore distinctio necessitatibus neque architecto, doloremque quod, reprehenderit quam deleniti aperiam sunt! Enim quaerat porro laboriosam sequi sunt.</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, repellendus quos. Perferendis numquam eligendi consequatur labore iure est! Vero dolorem facere ratione fugit labore dolor nam maxime ducimus fugiat officiis?</p>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque totam, alias quidem fuga accusantium odio voluptate consectetur dicta, perspiciatis distinctio magni rerum earum. Libero corporis temporibus soluta vero molestiae vel!. Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam a, vitae consequuntur necessitatibus fuga maiores velit maxime quasi optio. Nihil, animi modi sint cum mollitia eveniet perferendis quae delectus ipsum.</p>
    </div>
</body>
</html>
```

### Penerapan Floating Pada Layout Halaman Web

Teknik floating ini masih banyak digunakan dikarenakan kemudahannya dalam membuat multiple layout pada halaman web, berikut code htmlnya:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Floating</title>
    <style>
        * {
           /* digunakan untuk menghapus seluruh padding dan margin standar yang diberikan browser pada elemen */
           margin: 0;
           padding: 0;
 
           /* Menggunakan border-box dalam perhitungan dimensi box-nya */
           box-sizing: border-box;
       }

       .container {
           width: 800px;
           height: 400px;
           border: 1px solid black;
           margin: 0 auto;
       }
 
       .left-content {
           text-align: center;
           line-height: 400px;
           width: 30%;
           height: 100%;
           background-color: #00c7ed;
 
           /* digunakan untuk memindahkan posisi elemen ke sisi kiri container */
           float: left;
       }
 
       .right-content {
           text-align: center;
           line-height: 400px;
           width: 70%;
           height: 100%;
           background-color: #60d0a8;
 
           /* digunakan untuk memindahkan posisi elemen ke sisi kanan container */
           float: right;
       }
    </style>
</head>
<body>
    <div class="container">
        <div class="left-content">
            <h3>Left Content</h3>
        </div>
        <div class="right-content">
            <h3>Right Content</h3>
        </div>
    </div>
</body>
</html>
```

