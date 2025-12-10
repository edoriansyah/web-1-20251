# Workshop Praktikum JavaScript Advanced

## Workshop 1 – Manipulasi HTML DOM Dasar

### Task

Buat halaman HTML yang memiliki elemen:

- `<p id="teks">Halo semuanya!</p>`
- Tombol:
  - “Ubah Teks”
  - “Ubah Warna”
  - “Sembunyikan”
  - “Tampilkan”
    Gunakan JavaScript DOM untuk mengubah teks, warna, dan menampilkan/menyembunyikan elemen.

### Code

```html
<!DOCTYPE html>
<html>
  <head>
    <title>DOM Manipulation</title>
  </head>
  <body>
    <p id="teks">Halo semuanya!</p>

    <button onclick="ubahTeks()">Ubah Teks</button>
    <button onclick="ubahWarna()">Ubah Warna</button>
    <button onclick="sembunyikan()">Sembunyikan</button>
    <button onclick="tampilkan()">Tampilkan</button>

    <script>
      function ubahTeks() {
        document.getElementById("teks").innerHTML = "Teks sudah diubah!";
      }

      function ubahWarna() {
        document.getElementById("teks").style.color = "red";
      }

      function sembunyikan() {
        document.getElementById("teks").style.display = "none";
      }

      function tampilkan() {
        document.getElementById("teks").style.display = "block";
      }
    </script>
  </body>
</html>
```

---

## Workshop 2 – Menambah & Menghapus Elemen DOM

### Task

Buat fitur dinamis dengan ketentuan:

- Terdapat input teks
- Tombol "Tambah Item" untuk menambah `<li>` baru ke dalam `<ul>`
- Tombol "Hapus Terakhir" untuk menghapus item terakhir pada list
  Gunakan createElement(), appendChild(), dan removeChild().

### Code

```html
<input id="input" type="text" placeholder="Isi item" />
<button onclick="tambah()">Tambah Item</button>
<button onclick="hapus()">Hapus Terakhir</button>

<ul id="list"></ul>

<script>
  function tambah() {
    const teks = document.getElementById("input").value;
    if (!teks) return;

    const li = document.createElement("li");
    li.innerHTML = teks;
    document.getElementById("list").appendChild(li);
    document.getElementById("input").value = "";
  }

  function hapus() {
    const list = document.getElementById("list");
    list.removeChild(list.lastElementChild);
  }
</script>
```

---

## Workshop 3 – jQuery Selectors & Events

### Task

Dengan menggunakan jQuery:

- Sembunyikan seluruh elemen `<p>` saat tombol Hide diklik.
- Tampilkan kembali `<p>` saat tombol Show diklik.
- Ubah warna teks `<p>` menjadi biru saat mouse hover dan kembali menjadi hitam saat mouse keluar.

### Code

```html
<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>

<p class="p1">Paragraf 1</p>
<p class="p1">Paragraf 2</p>

<button id="hide">Hide</button>
<button id="show">Show</button>

<script>
  $(document).ready(function () {
    $("#hide").click(function () {
      $("p").hide();
    });

    $("#show").click(function () {
      $("p").show();
    });

    $("p").hover(
      function () {
        $(this).css("color", "blue");
      },
      function () {
        $(this).css("color", "black");
      }
    );
  });
</script>
```

---

## Workshop 4 – jQuery Effects

### Task

Buat halaman yang memiliki paragraf dan tombol berikut:

- Fade Out
- Fade In
- Slide Up
- Slide Down  
  Setiap tombol menjalankan efek jQuery sesuai fungsinya.

### Code

```html
<p id="box">Ini adalah paragraf efek jQuery.</p>

<button id="fadeOut">Fade Out</button>
<button id="fadeIn">Fade In</button>
<button id="slideUp">Slide Up</button>
<button id="slideDown">Slide Down</button>

<script>
  $(function () {
    $("#fadeOut").click(() => $("#box").fadeOut());
    $("#fadeIn").click(() => $("#box").fadeIn());
    $("#slideUp").click(() => $("#box").slideUp());
    $("#slideDown").click(() => $("#box").slideDown());
  });
</script>
```

---

## Workshop 5 – Method Chaining jQuery

### Task

Buat aksi chaining pada jQuery:

- Ubah warna teks menjadi merah
- Slide up selama 2 detik
- Slide down selama 2 detik  
  Semua dilakukan dalam satu perintah berantai (chaining).

### Code

```html
<p id="text">Contoh method chaining.</p>
<button id="run">Jalankan</button>

<script>
  $(function () {
    $("#run").click(function () {
      $("#text").css("color", "red").slideUp(2000).slideDown(2000);
    });
  });
</script>
```
