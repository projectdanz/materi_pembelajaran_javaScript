# Bab 2.4: Destructuring & Spread/Rest Operator

## 🎯 Tujuan Belajar
- Tau cara **destructuring** array dan object.  
- Bisa pake **spread operator** untuk nyebarin isi array/object.  
- Bisa pake **rest operator** untuk ngumpulin sisa data.  

---

## 🍬 Destructuring Array
Destructuring itu kayak “bongkar isi kotak” jadi variabel satu-satu.

```js
let angka = [1, 2, 3, 4];
let [a, b, c, d] = angka;

console.log(a); // 1
console.log(b); // 2
```

### 📝 Studi Kasus
1. Ambil nilai dari array `[10, 20, 30]` jadi variabel `x, y, z`.  
2. Ambil nilai pertama dan kedua dari array `["apel", "jeruk", "mangga"]`.  
3. Ambil nilai pertama dan sisanya dari array `[5, 6, 7, 8]`.  
4. Destructuring array `[100, 200]` jadi `satu` dan `dua`.  
5. Destructuring array `[true, false, true]` jadi `t1, t2, t3`.  

---

## 🍭 Destructuring Object
Sama kayak array, tapi buat object (pakai nama property).

```js
let mobil = { merek: "Toyota", tahun: 2020 };
let { merek, tahun } = mobil;

console.log(merek); // Toyota
console.log(tahun); // 2020
```

### 📝 Studi Kasus
1. Destructuring object `{ nama: "Budi", umur: 17 }`.  
2. Ambil `judul` dan `pengarang` dari object `{ judul: "Buku A", pengarang: "Andi" }`.  
3. Ambil `merk` dari object `{ merk: "Honda", warna: "merah" }`.  
4. Destructuring `{ username: "danz", password: "123" }`.  
5. Ambil `nama` dan `kelas` dari `{ nama: "Siti", kelas: "XI" }`.  

---

## 🌟 Spread Operator (...)
Spread itu kayak **nyebarin isi kotak**.  
Biasanya dipake buat gabung array atau copy object.

```js
let arr1 = [1, 2];
let arr2 = [3, 4];
let gabung = [...arr1, ...arr2];

console.log(gabung); // [1,2,3,4]
```

### 📝 Studi Kasus
1. Gabungkan `[1, 2]` dengan `[3, 4]`.  
2. Copy array `[10, 20, 30]` ke array baru.  
3. Gabungkan object `{ a: 1 }` dengan `{ b: 2 }`.  
4. Spread array `[5, 6, 7]` ke console.log.  
5. Gabungkan array `["a", "b"]` dan `["c", "d"]`.  

---

## 🍩 Rest Operator (...)
Rest itu kebalikan spread: **ngumpulin sisa isi**.  

```js
function jumlah(...angka) {
  return angka.reduce((total, n) => total + n, 0);
}

console.log(jumlah(1, 2, 3, 4)); // 10
```

### 📝 Studi Kasus
1. Buat function `tambah` yang bisa nerima banyak angka.  
2. Buat function `cetak` yang nerima banyak string dan print satu-satu.  
3. Buat function `kalikan` semua angka yang masuk.  
4. Buat function `gabungKalimat` yang nerima banyak kata jadi 1 kalimat.  
5. Buat destructuring array `[1,2,3,4,5]` jadi `awal` dan `...sisa`.  

---

## 🎯 Latihan Mandiri (Gabungan)
1. Gunakan destructuring array untuk ambil nilai `[1, 2, 3, 4]`.  
2. Buat object `mobil` dan destructuring `merek` dan `tahun`.  
3. Gabungkan dua array pakai spread operator.  
4. Buat function yang nerima banyak angka lalu jumlahkan pakai rest.  

---

## 📝 Rangkuman
- **Destructuring** = cara cepat ambil data dari array/object.  
- **Spread (`...`)** = nyebarin isi array/object.  
- **Rest (`...`)** = ngumpulin sisa isi jadi array.  

---

## 🎮 Evaluasi Harian (Studi Kasus Besar)
Buat program `dataSiswa`:  
1. Object `{ nama: "Dewi", umur: 16, kelas: "XI" }`.  
2. Pisahkan `nama` dan `kelas` dengan destructuring.  
3. Tambahkan properti baru `hobi` pakai spread.  
4. Buat function yang menerima nilai ujian (banyak angka) lalu hitung totalnya dengan rest.  
5. Tampilkan hasil akhir ke console.  
