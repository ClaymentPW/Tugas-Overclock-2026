Milk Quality Classification
## 1. Deskripsi Proyek
    Proyek ini bertujuan untuk mengklasifikasikan kualitas susu berdasarkan karakteristik fisik dan sensoriknya 
    menggunakan metode Machine Learning.

## 2. Jenis Permasalahan
Supervised Learning – Classification.
Target klasifikasi terdiri atas tiga kategori:
- Low
- Medium
- High
## 3. Dataset
Dataset yang digunakan adalah Milk Quality Dataset dari Kaggle.
Sumber: https://www.kaggle.com/datasets/cpluzshrijayan/milkquality
Dataset terdiri atas 1.059 baris dan 8 kolom, dengan 7 fitur dan 1 variabel target, yaitu Grade.
Fitur:
- pH
- Temprature
- Taste
- Odor
- Fat
- Turbidity
- Colour
Target: Grade.

## 4. Data Preprocessing
Tahapan preprocessing meliputi:
1. Memeriksa struktur dan tipe data.
2. Memeriksa missing values.
3. Memeriksa data duplikat.
4. Melakukan encoding pada variabel target menggunakan LabelEncoder.
5. Membagi dataset menjadi data training dan testing dengan mempertimbangkan kelompok data yang memiliki fitur identik.
Tidak ditemukan missing values. Sebanyak 976 baris duplikat identik ditemukan dan dipertahankan sementara 
karena belum terdapat bukti bahwa seluruh pengulangan merupakan kesalahan pencatatan.
Pembagian dataset:
- Training: 904 baris.
- Testing: 155 baris.

## 5. Exploratory Data Analysis (EDA)
EDA dilakukan untuk memahami distribusi dan karakteristik dataset.
Visualisasi yang digunakan:
- Bar Chart: Distribusi kualitas susu berdasarkan Grade.
- Box Plot: Sebaran temperatur berdasarkan Grade.
Dokumentasi lengkap tersedia pada file `Laporan_EDA_Milk_Quality_Classification.docx`.

## 6. Algoritma Machine Learning
Algoritma yang digunakan adalah Support Vector Machine (SVM) dengan kernel Radial Basis Function (RBF).
SVM digunakan untuk mengklasifikasikan data berdasarkan pola karakteristik yang dimiliki setiap kategori 
kualitas susu.

## 7. Evaluasi Model
Evaluasi dilakukan menggunakan:
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
Hasil pengujian model baseline pada notebook:
- Accuracy: 98,71%
- Macro F1-Score: 97,62%
Evaluasi tambahan dilakukan melalui repeated grouped cross-validation untuk membandingkan model baseline 
dan model hasil tuning.

## 8. Kesimpulan

Proyek ini menerapkan algoritma Support Vector Machine untuk mengklasifikasikan kualitas susu berdasarkan 
tujuh karakteristik dataset. Tahapan preprocessing, EDA, pelatihan, dan evaluasi dilakukan untuk menghasilkan 
model klasifikasi serta memahami performanya.
