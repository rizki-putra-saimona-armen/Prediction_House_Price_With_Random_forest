# Random Forest Regressor & Feature Scaling Optimization

Repository ini berisi proyek analisis regresi untuk memprediksi target kontinu menggunakan algoritma **Random Forest Regressor**. Fokus utama dari proyek ini adalah melakukan eksperimen pemodelan data, evaluasi performa model melalui berbagai metrik regresi, serta menganalisis pengaruh *Feature Scaling* dan penanganan *outliers* terhadap performa algoritma berbasis *tree*.

##  Fitur Utama Proyek
* **Data Preprocessing & Cleaning:** Penanganan *outliers* (pencilan) dan analisis distribusi data.
* **Feature Scaling Experiment:** Eksperimen perbandingan penanganan fitur menggunakan `MinMaxScaler`, `StandardScaler`, dan `RobustScaler` untuk melihat dampaknya pada model.
* **Machine Learning Modeling:** Implementasi *Random Forest Regressor* menggunakan *Scikit-Learn*.


---

## Alur Kerja Pemodelan (Workflow)

### 1. Data Splitting & Scaling Consistency
Untuk menghindari terjadinya **Data Leakage (Kebocoran Data)**, proses penanganan skala dilakukan dengan aturan baku:
* Aturan statistik (nilai minimum, maksimum, atau mean) disetel **hanya** menggunakan data *training* melalui fungsi `.fit(X_train)`.
* Transformasi data dilakukan pada kedua set menggunakan fungsi `.transform(X_train)` dan `.transform(X_test)` agar skala data uji tetap konsisten dengan pengetahuan yang dimiliki oleh model saat fase latihan.

### 2. Evaluasi Metrik yang Digunakan
Performa model regresi diukur menggunakan 3 jenis metrik untuk memahami karakteristik *error* secara detail:
* **MAE:** Digunakan untuk melihat rata-rata kesalahan prediksi secara linear tanpa mendramatisir nilai pencilan.
* **MSE & RMSE:** Digunakan untuk memantau performa model terhadap kesalahan yang fatal, karena kedua metrik ini memberikan bobot hukuman yang lebih berat (kuadratik) jika model membuat tebakan yang meleset jauh (*large errors*).

---

##  Tech Stack & Library
Proyek ini dibangun menggunakan ekosistem Data Science Python berikut:
* **Python** (Bahasa Pemrograman Utama)
* **Jupyter Notebook** (`.ipynb`)
* **Pandas & NumPy** (Manipulasi dan Analisis Data)
* **Scikit-Learn** (`MinMaxScaler`, `RandomForestRegressor`, `train_test_split`, dan `metrics`)
* **Matplotlib & Seaborn** (Visualisasi Data & Distribusi *Outliers*)

---

##  Cara Menjalankan Proyek

1. **Clone Repositori Ini:**
   ```bash
   git clone [https://github.com/username-kamu/nama-repositori.git](https://github.com/username-kamu/nama-repositori.git)
   cd nama-repositori
