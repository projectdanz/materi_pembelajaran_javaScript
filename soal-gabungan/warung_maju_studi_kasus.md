# 🏪 Studi Kasus: Warung Maju Jaya

## 📖 Soal Cerita
Suatu hari ada sebuah warung bernama **Warung Maju Jaya**.  
Warung ini menjual beberapa barang: *Indomie, Teh Botol, dan Kopi*.  

Tugas kamu adalah membuat program sederhana dengan **JavaScript** yang bisa melakukan hal-hal berikut:

1. **Tambah barang baru** ke daftar warung.
2. **Cari barang** berdasarkan nama.
3. **Hitung total belanjaan** dari beberapa barang yang dibeli.
4. **Update stok barang** setelah ada pembelian.
5. Tambahkan **promo berkedip setiap 3 detik** menggunakan `setInterval`.  
   Promo otomatis berhenti setelah 5 kali muncul.

Gunakan semua materi yang sudah dipelajari:
- Variabel  
- Operator (aritmatika, perbandingan, logika)  
- Function  
- Array & Array Method  
- Object  
- Destructuring  
- Spread & Rest  
- Modularisasi (import & export)  
- `setInterval` & `clearInterval`  

---

## 📂 Struktur Folder
```
warungMaju/
│── barang.js
│── utils.js
│── main.js
```

---

## 📑 Kerangka Jawaban

### **barang.js**
```javascript
// Data barang awal
const barang = [
  { id: 1, nama: "Indomie", harga: 3000, stok: 10 },
  { id: 2, nama: "Teh Botol", harga: 5000, stok: 8 },
  { id: 3, nama: "Kopi", harga: 4000, stok: 15 }
];

// Export biar bisa dipakai di file lain
export default barang;
```

---

### **utils.js**
```javascript
// Import data barang
import barang from "./barang.js";

// 1. Tambah barang baru
export function tambahBarang(barangBaru) {
  // TODO: gunakan spread operator ...
  // return [...barang, barangBaru]
}

// 2. Cari barang berdasarkan nama
export function cariBarang(nama) {
  // TODO: gunakan find()
  // return barang.find(...)
}

// 3. Hitung total harga belanjaan
export function hitungTotal(belanjaan) {
  // belanjaan = array berisi id barang
  // TODO: gunakan map() atau reduce()
  // return totalHarga
}

// 4. Update stok barang
export function updateStok(id, jumlahBeli) {
  // TODO: cari barang berdasarkan id
  // Destructuring stok
  // stok = stok - jumlahBeli
  // return barang yg sudah diupdate
}
```

---

### **main.js**
```javascript
import barang from "./barang.js";
import { tambahBarang, cariBarang, hitungTotal, updateStok } from "./utils.js";

// 1. Tambah barang baru
// console.log(tambahBarang({ id: 4, nama: "Roti", harga: 2000, stok: 20 }));

// 2. Cari barang
// console.log(cariBarang("Kopi"));

// 3. Hitung total belanjaan
// let belanjaan = [1, 2, 3]; // id barang yang dibeli
// console.log("Total Harga:", hitungTotal(belanjaan));

// 4. Update stok
// console.log(updateStok(1, 2)); // beli 2 Indomie

// 5. Promo setInterval
let hitung = 0;
const promo = setInterval(() => {
  hitung++;
  console.log("🔥 Promo Diskon 20% berlaku sekarang!");
  
  if (hitung === 5) {
    clearInterval(promo);
    console.log("Promo selesai ❌");
  }
}, 3000);
```

---

## 🎯 Catatan
- Murid harus **melengkapi logika function** di `utils.js`.
- Latihan **import/export** antar file.
- Latihan **destructuring**, **spread**, dan **array method**.
- Latihan **setInterval** + **clearInterval**.
