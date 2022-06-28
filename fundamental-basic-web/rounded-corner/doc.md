## Rounded Corner

CSS3 memperkenalkan kemampuan untuk membuat rounded corner atau sudut bundar pada box dengan menggunakan properti `border-radius`. Nilai dari properti ini merupakan tingkat lengkungan border dalam pixel.

```css
rounded {
    border-radius: 5px;
}
```

Kita bisa menetapkan nilai pada individu siku kotak dengan menggunakan properti yang terpisah, seperti ini:

```css
rounded {
    border-top-right-radius: 5px;
    border-bottom-right-radius: 10px;
    border-bottom-left-radius: 5px;
    border-top-left-radius: 10px;
}
```

Shorthand inline, menempatkan ke empat nilai dalam satu properti

```css
    border-radius: 10px 5px 10px 5px;
```