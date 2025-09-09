# Bab 2.2: Array Method (Basa Bayi)

## 🎯 Tujuan Belajar
- Paham apa itu cara-cara khusus (method) untuk main sama array.
- Bisa pakai `forEach`, `map`, `filter`, `reduce`, sama `find` buat mainin data di JavaScript.

---

## 🍼 Apa itu Array Method?
Jadi gini dek, kalau array itu kayak kotak mainan yang isinya banyak mainan, nah JavaScript ngasih **alat-alat khusus** biar kita bisa main sama mainan itu lebih gampang. Alat-alat itu namanya **method**.  
Kita nggak perlu ribet bikin aturan sendiri, tinggal pakai aja.

---

## 🛠️ Macam-macam Method

### 1. `forEach()` ➡️ Jalanin satu-satu
Bayangin kamu punya 5 permen. Kalau kamu mau makan satu-satu, itu kayak `forEach`. Jadi kita cuma *jalanin* semua isi array.

```javascript
let angka = [1, 2, 3];
angka.forEach(function(n) {
  console.log("Aku punya angka: " + n);
});
```

---

### 2. `map()` ➡️ Bikin kotak mainan baru
Kalau kamu punya mobil-mobilan warna putih semua, terus kamu cat jadi merah, kamu bikin kotak baru isinya mobil merah. Itu kayak `map`.

```javascript
let angka = [1, 2, 3];
let kaliDua = angka.map(function(n) {
  return n * 2;
});
console.log(kaliDua); // [2, 4, 6]
```

---

### 3. `filter()` ➡️ Pilih yang cocok aja
Misalnya kamu punya 10 kelereng, tapi kamu cuma mau ambil yang warna biru aja. Nah, itu kerjaan `filter`.

```javascript
let angka = [1, 2, 3, 4, 5, 6];
let genap = angka.filter(function(n) {
  return n % 2 === 0;
});
console.log(genap); // [2, 4, 6]
```

---

### 4. `reduce()` ➡️ Jadiin satu hasil
Bayangin kamu punya 5 koin, lalu kamu kumpulin jadi satu celengan. Itu kayak `reduce`, ngumpulin semua jadi satu nilai.

```javascript
let angka = [1, 2, 3, 4];
let jumlah = angka.reduce(function(total, n) {
  return total + n;
}, 0);
console.log(jumlah); // 10
```

---

### 5. `find()` ➡️ Cari yang pertama ketemu
Kamu punya tumpukan buku, terus nyari buku pertama yang warnanya merah. Itu kerja `find`.

```javascript
let angka = [5, 7, 10, 12];
let cari = angka.find(function(n) {
  return n > 8;
});
console.log(cari); // 10
```

---

## 🏋️ Latihan Main
1. Bikin array isi angka 1–10.  
2. Pakai `map` buat kaliin semua angka dengan 5.  
3. Pakai `filter` buat ambil angka genap.  
4. Pakai `reduce` buat jumlahin semua angka.  
5. Pakai `find` buat cari angka pertama yang lebih dari 8.  

---

## 📝 Rangkuman
- `forEach`: mainin semua isi, tapi nggak bikin array baru.  
- `map`: bikin array baru hasil modifikasi.  
- `filter`: pilih isi tertentu.  
- `reduce`: kumpulin jadi satu nilai.  
- `find`: cari isi pertama yang cocok.  

---

## 🎯 Studi Kasus (5 contoh)
1. Ada daftar nama buah, terus cetak semua pakai `forEach`.  
2. Ada daftar harga barang, kalikan semua harga dengan 10% pakai `map`.  
3. Ada daftar umur orang, ambil yang umurnya lebih dari 17 pakai `filter`.  
4. Ada daftar nilai ujian, jumlahkan semua nilai pakai `reduce`.  
5. Ada daftar nomor kursi, cari kursi pertama yang lebih dari nomor 20 pakai `find`.  
