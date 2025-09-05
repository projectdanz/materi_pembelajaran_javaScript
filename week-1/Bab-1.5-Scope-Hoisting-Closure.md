# Bab 1.5: Scope, Hoisting, dan Closure

## 🎯 Tujuan Belajar
- Paham apa itu **scope** (wilayah main variabel).
- Tahu apa itu **hoisting** (JavaScript suka angkat barang ke atas).
- Bisa bikin **closure** (fungsi yang ingat sesuatu walau rumahnya udah ditutup).

---

## 1. Scope (Lingkup Variabel)

Bayangkan variabel itu kayak **mainan**.  
Mainan bisa dipakai **di mana aja** atau **hanya di dalam kamar tertentu**.  
Itulah yang disebut **scope**.

- **Global Scope** → mainan ditaruh di ruang tamu. Semua orang bisa pakai.  
- **Local/Function Scope** → mainan ditaruh di kamar. Hanya yang ada di kamar itu yang bisa main.  
- **Block Scope** → mainan ditaruh di dalam kotak kecil `{ }`, hanya bisa dipakai kalau lagi di dalam kotaknya.

### Contoh kode:
```js
let mainan = "bola"; // Global

function main() {
  let mainanDalamKamar = "mobil-mobilan"; // Local
  console.log(mainan); // bisa lihat bola
  console.log(mainanDalamKamar); // bisa lihat mobil-mobilan
}

main();
console.log(mainan); // bisa
console.log(mainanDalamKamar); // ERROR, karena di dalam kamar
```

### 🧩 5 Studi Kasus Scope
1. Buat variabel `namaSekolah` di global, lalu tampilkan di dalam fungsi.  
2. Buat variabel `namaGuru` di dalam fungsi, coba tampilkan di luar fungsi.  
3. Buat perulangan `for` dengan `let i`, cek apakah `i` bisa dipakai di luar perulangan.  
4. Bandingkan `var` dan `let` di dalam perulangan (lihat bedanya).  
5. Buat dua fungsi berbeda, masing-masing punya variabel `namaSiswa`. Apakah mereka bisa saling ganggu?

---

## 2. Hoisting

**Hoisting** itu kayak guru yang bilang:  
_"Sebelum kamu mulai main, semua mainan sudah aku taruh dulu di atas lemari."_  

Artinya, JavaScript akan **mengangkat deklarasi variabel & fungsi ke atas** sebelum kode dijalankan.

- `var` diangkat tapi nilainya **belum diisi** (jadi `undefined`).  
- `let` dan `const` diangkat tapi **disimpan di kotak terkunci** (ga bisa dipakai dulu).  
- Fungsi normal (`function nama() {}`) bisa langsung dipanggil walaupun ditulis di bawah.

### Contoh kode:
```js
console.log(nama); // undefined (karena var diangkat tapi kosong)
var nama = "Budi";

console.log(umur); // ERROR (let masih dikunci)
let umur = 10;

halo(); // bisa jalan
function halo() {
  console.log("Halo teman!");
}
```

### 🧩 5 Studi Kasus Hoisting
1. Coba tampilkan variabel `var` sebelum didefinisikan.  
2. Coba tampilkan variabel `let` sebelum didefinisikan.  
3. Coba tampilkan variabel `const` sebelum didefinisikan.  
4. Buat fungsi normal di bawah, lalu panggil di atas.  
5. Buat fungsi versi panah (`const halo = () => {}`), panggil di atas. Apa bedanya?

---

## 3. Closure

Closure itu kayak **kotak rahasia**.  
Ada fungsi kecil yang bisa **ingat isi kotak**, walau fungsi besarnya sudah selesai dipakai.  

### Contoh sederhana:
```js
function buatCelengan() {
  let saldo = 0; // uang di dalam celengan

  function isiCelengan(jumlah) {
    saldo += jumlah; 
    console.log("Saldo sekarang: " + saldo);
  }

  return isiCelengan;
}

let celenganA = buatCelengan();
celenganA(5000); // Saldo sekarang: 5000
celenganA(2000); // Saldo sekarang: 7000
```

👉 Lihat? Fungsi `isiCelengan` **ingat saldo** walaupun `buatCelengan` sudah selesai.

### 🧩 5 Studi Kasus Closure
1. Buat fungsi `buatCounter()` yang setiap dipanggil nambah 1.  
2. Buat fungsi `buatTabungan()` yang bisa menyimpan uang.  
3. Buat fungsi `buatKeranjangBelanja()` yang bisa menambahkan barang baru.  
4. Buat fungsi `buatTimer()` yang menyimpan detik setiap kali dipanggil.  
5. Buat fungsi `buatCatatanNama()` yang bisa menambahkan nama siswa ke daftar.

---

## 📝 Latihan Mandiri
1. Buat variabel global `nama`, lalu tampilkan di fungsi.  
2. Uji coba hoisting dengan `var`, `let`, dan `const`.  
3. Buat fungsi closure `pencatatanPengeluaran()` untuk menyimpan total belanja harian.

---

## 📌 Rangkuman
- **Scope** = wilayah main variabel. Bisa global, lokal, atau block.  
- **Hoisting** = JavaScript suka angkat deklarasi ke atas.  
- **Closure** = fungsi kecil yang ingat isi dari luar, walau rumahnya udah ditutup.  
