# Chita-Asriani-Dewi
# 🎬 Movie Dataset Preprocessing

## 📌 Konteks

Dataset film sering digunakan dalam analisis data untuk memahami pola dalam industri hiburan, seperti faktor yang memengaruhi pendapatan, popularitas film, maupun preferensi penonton. Namun, dataset mentah biasanya mengandung banyak masalah seperti nilai kosong (missing values), ketidakkonsistenan penulisan, dan data yang tidak sesuai format. Oleh karena itu, perlu dilakukan preprocessing sebelum data dianalisis lebih lanjut.

## ❓ Problem Statement

Bagaimana cara melakukan preprocessing pada dataset film (CSV) agar:

1. Data bebas dari nilai kosong dan data tidak valid.
2. Format kolom sesuai (numerik, teks, atau kategorikal).
3. Informasi konsisten sehingga siap digunakan untuk analisis dan pemodelan.

## 🎯 Tujuan

* Memuat dan memeriksa dataset film dari file CSV.
* Membersihkan data dengan menghapus nilai kosong, memperbaiki ketidakkonsistenan, serta membuang data tidak valid.
* Melakukan transformasi seperti konversi tipe data, normalisasi teks, dan pemisahan genre.
* Menyimpan dataset yang telah diproses agar siap dipakai untuk analisis lanjutan.

## 📂 Dataset

Dataset yang digunakan adalah **movie_sample_dataset.csv**, berisi informasi:

* `color` → format tampilan film.
* `director_name` → nama sutradara.
* `duration` → durasi film.
* `gross` → pendapatan kotor film.
* `genres` → kategori/genre film.
* `movie_title` → judul film.
* `title_year` → tahun rilis.
* `language` → bahasa film.
* `country` → negara asal.
* `budget` → anggaran produksi.
* `imdb_score` → skor IMDb.
* `actors` → pemeran.
* `movie_facebook_likes` → jumlah likes di Facebook.

## ⚙️ Langkah Preprocessing

1. **Memuat Data** → Deteksi delimiter, muat ke Pandas DataFrame.
2. **Pemeriksaan Data** → Tampilkan beberapa baris pertama, cek tipe data, missing values, dan baris bermasalah.
3. **Pembersihan Data** →

   * Hapus nilai NaN pada kolom penting (`gross`, `budget`).
   * Samakan penulisan (contoh: `Color` → `color`).
   * Hilangkan nilai `"N/A"` dan angka negatif.
4. **Transformasi Data** →

   * Konversi `budget` dan `gross` ke numerik.
   * Normalisasi teks (`director_name`, `language`, `country`).
   * Pisahkan `genres` menjadi list.
5. **Penyimpanan Data** → Simpan hasil bersih ke file baru `movie_dataset_cleaned.csv`.
6. **Verifikasi** → Cek struktur, tipe data, missing values, nilai negatif, dan konsistensi teks.

## 📊 Hasil

* Dataset berhasil dibersihkan dari nilai kosong & tidak valid.
* Kolom numerik (`budget`, `gross`) sudah dalam format numerik.
* Kolom teks (`color`, `director_name`, `language`, `country`) sudah konsisten dengan huruf kecil.
* Kolom `genres` berhasil dipisahkan menjadi list untuk analisis kategori ganda.
* File hasil preprocessing: **movie_dataset_cleaned.csv**.

## ✅ Kesimpulan

Proses preprocessing membuat dataset menjadi lebih rapi, konsisten, dan siap digunakan untuk analisis lebih lanjut. Tanpa preprocessing, analisis dapat menghasilkan kesalahan atau bias karena adanya missing values, data tidak konsisten, atau tipe data yang tidak sesuai.

## 💡 Rekomendasi

* Lakukan **feature engineering** tambahan, misalnya membuat variabel dummy dari genre.
* Gunakan **visualisasi data** (matplotlib/seaborn) untuk eksplorasi lebih lanjut.
* Dataset yang sudah bersih dapat digunakan untuk **machine learning** seperti prediksi pendapatan film atau klasifikasi genre.
