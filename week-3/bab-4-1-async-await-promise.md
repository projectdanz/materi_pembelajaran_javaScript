# Bab 4.1: Async, Await, & Promise

## 🎯 Tujuan Pembelajaran
- Mengenal konsep asynchronous (kerjaan bisa ditunda).
- Memahami Promise sebagai "janji hasil".
- Belajar menggunakan async dan await untuk menunggu janji.
- Membuat kode lebih mudah dibaca seperti alur cerita.

---

## 🧩 Apa Itu Asynchronous?
Bayangkan kamu pesan mie ayam:
- Kamu pesan → tukang mie mulai masak (butuh waktu).
- Sambil nunggu, kamu bisa scroll HP.
- Kalau mie sudah selesai, baru kamu makan.

👉 Itulah asynchronous: ada kerjaan yang butuh waktu, tapi komputer nggak diem aja, dia bisa lanjut kerja lain.

---

## 🔑 Apa Itu Promise?
Promise adalah janji di JavaScript.  
Artinya: "Aku janji nanti bakal kasih hasil, tapi sekarang belum tentu sudah ada."

Promise punya 3 kondisi:
- **Pending** → janji masih proses (belum ada hasil).
- **Fulfilled** → janji ditepati (berhasil).
- **Rejected** → janji gagal ditepati (error).

### Contoh Promise
```javascript
let janji = new Promise((resolve, reject) => {
  let jadi = true;

  if (jadi) {
    resolve("Mie ayam selesai 🍜"); // janji ditepati
  } else {
    reject("Mie ayam habis ❌");   // janji gagal
  }
});

janji.then((hasil) => {
  console.log(hasil);
}).catch((error) => {
  console.log(error);
});
```

📌 **resolve()** = janji berhasil.  
📌 **reject()** = janji gagal.  
📌 **then()** = apa yang dilakukan kalau janji berhasil.  
📌 **catch()** = apa yang dilakukan kalau janji gagal.

---

## 🔑 Async & Await
- **async** = bikin fungsi bisa jalan asynchronous.  
- **await** = nunggu janji (Promise) selesai.

### Contoh dengan Promise + Async/Await
```javascript
// fungsi bikin janji masak mie
function masakMie() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Mie ayam sudah jadi 🍜");
    }, 2000);
  });
}

// fungsi utama
async function makan() {
  console.log("Pesan mie ayam...");

  let hasil = await masakMie(); // nunggu janji selesai

  console.log(hasil);
  console.log("Sekarang bisa makan!");
}

makan();
```

**Hasil di Console:**
```
Pesan mie ayam...
(2 detik kemudian)
Mie ayam sudah jadi 🍜
Sekarang bisa makan!
```

---

## 🏗️ Studi Kasus
### 1. Membeli Buku Online
```javascript
function beliBuku() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Buku sampai di rumah 📚"), 1500);
  });
}

async function bacaBuku() {
  console.log("Pesan buku...");
  let hasil = await beliBuku();
  console.log(hasil);
  console.log("Sekarang bisa membaca buku!");
}

bacaBuku();
```

---

### 2. Upload Foto ke Server
```javascript
function uploadFoto() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Foto berhasil diupload 📸"), 2000);
  });
}

async function prosesUpload() {
  console.log("Mulai upload foto...");
  let hasil = await uploadFoto();
  console.log(hasil);
}

prosesUpload();
```

---

### 3. Ambil Data Cuaca (Simulasi API)
```javascript
function ambilCuaca() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Cuaca hari ini cerah ☀️"), 1000);
  });
}

async function cekCuaca() {
  console.log("Cek cuaca...");
  let hasil = await ambilCuaca();
  console.log(hasil);
}

cekCuaca();
```

---

### 4. Simulasi Login
```javascript
function login(username, password) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (username === "admin" && password === "1234") {
        resolve("Login berhasil ✅");
      } else {
        reject("Login gagal ❌");
      }
    }, 2000);
  });
}

async function prosesLogin() {
  console.log("Sedang login...");
  try {
    let hasil = await login("admin", "1234");
    console.log(hasil);
  } catch (error) {
    console.log(error);
  }
}

prosesLogin();
```

---

### 5. Membuat Teh
```javascript
function buatTeh() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Teh sudah siap ☕"), 3000);
  });
}

async function sarapan() {
  console.log("Pesan teh...");
  let hasil = await buatTeh();
  console.log(hasil);
  console.log("Sekarang minum teh.");
}

sarapan();
```

---

## 📝 Latihan Mandiri
- Buat fungsi `buatKopi()` yang butuh 2 detik untuk selesai, hasilnya `"Kopi sudah siap ☕"`.
- Buat fungsi `mulaiNgoding()`:
  - Cetak `"Pesan kopi..."`.
  - Tunggu hasil `buatKopi()` dengan **await**.
  - Cetak hasilnya.
  - Terus tulis `"Sekarang ngoding sambil ngopi."`.

---

## 📌 Rangkuman
- **Promise** = janji yang bisa *pending*, *fulfilled*, atau *rejected*.  
- **resolve** = janji ditepati.  
- **reject** = janji gagal.  
- **then** = jalan kalau berhasil.  
- **catch** = jalan kalau gagal.  
- **async/await** = cara mudah menunggu Promise selesai.
