# Simple Linear Regression (SLR) & Multiple Linear Regression (MLR) Analysis

<div align="center">

  **Statistical Data Analysis — Regression Modeling**

  ![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
  ![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
  ![Status](https://img.shields.io/badge/Project-Academic%20Assignment-success)

</div>

## 📌 Project Overview

Repository ini berisi analisis **Simple Linear Regression (SLR)** dan **Multiple Linear Regression (MLR)** sebagai bagian dari pembelajaran analisis statistik. Analisis regresi digunakan untuk memahami hubungan antara variabel independen (X) dan variabel dependen (Y), serta membangun model untuk menjelaskan atau memprediksi nilai Y.

## 🎯 Objectives

- Memahami konsep dasar regresi linear sederhana dan berganda.
- Mengidentifikasi hubungan antara variabel independen dan dependen.
- Membentuk model regresi dan menginterpretasikan koefisiennya.
- Membandingkan pendekatan SLR dan MLR berdasarkan hasil analisis.
- Menyampaikan hasil analisis secara sistematis dan mudah dipahami.

## 📚 Analysis Overview

### 1. Simple Linear Regression (SLR)

SLR digunakan untuk menganalisis hubungan linear antara **satu variabel independen (X)** dengan **satu variabel dependen (Y)**.

Model umum:

\[
Y = a + bX + e
\]

Keterangan:
- **Y**: variabel dependen.
- **X**: variabel independen.
- **a**: konstanta/intercept.
- **b**: koefisien regresi.
- **e**: komponen error.

### 2. Multiple Linear Regression (MLR)

MLR digunakan untuk menganalisis hubungan linear antara **dua atau lebih variabel independen** dengan satu variabel dependen.

Model umum:

\[
Y = a + b1X1 + b2X2 + b..x.. + e
\]

Keterangan:
- **Y**: variabel dependen.
- **X₁, X₂, ..., Xₙ**: variabel independen.
- **a**: konstanta/intercept.
- **b₁, b₂, ..., bₙ**: koefisien regresi masing-masing variabel.
- **e**: komponen error.

## 🔎 Analysis Workflow

Secara umum, tahapan analisis dalam project ini meliputi:

1. **Data Preparation** — menyiapkan dan memeriksa dataset.
2. **Exploratory Analysis** — memahami karakteristik data dan hubungan antarvariabel.
3. **Model Construction** — membangun model SLR dan MLR.
4. **Model Evaluation** — mengevaluasi hasil model menggunakan ukuran yang relevan, seperti R-squared dan pengujian koefisien apabila tersedia.
5. **Interpretation** — menjelaskan hasil model dalam konteks data yang dianalisis.

## 📊 Understanding the Results

Beberapa hal yang perlu diperhatikan ketika membaca hasil regresi:

| Komponen | Interpretasi |
|---|---|
| Intercept | Nilai prediksi Y ketika seluruh variabel X bernilai nol. |
| Regression Coefficient | Perubahan rata-rata Y untuk setiap kenaikan satu unit X, dengan variabel lain tetap pada model MLR. |
| R-squared (R²) | Proporsi variasi Y yang dapat dijelaskan oleh model. |
| P-value | Digunakan dalam pengujian hipotesis untuk menilai bukti statistik terhadap koefisien. |

Nilai evaluasi perlu ditafsirkan sesuai konteks dataset. R-squared yang lebih tinggi tidak otomatis berarti model lebih baik dalam semua aspek.

## 🛠️ Tools & Technologies

- **Python** — pengolahan dan analisis data.
- **Jupyter Notebook** — lingkungan untuk menjalankan analisis secara interaktif.
- **Pandas / NumPy** — pengolahan data numerik (jika digunakan pada notebook).
- **Matplotlib / Seaborn** — visualisasi data (jika digunakan pada notebook).
- **Scikit-learn / Statsmodels** — pemodelan regresi (sesuai implementasi notebook).

## 👥 Authors

- **Dzu Fadli Raihandy**
- **Rizqo Misbahulghulam**
- **Glen**

## 👨‍🏫 Lecturer

**Amanatullah Pandu Zenklinov, S.Stat, M.Stat**

## ▶️ How to Run

1. Buka repository ini di GitHub.
2. Pilih file notebook analisis yang tersedia.
3. Jalankan notebook menggunakan Jupyter Notebook atau Google Colab.
4. Jalankan setiap cell secara berurutan untuk melihat proses dan hasil analisis.

---

<div align="center">

  *Academic project — Simple and Multiple Linear Regression Analysis.*

</div>
