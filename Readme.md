# 🧠 Klasifikasi Tweet Bencana

Proyek ini bertujuan untuk membangun model klasifikasi yang dapat mendeteksi apakah sebuah tweet mengandung informasi tentang bencana atau tidak.

---

## 📌 Deskripsi Masalah

Twitter telah menjadi saluran komunikasi penting ketika terjadi bencana. Dengan adanya smartphone, masyarakat bisa langsung melaporkan kejadian yang mereka saksikan secara real-time. Hal ini membuat banyak lembaga seperti organisasi bantuan bencana dan media tertarik untuk memantau informasi melalui Twitter secara otomatis.

Namun, tidak semua tweet yang terdengar "darurat" benar-benar menggambarkan kejadian bencana. Misalnya, seseorang bisa saja menggunakan kata "ABLAZE" secara metaforis. Ini mudah dikenali oleh manusia, tetapi tidak selalu demikian bagi computer.

Proyek ini bertujuan untuk membangun **model machine learning** yang dapat membedakan apakah sebuah tweet benar-benar terkait dengan bencana atau tidak.

---

## 📁 Dataset

Dataset yang digunakan berisi 10.876 tweet berbahasa Inggris yang terbagi menjadi 3.263 data test dan 7.613 data train yang telah diklasifikasi secara manual.  
Label:
- `1`: Tweet terkait bencana nyata
- `0`: Tweet tidak terkait bencana

Dataset ini berasal dari [Kaggle - NLP with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started).

---

## 🗂️ Struktur Proyek

```bash
.
├── dataset/
│   ├── sample_submission.csv
│   ├── train.csv
│   └── test.csv
├── models/
│   └── disaster_classifier.pkl
├── Data Submission/
│   ├── submission 1.csv
│   ├── submission 2.csv
│   └── ...
├── Scripts.ipynb # berisi script eksplorasi data dan optimasi model
├── Kaggle Submission.ipynb # berisi script untuk generate data submission ke Kaggle
├── requirements.txt
└── README.md 
```
---

## 📊 Tahapan Proyek
### 1. Exploratory Data Analysis (EDA)
- Visualisasi distribusi tweet, panjang karakter, frekuensi kata, dll.
### 2. Preprocessing
- Lowercasing, stopword removal, punctuation removal
- Tokenization
### 3. Vectorization
- TF-IDF (dengan pengaturan n-gram)
- Feature Selection
### 4. Modeling
- Logistic Regression
- Hyperparameter Tuning dengan GridSearch
- Evaluasi menggunakan: Accuracy, Precision, Recall, F1
### 5. Model Interpretability
- Analisis kesalahan klasifikasi
- Named Entity Extraction
- POS-based Feature Scoring

---

## ✅ Hasil
Dalam proyek ini, kami membangun model machine learning klasifikasi sederhana. Kami menemukan bahwa hanya dengan menggunakan teknik sederhana namun efektif seperti TF-IDF vectorization, N-Grams, Feature Selection, Hyperparameter Tuning dengan Grid Search kami berhasil meningkatkan performa model secara signifikan.

Evaluasi menunjukkan bahwa:

| Model                       | Accuracy  | Precision | Recall   | F1-score |
| --------------------------- | --------- | --------- | -------- | -------- |
| Logistic Regression  (Base) |  **80%**  | **0.81**  | **0.79** | **0.79** |
| Logistic Regression (Final) |  **84%**  | **0.83**  | **0.83** | **0.83** |

Meskipun model yang digunakan tergolong klasik dan ringan, Logistic Regression, hasilnya sangat kompetitif, bahkan mendekati kinerja model-model deep learning dalam klasifikasi teks bencana.

<img src="assets/Screenshot Kaggle  (3).png" alt="F1-Score test data" width="600">

pada data test, model berhasil mendapat f1-score sebesar 0.79 di situs resmi kaggle

## 🎯 Kesimpulan utama: 
Dengan preprocessing dan feature engineering yang tepat, model machine learning tradisional dapat bersaing dengan pendekatan deep learning, terutama pada dataset dengan ukuran terbatas seperti ini.

---

## 🛠️ Teknologi yang Digunakan
- Python
- Scikit-learn
- NLTK
- SpaCy
- Pandas, NumPy, Matplotlib, Seaborn

---

## Kontributor Utama
Studi ini dilakukan oleh mahasiswa **Universitas Islam Negeri Syarif Hidayatullah Jakarta**, Fakultas **Sains dan Teknologi**, Program Studi **Matematika**:  

| Nama                          | NIM            |
| ----------------------------- | -------------- |
| Ahmad Izza                    | 11220940000006 |
| Dani Hidayat                  | 11220940000014 |
