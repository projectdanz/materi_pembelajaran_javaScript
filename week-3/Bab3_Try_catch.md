# Bab 4.2: Error Handling (try...catch, then, catch, finally)

🎯 **Tujuan Pembelajaran**
- Memahami cara menangani error di JavaScript.
- Belajar menggunakan try...catch untuk mencegah program berhenti.
- Mengenal then, catch, dan finally di Promise.
- Membiasakan coding yang aman & rapi.

---

## 🧩 Kenapa Perlu Error Handling?
Bayangkan kamu pesan mie ayam via aplikasi:

- Kalau berhasil → mie datang 🍜.
- Kalau gagal → dapat notifikasi "maaf stok habis".

👉 Kalau nggak ada error handling, user bisa bingung atau aplikasi crash.

---

## 🔑 try...catch
Struktur try...catch dipakai untuk mencoba jalankan kode (try) dan kalau ada error ditangkap di bagian (catch).

```js
try {
  console.log("Mulai proses...");
  let hasil = 10 / 0; // ini valid (bukan error)
  console.log(hasil);
  
  JSON.parse("{nama:'Budi'}"); // ❌ ini error (JSON salah format)
  
  console.log("Kode setelah error (tidak jalan)");
} catch (error) {
  console.log("Terjadi error:", error.message);
}

console.log("Program tetap lanjut ✅");
📝 Hasil:

nginx
Copy code
Mulai proses...
Infinity
Terjadi error: Unexpected token n in JSON at position 1
Program tetap lanjut ✅
🔑 then, catch, finally di Promise
.then() → Jalan kalau janji berhasil (resolve).

.catch() → Jalan kalau janji gagal (reject).

.finally() → Jalan selalu, entah berhasil atau gagal.

js
Copy code
function pesanMie(adaMie) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (adaMie) {
        resolve("Mie ayam selesai 🍜");
      } else {
        reject("Mie ayam habis ❌");
      }
    }, 1000);
  });
}

pesanMie(false)
  .then((hasil) => {
    console.log("Berhasil:", hasil);
  })
  .catch((error) => {
    console.log("Gagal:", error);
  })
  .finally(() => {
    console.log("Proses pesanan selesai ✅");
  });
📝 Hasil (kalau false):

makefile
Copy code
Gagal: Mie ayam habis ❌
Proses pesanan selesai ✅
🔑 try...catch dengan async/await
js
Copy code
async function sarapan() {
  try {
    console.log("Pesan teh...");
    
    let hasil = await buatTeh(false); // simulasi gagal
    console.log(hasil);
    
  } catch (error) {
    console.log("Error saat bikin teh:", error);
  } finally {
    console.log("Proses bikin teh selesai ✅");
  }
}

function buatTeh(adaTeh) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (adaTeh) {
        resolve("Teh sudah siap ☕");
      } else {
        reject("Teh habis ❌");
      }
    }, 2000);
  });
}

sarapan();
📝 Hasil:

javascript
Copy code
Pesan teh...
Error saat bikin teh: Teh habis ❌
Proses bikin teh selesai ✅
📝 Latihan Mandiri
Buat Promise cuciBaju() (butuh 2 detik).

Kalau ada deterjen → "Baju sudah bersih 👕".

Kalau tidak ada → "Deterjen habis ❌".

Panggil dengan .then, .catch, .finally.

Ubah dengan versi async/await + try...catch.

📌 Rangkuman
try...catch → mencegah program berhenti saat error.

then() → dijalankan saat janji berhasil.

catch() → dijalankan saat janji gagal.

finally() → dijalankan selalu, apapun hasilnya.

Gunakan try...catch di async/await untuk tangani error.