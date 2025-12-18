# 📘 Judul Proyek
*(Isi judul proyek Anda di sini)*

## 👤 Informasi
- **Nama:** LYAN FAIRUS ATHALLAH  
- **Repo:** https://github.com/lynnfairss/DataScience---UAS-.git  
- **Video:** https://youtu.be/BaBfCCVRCFE

---

# 1. 🎯 Ringkasan Proyek
- Menyelesaikan permasalahan sesuai domain  
- Melakukan data preparation  
- Membangun 3 model: **Baseline(Logistic Regression)**, **Advanced(Random Forest)**, **Deep Learning(Multilayer Perceptron / MLP)**  
- Melakukan evaluasi dan menentukan model terbaik  

---

# 2. 📄 Problem & Goals
**Problem Statements:**  
- Dataset memiliki jumlah data yang relatif kecil dan distribusi kelas yang tidak seimbang 
- Diperlukan model yang mampu mengenali pola risiko fertilitas secara akurat
- Perlu membandingkan performa pendekatan klasik ML dan Deep Learning

Goals

**Goals:**  
- Membangun model klasifikasi dengan performa yang baik berdasarkan metrik evaluasi
- Membandingkan tiga pendekatan model (baseline, advanced, deep learning)
- Menentukan model terbaik berdasarkan Accuracy, Precision, Recall, F1-Score, dan ROC-AUC

---
## 📁 Struktur Folder
```
project/
│
├── data/                   # Dataset (tidak di-commit)
│
├── notebooks/              # Notebook eksperimen
│   └── ML_Project.ipynb
│
├── src/                    # Source code preprocessing & modeling
│
├── models/                 # Saved models
│   ├── model_baseline.pkl
│   ├── model_rf.pkl
│   └── model_mlp.h5
│
├── images/                 # Visualisasi (EDA, confusion matrix, training history)
│
├── requirements.txt        # Dependencies
├── .gitignore
└── README.md
```
---

# 3. 📊 Dataset
- **Sumber:** UCI Machine Learning Repository – Fertility Diagnosis Dataset
- **Jumlah Data:** 100 sampel
- **Jumlah Fitur:** 9 fitur + 1 target
- **Tipe:** Tabular (Numerik & Kategorikal)

### Fitur Utama
| Fitur                 | Deskripsi                     |
| --------------------- | ----------------------------- |
| Age                   | Usia individu                 |
| Season                | Musim saat pengambilan data   |
| Childish_Diseases     | Riwayat penyakit masa kecil   |
| Trauma                | Riwayat trauma                |
| Surgical_Intervention | Riwayat operasi               |
| Accident_Frequency    | Frekuensi kecelakaan          |
| Alcohol_Consumption   | Konsumsi alkohol              |
| Smoking_Status        | Status merokok                |
| Sitting_Hours         | Lama duduk per hari           |
| Diagnosis             | Target klasifikasi fertilitas |

---

# 4. 🔧 Data Preparation
- Data Cleaning:
Cek missing value dan duplikasi
Penanganan outlier pada fitur numerik
- Transformasi Data:
Encoding fitur kategorikal
Scaling fitur numerik menggunakan StandardScaler
- Data Splitting:
Train set: 80%
Test set: 20%
Stratified split untuk menjaga distribusi kelas

---

# 5. 🤖 Modeling
- **Model 1 – Baseline:**
 Logistic Regression
 Digunakan sebagai pembanding awal karena sederhana dan mudah diinterpretasi
- **Model 2 – Advanced ML:** 
 Random Forest Classifier
 Mampu menangkap hubungan non-linear dan lebih robust terhadap noise
- **Model 3 – Deep Learning:**
 Multilayer Perceptron (MLP)
 Minimal 2 hidden layers
 Menggunakan Dropout dan EarlyStopping untuk mencegah overfitting
 Training minimal 10 epochs

---

# 6. 🧪 Evaluation
Metrik Evaluasi:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

### Hasil Singkat
| Model         | Score (F1) | Catatan                          |
| ------------- | ---------- | -------------------------------- |
| Baseline      | Baik       | Model sederhana, performa stabil |
| Advanced      | Lebih baik | Menangkap pola non-linear        |
| Deep Learning | Kompetitif | Sensitif terhadap data imbalance |

---

# 7. 🏁 Kesimpulan
- Model terbaik: Random Forest
- Alasan: Memberikan keseimbangan terbaik antara precision, recall, dan F1-score pada data imbalanced
- Insight penting: 
Jumlah data sangat mempengaruhi stabilitas model
Threshold tuning penting untuk meningkatkan recall kelas minoritas

---

# 8. 🔮 Future Work
- [ ] Menambah jumlah data
- [ ] Melakukan hyperparameter tuning lebih lanjut
- [ ] Mencoba arsitektur deep learning yang lebih kompleks
- [ ] Deployment model ke web (Streamlit / FastAPI)

---

# 9. 🔁 Reproducibility
Gunakan environment: pip install -r requirements.txt

