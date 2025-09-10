# Bab 2.3: Object & Manipulasi Properti

## 🎯 Tujuan Belajar
- Tau apa itu **object** di JavaScript.  
- Bisa **membuat** object.  
- Bisa **nambah, ubah, dan hapus** isi object.  
- Bisa **baca data** di object pakai looping.  

---

## 🍼 Apa itu Object?
Kalau array isinya berderet (`["apel", "pisang"]`),  
**object** isinya berpasangan, kayak kotak data:  

👉 **key (nama)** = **value (isi)**  

Contoh:  
```js
let buku = {
  judul: "Belajar JS",
  pengarang: "Mas Danz",
  tahunTerbit: 2025
};
```

---

## 📖 Akses Properti Object
Ada 2 cara:  

1. **Dot (`.`)**  
```js
console.log(buku.judul); // Belajar JS
```

2. **Bracket (`[]`)**  
```js
console.log(buku["pengarang"]); // Mas Danz
```

### 📝 Studi Kasus
1. Buat object `mobil` dengan properti `merk` dan `warna`. Tampilkan `merk`.  
2. Buat object `siswa` dengan properti `nama` dan `kelas`. Tampilkan `kelas`.  
3. Buat object `hewan` dengan properti `jenis` dan `umur`. Tampilkan `jenis`.  
4. Buat object `film` dengan properti `judul` dan `tahun`. Tampilkan `tahun`.  
5. Buat object `akun` dengan properti `username` dan `password`. Tampilkan `username`.  

---

## ➕ Menambahkan Properti
Object bisa ditambah properti baru kapan aja.  

```js
buku.penerbit = "Pustaka Ilmu";
console.log(buku);
```

### 📝 Studi Kasus
1. Tambahkan properti `harga` pada object `mobil`.  
2. Tambahkan properti `alamat` pada object `siswa`.  
3. Tambahkan properti `makanan` pada object `hewan`.  
4. Tambahkan properti `genre` pada object `film`.  
5. Tambahkan properti `email` pada object `akun`.  

---

## ✏️ Mengubah Nilai Properti
Kalau udah ada, bisa diubah:  

```js
buku.tahunTerbit = 2030;
console.log(buku);
```

### 📝 Studi Kasus
1. Ubah `warna` mobil jadi `"hitam"`.  
2. Ubah `kelas` siswa jadi `"XI"`.  
3. Ubah `umur` hewan jadi `5`.  
4. Ubah `tahun` film jadi `2024`.  
5. Ubah `password` akun jadi `"rahasia123"`.  

---

## ❌ Menghapus Properti
Kalau gak mau disimpan, bisa dihapus:  

```js
delete buku.pengarang;
console.log(buku);
```

### 📝 Studi Kasus
1. Hapus `harga` dari mobil.  
2. Hapus `alamat` dari siswa.  
3. Hapus `makanan` dari hewan.  
4. Hapus `genre` dari film.  
5. Hapus `email` dari akun.  

---

## 🔁 Looping pada Object
Buat liat semua isi object, kita pake `for...in`:  

```js
for (let key in buku) {
  console.log(key + " : " + buku[key]);
}
```

### 📝 Studi Kasus
1. Loop semua isi `mobil`.  
2. Loop semua isi `siswa`.  
3. Loop semua isi `hewan`.  
4. Loop semua isi `film`.  
5. Loop semua isi `akun`.  

---

## 🎯 Latihan Mandiri (Gabungan)
1. Buat object `buku` dengan properti: `judul`, `pengarang`, `tahunTerbit`.  
2. Tambahkan properti `penerbit`.  
3. Ubah nilai `tahunTerbit`.  
4. Hapus `pengarang`.  
5. Tampilkan semua isi object dengan looping.  

---

## 📝 Rangkuman
- Object = data dengan pasangan **key-value**.  
- Bisa diakses pakai **dot** atau **bracket**.  
- Bisa ditambah, diubah, atau dihapus.  
- Bisa dilihat semua isinya dengan **looping**.  

---

## 🎮 Evaluasi Harian (Studi Kasus Besar)
Buat program `bukuFavorit` yang:  
1. Menyimpan `judul`, `pengarang`, `tahunTerbit`.  
2. Menambah properti `penerbit`.  
3. Mengubah `tahunTerbit`.  
4. Menghapus `pengarang`.  
5. Menampilkan semua isi object.  
