# Praktikum 3: CSS Dasar

## Identitas

**Nama:** maulana akbar
**NIM:** 312510381
**Kelas:** I251D 
**Mata Kuliah:** Pemrograman Web

---

## Deskripsi

Praktikum 3 membahas dasar-dasar CSS (Cascading Style Sheets) yang digunakan untuk mengatur tampilan dan struktur halaman web. Pada praktikum ini dipelajari penggunaan CSS Internal, Inline, dan External, serta penggunaan ID Selector dan Class Selector.

---

## Tujuan Praktikum

1. Memahami konsep dasar CSS.
2. Memahami aturan penulisan CSS.
3. Memahami penggunaan selector sebagai pengontrol CSS.
4. Membuat pengaturan CSS pada HTML.

---

## Langkah 1 — Membuat Dokumen HTML

Pada langkah pertama dibuat sebuah file HTML dengan nama `lab2_css_dasar.html`.

Dokumen HTML berisi struktur dasar HTML, header, navigation, heading, paragraf, serta tombol menggunakan class dan ID.

Contoh struktur yang digunakan:


<img width="813" height="977" alt="Screenshot 2026-10-08 104613" src="https://github.com/user-attachments/assets/82a015cc-1784-40bc-ac32-1fcf1a2374da" />
<img width="445" height="936" alt="Screenshot 2026-10-08 104729" src="https://github.com/user-attachments/assets/1b0a5b5b-97b9-4ff6-873a-2ca44c221ccc" />


---

## Langkah 2 — Menambahkan CSS Internal

Pada langkah kedua ditambahkan CSS Internal menggunakan tag `<style>` pada bagian `<head>`.

CSS digunakan untuk mengatur jenis font, ukuran heading, warna teks, serta tampilan header.

Contoh:

```css
body {
    font-family: 'Open Sans', sans-serif;
}

header {
    min-height: 80px;
    border-bottom: 1px solid #77CCEF;
}

h1 {
    font-size: 24px;
    color: #0F189F;
    text-align: center;
    padding: 20px 10px;
}

h1 i {
    color: #6d6a6b;
}
```

### Screenshot

<img width="445" height="936" alt="Screenshot 2026-10-08 104729" src="https://github.com/user-attachments/assets/82d0f1eb-297c-4b70-ba48-0b5d35aa728d" />




---

## Langkah 3 — Menambahkan Inline CSS

Pada langkah ketiga ditambahkan Inline CSS secara langsung pada tag `<p>`.

Contoh:

```html
<p style="text-align: center; color: brown;">
    Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
    <b>Pemrograman Web</b> di
    <i>Universitas Pelita Bangsa</i>.
</p>
```

Inline CSS digunakan untuk mengatur paragraf agar berada di tengah dan memiliki warna cokelat.

### Screenshot

<img width="610" height="237" alt="Screenshot 2026-10-08 104234" src="https://github.com/user-attachments/assets/dda39391-40e7-490f-822f-020a17d309bd" />


---

## Langkah 4 — Membuat CSS Eksternal

Pada langkah keempat dibuat file CSS baru dengan nama:

`style_eksternal.css`

CSS eksternal digunakan untuk memisahkan kode CSS dari dokumen HTML.

File CSS kemudian dihubungkan dengan HTML menggunakan tag:

```html
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```

CSS eksternal digunakan untuk mengatur tampilan navigation dan link.

### Screenshot

<img width="596" height="122" alt="image" src="https://github.com/user-attachments/assets/73ded269-78ec-4e00-85c9-f440a9433532" />
dengan struktur folder dan file 
<img width="293" height="72" alt="Screenshot 2026-10-08 104151" src="https://github.com/user-attachments/assets/89961b83-9efb-40d0-89f5-c3c5f33d8a4c" />
<img width="323" height="92" alt="image" src="https://github.com/user-attachments/assets/1b266d76-c40f-4bfe-adab-7976ac76b590" />


---

## Langkah 5 — Menambahkan CSS Selector

Pada langkah kelima digunakan **ID Selector** dan **Class Selector**.

### ID Selector

```css
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}

#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
```

### Class Selector

```css
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}

.btn-primary {
    background: #E42A42;
}
```

ID Selector digunakan dengan tanda `#`, sedangkan Class Selector menggunakan tanda `.`.

### Screenshot

<img width="293" height="72" alt="Screenshot 2026-10-08 104151" src="https://github.com/user-attachments/assets/07ef26f6-1756-493c-9a0e-6b827032cefc" />


---

# Eksperimen dan Pertanyaan

## 1. Eksperimen CSS

Pada eksperimen dilakukan perubahan dan penambahan beberapa properti CSS, seperti `border-radius`, `font-size`, `padding`, `background`, dan `:hover`.

Contoh:

```css
#intro {
    border-radius: 10px;
    padding: 20px;
}

.btn-primary:hover {
    background: #a7192d;
}
```

Perubahan tersebut digunakan untuk melihat pengaruh properti CSS terhadap tampilan halaman web.

### Screenshot

<img width="372" height="282" alt="kodingan nav1" src="https://github.com/user-attachments/assets/e9c3bb22-fa36-4ef4-94f0-0aa28bfa1b24" />
hasil nya
<img width="1917" height="415" alt="hasil nav1" src="https://github.com/user-attachments/assets/366ca623-20f3-4c1f-955e-38d6a06d91f8" />



---

## 2. Perbedaan `h1` dan `#intro h1`

`h1 { ... }` merupakan **element selector** yang akan diterapkan pada semua elemen `<h1>`.

Sedangkan `#intro h1 { ... }` digunakan untuk memberikan CSS pada elemen `<h1>` yang berada di dalam elemen yang memiliki `id="intro"`.

Contoh:

```css
h1 {
    color: blue;
}

#intro h1 {
    color: white;
}
```

Dengan demikian, selector `h1` memiliki cakupan yang lebih umum, sedangkan `#intro h1` lebih spesifik.

---

## 3. Prioritas CSS Internal, Eksternal, dan Inline

Jika terdapat CSS Internal, CSS Eksternal, dan Inline CSS yang mengatur elemen yang sama, maka **Inline CSS memiliki prioritas lebih tinggi**.

Contoh:

```css
p {
    color: blue;
}
```

Kemudian pada HTML:

```html
<p style="color: brown;">
    Belajar CSS
</p>
```

Hasilnya teks akan berwarna cokelat karena aturan Inline CSS memiliki prioritas lebih tinggi.

---

## 4. Prioritas ID dan Class Selector

Jika sebuah elemen memiliki ID dan Class, kemudian keduanya memiliki deklarasi CSS untuk properti yang sama, maka **ID Selector memiliki prioritas lebih tinggi daripada Class Selector**.

Contoh:

```html
<p id="paragraf-1" class="text-paragraf">
    Belajar CSS
</p>
```

```css
#paragraf-1 {
    color: red;
}

.text-paragraf {
    color: blue;
}
```

Hasilnya teks akan berwarna merah karena ID Selector memiliki prioritas lebih tinggi daripada Class Selector.

---

## Kesimpulan

Pada Praktikum 3 ini telah dipelajari dasar-dasar CSS, mulai dari CSS Internal, Inline, dan External hingga penggunaan ID Selector dan Class Selector. Selain itu, dilakukan eksperimen terhadap beberapa properti CSS serta dipelajari perbedaan prioritas selector dalam menentukan tampilan halaman web.

---

## Repository

Repository ini dibuat untuk memenuhi laporan Praktikum 3 Pemrograman Web.

**Nama Repository:** `Lab3Web`
