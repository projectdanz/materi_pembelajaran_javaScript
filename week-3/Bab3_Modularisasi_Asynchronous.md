# 📘 Bab 3: Modularisasi & Asynchronous di JavaScript

## 🎯 Tujuan Belajar
1. Paham kenapa kode perlu dipisah-pisah (modularisasi).  
2. Bisa pakai `import` dan `export` buat saling pinjam fungsi/variabel antar file.  
3. Paham dasar *asynchronous* → cara JavaScript ngerjain banyak hal tanpa harus nunggu satu-satu.  

---

## 🔹 Bab 3.1: Modularisasi File JavaScript & Import/Export  

### 🔎 Kenapa Perlu Modularisasi?
Bayangin kamu lagi nulis catatan:  
- Kalau semua catatan kamu tulis di **satu halaman besar**, pasti susah cari bagian tertentu.  
- Kalau kamu pisah-pisah catatan jadi **buku kecil-kecil sesuai topik**, pasti lebih gampang dicari dan dibaca.  

👉 Sama dengan coding. Kalau program makin besar, file `main.js` bisa panjang banget. Nah, **modularisasi** bikin kita bisa:  
- 📂 Pisah kode jadi file kecil-kecil.  
- 🛠️ Fokus ke tugas tertentu di tiap file.  
- 🔍 Lebih gampang cari error.  
- 🔄 Bisa pakai ulang kode di tempat lain.  

---

### 🔹 Jenis Export & Import
#### 1. Named Export
- Bisa ekspor banyak hal dari 1 file.  
- Saat dipanggil harus sama persis namanya.  

```javascript
// math.js
export function tambah(a, b) { return a + b; }
export function kurang(a, b) { return a - b; }
```

```javascript
// main.js
import { tambah, kurang } from './math.js';

console.log(tambah(2, 3)); // 5
console.log(kurang(5, 2)); // 3
```

#### 2. Default Export
- Hanya ada **1 ekspor utama** per file.  
- Saat dipanggil bisa ganti nama sesuka hati.  

```javascript
// halo.js
export default function halo() {
  return "Halo semua!";
}
```

```javascript
// main.js
import sapa from './halo.js'; // nama bebas
console.log(sapa()); // "Halo semua!"
```

#### 3. Mix Export (Named + Default)
- Bisa dipakai barengan, tapi jangan kebanyakan biar gak bingung.  

```javascript
// tools.js
export default function defaultFunc() { return "Ini default"; }
export function helper() { return "Ini helper"; }
```

```javascript
// main.js
import apaaja, { helper } from './tools.js';
console.log(apaaja()); // "Ini default"
console.log(helper()); // "Ini helper"
```

---

### 🍼 5 Studi Kasus Modularisasi
1. **Bangun Datar**  
   - File `persegi.js`: fungsi luas persegi (`sisi * sisi`).  
   - File `lingkaran.js`: fungsi luas lingkaran (`π * r * r`).  
   - File `main.js`: import keduanya dan tampilkan hasil.  

2. **Pengolahan String**  
   - File `teks.js`: fungsi `besar(teks)` → ubah semua huruf ke huruf besar.  
   - File `main.js`: pakai fungsi `besar("belajar modular")`.  

3. **Waktu**  
   - File `waktu.js`: fungsi `jamSekarang()` → return jam saat ini (`new Date().toLocaleTimeString()`).  
   - File `main.js`: import dan tampilkan jam sekarang.  

4. **Salam Default**  
   - File `salam.js`: `export default` fungsi `sapa(nama)` → return `"Halo, nama!"`.  
   - File `main.js`: panggil dengan nama bebas.  

5. **Utility Campuran**  
   - File `utils.js`: default export fungsi `versi()` dan named export `hitung(a, b)`.  
   - File `main.js`: import keduanya dan tampilkan.  

---

## 🔹 Bab 3.2: Asynchronous di JavaScript  

### 🔎 Apa itu Asynchronous?
JavaScript punya gaya kerja unik: **single-threaded** → artinya cuma ada 1 jalur kerja.  
Kalau semua dikerjain **synchronous** (ngantri satu-satu), program jadi lambat.  
Makanya ada **asynchronous**: bisa ngerjain hal lain sambil nunggu tugas selesai.  

⚡ Analogi:  
- Kamu bikin mie instan.  
- Nunggu air mendidih (butuh waktu).  
- Sambil nunggu, kamu bisa **ambil piring** atau **ambil sendok**.  

Kalau synchronous → kamu cuma berdiri nunggu air mendidih, buang-buang waktu.  
Kalau asynchronous → lebih efisien karena kamu bisa multitasking.  

---

### 🔹 Cara Asynchronous di JS
#### 1. setTimeout
Jalankan kode setelah jeda waktu tertentu.  

```javascript
console.log("Mulai");
setTimeout(() => {
  console.log("Halo setelah 2 detik");
}, 2000);
console.log("Selesai");
```

📌 Hasil:  
```
Mulai
Selesai
Halo setelah 2 detik
```

#### 2. setInterval
Jalankan kode berulang-ulang tiap beberapa detik.  

```javascript
setInterval(() => {
  console.log("Loading...");
}, 1000);
```

#### 3. Promise
Janji bahwa suatu saat kerjaan selesai.  

```javascript
function cekAngka(n) {
  return new Promise((resolve, reject) => {
    if (n % 2 === 0) resolve("Genap");
    else reject("Ganjil");
  });
}

cekAngka(4).then(res => console.log(res)).catch(err => console.log(err));
```

#### 4. async/await
Cara nulis promise biar keliatan rapi.  

```javascript
async function ambilData() {
  return "Data berhasil diambil";
}

async function main() {
  let hasil = await ambilData();
  console.log(hasil);
}
main();
```

---

### 🍼 5 Studi Kasus Asynchronous
1. **Alarm**  
   - Pakai `setTimeout` buat cetak `"Bangun!"` setelah 5 detik.  

2. **Jam Dinding**  
   - Pakai `setInterval` untuk cetak jam sekarang setiap detik.  

3. **Loading Screen**  
   - Cetak `"Loading..."` setiap detik, tapi berhenti setelah 5 detik.  

4. **Cek Nomor (Promise)**  
   - Bikin `cekNomor(n)` → kalau genap `resolve("Genap")`, kalau ganjil `reject("Ganjil")`.  

5. **Data Palsu (async/await)**  
   - Fungsi `ambilUser()` yang pura-puranya ambil data setelah 3 detik.  
   - Cetak `"Data User: Budi"` setelah selesai.  

---

## 📌 Rangkuman
- Modularisasi = bikin kode rapi dengan pisah file.  
- `export` & `import` = cara saling pinjam kode.  
- Ada 2 jenis ekspor: **named** & **default**.  
- Asynchronous = kerjaan bisa jalan bareng, gak harus ngantri satu-satu.  
- Tools utama: `setTimeout`, `setInterval`, `Promise`, `async/await`.  
