# 🌟 بِسْمِ اللهِ الرَّحْمٰنِ الرَّحِيْمِ

*Dengan menyebut nama Allah Yang Maha Pengasih lagi Maha Penyayang*

------------------------------------------------------------------------

## Doa Sebelum Menuntut Ilmu

**اللَّهُمَّ انْفَعْنَا بِمَا عَلَّمْتَنَا وَعَلِّمْنَا مَا يَنْفَعُنَا
وَزِدْنَا عِلْمًا**

"Ya Allah, manfaatkanlah ilmu yang telah Engkau ajarkan kepada kami,
ajarkanlah kami ilmu yang bermanfaat, dan tambahkanlah kami ilmu."

**اللّهُمَّ لاَ سَهْلَ إِلاَّ مَا جَعَلْتَهُ سَهْلاً، وَأَنْتَ تَجْعَلُ
الْحَزْنَ إِذَا شِئْتَ سَهْلاً**

"Ya Allah, tidak ada kemudahan kecuali yang Engkau jadikan mudah, dan
Engkau menjadikan kesulitan itu mudah jika Engkau kehendaki."

------------------------------------------------------------------------

# Soal Evaluasi Akhir --- Proyek Web Sederhana (Frontend JS)

## 1. Deskripsi Proyek

Buat sebuah **website yang bermanfaat** (contoh: aplikasi catatan,
manajemen tugas, katalog produk, atau aplikasi Al-Qur'an). Website harus
interaktif, modular, dan memakai teknik modern JavaScript (**web fetch,
async/await, error handling, DOM manipulation,
localStorage/sessionStorage, dll.**) Minimal **2 halaman** (misalnya
`index.html` + `detail.html`).

## 2. Fitur Wajib

-   **Web Fetch API**\
    Ambil data dari API publik yang memiliki struktur kompleks (misalnya
    data film, Al-Qur'an, resep makanan, atau game).
-   **Error handling (try...catch)**\
    Tangani error fetch dan tampilkan pesan ramah di UI.
-   **async/await**\
    Semua pengambilan data memakai async/await.
-   **Modularisasi**\
    Pisahkan kode ke modul: `api.js`, `ui.js`, `storage.js`, dll.
    Gunakan ES Modules (`export` / `import`).
-   **DOM manipulation**\
    Render daftar, detail, dan form secara dinamis.
-   **localStorage & sessionStorage**\
    Simpan data seperti preferensi, cache fetch, atau draft catatan.
-   **Minimal 2 halaman**\
    Halaman utama + detail (misalnya `detail.html?id=...`).
-   **Struktur folder rapi**\
    Gunakan pola `src/`, `modules/`, `assets/`.
-   **UI sederhana & rapi**\
    CSS dasar atau framework ringan (Tailwind/Bootstrap diperbolehkan).

## 3. Konsep & Teknologi yang Wajib Dipakai

-   Web Fetch API (GET/POST bila relevan)
-   async/await + try...catch
-   Promises & Callback function
-   JSON (`JSON.parse()` & `JSON.stringify()`)
-   Array & Object, Destructuring, Spread Operator
-   Array methods: `map`, `filter`, `reduce`, `forEach`
-   Modular JavaScript (`import/export`)
-   localStorage & sessionStorage

## 4. Contoh Struktur Folder

    project-name/
    ├─ index.html
    ├─ detail.html
    ├─ assets/
    │  ├─ css/
    │  │  └─ styles.css
    │  └─ img/
    ├─ src/
    │  ├─ main.js
    │  ├─ modules/
    │  │  ├─ api.js
    │  │  ├─ ui.js
    │  │  ├─ storage.js
    │  │  └─ utils.js
    │  └─ components/
    └─ README.md

## 5. Kriteria Penilaian (Total 100 Poin)

-   **Fungsionalitas (35 pts)**\
    Fitur wajib berjalan (fetch, detail, storage, dll).
-   **Penerapan Konsep JS (22 pts)**\
    async/await, modularisasi, array methods, promises, callbacks.
-   **Kebersihan Kode & Struktur (13 pts)**\
    Folder rapi, nama konsisten, ada komentar penting.
-   **UI/UX (8 pts)**\
    Tampilan sederhana tapi rapi, navigasi jelas.
-   **Kreativitas & Nilai Tambah (7 pts)**\
    Fitur ekstra, ide orisinal.
-   **Presentasi (10 pts)**\
    Slide terstruktur, demo berjalan, penjelasan jelas.
-   **Deployment ke Vercel (5 pts)**\
    Link live aktif, konfigurasi benar, API key aman.

## 6. Panduan Pengumpulan

Siswa wajib menyerahkan: - Link GitHub repository - Link Vercel
(Production URL) - File presentasi (PDF / PPTX) atau link Google
Slides - README.md dengan deskripsi, fitur, cara menjalankan, dan cara
deploy - Catatan tantangan & solusinya (3--5 poin) - File video presentasi

## 7. Outline Slide Presentasi (6--8 slide)

1.  Cover --- Judul, nama, link repo & live URL
2.  Masalah & Solusi --- manfaat aplikasi
3.  Tech Stack & Struktur Folder
4.  Fitur Utama
5.  Highlight Kode (async/await, modul, storage)
6.  Demo Live & Screenshot
7.  Tantangan & Rencana Pengembangan

## 8. API Rekomendasi (lebih menantang)

-   **TMDB API** --- data film & series (butuh API key gratis)
-   **PokeAPI** --- daftar Pokémon (nested data kompleks)
-   **TheMealDB / CocktailDB** --- resep makanan & minuman
-   **Quran API** --- ayat, tafsir, audio (struktur data dalam)
-   **RAWG Video Games API** --- data game populer

## 9. Bonus (opsional, nilai tambah)

-   Caching offline dengan localStorage
-   Form input → simpan ke storage
-   Loading state / skeleton UI
-   Search atau pagination client-side
-   Testing ringan fungsi utils
