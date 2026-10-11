# Pembersihan-dan-Persiapan-Data-Penjualan-Kafe
Repositori ini menyediakan dokumentasi komprehensif mengenai struktur data mentah (raw data) serta tahapan pembersihan dan persiapan data (preprocessing) untuk memastikan kualitas data siap digunakan secara optimal dalam proses analisis maupun pemodelan lanjutan.

Dokumentasi Data Mentah & Preprocessing

Dokumen ini menjelaskan struktur data mentah (raw data) yang digunakan serta tahapan pembersihan dan persiapan data (preprocessing) sebelum data tersebut digunakan untuk pemodelan atau analisis lebih lanjut.

1. Deskripsi Data Mentah (Raw Data)

Data mentah mencakup informasi yang dikumpulkan langsung dari sumbernya tanpa modifikasi. Berikut adalah spesifikasi dari dataset mentah:

Format File: .csv (atau sesuaikan dengan format file Anda, misal .xlsx, .json)

Lokasi File: data/raw/dataset_mentah.csv

Jumlah Baris & Kolom: (Contoh: 5.000 baris dan 10 kolom)

Keterangan Kolom:

id: Identifikasi unik untuk setiap baris data.

tanggal: Waktu pencatatan data (Format: YYYY-MM-DD).

kategori: Jenis atau kategori item.

nilai_mentah: Nilai numerik mentah yang mungkin mengandung missing values atau outliers.

keterangan: Catatan teks tambahan (data kategorikal/teks bebas).

2. Masalah yang Ditemukan pada Data Mentah

Sebelum masuk ke tahap preprocessing, data mentah biasanya memiliki beberapa kendala umum, antara lain:

Missing Values (Nilai Kosong): Terdapat beberapa baris yang kosong pada kolom numerik maupun kategorikal.

Duplikasi Data: Adanya baris data yang tercatat ganda.

Outlier / Anomali: Nilai numerik yang berada di luar kewajaran (ekstrem).

Format Tidak Konsisten: Perbedaan penulisan huruf besar/kecil atau format tanggal yang tidak seragam.

3. Tahapan Preprocessing Data

Tahapan preprocessing dilakukan untuk mengubah data mentah menjadi data yang bersih, terstruktur, dan siap dianalisis. Langkah-langkah yang dilakukan meliputi:

A. Pembersihan Data (Data Cleaning)

Penanganan Missing Values:

Untuk kolom numerik, nilai kosong diisi menggunakan nilai rata-rata (mean) atau median.

Untuk kolom kategorikal, nilai kosong diisi dengan modus atau kategori khusus seperti 'Unknown'.

Penghapusan Duplikat: Menghapus baris data yang identik menggunakan fungsi drop_duplicates().

B. Transformasi & Standarisasi (Data Transformation)

Keseragaman Teks: Mengubah seluruh teks pada kolom kategorikal menjadi huruf kecil (lowercase) dan menghapus spasi berlebih (strip).

Konversi Tipe Data: Memastikan kolom tanggal bertipe datetime dan kolom angka bertipe float atau integer.

Normalisasi / Standarisasi: Menskalakan fitur numerik (misalnya menggunakan Min-Max Scaling atau Standard Scaler) agar berada dalam rentang yang seragam.

C. Pembagian Data (Data Splitting)

Data yang sudah bersih dibagi menjadi data latih (training set) dan data uji (testing set) dengan proporsi tertentu (misalnya 80:20).

4. Struktur Output Data (Processed Data)

Hasil akhir dari proses preprocessing disimpan ke dalam direktori terpisah agar tetap bersih:

Lokasi File Bersih: data/processed/dataset_cleaned.csv

Fitur Tambahan: Kolom baru hasil feature engineering (jika ada) ditambahkan di tahap ini.

Dokumen ini diperbarui secara berkala seiring dengan pembaruan pipeline data.
