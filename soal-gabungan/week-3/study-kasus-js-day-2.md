# 📚 Study Kasus JavaScript

## 1. Modularisasi (5 Kasus)
1. **Kalkulator Modular**  
   Buat 3 file JS: `math.js` (isi fungsi tambah, kurang, kali, bagi), `string.js` (isi fungsi ubah huruf besar/kecil), dan `index.js` untuk mengimpor lalu mencoba semua fungsi.
2. **Pengelola Daftar Nama**  
   Buat modul `names.js` berisi fungsi tambahNama, hapusNama, dan tampilkanNama. Gunakan di `app.js`.
3. **Perpustakaan Buku**  
   Buat modul `book.js` dengan fungsi tambahBuku, cariBuku, hapusBuku. Uji dari `main.js`.
4. **Utility Modular**  
   Buat modul `utils.js` berisi fungsi cekGanjilGenap, balikString, dan randomNumber. Gunakan di `test.js`.
5. **Game Tebak Angka**  
   Buat modul `game.js` (logika tebak angka) dan `app.js` (input dari user lalu jalankan game).

---

## 2. JSON & Object Convert (5 Kasus)
1. **Convert User Object ke JSON**  
   Buat object user {nama, umur, email}, lalu konversi ke JSON.
2. **Convert JSON ke Object**  
   Dari string JSON `{"nama":"Ali","umur":20}`, ubah ke object dan akses data.
3. **Simpan Daftar Produk**  
   Buat array of object produk, simpan dalam JSON, lalu parsing kembali.
4. **Filter dari JSON**  
   Buat JSON daftar siswa, lalu parsing dan tampilkan siswa dengan nilai > 75.
5. **Gabungkan JSON**  
   Dua string JSON berbeda (user & alamat), parsing keduanya lalu gabungkan jadi satu object.

---

## 3. setTimeout (5 Kasus)
1. **Pesan Tertunda**  
   Tampilkan "Halo dunia!" setelah 3 detik.
2. **Hitung Mundur 5 Detik**  
   Gunakan setTimeout berantai untuk menampilkan 5…4…3…2…1.
3. **Loading Simulation**  
   Tampilkan "Loading..." → 2 detik kemudian "Selesai!".
4. **Pesan Bertahap**  
   Cetak "Start" → (2 detik) "Proses…" → (2 detik) "Done".
5. **Simulasi Alarm**  
   Setelah 5 detik tampilkan "Waktunya belajar!".

---

## 4. setInterval (5 Kasus)
1. **Jam Digital**  
   Tampilkan waktu sekarang setiap 1 detik.
2. **Hitung Mundur**  
   Hitung mundur dari 10 sampai 0, lalu berhenti (clearInterval).
3. **Notifikasi Berkala**  
   Tampilkan pesan "Minum air dulu!" tiap 3 detik.
4. **Simulasi Loading**  
   Setiap 1 detik tambahkan tanda titik ke "Loading", berhenti setelah 5 kali.
5. **Counter Naik**  
   Mulai dari 0, naik terus tiap 2 detik sampai angka 10, lalu berhenti.

---

## 5. Callback Function Dasar (5 Kasus)
1. **Kalkulasi dengan Callback**  
   Buat fungsi kalkulasi(angka1, angka2, callback). Callback bisa tambah, kali, dsb.
2. **Sapa dengan Callback**  
   Buat fungsi greet(nama, callback). Callback tentukan format sapaan.
3. **Filter Angka dengan Callback**  
   Buat fungsi filterAngka(arr, callback) → callback tentukan logika (ganjil/genap).
4. **Sorting dengan Callback**  
   Buat fungsi sortData(arr, callback) → callback tentukan urutan naik/turun.
5. **Validasi Input**  
   Fungsi validasi(data, callback). Callback tentukan apakah data valid atau tidak.

---

## 6. Callback Function Anonim (5 Kasus)
1. **Hitung Luas**  
   Panggil fungsi hitung(angka, callback) dengan callback anonim untuk kuadratkan angka.
2. **Tampilkan Pesan**  
   Fungsi tampilkanPesan(callback), panggil dengan callback anonim `console.log("Halo")`.
3. **Operasi Array**  
   Gunakan forEach dengan callback anonim untuk menampilkan tiap elemen array.
4. **Filter Data**  
   Gunakan filter dengan callback anonim untuk ambil angka genap.
5. **Map Data**  
   Gunakan map dengan callback anonim untuk ubah semua angka jadi kuadrat.
