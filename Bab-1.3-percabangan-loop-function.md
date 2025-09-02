# Bab 1.3: Struktur Kontrol (Percabangan & Perulangan)

## 🎯 Tujuan Pembelajaran
- Memahami alur kontrol dalam program
- Bisa membuat percabangan dengan `if`, `else if`, `else`, dan `switch`
- Bisa memakai perulangan `for`, `while`, dan `do...while`

---

## 📝 Penjelasan Materi

### 1. Percabangan (Conditional Statement)
Percabangan itu seperti jalan bercabang. Komputer harus memilih jalur mana yang dipakai berdasarkan kondisi tertentu.

#### 👉 `if`, `else if`, `else`
Gunanya untuk membuat keputusan dengan beberapa kemungkinan.

```javascript
let umur = 18;

if (umur < 12) {
  console.log("Anak-anak");
} else if (umur < 18) {
  console.log("Remaja");
} else {
  console.log("Dewasa");
}
```

**5 Studi Kasus:**
1. Menentukan apakah angka ganjil atau genap.
2. Menentukan apakah seseorang boleh masuk bioskop (usia > 17).
3. Menentukan apakah suhu termasuk dingin, normal, atau panas.
4. Mengecek login dengan username dan password.
5. Mengecek apakah nilai ujian lulus atau tidak.

---

#### 👉 `switch`
Dipakai kalau pilihannya sudah pasti/terbatas.

```javascript
let hari = 3;

switch (hari) {
  case 1:
    console.log("Senin");
    break;
  case 2:
    console.log("Selasa");
    break;
  case 3:
    console.log("Rabu");
    break;
  default:
    console.log("Hari tidak valid");
}
```

**5 Studi Kasus:**
1. Menampilkan nama bulan dari angka (1–12).
2. Menampilkan menu makanan berdasarkan pilihan nomor.
3. Menentukan jenis kelamin (L/P).
4. Menentukan tingkat pendidikan (SD, SMP, SMA).
5. Menentukan status lampu lalu lintas (Merah, Kuning, Hijau).

---

### 2. Perulangan (Looping)
Perulangan itu seperti saat kamu disuruh menulis "Saya tidak akan terlambat lagi" sebanyak 10 kali. Kamu tidak perlu tulis manual, komputer bisa otomatis mengulang.

#### 👉 `for`
Digunakan kalau **jumlah pengulangan sudah jelas**.

```javascript
for (let i = 1; i <= 5; i++) {
  console.log("Perulangan ke-" + i);
}
```

**5 Studi Kasus:**
1. Cetak angka 1 sampai 100.
2. Cetak semua bilangan genap dari 1 sampai 50.
3. Hitung jumlah dari angka 1 sampai 10.
4. Buat tabel perkalian 5.
5. Cetak bintang membentuk segitiga.

---

#### 👉 `while`
Dipakai kalau **kita tidak tahu pasti berapa kali harus mengulang**, tapi ada kondisi yang harus dicek.

```javascript
let angka = 1;
while (angka <= 5) {
  console.log("Angka ke-" + angka);
  angka++;
}
```

**5 Studi Kasus:**
1. Terus minta password sampai benar.
2. Jalan terus sampai bensin habis.
3. Ulangi lempar dadu sampai dapat angka 6.
4. Terus tambah uang tabungan sampai cukup untuk beli barang.
5. Ulangi proses input sampai user mengetik "stop".

---

#### 👉 `do...while`
Hampir sama dengan `while`, tapi **pasti dijalankan sekali dulu**, baru dicek kondisinya.

```javascript
let angka = 1;
do {
  console.log("Angka ke-" + angka);
  angka++;
} while (angka <= 5);
```

**5 Studi Kasus:**
1. Menampilkan menu minimal sekali walau input salah.
2. Meminta user memasukkan angka minimal sekali.
3. Cetak daftar belanja minimal sekali.
4. Tampilkan iklan minimal sekali meskipun user klik skip.
5. Coba login minimal sekali walau salah.

---

### 📌 Kapan dan Kenapa Memakai Loop?
- **for** → dipakai kalau jumlah pengulangan sudah jelas. Contoh: cetak angka 1–10.
- **while** → dipakai kalau jumlah pengulangan belum jelas, tergantung kondisi. Contoh: terus ulangi sampai password benar.
- **do...while** → dipakai kalau kamu ingin jalankan minimal sekali dulu. Contoh: tampilkan menu minimal sekali walaupun user salah input.

---

## 🏋️ Latihan Mandiri
1. Buat program yang memeriksa apakah usia termasuk anak-anak, remaja, atau dewasa.
2. Gunakan `for` loop untuk mencetak angka 1 sampai 10.
3. Buat `switch` statement untuk menampilkan nama hari dari angka (1–7).

---

## 📝 Rangkuman
- Percabangan dipakai untuk membuat keputusan logika dalam program.
- `if...else` cocok untuk kondisi fleksibel/kompleks, `switch` cocok untuk pilihan tetap.
- Loop dipakai untuk mengulang: `for` (jumlah pasti), `while` (jumlah tidak pasti), `do...while` (jalan minimal sekali).

---

## 🎯 Evaluasi Harian (Studi Kasus)
Kamu sedang membuat sistem penilaian otomatis. Tulis program JavaScript yang menerima nilai siswa, lalu menentukan grade-nya:

- A jika >= 90  
- B jika >= 80  
- C jika >= 70  
- D jika >= 60  
- E jika < 60  

Tampilkan hasilnya dengan teks:  
`"Nilai kamu: B (Bagus)"`

---

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
