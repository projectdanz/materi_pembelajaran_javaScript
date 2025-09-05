# Bab 1.4: Fungsi – Deklarasi, Parameter, Return

## 🎯 Tujuan Pembelajaran
- Memahami konsep fungsi dalam JavaScript
- Bisa membuat fungsi dengan parameter dan return
- Mengetahui perbedaan antara deklarasi, ekspresi, dan arrow function

---

## 📝 Penjelasan Materi

### Apa itu Fungsi?
Fungsi adalah blok kode yang bisa dipakai berulang-ulang. Daripada menulis kode yang sama berkali-kali, kita bungkus dalam satu fungsi.

---

### 1. Fungsi Deklaratif
```javascript
function sapa() {
  console.log("Halo, selamat datang!");
}
sapa();
```

**5 Studi Kasus:**
1. Fungsi untuk menyapa user.
2. Fungsi untuk menghitung luas persegi.
3. Fungsi untuk menampilkan biodata.
4. Fungsi untuk mengecek bilangan ganjil/genap.
5. Fungsi untuk mencetak daftar menu.

---

### 2. Fungsi Ekspresi
Fungsi disimpan ke dalam variabel.

```javascript
let hitungLuas = function(panjang, lebar) {
  return panjang * lebar;
};
console.log(hitungLuas(5, 4));
```

**5 Studi Kasus:**
1. Fungsi hitung luas segitiga.
2. Fungsi hitung keliling lingkaran.
3. Fungsi menambahkan dua angka.
4. Fungsi mengubah huruf jadi kapital.
5. Fungsi menghitung diskon belanja.

---

### 3. Arrow Function (ES6)
Bentuk singkat dari fungsi.

```javascript
let tambah = (a, b) => a + b;
console.log(tambah(3, 2));
```

**5 Studi Kasus:**
1. Fungsi mengurangi angka.
2. Fungsi menghitung pajak.
3. Fungsi menampilkan salam.
4. Fungsi menghitung umur dari tahun lahir.
5. Fungsi mengonversi suhu Celcius ke Fahrenheit.

---

### Parameter dan Return
- **Parameter** → input ke dalam fungsi.
- **Return** → output dari fungsi.

```javascript
function kali(a, b) {
  return a * b;
}
console.log(kali(4, 5)); // 20
```

**5 Studi Kasus:**
1. Fungsi menghitung nilai rata-rata.
2. Fungsi menggabungkan dua string.
3. Fungsi mencari angka terbesar dari 2 angka.
4. Fungsi menghitung luas lingkaran.
5. Fungsi menghitung gaji bersih setelah potongan.

---

## 📝 Rangkuman
- Fungsi = blok kode yang bisa dipakai ulang.
- Ada 3 jenis utama: deklaratif, ekspresi, dan arrow function.
- Parameter adalah input, return adalah output.

---