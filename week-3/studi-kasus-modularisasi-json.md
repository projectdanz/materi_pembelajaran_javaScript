# 📘 Studi Kasus – Modularisasi & JSON

### 🎯 Tujuan
- Memahami bagaimana membagi kode ke dalam **modul** (export/import).
- Menggunakan **JSON** untuk menyimpan, membaca, dan memanipulasi data.

---

## 1. Modul Biodata Sederhana  
Buat sebuah file `biodata.js` yang mengekspor objek JSON berisi data diri (`nama`, `umur`, `alamat`).  
Lalu import di `index.js` dan tampilkan biodata ke console.

---

## 2. Modul Operasi Matematika  
Buat file `math.js` yang berisi fungsi `tambah`, `kurang`, `kali`, `bagi`.  
Export semua fungsi.  
Import di `index.js`, lalu hitung:  
- 20 + 5  
- 30 - 10  
- 6 × 7  
- 50 ÷ 2  

---

## 3. Daftar Produk JSON  
Buat file `produk.json` yang berisi array objek produk (`id`, `nama`, `harga`).  
Import JSON di `index.js` lalu tampilkan semua produk dengan format:  
`Produk: [nama], Harga: [harga]`

---

## 4. Modul Helper Format Rupiah  
Buat file `helper.js` dengan fungsi `formatRupiah(number)` yang mengubah angka menjadi format rupiah.  
Gunakan untuk menampilkan harga produk dari `produk.json`.

---

## 5. Simpan dan Ambil Data User  
Buat `user.json` berisi daftar user (`id`, `username`, `email`).  
Buat modul `userService.js` dengan fungsi:  
- `getAllUser()` → tampilkan semua user  
- `getUserById(id)` → cari user berdasarkan id  

---

## 6. Modul CRUD Task  
Buat `taskService.js` yang menyimpan daftar task dalam array JSON.  
Fungsi yang harus ada:  
- `addTask(judul)`  
- `getAllTask()`  
- `deleteTask(id)`  

Gunakan di `index.js` untuk menambah 3 task, tampilkan semua, lalu hapus 1 task.

---

## 7. Modul Auth Sederhana  
Buat `auth.js` dengan fungsi:  
- `login(username, password)` → cek apakah cocok dengan data di `users.json`.  
- `register(username, password)` → tambahkan user baru ke `users.json`.  

---

## 8. Import JSON API (dummy)  
Gunakan `fetch` untuk ambil data JSON dari:  
`https://jsonplaceholder.typicode.com/posts`  
Buat modul `postService.js` dengan fungsi `getPosts()` dan tampilkan 5 post pertama di `index.js`.

---

## 9. Modul Statistik Nilai  
Buat file `nilai.json` berisi array nilai angka.  
Buat modul `statistik.js` dengan fungsi:  
- `rataRata()`  
- `nilaiTertinggi()`  
- `nilaiTerendah()`  

Import dan tampilkan hasilnya.

---

## 10. Mini Project – Aplikasi Perpustakaan  
- Buat `books.json` berisi daftar buku (`id`, `judul`, `penulis`, `tahun`).  
- Buat `libraryService.js` dengan fungsi:  
  - `getAllBooks()`  
  - `addBook(book)`  
  - `findBookByTitle(title)`  
- Buat `index.js` untuk menambah buku baru, menampilkan semua buku, dan mencari buku tertentu.  

---
