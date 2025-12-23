# Workshop Praktikum Tailwind CSS

**Mata Kuliah:** Pemrograman Web 1  
**Topik:** Utility-First CSS Framework (Tailwind CSS)

---

## Tujuan Pembelajaran

Setelah mengikuti workshop ini, mahasiswa diharapkan mampu:

1. Memahami konsep utility-first pada Tailwind CSS
2. Menggunakan Tailwind CSS melalui Play CDN
3. Menginstal dan mengonfigurasi Tailwind CSS menggunakan Vite
4. Menerapkan styling teks, warna, margin, dan padding
5. Membuat layout menggunakan Flexbox dan Grid
6. Membuat halaman web responsif

---

## Tools & Persiapan

- Node.js (LTS)
- NPM
- Visual Studio Code
- Browser (Chrome / Firefox)
- Ekstensi VS Code: Tailwind CSS IntelliSense (opsional)

---

## Sesi 1 – Pengenalan Tailwind CSS (Play CDN)

> Play CDN digunakan untuk latihan awal dan pengenalan utility class.

### Langkah Praktikum

Buat file `index.html` lalu tuliskan kode berikut:

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <title>Workshop Tailwind CSS</title>
    <script src="https://cdn.tailwindcss.com"></script>
  </head>
  <body class="p-6">
    <h1 class="text-3xl font-bold text-blue-600">Workshop Tailwind CSS</h1>

    <p class="text-gray-700 mt-2">
      Tailwind CSS adalah utility-first CSS framework.
    </p>
  </body>
</html>
```

---

## Sesi 2 – Instalasi Tailwind CSS Menggunakan Vite

> Metode ini direkomendasikan untuk pengembangan proyek modern.

---

### Task 1 – Membuat Project Vite

Jalankan perintah berikut di terminal:

```bash
npm create vite@latest tailwind-vite
```

Pilih:

- Framework: **Vanilla**
- Variant: **JavaScript**

Masuk ke folder project dan install dependency:

```bash
cd tailwind-vite
npm install
```

---

### Task 2 – Install Tailwind CSS

```bash
npm install tailwindcss @tailwindcss/vite
```

---

### Task 3 – Konfigurasi Vite

Buka file `vite.config.js` lalu ubah menjadi:

```js
import { defineConfig } from "vite";
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [tailwindcss()],
});
```

---

### Task 4 – Import Tailwind CSS

Buka file `src/style.css` lalu isi dengan:

```css
@import "tailwindcss";
```

---

### Task 5 – Menggunakan Tailwind di HTML

Edit file `index.html` yang ada pada folder root project:

```html
<body class="bg-slate-100 min-h-screen flex items-center justify-center">
  <div class="bg-white p-6 rounded-xl shadow-lg w-80">
    <h2 class="text-lg font-semibold text-gray-800">Tailwind Card</h2>

    <p class="text-sm text-gray-600 mt-2">
      This card is styled using Tailwind utility classes without writing custom
      CSS.
    </p>

    <button
      class="mt-4 w-full bg-indigo-500 text-white py-2 rounded-lg hover:bg-indigo-600"
    >
      Learn More
    </button>
  </div>
</body>
```

---

### Task 6 – Menjalankan Project

```bash
npm run dev
```

Buka URL yang ditampilkan di browser.

---

## Sesi 3 – Utility-First Structure

Buat file `information-card.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Information Card</title>
  </head>
  <body class="bg-gray-100 flex items-center justify-center min-h-screen">
    <div class="bg-white p-6 rounded-lg shadow-md max-w-md text-center">
      <h1 class="text-2xl font-bold text-gray-800 mb-2">
        Apa Itu Tailwind CSS?
      </h1>
      <p class="text-gray-600">
        Tailwind CSS adalah framework modern berbasis
        <span class="font-semibold">utility-class</span> yang memudahkan kita
        membangun tampilan web dengan cepat dan fleksibel.
      </p>
    </div>
  </body>
</html>
```

---

## Sesi 4 – Text & Font Styling

Buat file `typography.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Typography</title>
  </head>
  <body class="bg-gray-50 p-6">
    <div class="max-w-2xl mx-auto bg-white p-6 rounded-lg shadow">
      <h1 class="text-3xl font-bold text-gray-800 mb-2">
        Belajar Typography di Tailwind
      </h1>
      <p class="text-gray-700 text-base leading-relaxed">
        Dengan menggunakan <span class="font-semibold">utility class</span> dari
        Tailwind CSS, kita dapat mengatur tampilan teks seperti ukuran, warna,
        dan spasi dengan mudah dan cepat.
      </p>
      <p
        class="text-blue-600 font-medium mt-4 underline hover:text-blue-800 transition"
      >
        Ini adalah contoh teks dengan efek hover dan underline.
      </p>
      <p class="text-sm text-gray-500 mt-6 uppercase tracking-wide">
        teks kecil dengan huruf kapital dan spasi huruf lebar
      </p>
    </div>
  </body>
</html>
```

---

## Sesi 5 – Margin & Padding

Buat file `layout-spacing.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Layout Spacing</title>
  </head>
  <body class="bg-gray-100 p-6">
    <div class="max-w-md mx-auto bg-white p-6 rounded-lg shadow-lg">
      <h2 class="text-xl font-bold text-gray-800 mb-4">Judul Kartu</h2>
      <p class="text-gray-700 mb-6">
        Ini adalah contoh kartu sederhana dengan padding di dalam dan margin
        antar elemen yang rapi.
      </p>
      <button
        class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700 transition"
      >
        Klik Saya
      </button>
    </div>
  </body>
</html>
```

---

## Sesi 6 – Colors, Background, dan Border

Buat file `colorful-card.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Colorful Card</title>
  </head>
  <body class="bg-gray-100 p-6">
    <div
      class="max-w-md mx-auto bg-white p-6 rounded-lg shadow-md border border-blue-300"
    >
      <h2 class="text-xl font-bold text-blue-700 mb-2">Judul Kartu</h2>
      <p class="text-gray-700 mb-4">
        Ini adalah kartu dengan warna teks abu-abu, latar putih, dan garis tepi
        biru. Kombinasi warna ini mudah dibuat dengan Tailwind CSS.
      </p>
      <button
        class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-800 transition"
      >
        Klik Saya
      </button>
    </div>
  </body>
</html>
```

---

## Sesi 7 – Flexbox Layout

Buat file `navigation-header.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Navigation Header</title>
  </head>
  <body class="bg-gray-100 p-6">
    <header
      class="flex justify-between items-center bg-white p-4 rounded shadow"
    >
      <h1 class="text-xl font-bold text-blue-600">Logo</h1>
      <nav class="flex gap-4">
        <a href="#" class="text-gray-700 hover:text-blue-500">Beranda</a>
        <a href="#" class="text-gray-700 hover:text-blue-500">Tentang</a>
        <a href="#" class="text-gray-700 hover:text-blue-500">Kontak</a>
      </nav>
    </header>
  </body>
</html>
```

---

## Sesi 8 – Grid Layout

Buat file `grid-gallery.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Grid Gallery</title>
  </head>
  <body class="bg-gray-100 p-6">
    <div class="max-w-4xl mx-auto">
      <h2 class="text-2xl font-bold text-gray-800 mb-4">Galeri Grid</h2>
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <div class="bg-white p-4 rounded shadow">Item 1</div>
        <div class="bg-white p-4 rounded shadow">Item 2</div>
        <div class="bg-white p-4 rounded shadow">Item 3</div>
        <div class="bg-white p-4 rounded shadow">Item 4</div>
        <div class="bg-white p-4 rounded shadow">Item 5</div>
        <div class="bg-white p-4 rounded shadow">Item 6</div>
      </div>
    </div>
  </body>
</html>
```

---

## Sesi 9 – Responsive Design

Buat file `responsive-card-layout.html` pada folder root project:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/src/style.css" rel="stylesheet" />
    <title>Responsive Card</title>
  </head>
  <body class="bg-gray-100 p-6">
    <div class="max-w-4xl mx-auto">
      <h2
        class="text-2xl font-bold text-gray-800 mb-4 text-center sm:text-left"
      >
        Kartu Responsif
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
        <div class="bg-white p-4 rounded shadow">
          <h3 class="text-lg font-semibold mb-2">Item 1</h3>
          <p class="text-gray-600">
            Konten ini akan disusun otomatis sesuai ukuran layar.
          </p>
        </div>
        <div class="bg-white p-4 rounded shadow">
          <h3 class="text-lg font-semibold mb-2">Item 2</h3>
          <p class="text-gray-600">
            Cobalah buka di layar besar untuk melihat perbedaannya.
          </p>
        </div>
        <div class="bg-white p-4 rounded shadow">
          <h3 class="text-lg font-semibold mb-2">Item 3</h3>
          <p class="text-gray-600">Grid akan menyesuaikan dari 1 ke 3 kolom.</p>
        </div>
      </div>
    </div>
  </body>
</html>
```
