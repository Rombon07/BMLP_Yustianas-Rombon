# 🚀 Financial Fraud Detection & Segmentation: Machine Learning Submission

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)

Repository ini berisi **Submission Akhir** untuk kelas **Belajar Machine Learning untuk Pemula (BMLP)** dari **Dicoding Indonesia**. Proyek ini berfokus pada analisis data transaksi keuangan untuk mengidentifikasi pola nasabah dan potensi anomali (fraud detection).

---

## 🌟 Tentang Proyek Ini

Dalam proyek ini, saya melakukan **End-to-End Machine Learning** yang dibagi menjadi dua tahap utama:
1.  **Unsupervised Learning (Clustering):** Mengelompokkan nasabah/transaksi tanpa label sebelumnya untuk menemukan pola tersembunyi.
2.  **Supervised Learning (Klasifikasi):** Membangun model untuk memprediksi kelompok (cluster) tersebut pada data baru.

Dataset yang digunakan memiliki **2.512 entri** data transaksi dengan fitur seperti `TransactionAmount`, `CustomerAge`, `AccountBalance`, `Location`, dan lainnya.

---

## 📂 Struktur Repository

### 1. 🧩 Clustering (Unsupervised Learning)
* **File:** `[Clustering]_Submission_Akhir_BMLP_Yustianas_Rombon.ipynb`
* **Tujuan:** Melakukan segmentasi data transaksi untuk menemukan pola perilaku atau anomali.
* **Metodologi:**
    * **Preprocessing:** `MinMaxScaler`/`StandardScaler`, Encoding fitur kategorikal, dan `PCA` (Principal Component Analysis).
    * **Modeling:** Algoritma **K-Means Clustering**.
    * **Evaluasi:** Menggunakan **Elbow Method** (dengan `KElbowVisualizer`) dan **Silhouette Score** untuk menentukan jumlah cluster optimal.
    * **Output:** Dataset baru dengan label cluster (`Target`) yang disimpan sebagai `data_clustering_inverse.csv`.

### 2. 🤖 Klasifikasi (Supervised Learning)
* **File:** `[Klasifikasi]_Submission_Akhir_BMLP_Yustianas_Rombon.ipynb`
* **Tujuan:** Memprediksi kategori cluster nasabah berdasarkan fitur transaksi mereka.
* **Metodologi:**
    * **Input Data:** Menggunakan hasil dari proses clustering sebelumnya.
    * **Modeling:** Membandingkan algoritma **Decision Tree** dan **Random Forest Classifier**.
    * **Optimasi:** Menggunakan **GridSearchCV** untuk mencari *hyperparameters* terbaik.
    * **Evaluasi:** Mengukur performa dengan *Accuracy Score*, *Classification Report*, dan *Confusion Matrix*.

---

## 💡 Key Takeaways (Hasil Belajar)

Melalui proyek ini, saya belajar bagaimana:
* Menganalisis dataset finansial yang kompleks.
* Menentukan jumlah cluster yang optimal secara matematis, bukan sekadar tebakan.
* Menghubungkan hasil *Unsupervised Learning* (sebagai label) ke dalam proses *Supervised Learning*.
* Melakukan *Hyperparameter Tuning* untuk meningkatkan akurasi model klasifikasi.

---

## 🛠️ Cara Menjalankan

1.  Clone repository ini:
    ```bash
    git clone [https://github.com/Rombon07/BMLP_Yustianas-Rombon.git](https://github.com/Rombon07/BMLP_Yustianas-Rombon.git)
    ```
2.  Buka file `.ipynb` menggunakan Jupyter Notebook, Google Colab, atau VS Code.
3.  Pastikan library berikut sudah terinstall:
    ```python
    pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick
    ```

---

> **Disclaimer:** Proyek ini dikerjakan sebagai bagian dari proses belajar saya di Dicoding. Kritik dan saran sangat terbuka untuk pengembangan lebih lanjut! 👋

**Author:** Yustianas Rombon  
**Program:** Dicoding - Belajar Machine Learning untuk Pemula
