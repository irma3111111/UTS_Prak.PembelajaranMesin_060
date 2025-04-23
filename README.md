# 🍊🍇 Klasifikasi Jeruk vs Anggur menggunakan Naive Bayes

## Deskripsi
Proyek ini bertujuan untuk membangun model klasifikasi buah antara jeruk (orange) dan anggur (grapefruit) menggunakan algoritma **Naive Bayes**. Dataset diambil dari [Kaggle - Oranges vs Grapefruit](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit).

---

## Dataset
Dataset berisi fitur-fitur:
- `diameter` (diameter buah)
- `weight` (berat buah)
- `color_score` (skor warna buah)
- `fruit_name` (nama buah sebagai label)

---

## Tahapan Pengerjaan
1. **Import Library**  
   Menggunakan library: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.

2. **Load Dataset**  
   Membaca file `fruit_data_with_colors.csv`.

3. **Eksplorasi Data**  
   - Menampilkan sample data.
   - Mengecek missing value.
   - Melihat distribusi label buah.

4. **Preprocessing**  
   - Memilih fitur: diameter, weight, color_score.
   - Label encoding: `orange` → 0, `grapefruit` → 1.
   - Menghapus data buah selain orange dan grapefruit.

5. **Split Dataset**  
   Membagi data menjadi train dan test set (80:20).

6. **Membangun dan Melatih Model**  
   Menggunakan **Gaussian Naive Bayes**.

7. **Evaluasi Model**  
   - Menampilkan confusion matrix.
   - Menampilkan classification report.
   - Menghitung akurasi.

8. **Visualisasi Confusion Matrix**  
   Menggunakan `seaborn` heatmap untuk visualisasi prediksi.

---

## Hasil
- Akurasi model tercapai sesuai evaluasi pada data test set.
- Confusion matrix divisualisasikan untuk analisis kesalahan klasifikasi.

---

## Tools
- Python 3
- Jupyter Notebook
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

---


