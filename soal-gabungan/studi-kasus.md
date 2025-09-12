# 🎯 Studi Kasus: Sistem Pemesanan Restoran

Seorang **client** (pemilik restoran online) datang kepadamu sebagai programmer. Dia ingin kamu membuat simulasi data dan operasi sederhana menggunakan **JavaScript**.  

---

## 📖 Cerita Kasus
Client berkata:  
> "Saya punya restoran online. Saya ingin datanya bisa disimpan dalam JavaScript agar gampang diuji sebelum masuk database. Tolong buatkan saya simulasi yang bisa:  
> 1. Menyimpan data menu makanan dalam **array of object**.  
> 2. Bisa mencari menu tertentu dengan cepat (misalnya menu dengan harga di bawah Rp30.000).  
> 3. Bisa menghitung total semua harga menu.  
> 4. Bisa menampilkan daftar nama menu saja.  
> 5. Bisa mengambil data dari object dengan cepat menggunakan **destructuring**."  

---

## 📝 Tugas (Soal Studi Kasus)

1. **Buat sebuah array of object** bernama `menu` yang berisi minimal 5 makanan.  
   Tiap object punya property:  
   - `nama` (string)  
   - `kategori` (string, contoh: "makanan", "minuman")  
   - `harga` (number)  

2. **Gunakan `forEach`** untuk menampilkan semua menu dengan format:  
   ```
   Nama: Nasi Goreng | Kategori: Makanan | Harga: 20000
   ```

3. **Gunakan `filter`** untuk mencari semua makanan/minuman dengan harga di bawah Rp30.000.

4. **Gunakan `map`** untuk membuat array baru yang hanya berisi nama-nama menu.

5. **Gunakan `reduce`** untuk menghitung total harga semua menu.

6. **Gunakan `find`** untuk mencari satu menu dengan nama tertentu (misal: "Es Teh").

7. **Gunakan destructuring array** untuk mengambil 2 makanan pertama dari `menu` ke variabel `makanan1` dan `makanan2`.

8. **Gunakan destructuring object** untuk mengambil `nama` dan `harga` dari salah satu menu (misal `menu[0]`).

---

## 🎯 Contoh Output yang Diharapkan
```
Daftar Menu:
Nama: Nasi Goreng | Kategori: Makanan | Harga: 20000
Nama: Ayam Bakar  | Kategori: Makanan | Harga: 35000
...

Menu murah (<30000):
Nasi Goreng, Es Teh, Tahu Crispy

Nama-nama Menu:
["Nasi Goreng", "Ayam Bakar", "Es Teh", "Sate Ayam", "Tahu Crispy"]

Total Harga Semua Menu:
100000

Menu ditemukan:
Es Teh

Destructuring Array:
makanan1 = { nama: "Nasi Goreng", harga: 20000 }
makanan2 = { nama: "Ayam Bakar", harga: 35000 }

Destructuring Object:
nama = "Nasi Goreng", harga = 20000
```
