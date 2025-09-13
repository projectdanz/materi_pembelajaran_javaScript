# 🏢 Soal Cerita: Permintaan dari Client

Kamu adalah seorang **junior programmer** di sebuah kursus pemrograman.  
Suatu hari, direktur kursus datang kepadamu dengan sebuah permintaan:

> “Kami butuh sebuah aplikasi kecil untuk mengelola data siswa.  
> Sederhana saja, tapi harus bisa dipakai admin untuk menambah siswa baru, melihat semua siswa, memperbarui data kalau ada perubahan, dan juga menghapus siswa kalau sudah tidak aktif.  
> Selain itu, saya pengin ada fitur cari siswa berdasarkan nama, biar gampang kalau datanya banyak.  
> Dan kalau bisa, tolong tambahkan juga fitur untuk menghitung rata-rata nilai semua siswa.  
> Oh iya, tolong kodenya dibuat rapi, dipisahkan ke beberapa file supaya mudah dikembangkan di masa depan.”  

---

## 📌 Detail Permintaan Client

### Data Siswa
- Disimpan dalam **array of object**.  
- Setiap siswa punya properti:
  - `id` (unik, auto increment mulai dari 1)  
  - `nama` (string)  
  - `kelas` (string)  
  - `nilai` (angka)  

Contoh data awal:
```js
[
  { id: 1, nama: "Ali", kelas: "JavaScript Dasar", nilai: 85 },
  { id: 2, nama: "Budi", kelas: "JavaScript Dasar", nilai: 90 }
]
Fitur Wajib (CRUD)
Tambah Siswa (Create) → admin bisa menambah siswa baru.

Tampilkan Semua Siswa (Read) → tampilkan seluruh data dengan format rapi.

Update Data Siswa (Update) → ubah data siswa berdasarkan id.

Hapus Siswa (Delete) → hapus siswa berdasarkan id.

Fitur Tambahan
Cari siswa berdasarkan nama.

Hitung rata-rata nilai semua siswa.

Saat menampilkan data, gunakan object destructuring.

Struktur Program (Modularisasi)
data.js → menyimpan array siswa.

functions.js → berisi semua function (CRUD + tambahan).

app.js → file utama untuk menjalankan aplikasi.

