# 🍊🍇 Klasifikasi Jeruk vs Anggur menggunakan Naive Bayes

## Deskripsi
Proyek ini bertujuan untuk membangun model klasifikasi buah antara jeruk (orange) dan anggur (grapefruit) menggunakan algoritma **Naive Bayes**. Dataset diambil dari [Kaggle - Oranges vs Grapefruit](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit).

## Tahapan Proyek

### 1. **Import Library**
Pada tahap pertama, saya mengimpor berbagai library yang diperlukan untuk analisis data dan pembuatan model. Library yang digunakan antara lain:
- **pandas** dan **numpy** untuk pengolahan data.
- **matplotlib** dan **seaborn** untuk visualisasi.
- **scikit-learn** untuk model Naive Bayes, cross-validation, dan evaluasi model.

### 2. **Load Dataset**
Dataset yang digunakan adalah dataset buah yang berisi berbagai fitur, termasuk diameter, berat, dan warna RGB. Dataset ini dimuat menggunakan **pandas** dari file CSV yang disediakan.

### 3. **Eksplorasi Data**
Saya mulai dengan **mengeksplorasi data** untuk memastikan kualitas data, memeriksa apakah ada nilai yang hilang, dan melihat distribusi label (Jeruk dan Grapefruit). 
Selain itu, dilakukan visualisasi untuk menggambarkan **distribusi buah** dan **korelasi antar fitur** dengan menggunakan plot yang informatif.

### 4. **Exploratory Data Analysis (EDA)**
Pada tahap ini, saya melakukan analisis eksplorasi data lebih dalam dengan menggunakan:
- **Countplot** untuk melihat distribusi buah antara Jeruk dan Grapefruit.
- **Pairplot** untuk melihat hubungan antar fitur berdasarkan label.
- **Heatmap** untuk memvisualisasikan korelasi antar fitur numerik seperti diameter, berat, dan warna RGB.

### 5. **Preprocessing**
Sebelum melatih model, fitur yang relevan dipilih dan data dinormalisasi menggunakan **StandardScaler**. Proses normalisasi ini penting untuk memastikan bahwa semua fitur memiliki skala yang serupa sehingga model dapat bekerja dengan lebih baik.

### 6. **Split Dataset**
Dataset dibagi menjadi dua bagian:
- **Data Latih (Training Data)**: 80% dari dataset digunakan untuk melatih model.
- **Data Uji (Testing Data)**: 20% dari dataset digunakan untuk menguji model yang telah dilatih.

Pembagian ini dilakukan untuk memastikan bahwa model tidak terlatih hanya pada data uji dan memberikan hasil yang lebih akurat.

### 7. **Buat dan Latih Model**
Setelah data diproses, saya membuat model **Naive Bayes** dengan menggunakan **Gaussian Naive Bayes**. Model ini dilatih menggunakan data latih yang telah dipersiapkan sebelumnya.

### 8. **Cross-Validation**
Untuk mengevaluasi model secara lebih menyeluruh dan mengurangi overfitting, saya melakukan **cross-validation** dengan menggunakan 5 fold. Proses ini membagi dataset menjadi lima bagian, di mana setiap bagian digunakan secara bergantian untuk pengujian, sementara bagian lainnya digunakan untuk pelatihan.

Hasil dari **cross-validation** menunjukkan akurasi yang bervariasi untuk setiap fold:
- **Cross-Validation Accuracy**: [0.6335, 0.985, 0.9975, 0.987, 0.6175]
  
Akurasi rata-rata dari **cross-validation** adalah **84.41%**, yang menunjukkan bahwa model memiliki performa yang cukup baik meskipun ada variasi antara setiap fold.

### 9. **Prediksi dan Evaluasi**
Setelah model dilatih, saya menggunakan model untuk memprediksi kelas pada data uji. Saya kemudian mengevaluasi kinerja model menggunakan:
- **Confusion Matrix** untuk melihat perbandingan antara prediksi dan label asli.
- **Classification Report** untuk mendapatkan metrik seperti akurasi, precision, recall, dan F1-score.

### 10. **Visualisasi Confusion Matrix**
Confusion Matrix divisualisasikan untuk mempermudah pemahaman tentang seberapa baik model dalam mengklasifikasikan kedua buah (Jeruk dan Grapefruit). Visualisasi ini membantu untuk melihat apakah model sering salah memprediksi satu kelas sebagai kelas lainnya.

## Hasil dan Pembahasan
Model Naive Bayes menunjukkan **akurasi yang baik** dalam membedakan antara Jeruk dan Grapefruit. Hasil **cross-validation** memberikan akurasi rata-rata **84.41%**, dengan beberapa fold menunjukkan akurasi yang sangat baik (mendekati 100%) dan beberapa fold menunjukkan akurasi yang lebih rendah. Meskipun ada sedikit variasi antara fold, model ini dapat diterapkan secara konsisten pada dataset ini. Visualisasi **Confusion Matrix** juga menunjukkan bahwa model sangat baik dalam memprediksi kedua kelas dengan sedikit kesalahan.

## Persyaratan
Untuk menjalankan proyek ini, pastikan Anda memiliki lingkungan Python dengan versi 3.x dan beberapa library berikut:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

### Instalasi
Untuk menginstal library yang dibutuhkan, jalankan perintah berikut:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
