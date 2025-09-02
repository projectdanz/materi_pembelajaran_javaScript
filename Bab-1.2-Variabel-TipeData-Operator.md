# 📘 Bab 1.2: Variabel, Tipe Data, Operator, Console, dan Pop-up di JavaScript

## 🎯 Tujuan
- Bisa membuat variabel di JavaScript.
- Mengenal tipe data dasar (primitif).
- Bisa pakai operator matematika, perbandingan, logika.
- Mengenal cara pakai `console` dan pop-up (`alert`, `prompt`, `confirm`).

---

## 🔹 1. Variabel

Variabel = tempat simpan data.  
- `var` → cara lama, jarang dipakai.  
- `let` → bisa diubah nilainya.  
- `const` → tidak bisa diubah nilainya.  

```js
var nama = "Danz";   // lama
let umur = 20;       // bisa diubah
const pi = 3.14;     // tidak bisa diubah
```

### ✅ Study Case
1. Buat variabel `nama`, `umur`, `status`.  
2. Ubah nilai `umur` setelah deklarasi.  
3. Coba deklarasi pakai `const` lalu ubah nilainya → error.  
4. Coba bikin variabel tanpa `var/let/const`.  
5. Hitung saldo akhir: `saldoAwal - pengeluaran`.  

---

## 🔹 2. Tipe Data Primitif

- **String** → teks `"Halo"`  
- **Number** → angka `25`  
- **Boolean** → `true` / `false`  
- **Null** → kosong sengaja  
- **Undefined** → belum ada nilai  

```js
let nama = "Danz";        // string
let umur = 25;            // number
let sudahLogin = true;    // boolean
let pasangan = null;      // null
let alamat;               // undefined
```

### ✅ Study Case
1. Buat variabel: `judulBuku`, `jumlahHalaman`, `tersedia`.  
2. Simulasikan lampu nyala/mati dengan boolean.  
3. Buat variabel `uangDompet = null`.  
4. Buat variabel tanpa nilai → hasilnya `undefined`.  
5. Gabungkan string dengan variabel.  

---

## 🔹 3. Operator

### Aritmatika
`+ - * / %`  
```js
let a = 10, b = 3;
console.log(a + b); // 13
console.log(a % b); // 1
```

### Perbandingan
`==  ===  !=  !==  >  <  >=  <=`  
```js
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

### Logika
`&&` (dan), `||` (atau), `!` (not)  
```js
let login = true;
let premium = false;
console.log(login && premium); // false
```

### ✅ Study Case
1. Hitung luas segitiga (alas × tinggi ÷ 2).  
2. Cek apakah umur ≥ 17.  
3. Bandingkan `==` dan `===`.  
4. Simulasi belanja: cek saldo cukup/tidak.  
5. Cek syarat lomba: umur ≥ 18 **dan** punyaKTP.  

---

## 🔹 4. Console & Pop-up

### Console
- `console.log()` → tampilkan biasa  
- `console.error()` → tampilkan error  
- `console.warn()` → tampilkan peringatan  
- `console.table()` → tampilkan tabel  

### Pop-up
- `alert("Pesan")` → hanya tampil pesan  
- `prompt("Masukkan nama:")` → input teks  
- `confirm("Yakin?")` → pilih OK / Cancel  

```js
alert("Halo Danz!");
let nama = prompt("Masukkan nama:");
let yakin = confirm("Apakah kamu yakin?");
```

### ✅ Study Case
1. Tampilkan biodata pakai `console.log()`.  
2. Buat array buah lalu tampilkan dengan `console.table()`.  
3. Minta nama lewat `prompt()`, lalu `alert()` sapa user.  
4. Konfirmasi hapus data pakai `confirm()`.  
5. Jika variabel `user` kosong → tampilkan `console.error()`.  
