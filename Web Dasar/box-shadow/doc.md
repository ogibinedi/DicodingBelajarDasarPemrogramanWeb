## Box Shadow

Pada materi *formatting* text kita sudah belajar cara menambahkan *drop shadow* pada teks. Pada CSS3 kita juga dapat menambahkan *drop shadow* di sekitar kotak elemen (tidak termasuk ma*rgin) dengan menggunakan properti `box-shadow`.

Nilai dan cara kerja dari properti `box-shadow` mirip seperti `text-shadow`, yaitu nilainya menentukan jarak vertikal dan horizontal, tingkat keburaman, dan warna pada bayangan. Pada *box shadow*, kita juga dapat menentukan tingkat sebaran (spread) bayangan. Semakin besar  nilai, bayangan yang nampak akan semakin luas. Berikut contoh penerapan *box shadow* pada CSS:

```css
box-shadow: 6px 6px 5px 10px #666;
```

Berikut penjelasan tiap-tiap nilai dari propertinya:

- Nilai pertama : menunjukkan seberapa jauh ke kiri atau kanan (horizontal) bayangan harus ditampakkan.
- Nilai kedua : menunjukkan jarak ke atas atau ke bawah (vertical) bayangan harus ditampakkan. 
- Nilai Ketiga (opsional) : menentukan tingkat keburaman yang harus diterapkan pada bayangan.
- Nilai Keempat (opsional) : menentukan tingkat sebaran (spread) bayangan. Semakin besar nilai yang ditentukan, bayangan yang nampak pun semakin luas.
- Nilai Kelima : menentukan warna yang digunakan pada bayangan.