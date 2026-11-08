# Analisis Indeks Kebahagiaan Penduduk dengan Model Regresi Linear

<div align="center">

  **Simple Linear Regression (SLR) & Multiple Linear Regression (MLR)**

  ![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
  ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
  ![Project](https://img.shields.io/badge/Project-Statistical%20Analysis-success)

  *Kelompok 3 — Analisis Data Indeks Kebahagiaan Penduduk*

</div>

## 📌 Gambaran Proyek

Proyek ini menganalisis **Indeks Kebahagiaan Penduduk (Happiness Score)** menggunakan metode **regresi linear sederhana (Simple Linear Regression/SLR)** dan **regresi linear berganda (Multiple Linear Regression/MLR)**.

Analisis dilakukan untuk melihat hubungan antara indikator ekonomi dan sosial dengan tingkat kebahagiaan penduduk antarnegara, serta membandingkan kemampuan model SLR dan MLR dalam menjelaskan dan memprediksi *Happiness Score*.

## 🎯 Tujuan Analisis

- Mengidentifikasi hubungan antara indikator ekonomi dan sosial dengan *Happiness Score*.
- Menganalisis hubungan antarvariabel menggunakan korelasi.
- Membentuk model regresi linear sederhana dan berganda.
- Mengevaluasi kinerja prediksi kedua model menggunakan MAE, RMSE, dan R².
- Memeriksa beberapa asumsi model regresi berganda.

## 📂 Dataset

Dataset yang digunakan adalah **Happiness Index 2018–2019**, yang bersumber dari Kaggle dan diunggah oleh **Sougata Pramanick (2022)**.

- **Sumber:** [Happiness Index 2018–2019 — Kaggle](https://www.kaggle.com/datasets/sougatapramanick/happiness-index-2018-2019)
- **Ukuran dataset:** 156 baris × 9 kolom.

### Variabel dalam Dataset

| Variabel | Keterangan |
|---|---|
| Country or Region | Negara atau wilayah yang menjadi objek pengamatan. |
| Score / Happiness Score (Y) | Skor tingkat kebahagiaan penduduk. |
| GDP per capita (X₁) | Indikator kondisi ekonomi. |
| Social Support (X₂) | Tingkat dukungan sosial yang dirasakan masyarakat. |
| Healthy Life Expectancy (X₃) | Harapan hidup sehat masyarakat. |
| Freedom to make life choices | Tingkat kebebasan individu dalam menentukan pilihan hidup. |
| Generosity | Tingkat kedermawanan masyarakat. |
| Perceptions of Corruption (X₄) | Persepsi masyarakat terhadap tingkat korupsi. |

Dalam pemodelan yang disajikan, **Happiness Score** digunakan sebagai variabel dependen (Y). Variabel prediktor pada model SLR adalah GDP per capita, sedangkan model MLR menggunakan GDP per capita, Social Support, Healthy Life Expectancy, dan Perceptions of Corruption.

## 📊 Tahapan Analisis

1. **Statistika deskriptif** — melihat karakteristik, pemusatan, dan penyebaran data.
2. **Visualisasi data** — menggunakan boxplot untuk mengamati sebaran dan indikasi pencilan.
3. **Analisis korelasi** — mengukur hubungan antarindikator dengan *Happiness Score*. Dalam hasil analisis, GDP per capita memiliki korelasi paling kuat dengan Y, yaitu **0,80**.
4. **Pemodelan SLR** — menggunakan GDP per capita sebagai satu-satunya prediktor.
5. **Pemodelan MLR** — menggunakan empat prediktor, yaitu GDP per capita, Social Support, Healthy Life Expectancy, dan Perceptions of Corruption.
6. **Evaluasi dan diagnostik** — membandingkan MAE, RMSE, R², serta memeriksa residual dan indikator multikolinearitas.

## 1. Simple Linear Regression (SLR)

Model regresi linear sederhana menggunakan **GDP per capita (X₁)** untuk memprediksi **Happiness Score (Y)**.

### Pembagian Data

| Dataset | Proporsi | Jumlah Observasi |
|---|---:|---:|
| Training | 75% | 117 |
| Testing | 25% | 39 |
| **Total** | **100%** | **156** |

### Persamaan Model

\[
\hat{Y} = 3.211 + 2.441X_1
\]

Koefisien GDP per capita bernilai positif. Artinya, dalam model ini GDP per capita memiliki hubungan searah dengan *Happiness Score*.

### Evaluasi Model SLR

| Metrik | Hasil |
|---|---:|
| MAE | 0,56 |
| RMSE | 0,70 |
| R² | 0,50 |

Nilai R² sebesar 0,50 menunjukkan bahwa model menjelaskan sekitar **50% variasi Happiness Score** berdasarkan GDP per capita. Sisanya berkaitan dengan faktor lain yang tidak dimasukkan ke dalam model.

## 2. Multiple Linear Regression (MLR)

Model regresi linear berganda menggunakan empat variabel prediktor:

- **X₁:** GDP per capita
- **X₂:** Social Support
- **X₃:** Healthy Life Expectancy
- **X₄:** Perceptions of Corruption

Variabel targetnya adalah **Happiness Score (Y)**.

### Pembagian Data

Data dibagi menjadi **80% training** dan **20% testing**, sesuai dengan presentasi analisis.

### Persamaan Model

\[
\hat{Y} = 2.51 + 1.01X_1 + 1.29X_2 + 0.81X_3 + 1.75X_4
\]

Keempat koefisien prediktor pada persamaan yang diperoleh bernilai positif. Interpretasi koefisien dalam regresi berganda dilakukan dengan mempertimbangkan variabel prediktor lainnya dalam model.

### Evaluasi Model MLR

| Metrik | Hasil |
|---|---:|
| MAE | 0,34 |
| RMSE | 0,43 |
| R² | 0,80 |

Nilai R² sebesar 0,80 menunjukkan bahwa model menjelaskan sekitar **80% variasi Happiness Score** berdasarkan empat variabel prediktor yang digunakan.

### Pemeriksaan Model

Berdasarkan hasil diagnostik yang ditampilkan dalam analisis:

- **Residual vs Fitted:** residual umumnya tersebar di sekitar garis nol dan tidak menunjukkan pola sistematis yang jelas.
- **Q-Q Plot:** sebagian besar residual mengikuti garis ideal, dengan beberapa penyimpangan pada bagian ujung atas.
- **Multikolinearitas:** nilai VIF untuk seluruh prediktor dilaporkan kurang dari 5.
- **Durbin-Watson:** nilai yang dilaporkan adalah 1,23; presentasi menginterpretasikannya sebagai tidak adanya autokorelasi.

## ⚖️ Perbandingan SLR dan MLR

| Metrik | SLR | MLR |
|---|---:|---:|
| MAE | 0,56 | **0,34** |
| RMSE | 0,70 | **0,43** |
| R² | 0,50 | **0,80** |

Berdasarkan hasil tersebut, MLR memiliki MAE dan RMSE yang lebih rendah serta R² yang lebih tinggi dibandingkan SLR. Dengan demikian, **MLR menunjukkan kinerja yang lebih baik pada hasil evaluasi yang dilaporkan dalam proyek ini**.

## 📝 Kesimpulan

Berdasarkan analisis dataset *Happiness Index 2018–2019*, GDP per capita, Social Support, Healthy Life Expectancy, dan Perceptions of Corruption menunjukkan hubungan positif dengan *Happiness Score* pada model yang dibangun.

Model MLR memberikan hasil evaluasi yang lebih baik dibandingkan SLR. MLR memperoleh **MAE 0,34**, **RMSE 0,43**, dan **R² 0,80**, sedangkan SLR memperoleh **MAE 0,56**, **RMSE 0,70**, dan **R² 0,50**. Hasil ini menunjukkan bahwa penggunaan beberapa indikator ekonomi dan sosial secara bersama-sama lebih mampu menjelaskan variasi skor kebahagiaan dalam dataset yang dianalisis.

## 📄 Dokumentasi Proyek

File presentasi yang memuat tahapan, visualisasi, hasil model, dan kesimpulan analisis:

[Analisis Data Indeks Kebahagiaan Penduduk (PDF)](./Analisis%20data%20indeks%20kebahagiaan%20penduduk_20261108_163657_0000.pdf)

## 🛠️ Tools

- **Python** — pengolahan dan analisis data.
- **Jupyter Notebook / Google Colab** — lingkungan kerja analisis.
- **Pandas dan NumPy** — pengolahan data.
- **Matplotlib / Seaborn** — visualisasi data.
- **Scikit-learn / Statsmodels** — pemodelan dan evaluasi regresi, sesuai implementasi yang digunakan.

## 👥 Authors

- **Dzu Fadli Raihandy**
- **Rizqo Misbahulghulam**
- **Glen**

## 👨‍🏫 Lecturer

**Amanatullah Pandu Zenklinov, S.Stat, M.Stat**

---

<div align="center">

  *Kelompok 3 — Statistical Data Analysis Project*

</div>
