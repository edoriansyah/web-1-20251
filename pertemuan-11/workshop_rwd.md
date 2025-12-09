# Workshop Praktikum Responsive Web Design

# 🧪 **Sesi 1 – Viewport & Dasar Responsive**

## **Task 1 – Menambahkan Viewport**

**Keterangan:**  
Mahasiswa memahami pentingnya viewport untuk membuat halaman web tampil responsif di perangkat mobile. Hal ini memungkinkan layout menyesuaikan ukuran layar.

### ✔ Code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Viewport Example</title>
  </head>
  <body>
    <h1>Halaman dengan Viewport Responsif</h1>
    <p>Resize browser untuk melihat perbedaan.</p>
  </body>
</html>
```

---

## **Task 2 – Ukuran Elemen Fleksibel**

**Keterangan:**  
Mahasiswa membuat elemen HTML yang fleksibel dengan menggunakan unit persentase sehingga tidak menimbulkan horizontal scrolling.

### ✔ Code

```html
<style>
  .container {
    width: 100%;
  }
  .box {
    background: lightblue;
    padding: 20px;
    margin: 10px 0;
    width: 100%;
  }
</style>

<div class="container">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>
```

---

# 🧪 **Sesi 2 – Flexible Layout dengan Flexbox**

## **Task 3 – Layout Flex Responsif**

**Keterangan:**  
Mahasiswa menerapkan Flexbox yang berubah sesuai breakpoints: 1 kolom (mobile), 2 kolom (tablet), 3 kolom (desktop).

### ✔ Code

```html
<style>
  .flex-container {
    display: flex;
    flex-wrap: wrap;
  }
  .item {
    flex: 1 1 100%;
    padding: 20px;
    margin: 5px;
    background: lightgreen;
  }

  @media (min-width: 600px) {
    .item {
      flex: 1 1 45%;
    }
  }

  @media (min-width: 992px) {
    .item {
      flex: 1 1 30%;
    }
  }
</style>

<div class="flex-container">
  <div class="item">Box 1</div>
  <div class="item">Box 2</div>
  <div class="item">Box 3</div>
</div>
```

---

# 🧪 **Sesi 3 – Responsive Layout dengan CSS Grid**

## **Task 4 – Grid 12 Kolom**

**Keterangan:**  
Mahasiswa belajar membuat layout berbasis grid dengan 12 kolom menggunakan CSS Grid.

### ✔ Code

```html
<style>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: 10px;
  }
  .box1 {
    grid-column: span 12;
    background: #a2d2ff;
    padding: 20px;
  }
  .box2 {
    grid-column: span 6;
    background: #bde0fe;
    padding: 20px;
  }
  .box3 {
    grid-column: span 3;
    background: #caffbf;
    padding: 20px;
  }
  .box4 {
    grid-column: span 3;
    background: #ffd6a5;
    padding: 20px;
  }
</style>

<div class="grid-container">
  <div class="box1">Box 1</div>
  <div class="box2">Box 2</div>
  <div class="box3">Box 3</div>
  <div class="box4">Box 4</div>
</div>
```

---

## **Task 5 – Grid Responsif dengan Breakpoints**

**Keterangan:**  
Mahasiswa membuat grid yang berubah sesuai ukuran layar (mobile, tablet, desktop).

### ✔ Code

```html
<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: 10px;
  }
  .grid > div {
    background: #f8c4b4;
    padding: 20px;
  }

  @media (max-width: 600px) {
    .grid > div {
      grid-column: span 12;
    }
  }

  @media (min-width: 600px) and (max-width: 992px) {
    .item-large {
      grid-column: span 12;
    }
    .item-medium {
      grid-column: span 6;
    }
  }

  @media (min-width: 992px) {
    .item-large {
      grid-column: span 12;
    }
    .item-medium {
      grid-column: span 6;
    }
    .item-small {
      grid-column: span 3;
    }
  }
</style>
```

---

# 🧪 **Sesi 4 – Media Queries**

## **Task 6 – Warna Berdasarkan Ukuran Layar**

**Keterangan:**  
Mahasiswa belajar membuat breakpoints sederhana menggunakan media query.

### ✔ Code

```html
<style>
  body {
    background: lightblue;
  }

  @media (min-width: 600px) {
    body {
      background: lightgreen;
    }
  }

  @media (min-width: 900px) {
    body {
      background: lightyellow;
    }
  }
</style>
```

---

## **Task 7 – Orientation Query**

**Keterangan:**  
Mahasiswa memahami media query berdasarkan orientasi layar (portrait/landscape).

### ✔ Code

```html
<style>
  body {
    text-align: center;
  }

  @media (orientation: landscape) {
    body {
      text-align: left;
    }
  }
</style>
```

---

# 🧪 **Sesi 5 – Responsive Images**

## **Task 8 – Gambar Responsif**

**Keterangan:**  
Mahasiswa menggunakan `max-width` dan `height: auto` agar gambar menyesuaikan ukuran layar.

### ✔ Code

```html
<img
  src="big-image.jpg"
  alt="Responsive Image"
  style="max-width: 100%; height: auto;"
/>
```

---

## **Task 9 – Tag `<picture>`**

**Keterangan:**  
Mahasiswa menerapkan teknik memilih gambar berbeda sesuai ukuran layar.

### ✔ Code

```html
<picture>
  <source media="(max-width: 600px)" srcset="img-small.jpg" />
  <source media="(min-width: 601px)" srcset="img-large.jpg" />
  <img src="img-large.jpg" alt="Picture Element Example" style="width:100%;" />
</picture>
```

---

# 🧪 **Sesi 6 – Mini Project RWD (Tanpa Framework)**

## **Task 10 – Website Responsif 1 Halaman**

**Keterangan:**  
Mahasiswa membuat website lengkap dengan header, nav, hero, card, dan footer. Wajib menggunakan media queries.

### ✔ Code

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <style>
      body {
        margin: 0;
        font-family: Arial;
      }
      header,
      footer {
        background: #222;
        color: white;
        padding: 20px;
        text-align: center;
      }
      nav {
        background: #444;
        color: white;
        padding: 10px;
      }
      .hero {
        background: #ddd;
        padding: 50px;
        text-align: center;
      }

      .cards {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        padding: 20px;
      }
      .card {
        background: white;
        padding: 20px;
        flex: 1 1 100%;
      }

      @media (min-width: 600px) {
        .card {
          flex: 1 1 45%;
        }
      }
      @media (min-width: 992px) {
        .card {
          flex: 1 1 30%;
        }
      }
    </style>
  </head>

  <body>
    <header>Header</header>
    <nav>Navigation Menu</nav>
    <div class="hero">Hero Banner</div>

    <section class="cards">
      <div class="card">Card 1</div>
      <div class="card">Card 2</div>
      <div class="card">Card 3</div>
    </section>

    <footer>Footer</footer>
  </body>
</html>
```

---

# 🧪 **Sesi 7 – CSS Framework**

## **Task 11 – Layout Framework (Bootstrap 5)**

**Keterangan:**  
Mahasiswa membuat layout responsif menggunakan komponen Bootstrap.

### ✔ Code

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
/>

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container">
    <a class="navbar-brand" href="#">MySite</a>
  </div>
</nav>

<div class="container my-4">
  <div class="row">
    <div class="col-md-4 mb-3">
      <div class="card p-3">Card 1</div>
    </div>
    <div class="col-md-4 mb-3">
      <div class="card p-3">Card 2</div>
    </div>
    <div class="col-md-4 mb-3">
      <div class="card p-3">Card 3</div>
    </div>
  </div>
</div>

<footer class="bg-dark text-center text-white p-3">Footer</footer>
```
