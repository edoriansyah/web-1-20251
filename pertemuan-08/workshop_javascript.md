# Workshop Praktikum -- JavaScript Basics

## Sesi 1 -- Menggunakan JavaScript di HTML

### 1.1 Praktik Inline JavaScript

Instruksi: 1. Buat file baru: `index.html` 2. Tambahkan tombol dengan
event `onclick`:

``` html
<button onclick="alert('Halo, saya belajar JavaScript!')">Klik Saya</button>
```

Tugas: - Buat 2 tombol tambahan dengan `onmouseover` dan `ondblclick`.

------------------------------------------------------------------------

### 1.2 Praktik Internal JavaScript

``` html
<script>
  function ubahTeks() {
    document.getElementById("judul").innerText = "Teks sudah berubah oleh JavaScript!";
  }
</script>

<h2 id="judul">Ini Judul Awal</h2>
<button onclick="ubahTeks()">Ubah Judul</button>
```

Tugas: - Tambahkan fungsi `ubahWarna()` untuk mengubah warna teks judul.

------------------------------------------------------------------------

### 1.3 Praktik External JavaScript

File `script.js`:

``` javascript
function tambahBorder() {
  document.getElementById("box").style.border = "3px solid blue";
}
```

HTML:

``` html
<script src="script.js"></script>

<div id="box" style="width:100px;height:100px;background:lightgray;"></div>
<button onclick="tambahBorder()">Tambah Border</button>
```

Tugas: - Tambahkan fungsi `hapusBorder()` dalam `script.js`.

------------------------------------------------------------------------

## Sesi 2 -- JavaScript Output

### 2.1 innerHTML

``` html
<p id="demo"></p>
<script>
  document.getElementById("demo").innerHTML = "Output dengan innerHTML!";
</script>
```

### 2.2 alert()

``` javascript
alert("Halo dari alert!");
```

### 2.3 console.log()

``` javascript
console.log("Pesan ini muncul di console");
```

### 2.4 document.write()

``` javascript
document.write("Ini ditulis dengan document.write()");
```

Tugas: - Buat halaman yang menggunakan semua jenis output.

------------------------------------------------------------------------

## Sesi 3 -- Syntax, Variabel, dan Data Types

### 3.1 Deklarasi Variabel

``` javascript
let nama = "Edo";
const umur = 21;
let isStudent = true;
```

### 3.2 Identifiers

Perbaiki variabel berikut:

``` javascript
let 1nama = "Salah";
let let = 10;
let Nama = "Benar tetapi berbeda";
```

### 3.3 Data Types

``` javascript
let mahasiswa = { nama: "Edo", prodi: "TI" };
let hobi = ["coding", "game", "olahraga"];
```

Tugas: - Tampilkan semua data dengan `console.table()`.

------------------------------------------------------------------------

## Sesi 4 -- Operators

### 4.1 Arithmetic

``` javascript
let x = 10;
let y = 3;
```

### 4.2 Assignment

``` javascript
let a = 10;
a += 5;
a -= 2;
```

### 4.3 Comparison

``` javascript
let p = 5;
console.log(p == 5);
console.log(p === "5");
console.log(p != 10);
console.log(p > 8);
```

### 4.4 Logical

``` javascript
let usia = 20;
let punyaKTP = true;

console.log(usia >= 18 && punyaKTP);
console.log(usia < 18 || punyaKTP);
console.log(!punyaKTP);
```

Tugas: - Buat logika pengecekan izin mengendarai motor.

------------------------------------------------------------------------

## Mini Project -- Kalkulator Sederhana

HTML:

``` html
<h2>Kalkulator Sederhana</h2>

<input id="angka1" type="number" placeholder="Angka 1">
<input id="angka2" type="number" placeholder="Angka 2">

<button onclick="tambah()">Tambah</button>
<button onclick="kurang()">Kurang</button>

<p id="hasil"></p>
```

script.js:

``` javascript
function tambah() {
  let a = Number(document.getElementById("angka1").value);
  let b = Number(document.getElementById("angka2").value);
  document.getElementById("hasil").innerHTML = "Hasil: " + (a + b);
}

function kurang() {
  let a = Number(document.getElementById("angka1").value);
  let b = Number(document.getElementById("angka2").value);
  document.getElementById("hasil").innerHTML = "Hasil: " + (a - b);
}
```

Tambahan: - Tambahkan operasi perkalian & pembagian.
