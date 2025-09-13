# Bab 3.2: Belajar JSON (Bahasa Data)

## 🎯 Tujuan Belajar
- Kenal apa itu **JSON** (cara menulis data supaya gampang dipahami komputer & manusia).  
- Bisa **mengubah data biasa jadi JSON**.  
- Bisa **membaca JSON jadi data biasa lagi**.  
- Tahu JSON dipakai buat apa di dunia nyata.  

---

## 📖 Penjelasan Materi

### 1. Apa itu JSON?  
Bayangkan kamu punya **kotak penyimpanan data**. Supaya kotak ini rapi, data ditulis dengan aturan khusus.  
Nah aturan itu namanya **JSON** (JavaScript Object Notation).  

JSON itu:  
- Ringan (nggak ribet).  
- Bisa dibaca manusia (kayak tulisan biasa).  
- Bisa dibaca mesin (komputer paham aturannya).  

JSON biasanya dipakai kalau komputer **berbicara dengan komputer lain**.  
Contoh: server kasih data ke web browser.  

---

### 2. Contoh Data JSON
```json
{
  "nama": "Budi",
  "umur": 17,
  "alamat": "Jl. Melati No. 10",
  "hobi": ["membaca", "berenang", "ngoding"]
}
```

👉 Perhatikan:  
- Ada **key (kunci)** → `"nama"`, `"umur"`, `"alamat"`, `"hobi"`.  
- Ada **value (nilai)** → `"Budi"`, `17`, `"Jl. Melati..."`, `[...]`.  

---

### 3. Ciri-Ciri JSON  
- Selalu pakai **key-value** (kunci → nilai).  
- Kunci harus **pakai tanda kutip dua** `"..."`.  
- Nilai boleh berupa:  
  - **String** (tulisan dalam `"..."`)  
  - **Number** (angka, misalnya 17)  
  - **Boolean** (`true` atau `false`)  
  - **Array** (`[...]`)  
  - **Object** (`{...}`)  
  - **null** (kosong)  
- ❌ JSON tidak boleh menyimpan **fungsi** (hanya data).  

---

### 4. Bedanya JSON dengan Objek JavaScript  
- JSON: selalu pakai `"..."` di key.  
- Objek JS: boleh tanpa kutip.  

Contoh Objek JS:
```js
let orang = { nama: "Budi", umur: 17 };
```

Contoh JSON:
```json
{ "nama": "Budi", "umur": 17 }
```

---

### 5. Konversi JSON <-> JavaScript  
JavaScript punya 2 alat penting:  

1. `JSON.stringify()` → ubah **object JS → string JSON**.  
   ```js
   let orang = { nama: "Budi", umur: 17 };
   let jsonString = JSON.stringify(orang);
   console.log(jsonString); 
   // Hasil: {"nama":"Budi","umur":17}
   ```

2. `JSON.parse()` → ubah **string JSON → object JS**.  
   ```js
   let data = '{"nama":"Budi","umur":17}';
   let orang = JSON.parse(data);
   console.log(orang.nama); 
   // Hasil: Budi
   ```

---

### 6. Penggunaan JSON di Dunia Nyata
1. **API**  
   - Server kirim data ke web dalam bentuk JSON.  
   - Contoh respon API:  
     ```json
     { "status": "ok", "user": "Budi" }
     ```

2. **Penyimpanan di Browser**  
   - Simpan data JSON di `localStorage`.  

3. **Konfigurasi Program**  
   - Contoh: file `package.json` di Node.js.  

---

### 7. Tips Praktis
- Gunakan `try...catch` saat `JSON.parse()` (jaga-jaga kalau datanya rusak).  
- Jangan simpan **fungsi** dalam JSON.  
- Pastikan format JSON valid sebelum dipakai.  

---

## ✍️ Latihan Mandiri
1. Buat objek JavaScript berisi data diri (nama, umur, alamat).  
   Ubah ke JSON pakai `JSON.stringify()`.  
2. Simpan data JSON di `localStorage`.  
3. Ambil lagi datanya pakai `JSON.parse()` dan tampilkan.  
4. Ambil data dari API publik (contoh: https://jsonplaceholder.typicode.com/users) lalu tampilkan di console.  

---

## 📌 Rangkuman
- JSON = format penyimpanan & kirim data.  
- Pakai `JSON.stringify()` untuk ubah object → JSON.  
- Pakai `JSON.parse()` untuk ubah JSON → object.  
- Dipakai di API, localStorage, dan konfigurasi program.  

---

## 🎯 Evaluasi Harian (Studi Kasus)
**Tugas:**  
Buat halaman HTML sederhana yang menampilkan daftar produk.  

### 🔹 Skenario:  
- Data produk (misalnya: nama, harga, stok) disimpan di `localStorage` dalam bentuk JSON.  
- Saat halaman dibuka, data dibaca dan ditampilkan di web.  

### 🔹 Contoh data produk:
```json
[
  { "nama": "Laptop", "harga": 7000000, "stok": 5 },
  { "nama": "HP", "harga": 3000000, "stok": 10 },
  { "nama": "Headset", "harga": 200000, "stok": 15 }
]
```
