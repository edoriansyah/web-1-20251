# Workshop Praktikum

## Membangun Website Kampus dengan HTML, CSS, JavaScript & Bootstrap

### Deskripsi Umum

Workshop ini dirancang untuk mahasiswa yang telah mempelajari dasar HTML, CSS, JavaScript, serta CSS Framework (Bootstrap). Melalui praktikum bertahap, mahasiswa akan membangun sebuah **website kampus sederhana** yang terdiri dari minimal **3 halaman**, responsif, dan interaktif.

### Capaian Pembelajaran

Setelah mengikuti workshop ini, mahasiswa diharapkan mampu:

1. Membuat struktur website multi-halaman menggunakan HTML.
2. Menerapkan Bootstrap untuk layout dan komponen UI.
3. Mengelola navigasi antar halaman.
4. Menambahkan interaksi sederhana menggunakan JavaScript.
5. Menyusun struktur folder project web yang rapi.

---

## Spesifikasi Project

- **Tema**: Website Kampus
- **Teknologi**:
  - HTML5
  - CSS3
  - JavaScript
  - Bootstrap 5
- **Minimal Halaman**:
  1. Halaman Utama (Home)
  2. Halaman Tentang Kampus
  3. Halaman Visi & Misi
  4. (Opsional) Akademik / Fasilitas / Kontak

---

## Struktur Folder Project

```
website-kampus/
├── index.html
├── tentang.html
├── visi-misi.html
├── kontak.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── assets/
    └── images/
```

---

## Tahap 1 – Persiapan Project

**Tujuan**: Menyiapkan struktur awal project.

### Langkah:

1. Buat folder project `website-kampus`.
2. Buat file HTML sesuai struktur.
3. Hubungkan Bootstrap (CDN) pada setiap halaman.
4. Hubungkan file CSS dan JavaScript eksternal.

### Contoh Kode (index.html – kerangka awal)

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Website Kampus</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="css/style.css" />
  </head>
  <body>
    <!-- Konten -->

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
    <script src="js/script.js"></script>
  </body>
</html>
```

---

## Tahap 2 – Membuat Navbar dan Footer

**Tujuan**: Menyediakan navigasi konsisten di semua halaman.

### Contoh Kode Navbar (digunakan di semua halaman)

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container">
    <a class="navbar-brand" href="index.html">KampusKu</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
        <li class="nav-item">
          <a class="nav-link" href="tentang.html">Tentang</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="visi-misi.html">Visi & Misi</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="kontak.html">Kontak</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

### Contoh Kode Footer

```html
<footer class="bg-dark text-white text-center p-3 mt-5">
  <p class="mb-0">© 2025 KampusKu. All Rights Reserved.</p>
</footer>
```

---

## Tahap 3 – Halaman Utama (Home)

**Tujuan**: Menampilkan gambaran umum kampus.

### Contoh Kode Konten Home

```html
<header class="bg-light p-5 text-center">
  <h1>Selamat Datang di KampusKu</h1>
  <p>Kampus Unggul, Inovatif, dan Berdaya Saing</p>
  <a href="tentang.html" class="btn btn-primary">Selengkapnya</a>
</header>

<section class="container my-5">
  <div class="row">
    <div class="col-md-4">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">Fasilitas Lengkap</h5>
          <p class="card-text">Didukung fasilitas modern.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">Dosen Profesional</h5>
          <p class="card-text">Tenaga pengajar berpengalaman.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">Lingkungan Nyaman</h5>
          <p class="card-text">Mendukung proses belajar.</p>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## Tahap 4 – Halaman Tentang Kampus

**Tujuan**: Menyajikan informasi detail tentang kampus.

### Contoh Kode tentang.html

```html
<div class="container my-5">
  <h2>Tentang Kampus</h2>
  <p>
    KampusKu berdiri sejak tahun 2000 dan berkomitmen mencetak lulusan
    berkualitas.
  </p>
  <div class="row">
    <div class="col-md-6">
      <img
        src="assets/images/kampus.jpg"
        class="img-fluid rounded"
        alt="Kampus"
      />
    </div>
    <div class="col-md-6">
      <p>Lokasi kampus berada di pusat kota dan mudah diakses.</p>
    </div>
  </div>
</div>
```

---

## Tahap 5 – Halaman Visi & Misi

**Tujuan**: Menampilkan nilai dan tujuan kampus.

### Contoh Kode visi-misi.html

```html
<div class="container my-5">
  <h2>Visi</h2>
  <p>Menjadi kampus unggul tingkat nasional.</p>

  <h2>Misi</h2>
  <ul>
    <li>Menyelenggarakan pendidikan berkualitas</li>
    <li>Mengembangkan riset dan inovasi</li>
    <li>Mengabdi kepada masyarakat</li>
  </ul>

  <button class="btn btn-success" onclick="showMessage()">Lihat Detail</button>
</div>
```

### JavaScript (script.js)

```javascript
function showMessage() {
  alert("Visi dan Misi KampusKu berorientasi pada masa depan!");
}
```

---

## Tahap 6 – Halaman Tambahan (Kontak)

**Tujuan**: Melatih penggunaan form dan JavaScript.

### Contoh Kode kontak.html

```html
<div class="container my-5">
  <h2>Kontak Kami</h2>
  <form onsubmit="return validateForm()">
    <div class="mb-3">
      <label class="form-label">Nama</label>
      <input type="text" id="nama" class="form-control" />
    </div>
    <div class="mb-3">
      <label class="form-label">Email</label>
      <input type="email" id="email" class="form-control" />
    </div>
    <div class="mb-3">
      <label class="form-label">Pesan</label>
      <textarea id="pesan" class="form-control"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Kirim</button>
  </form>
</div>
```

### JavaScript Validasi

```javascript
function validateForm() {
  let nama = document.getElementById("nama").value;
  let email = document.getElementById("email").value;
  let pesan = document.getElementById("pesan").value;

  if (nama === "" || email === "" || pesan === "") {
    alert("Semua field harus diisi!");
    return false;
  }

  alert("Pesan berhasil dikirim!");
  return true;
}
```

---

## Tahap 7 – Styling Tambahan dengan CSS

**Tujuan**: Meningkatkan tampilan visual website.

### Task:

1. Ubah warna tema kampus.
2. Atur font dan spacing.
3. Tambahkan efek hover pada menu dan tombol.

---

## Tahap 8 – Halaman Program Studi

**Tujuan**: Menampilkan daftar program studi kampus.

### Contoh Kode prodi.html

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Program Studi - STT NF</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />
  </head>
  <body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container">
        <a class="navbar-brand" href="index.html">STT-NF</a>
      </div>
    </nav>

    <div class="container my-5">
      <h2>Program Studi</h2>
      <div class="row">
        <div class="col-md-4">
          <div class="card mb-3">
            <div class="card-body">
              <h5>Teknik Informatika</h5>
              <p>Fokus pada software engineering, AI, dan keamanan sistem.</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card mb-3">
            <div class="card-body">
              <h5>Sistem Informasi</h5>
              <p>Mengintegrasikan teknologi dan kebutuhan bisnis.</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card mb-3">
            <div class="card-body">
              <h5>Bisnis Digital</h5>
              <p>Menyiapkan lulusan siap menghadapi transformasi digital.</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <footer class="bg-dark text-white text-center p-3">
      © 2025 STT Terpadu Nurul Fikri
    </footer>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```

---

## Tahap 9 – Halaman Berita Kampus (News)

**Tujuan**: Melatih manipulasi DOM JavaScript.

### Contoh Kode news.html

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Berita Kampus</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />
  </head>
  <body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container">
        <a class="navbar-brand" href="index.html">STT-NF</a>
      </div>
    </nav>

    <div class="container my-5">
      <h2>Berita Kampus</h2>
      <ul id="newsList" class="list-group"></ul>
    </div>

    <script>
      const news = [
        "STT-NF membuka pendaftaran mahasiswa baru",
        "Workshop Web Development untuk Mahasiswa",
        "Kerja sama industri teknologi nasional",
      ];

      let list = document.getElementById("newsList");
      news.forEach((item) => {
        let li = document.createElement("li");
        li.className = "list-group-item";
        li.textContent = item;
        list.appendChild(li);
      });
    </script>

    <footer class="bg-dark text-white text-center p-3">
      © 2025 STT Terpadu Nurul Fikri
    </footer>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```

---

## Tahap 10 – Testing & Evaluasi Akhir

**Checklist Akhir**:

- Semua halaman saling terhubung
- Tidak ada error HTML/JS
- Layout responsif
- Konten sesuai profil kampus

---

## Penutup

Dengan modul ini mahasiswa membangun website kampus nyata berbasis **STT Terpadu Nurul Fikri** secara bertahap dan aplikatif.
