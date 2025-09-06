
# Bab 2.1: Array & Operasi Dasar (Basa Bayi)

## 🎯 Tujuan Belajar
- Tau apa itu **array** (wadah buat banyak data).
- Bisa bikin, baca, dan ubah isi array.
- Kenal cara-cara dasar ngoprek array: `push`, `pop`, `shift`, `unshift`, `length`, sama `splice`.

---

## 🍼 Apa itu Array?

Bayangin kamu punya **kotak mainan**. Di dalam kotak itu kamu bisa taruh banyak mainan sekaligus: mobil-mobilan, boneka, robot, bola, dan lain-lain.  
Nah, **array itu kayak kotak mainan** di dunia pemrograman. Bedanya, yang disimpan bukan mainan, tapi **data** kayak angka, huruf, atau kata.

👉 Jadi, array = **satu wadah, banyak isi**.

Contoh:
```js
let teman = ["Budi", "Siti", "Ani", "Rizky", "Dina"];
```
Artinya kita punya kotak (array) bernama `teman` yang isinya 5 nama.  
Kalau mau ambil isinya, kita pakai **nomor urut** yang mulai dari **0** (bukan 1 ya!).  
- `teman[0]` → "Budi"  
- `teman[1]` → "Siti"  
dst.

---

## 🍼 Operasi Dasar pada Array

### 1. Menambahkan Isi ke Array
- **`push()`** → masukin isi ke **belakang kotak**.  
- **`unshift()`** → masukin isi ke **depan kotak**.  

📦 Contoh:
```js
let buah = ["apel", "mangga"];
buah.push("pisang");   // ["apel", "mangga", "pisang"]
buah.unshift("jeruk"); // ["jeruk", "apel", "mangga", "pisang"]
```

---

### 2. Menghapus Isi dari Array
- **`pop()`** → buang isi dari **belakang kotak**.  
- **`shift()`** → buang isi dari **depan kotak**.  

📦 Contoh:
```js
let hewan = ["kucing", "anjing", "kelinci"];
hewan.pop();   // ["kucing", "anjing"]
hewan.shift(); // ["anjing"]
```

---

### 3. Cek Panjang Kotak (Jumlah Isi)
- **`length`** → tau berapa banyak isi dalam kotak.  

📦 Contoh:
```js
let angka = [1, 2, 3, 4];
console.log(angka.length); // 4
```

---

### 4. Sisip/Hapus Isi di Tengah
- **`splice(index, jumlah, elemenBaru)`**  
   - index = posisi mulai  
   - jumlah = berapa yang mau dihapus  
   - elemenBaru = isi baru (boleh ada, boleh nggak)  

📦 Contoh:
```js
let warna = ["merah", "kuning", "hijau"];
warna.splice(1, 0, "biru");   // ["merah", "biru", "kuning", "hijau"]
warna.splice(2, 1);           // ["merah", "biru", "hijau"]
```

---

## 🍼 Rangkuman
- Array itu kayak **kotak ajaib** buat nyimpen banyak hal dalam 1 variabel.  
- Bisa ditambah (`push`, `unshift`), dikurang (`pop`, `shift`), dihitung (`length`), atau diselipin/diambil di tengah (`splice`).  
- Array punya nomor urut (indeks), mulai dari **0**.  
- Array bisa diubah-ubah (mutable).

---

## 🎮 Latihan Mandiri
1. Buat array berisi 5 nama temanmu.  
2. Tambahin 1 nama di depan dan di belakang.  
3. Hapus 1 nama dari depan dan belakang.  
4. Selipin nama baru di posisi ke-2.  
5. Hitung berapa jumlah teman sekarang pakai `.length`.  

---

## 🎯 Studi Kasus (per materi)

### 1. `push()` & `unshift()` (Tambah Isi)
1. Kamu punya array buah, tambahin 2 buah baru di depan dan belakang.  
2. Kamu bikin array daftar belanja, masukin barang baru yang baru aja kamu ingat.  
3. Kamu punya array hewan peliharaan, tambahin hewan baru di depan.  
4. Kamu punya array film favorit, tambahin film terbaru.  
5. Kamu punya array angka, masukin angka 0 di awal.

---

### 2. `pop()` & `shift()` (Hapus Isi)
1. Kamu punya array mainan, buang mainan terakhir karena rusak.  
2. Kamu punya array baju, buang baju paling depan karena kotor.  
3. Kamu punya array makanan, makan makanan terakhir (hapus terakhir).  
4. Kamu punya array tugas sekolah, hapus tugas pertama karena udah selesai.  
5. Kamu punya array daftar antrian, hapus orang pertama (udah dilayani).  

---

### 3. `length` (Hitung Isi)
1. Hitung jumlah buah di array.  
2. Hitung jumlah teman di array.  
3. Hitung jumlah angka di array.  
4. Hitung jumlah barang di daftar belanja.  
5. Hitung jumlah hewan di array.  

---

### 4. `splice()` (Sisip/Hapus di Tengah)
1. Kamu punya array warna ["merah", "kuning", "hijau"], sisipkan "biru" di posisi ke-2.  
2. Kamu punya array teman, hapus teman di posisi ke-3.  
3. Kamu punya array angka [1,2,3,4,5], hapus angka 3 dan ganti dengan 30.  
4. Kamu punya array makanan, tambahin makanan baru di tengah.  
5. Kamu punya array benda ["buku", "pensil", "penghapus"], ganti "pensil" jadi "pulpen".  

---

### 5. Kombinasi Semua
1. Buat array daftar belanja, tambahin barang, hapus barang, terus hitung jumlah barang.  
2. Buat array hewan peliharaan, masukin hewan baru, hapus hewan lama, lalu selipin hewan baru di tengah.  
3. Buat array angka, tambahin angka baru di akhir, buang angka awal, lalu cek jumlahnya.  
4. Buat array teman, tambahin teman baru di awal, hapus teman terakhir, lalu ganti teman ke-2 pakai nama lain.  
5. Buat array makanan, tambahin makanan, hapus makanan, selipin makanan, terus tampilkan semua.  
