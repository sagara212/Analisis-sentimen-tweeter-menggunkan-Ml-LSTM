# 🔍 **Analisis Sentimen Kenaikan PPN 12%**

Proyek ini bertujuan untuk menganalisis sentimen masyarakat terhadap kebijakan kenaikan Pajak Pertambahan Nilai (PPN) menjadi 12%. Dengan menggunakan algoritma Machine Learning (ML) dan model Long Short-Term Memory (LSTM), kami mengevaluasi bagaimana opini publik dipengaruhi oleh kebijakan tersebut.

---

## 📂 **Dataset**

**Sumber Data**: Data dikumpulkan dari media sosial (X) menggunakan web scraping.

**Isi Dataset**:
- **Teks**: Ulasan, komentar, atau berita terkait kebijakan PPN 12%.
- **Label**:
  - **1**: Sentimen positif
  - **0**: Sentimen negatif
- **Jumlah Data**:
  - **Negatif**: 64.9% dari total data
  - **Positif**: 35.1% dari total data

**Langkah Persiapan Data**:
- **Preprocessing**:
  - Tokenisasi
  - Lowercasing
  - Menghapus tanda baca dan stopwords
- **Sequencing**: Mengubah teks menjadi urutan angka dengan teknik word embedding.

---

## 🛠️ **Pemodelan dan Evaluasi**
Kami menggunakan dua model utama untuk menganalisis sentimen:

### 1. **Support Vector Machine (SVM)**
- **Akurasi**: 87.21%
- **Precision**: 87.21%
- **Recall**: 87.16%

### 2. **Long Short-Term Memory (LSTM)**
- **Training Accuracy**: 98.51%
- **Training Loss**: 0.0590
- **Training Precision**: 98.81%
- **Training Recall**: 97.07%
- **Validation Accuracy**: 84.88%
- **Validation Loss**: 0.7300
- **Validation Precision**: 75.89%
- **Validation Recall**: 77.27%

**Langkah-Langkah**:
1. **Eksplorasi Data**: Melihat distribusi data dan pola sentimen.
2. **Feature Engineering**: Menggunakan embedding teks untuk mendukung analisis mendalam.
3. **Pelatihan Model**:
   - Melatih model SVM dengan data term frequency-inverse document frequency (TF-IDF).
   - Melatih model LSTM dengan representasi vektor teks.
4. **Evaluasi Model**: Membandingkan hasil prediksi dengan data validasi menggunakan metrik akurasi, precision, dan recall.

---

## 🏆 **Hasil**

### **Kinerja Model**
| Model | Akurasi | Precision | Recall |
|-------|---------|-----------|--------|
| SVM   | 87.21%  | 87.21%    | 87.16% |
| LSTM  | 98.51% (train), 84.88% (val) | 98.81% (train), 75.89% (val) | 97.07% (train), 77.27% (val) |

**Kesimpulan Awal**:
- Model LSTM menunjukkan performa tinggi pada data training namun perlu dioptimalkan untuk data validasi.
- Model SVM stabil dan cukup andal untuk analisis sentimen awal.

### **Distribusi Sentimen**
- **Negatif**: Mayoritas ulasan mengungkapkan ketidakpuasan terhadap kebijakan kenaikan PPN 12%.
- **Positif**: Sebagian kecil mendukung kebijakan dengan alasan peningkatan pendapatan negara.

---

## 💻 **Teknologi yang Digunakan**

- **Python**: Pengolahan data dan pemodelan.
- **TensorFlow & Keras**: Membangun dan melatih model LSTM.
- **Scikit-learn**: Implementasi model SVM.
- **NLTK & SpaCy**: Preprocessing data teks.
- **Matplotlib & Seaborn**: Visualisasi hasil analisis.

---

## 📈 **Visualisasi**
Kami menyediakan grafik untuk:
- Perbandingan distribusi sentimen positif dan negatif.
- Kurva loss dan akurasi selama pelatihan LSTM.
- Confusion matrix untuk SVM dan LSTM.

---

## 🔗 **Langkah Selanjutnya**
1. **Optimasi Model LSTM**: Menggunakan hyperparameter tuning untuk meningkatkan performa pada data validasi.
2. **Analisis Lanjutan**: Mengidentifikasi tema utama dalam sentimen negatif.
3. **Penerapan**: Mengembangkan dashboard interaktif untuk memvisualisasikan hasil analisis secara real-time.

