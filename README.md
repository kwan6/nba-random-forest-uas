# Klasifikasi Performa Pemain NBA Menggunakan Random Forest

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun model klasifikasi performa pemain NBA menggunakan algoritma **Random Forest** berbasis data statistik pertandingan. Performa pemain dikategorikan ke dalam tiga kelas, yaitu **Low**, **Medium**, dan **High**, yang dibentuk melalui pendekatan kuantitatif berbasis distribusi data.

Pendekatan ini menerapkan tahapan data mining secara sistematis, mulai dari preprocessing data, exploratory data analysis (EDA), seleksi fitur, pelatihan model, hingga evaluasi menggunakan metrik klasifikasi standar seperti akurasi, presisi, recall, dan F1-score. Proyek ini dikembangkan dalam konteks mata kuliah **Big Data & Data Mining (ST168)**.

---

## Dataset
Dataset yang digunakan merupakan dataset publik statistik pemain NBA yang diperoleh dari platform Kaggle dan berisi data historis performa pemain dalam berbagai musim.

**Sumber:**  
https://www.kaggle.com/datasets/justinas/nba-players-data

---

## Metodologi
Tahapan yang diterapkan dalam proyek ini meliputi:

1. **Preprocessing Data**  
   - Menghapus atribut non-numerik yang tidak relevan terhadap proses klasifikasi.  
   - Menangani nilai hilang (missing values) untuk menjaga konsistensi data.  
   - Membentuk label performa pemain menggunakan pendekatan kuartil berbasis variabel statistik.

2. **Exploratory Data Analysis (EDA)**  
   - Visualisasi distribusi kategori performa pemain.  
   - Analisis korelasi antar fitur numerik untuk mengidentifikasi hubungan statistik utama.

3. **Seleksi Fitur**  
   - Menggunakan metode **SelectKBest** dengan fungsi ANOVA (*f-classif*) untuk memilih fitur yang paling berkontribusi terhadap kelas performa.

4. **Pemodelan**  
   - Melatih model **Random Forest Classifier** dengan pendekatan *train-test split* (80:20).  
   - Menggunakan pendekatan ensemble untuk meningkatkan stabilitas dan generalisasi model.

5. **Evaluasi Model**  
   - Menggunakan **confusion matrix** dan metrik evaluasi berupa akurasi, presisi, recall, dan F1-score.  
   - Melakukan analisis kritis terhadap hasil prediksi dan potensi terjadinya data leakage.

---

## Struktur Berkas
nba-random-forest-uas/

│

├── modellingUAS.ipynb

├── nba_random_forest_model.pkl

├── all_seasons.csv

└── README.md


---

## Cara Menjalankan
1. Unduh atau kloning repository ini.  
2. Buka berkas **modellingUAS.ipynb** menggunakan Google Colab atau Jupyter Notebook.  
3. Jalankan seluruh sel secara berurutan untuk mereproduksi proses preprocessing, pelatihan model, dan evaluasi.

---

## Hasil Singkat
Model Random Forest mampu mengklasifikasikan performa pemain NBA ke dalam tiga kategori performa dengan tingkat akurasi yang tinggi. Analisis lebih lanjut menunjukkan bahwa hasil model dipengaruhi oleh hubungan langsung antara fitur statistik dan proses pembentukan label, sehingga dilakukan langkah pencegahan terhadap *data leakage* dengan menghilangkan variabel tertentu dari fitur input.

---

## Catatan Akademik
Seluruh kode, dataset, dan model disediakan secara publik untuk memastikan transparansi dan reproduktibilitas eksperimen dalam konteks pembelajaran dan penelitian akademik.

---

## Penulis
**Muhammad Noer Attalah Dzahkwan**  
Program Studi S1 Informatika  
Universitas AMIKOM Yogyakarta  
Mata Kuliah: Big Data & Data Mining (ST168)

