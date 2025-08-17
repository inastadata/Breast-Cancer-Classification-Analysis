# Breast-Cancer-Classification-Analysis
End-to-end machine learning project to classify breast cancer tumors as malignant or benign. This project covers data cleaning, EDA, baseline modeling, and optimization with feature scaling.

# Analisis Klasifikasi Kanker Payudara: Sebuah Studi Kasus Machine Learning


Proyek ini adalah implementasi end-to-end dari alur kerja data science untuk memprediksi apakah tumor payudara bersifat **ganas (Malignant)** atau **jinak (Benign)**. Studi kasus ini mencakup pembersihan data, analisis eksplorasi, pembuatan model dasar, hingga optimasi untuk meningkatkan performa.

---

## 📜 Latar Belakang

Deteksi dini kanker payudara secara signifikan meningkatkan peluang kesembuhan. Pemanfaatan *machine learning* dapat membantu radiologis dalam membuat diagnosis yang lebih cepat dan akurat. Proyek ini bertujuan untuk membangun sebuah model klasifikasi yang andal menggunakan dataset karakteristik sel tumor dari *Wisconsin Diagnostic Breast Cancer (WDBC)*.

---

## 🎯 Tujuan Proyek

1.  **Analisis Eksplorasi Data (EDA):** Memahami distribusi dan korelasi antar fitur dalam dataset.
2.  **Pembuatan Model Dasar:** Melatih model *Logistic Regression* sebagai *baseline* untuk mengukur performa awal.
3.  **Optimasi Model:** Menerapkan teknik *Feature Scaling* untuk meningkatkan akurasi dan metrik evaluasi lainnya.
4.  **Evaluasi Komparatif:** Membandingkan performa model sebelum dan sesudah optimasi untuk menunjukkan dampak dari teknik preprocessing yang diterapkan.

---

## 📊 Dataset

Dataset yang digunakan adalah **Breast Cancer Wisconsin (Diagnostic) Data Set** yang bersumber dari [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data).

Dataset ini terdiri dari **569 sampel** dengan **30 fitur numerik** yang décitrasikan dari citra digital aspirasi jarum halus (FNA) dari massa payudara.

---

## 🛠️ Alur Kerja Proyek

Proyek ini dibagi menjadi beberapa tahap utama:

1.  **Pemuatan & Pembersihan Data:** Mengimpor data dan menghapus kolom yang tidak relevan serta menangani data kategorikal.
2.  **Analisis Eksplorasi Data (EDA):** Melakukan visualisasi untuk memahami distribusi kelas target.
3.  **Pembuatan Model Dasar:** Melatih model *Logistic Regression* pada data mentah (tanpa penskalaan).
4.  **Evaluasi Model Dasar:** Menganalisis performa menggunakan metrik Akurasi, Precision, Recall, dan Confusion Matrix.
5.  **Optimasi dengan Feature Scaling:** Menerapkan `StandardScaler` untuk menormalisasi rentang fitur.
6.  **Pembuatan Model Optimasi:** Melatih ulang model pada data yang telah diskalakan.
7.  **Evaluasi Komparatif & Kesimpulan:** Membandingkan kedua model dan menarik kesimpulan berdasarkan hasilnya.

---

## 📈 Hasil & Analisis

Optimasi menggunakan *Feature Scaling* menunjukkan peningkatan performa yang signifikan:

| Metrik                | Model Dasar (Tanpa Scaling) | Model Optimasi (Dengan Scaling) | Peningkatan            |
| :-------------------- | :-------------------------: | :-----------------------------: | :--------------------: |
| **Akurasi** | 93.86%                      | **96.49%** | **+2.63%** |
| **Recall (Ganas)** | 86%                         | **93%** | **+7%** |
| **False Negative** | 6 Kasus                     | **3 Kasus** | **Berkurang 50%** |


**Analisis Kunci:**
* **Akurasi Meningkat:** Penskalaan fitur berhasil meningkatkan akurasi keseluruhan, membuat model lebih andal.
* **Pengurangan Kesalahan Kritis:** Yang terpenting, jumlah **False Negative** (kasus ganas yang salah didiagnosis sebagai jinak) berhasil **dikurangi sebesar 50%**. Ini adalah peningkatan vital dalam konteks medis.

---

## 🚀 Cara Menjalankan Proyek

1.  **Clone repository ini:**
    ```bash
    git clone [https://github.com/inastadata/Breast-Cancer-Classification-Analysis.git](https://github.com/inastadata/Breast-Cancer-Classification-Analysis.git)
    ```
2.  **Buka file notebook:**
    Buka file `analisis-kanker-payudara.ipynb` menggunakan Jupyter Notebook atau Google Colab.

3.  **Jalankan semua sel:**
    Notebook ini dirancang untuk dijalankan secara berurutan dari atas ke bawah.

---

## 🔧 Teknologi yang Digunakan

* **Python**
* **Pandas** (untuk manipulasi data)
* **Matplotlib & Seaborn** (untuk visualisasi)
* **Scikit-learn** (untuk pemodelan dan evaluasi machine learning)
