![Header Image](https://rumahitindonesia.com/wp-content/uploads/2023/11/1.png)

# 🌟 بِسْمِ اللهِ الرَّحْمٰنِ الرَّحِيْمِ

*Dengan menyebut nama Allah Yang Maha Pengasih lagi Maha Penyayang*

---

## Doa Sebelum Menuntut Ilmu

**اللَّهُمَّ انْفَعْنَا بِمَا عَلَّمْتَنَا وَعَلِّمْنَا مَا يَنْفَعُنَا وَزِدْنَا عِلْمًا**

> "Ya Allah, manfaatkanlah ilmu yang telah Engkau ajarkan kepada kami, ajarkanlah kami ilmu yang bermanfaat, dan tambahkanlah kami ilmu."

**اللّهُمَّ لاَ سَهْلَ إِلاَّ مَا جَعَلْتَهُ سَهْلاً، وَأَنْتَ تَجْعَلُ الْحَزْنَ إِذَا شِئْتَ سَهْلاً**

> "Ya Allah, tidak ada kemudahan kecuali yang Engkau jadikan mudah, dan Engkau menjadikan kesulitan itu mudah jika Engkau kehendaki."

---

# Soal Evaluasi Akhir — Proyek Web Sederhana (Frontend JS)

> Instruksi ini berisi deskripsi proyek, daftar fitur wajib, teknologi & konsep yang harus dipakai, struktur folder contoh, kriteria penilaian, checklist pengumpulan, panduan deploy ke Vercel, dan outline slide presentasi. Silakan gunakan langsung atau sesuaikan.

---

## 1. Deskripsi Proyek (singkat)

Buat sebuah **website yang bermanfaat** (pilih salah satu: aplikasi cuaca, aplikasi catatan, aplikasi manajemen tugas, katalog produk, atau aplikasi Al-Qur’an). Website harus interaktif, modular, dan memakai teknik modern JavaScript (fetch/async/await, error handling, DOM manipulation, localStorage/sessionStorage, dll.). Minimal **2 halaman** (mis. `index.html` + `detail.html` atau `index.html` + `about.html`).

---

## 2. Daftar Fitur Wajib

Setiap tim/siswa harus mengimplementasikan semua item ini:

1. **Fetch API**

   * Ambil data dari API publik (mis. data cuaca / daftar produk / ayat Al-Qur’an / placeholder JSON).
2. **Error handling**

   * Gunakan `try...catch` ketika melakukan fetch dan operasi penting lain; tampilkan pesan error di UI jika terjadi.
3. **async/await**

   * Semua pengambilan data memakai `async/await` (bukan `.then` chaining).
4. **Modularisasi**

   * Pisahkan kode ke modul/file berbeda (mis. `api.js`, `ui.js`, `storage.js`, `main.js`). Gunakan ES Modules (`export` / `import`) atau pattern modul.
5. **DOM manipulation**

   * Render daftar, detail, form input secara dinamis; update DOM saat data berubah.
6. **localStorage & sessionStorage**

   * Simpan data yang relevan: mis. preferensi pengguna, cache fetch, atau draft catatan.
7. **Minimal 2 halaman**

   * Halaman utama + halaman detail (contoh: klik item → buka `detail.html?id=...`).
8. **Struktur folder rapi**

   * Contoh: `src/`, `modules/`, `assets/` (lihat contoh di bawah).
9. **UI sederhana & rapi**

   * CSS dasar atau framework ringan (Tailwind/Bootstrap CDN diperbolehkan).

---

## 3. Konsep & Teknologi yang Harus Dipakai

Siswa wajib menggunakan dan menunjukkan pemahaman pada konsep ini:

* **Fetch API** (GET/POST jika relevan)
* **async/await** + **try...catch**
* **Promises** (tunjukkan minimal satu penggunaan eksplisit atau penjelasan)
* **Callback function** (contoh: callback validasi atau callback pada event handler)
* **JSON**: `JSON.parse()` & `JSON.stringify()` saat menyimpan/menarik data
* **Array & Object** (manipulasi data, state management sederhana)
* **Destructuring & Spread operator** (`...`)
* **Array methods**: `map`, `filter`, `reduce`, `forEach`, dsb.
* **Dasar JS**: variabel (`let/const`), fungsi, kontrol alur (`if`, `switch`, loops).
* **Modular JS**: `import`/`export` atau module pattern.
* **localStorage/sessionStorage** untuk menyimpan state/setting/temp data.

---

## 4. Contoh Struktur Folder (direkomendasikan)

```
project-name/
├─ index.html
├─ detail.html
├─ assets/
│  ├─ css/
│  │  └─ styles.css
│  └─ img/
├─ src/
│  ├─ main.js            // entry (import modul lain)
│  ├─ modules/
│  │  ├─ api.js         // fungsi fetch / komunikasi API
│  │  ├─ ui.js          // fungsi render DOM
│  │  ├─ storage.js     // wrapper localStorage/sessionStorage
│  │  └─ utils.js       // helper: format date, dll.
│  └─ components/       // optional: small components
└─ README.md
```

---

## 5. Contoh Minimal Cara Modularisasi (snippet)

```js
// src/modules/api.js
export async function fetchItems() {
  try {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts');
    if (!res.ok) throw new Error('Network response not ok');
    return await res.json();
  } catch (err) {
    throw err; // ditangani oleh caller
  }
}

// src/main.js
import { fetchItems } from './modules/api.js';
import { renderList, showError } from './modules/ui.js';

(async function init() {
  try {
    const items = await fetchItems();
    renderList(items);
  } catch (e) {
    showError(e.message);
  }
})();
```

---

## 6. Kriteria Penilaian & Bobot (contoh — total 100 poin)

1. **Fungsionalitas (40 pts)**

   * Semua fitur wajib berjalan (fetch, detail page, storage, dll) — 25 pts
   * Error handling & UX saat error — 5 pts
   * Responsiveness / navigasi antar halaman — 10 pts
2. **Penerapan Materi & Teknik JS (25 pts)**

   * Penggunaan async/await, try/catch — 8 pts
   * Modularisasi & penggunaan module — 7 pts
   * Penggunaan array methods, destructuring, promises, callbacks — 10 pts
3. **Kebersihan Kode & Struktur (15 pts)**

   * Kode rapi, jelas, komentar cukup, struktur folder baik — 10 pts
   * README & instruksi menjalankan proyek — 5 pts
4. **UI / UX (10 pts)**

   * Tampilan sederhana tapi rapi; aksesibilitas dasar (label form, tombol jelas) — 6 pts
   * Interaksi halus (loading state, feedback) — 4 pts
5. **Kreativitas & Nilai Tambah (10 pts)**

   * Fitur ekstra, orisinalitas, optimasi/performance — 10 pts

**Catatan penilaian**: berikan deskripsi rubrik (Excellent / Good / Fair / Poor) untuk tiap bagian saat menilai.

---

## 7. Kriteria Penilaian Detil (rubrik singkat)

* **Fungsionalitas (25 pts)**

  * Excellent (22–25): Semua fitur wajib lengkap, semua API bekerja, navigasi & detail sempurna.
  * Good (17–21): Minor bug non-kritis.
  * Fair (12–16): Beberapa fitur tak jalan, tapi inti masih ada.
  * Poor (<12): Banyak fitur tak jalan.
* **Error Handling (5 pts)**

  * Menangani network error & menampilkan pesan user-friendly.
* **Modular & Code Quality (15 pts)**

  * Module terpisah, naming konsisten, tidak ada duplications.
* **LocalStorage/sessionStorage (5 pts)**

  * Ada penggunaan nyata dan dokumentasinya (apa disimpan & mengapa).
* **Async/Promises/Callbacks/Array methods (10 pts)**

  * Tunjukkan kombinasi penggunaan yang jelas.
* **UI/UX & Kreativitas (20 pts)**

  * Simpel tapi menarik; plus creative feature.

---

## 8. Panduan Pengumpulan

Siswa wajib menyerahkan:

* Link GitHub repository (public/private dengan akses) **atau** file zip.
* README.md yang berisi: deskripsi singkat, cara menjalankan, daftar fitur, API yang dipakai (dan jika perlu: API key).
* Tanya jawab singkat (3–5 poin) apa tantangan yang ditemui dan bagaimana menyelesaikannya.
* Demo live (opsional) — GitHub Pages atau Netlify.

---

## 9. Checklist Penilaian Otomatis & Manual (untuk penguji)

* [ ] `index.html` berisi daftar item yang dirender dari API.
* [ ] Ketika klik item, buka `detail.html?id=...` dan tampilkan data detail.
* [ ] Semua fetch memakai `async/await`.
* [ ] Ada `try...catch` yang menangani error fetch, menampilkan pesan ke user.
* [ ] Kode dipisah ke modul (lihat struktur folder).
* [ ] Data tertentu disimpan di `localStorage` atau `sessionStorage`.
* [ ] Ada penggunaan `map`, `filter`, `reduce` atau `forEach` yang jelas.
* [ ] Ada contoh `JSON.stringify`/`JSON.parse` pada simpan/pengambilan dari storage.
* [ ] README & instruksi menjalankan tersedia.

---

## 10. Ide API Publik (opsional, pilih satu sesuai proyek)

* **JSONPlaceholder** — fake posts/users (bagus untuk katalog / demo CRUD).
* **OpenWeatherMap** — data cuaca (butuh API key gratis).
* **PokeAPI** — daftar Pokémon (katalog menarik).
* **TheMealDB / TheCocktailDB** — resep / minuman.
* **Public Quran APIs** — untuk aplikasi Al-Qur’an (cek yang public & CORS).

> Catatan: beberapa API butuh API key; siswa harus mencatat cara mendapatkan key di README.

---

## 11. Bonus (nilai tambah)

* Offline caching sederhana (menggunakan `localStorage` untuk cache hasil fetch ketika offline).
* Mock form (tambah item) yang disimpan di localStorage.
* Loading state & skeleton UI.
* Unit test ringan (mis. fungsi util di-testing).
* Implementasi pagination atau search/filter client-side.

---

## 12. Persyaratan Tambahan — Presentasi & Deploy (ditambahkan)

### Presentasi

* Setelah selesai coding, tiap siswa/kelompok wajib membuat presentasi singkat (slide) yang menjelaskan web yang dibuat.
* Durasi presentasi: **5–7 menit** (saran). Jumlah slide: **~6–10 slide**.
* Isi wajib slide:

  1. Judul & nama peserta
  2. Problem & solusi (apa manfaat web)
  3. Tech stack & arsitektur singkat (struktur folder)
  4. Fitur utama & demo (screenshot / link live)
  5. Highlight penerapan konsep (contoh: modul `api.js`, contoh `async/await + try/catch`, contoh penggunaan `localStorage`)
  6. Tantangan & solusi
  7. Rencana pengembangan ke depan
* Format file slide: PDF / PPTX / Google Slides (link). Jika mau, boleh rekam demo singkat (opsional).

### Deploy ke Vercel

* Setiap proyek harus dideploy ke **Vercel** ([https://vercel.com](https://vercel.com)) dan mengumpulkan link produksi (live URL).
* Jika proyek menggunakan API key, jangan commit key ke repo. Simpan key di **Environment Variables** Vercel.
* Harus disertakan di README langkah singkat bagaimana cara deploy di Vercel (atau link Vercel).

---

## Panduan Deploy ke Vercel — Langkah Singkat (untuk README)

```
1. Push project ke GitHub.
2. Masuk ke https://vercel.com -> New Project -> Import GitHub repo.
3. Jika menggunakan framework, atur:
   - Build Command: `npm run build` (jika ada)
   - Output Directory: `dist` atau `build` (sesuaikan)
4. Tambahkan Environment Variables (jika API key dipakai) di Settings -> Environment Variables.
5. Klik Deploy, tunggu sampai selesai. Salin Production URL dan sertakan di laporan.
```

**Catatan teknis singkat**:

* Pastikan `index.html` di root (untuk static) atau konfigurasi build output benar.
* Jika menggunakan `package.json`, pastikan `scripts.build` tersedia (mis. `"build": "vite build"`).
* Untuk SPA pastikan routing bekerja pada deploy (Vercel menangani fallback).

---

## Penilaian Tambahan (Rubrik Diperbarui)

Bobot total 100 poin (disesuaikan supaya mencakup presentasi & deployment):

* **Fungsionalitas (35 pts)**
* **Penerapan Materi & Teknik JS (22 pts)**
* **Kebersihan Kode & Struktur (13 pts)**
* **UI / UX (8 pts)**
* **Kreativitas & Nilai Tambah (7 pts)**
* **Presentasi (10 pts)**

  * Content clarity (4 pts)
  * Demo live/rekaman (3 pts)
  * Slide design & struktur (2 pts)
  * Jawaban Q&A (1 pt)
* **Deployment ke Vercel (5 pts)**

  * Live URL aktif & dapat diakses (3 pts)
  * Build logs bersih / tidak error (1 pt)
  * Environment variables disimpan aman (1 pt)

---

## Checklist Pengumpulan (wajib)

Siswa wajib menyerahkan (link / file):

* [ ] Link GitHub repository (repo penuh kode).
* [ ] Link Vercel (Production URL).
* [ ] File presentasi (PDF / PPTX) atau link Google Slides.
* [ ] README.md jelas berisi: cara menjalankan lokal, API yang dipakai, cara deploy ke Vercel, catatan env vars.
* [ ] Jawaban singkat (3–5 poin) tentang tantangan yang ditemui dan bagaimana menyelesaikannya.
* [ ] (Opsional) Rekaman demo 2–3 menit.

---

## Outline Slide (Template singkat — 7 slide)

1. **Cover** — Judul, nama, kelas, repo & live URL.
2. **Masalah & Solusi** — Kenapa membuat aplikasi ini, manfaat.
3. **Tech Stack & Struktur** — HTML/CSS/JS, library, struktur folder.
4. **Fitur Utama** — Daftar fitur wajib yang sudah dipenuhi.
5. **Highlight Kode** — 1–2 snippet (mis. `api.js` dengan `async/await + try/catch`, contoh `storage.js`).
6. **Demo Live & Screenshot** — buka live URL / demo singkat.
7. **Tantangan & Rencana Pengembangan** — apa yang sulit & rencana perbaikan.

---

## Checklist Verifier (untuk penguji, cepat)

* [ ] Buka repo → ada src/ & modul (api/ui/storage).
* [ ] README berisi langkah menjalankan & deploy.
* [ ] Live URL aktif.
* [ ] Di aplikasi: ada fetch ke API publik; `try...catch` menangani error; `async/await` dipakai.
* [ ] localStorage/sessionStorage dipakai (cek Application → Storage di DevTools).
* [ ] Minimal 2 halaman (cek link detail).
* [ ] Presentasi (slide) tersedia & durasi/isi sesuai.

---

Jika Anda ingin saya juga membuat **starter repo** atau **template slide (PPTX/Google Slides)** sekarang, beri tahu — saya bisa siapkan starter file yang bisa diunduh.
