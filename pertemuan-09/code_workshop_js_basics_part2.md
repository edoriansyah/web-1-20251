
# Template Jawaban Workshop JavaScript – Basics Part 2

## Bagian 1 — Conditionals

### 1.1 If–Else Sederhana
```js
let nilai = 85;

if (nilai >= 90) {
    console.log("A");
} else if (nilai >= 80) {
    console.log("B");
} else if (nilai >= 70) {
    console.log("C");
} else if (nilai >= 60) {
    console.log("D");
} else {
    console.log("E");
}
```

### 1.2 Switch Case
```js
let hari = 3;
switch (hari) {
    case 1: console.log("Senin"); break;
    case 2: console.log("Selasa"); break;
    case 3: console.log("Rabu"); break;
    case 4: console.log("Kamis"); break;
    case 5: console.log("Jumat"); break;
    case 6: console.log("Sabtu"); break;
    case 7: console.log("Minggu"); break;
    default: console.log("Input tidak dikenal");
}
```

### 1.3 Ternary Operator
```js
let usia = 17;
let status = usia >= 17 ? "boleh_buat_ktp" : "belum_boleh_buat_ktp";
console.log(status);
```

---

## Bagian 2 — Loops

### 2.1 For Loop
```js
for (let i = 1; i <= 20; i++) {
    console.log(i);
}
```

### 2.2 While Loop
```js
let i = 10;
while (i >= 1) {
    console.log(i);
    i--;
}
```

### 2.3 Do–While Loop
```js
let count = 0;
do {
    console.log("Halo!");
    count++;
} while (count < 0);
```

### 2.4 Break & Continue
```js
for (let i = 1; i <= 10; i++) {
    if (i === 5) continue;
    if (i === 8) break;
    console.log(i);
}
```

---

## Bagian 3 — Functions

### 3.1 Function Declaration
```js
function luasPersegi(sisi) {
    return sisi * sisi;
}
console.log(luasPersegi(4));
```

### 3.2 Function Expression
```js
const greet = function(nama) {
    console.log("Halo, " + nama + "!");
}
greet("Budi");
```

### 3.3 Arrow Function
```js
const jumlah = (a, b) => a + b;
console.log(jumlah(5, 7));
```

### 3.4 Default & Rest Parameter
```js
function salam(nama = "Mahasiswa") {
    console.log("Halo " + nama);
}

function jumlahSemua(...nums) {
    return nums.reduce((total, n) => total + n, 0);
}

salam();
console.log(jumlahSemua(1, 2, 3, 4, 5));
```

---

## Bagian 4 — Objects

### 4.1 Object Literal
```js
let mahasiswa = {
    nama: "Andi",
    nim: "20231001",
    jurusan: "Informatika",
    tampilkanData() {
        console.log(this.nama, this.nim, this.jurusan);
    }
};
mahasiswa.tampilkanData();
```

### 4.2 new Object()
```js
let mobil = new Object();
mobil.brand = "Toyota";
mobil.tahun = 2020;
mobil.warna = "Hitam";
```

### 4.3 Mengubah Property
```js
mobil.warna = "Merah";
mobil.mesin = "1500cc";
```

---

## Bagian 5 — Arrays

### 5.1 Membuat Array
```js
let buah = ["apel", "mangga", "pisang"];
console.log(buah[0]);
console.log(buah.length);
```

### 5.2 Menambah Elemen
```js
buah.push("jeruk");
buah[buah.length] = "anggur";
```

### 5.3 Looping Array
```js
for (let i = 0; i < buah.length; i++) {
    console.log(buah[i]);
}
```

### 5.4 Array toString
```js
console.log(buah.toString());
```

### 5.5 Array Berisi Berbagai Tipe
```js
let campur = ["teks", 123, true, {nama: "Budi"}, [1,2,3]];
console.log(campur[1]);
console.log(campur[3].nama);
```

---

## Mini Project – Daftar Belanja
```js
let daftar = [];

function tambahItem(item) {
    daftar.push(item);
    console.log(`Item "${item}" ditambahkan!`);
}

function hapusItem(item) {
    let index = daftar.indexOf(item);
    if (index !== -1) {
        daftar.splice(index, 1);
        console.log(`Item "${item}" dihapus!`);
    } else {
        console.log("Item tidak ditemukan");
    }
}

function tampilkanDaftar() {
    console.log("Daftar Belanja:");
    daftar.forEach((val, i) => {
        console.log(`${i+1}. ${val}`);
    });
}

tambahItem("Susu");
tambahItem("Roti");
tampilkanDaftar();
hapusItem("Roti");
tampilkanDaftar();
```
