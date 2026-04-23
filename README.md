# Customer Segmentation Analysis Using RFM and K-Means Clustering on Superstore Dataset

## 📌 Project Overview

Proyek ini berfokus pada **analisis segmentasi pelanggan (customer segmentation)** menggunakan pendekatan **RFM (Recency, Frequency, Monetary)** dan **K-Means Clustering** pada dataset *Superstore*.

Tujuan utama dari proyek ini adalah untuk mengelompokkan pelanggan berdasarkan perilaku transaksi mereka sehingga dapat membantu perusahaan dalam:

* Meningkatkan strategi pemasaran
* Mengoptimalkan program loyalitas pelanggan
* Mengidentifikasi pelanggan bernilai tinggi
* Mengurangi risiko churn

---

## 📊 Dataset

Dataset yang digunakan adalah **Superstore Dataset**, yang berisi data transaksi pelanggan dengan fitur utama seperti:

* Order Date, Ship Date
* Customer ID & Customer Name
* Segment, Region, Category
* Sales, Quantity, Discount, Profit

Dataset ini dapat diakses melalui sumber publik (dicoding / superstore dataset).

---

## 🧠 Metodologi

### 1. Data Preparation

Tahapan awal meliputi:

* Cleaning data (missing values, tipe data)
* Feature engineering (discount amount, aggregation per customer)
* Transformasi data berbasis customer-level

### 2. RFM Analysis

RFM digunakan untuk memahami perilaku pelanggan:

* **Recency**: kapan terakhir transaksi
* **Frequency**: seberapa sering transaksi
* **Monetary**: total nilai transaksi

Kemudian dilakukan:

* Ranking skor RFM
* Normalisasi skor
* Perhitungan **RFM Score**
* Segmentasi pelanggan:

  * Low Value Customers
  * Medium Value Customers
  * High Value Customers
  * Top Customers

---

### 3. Machine Learning: K-Means Clustering

Algoritma yang digunakan:

* **K-Means Clustering (Unsupervised Learning)**

Langkah:

* Seleksi fitur numerik (Recency, Frequency, Monetary, Discount)
* Transformasi data menggunakan **PowerTransformer**
* Menentukan jumlah cluster optimal menggunakan:

  * Elbow Method (Inertia)
  * Silhouette Score
* Training model K-Means dengan K = 4

---

## 📈 Hasil Segmentasi

Hasil clustering menghasilkan 4 segmen utama:

* **Cluster 0** → Low Value Customers
* **Cluster 1** → Top Customers
* **Cluster 2** → Medium Value Customers
* **Cluster 3** → High Value Customers

Setiap cluster memiliki karakteristik berbeda berdasarkan:

* Frekuensi transaksi
* Total pembelian
* Tingkat diskon yang digunakan
* Recency transaksi

---

## 🧰 Tech Stack

* Python
* Pandas & NumPy
* Scikit-learn
* Matplotlib & Seaborn
* Joblib
* Jupyter Notebook

---

## 📁 Repository Structure

```
proyek_customer_segmentation/
│
├── Superstore.ipynb
├── kmeans_clustering_model.joblib
├── transformer_discount.joblib
├── transformer_frequency.joblib
├── transformer_monetary.joblib
├── transformer_recency.joblib
```

---

## ⚙️ How to Run the Project

1. Clone repository

```bash
git clone https://github.com/username/repo-name.git
```

2. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib
```

3. Jalankan notebook

```bash
jupyter notebook Superstore.ipynb
```

---

## 📌 Output Project

* Model K-Means Clustering (saved as `.joblib`)
* Transformer untuk preprocessing data
* Segmentasi pelanggan berdasarkan RFM & ML
* Visualisasi distribusi customer behavior

---

## 🚀 Conclusion

Proyek ini menunjukkan bahwa kombinasi **RFM Analysis + K-Means Clustering** efektif dalam mengelompokkan pelanggan berdasarkan perilaku transaksi. Hasil segmentasi ini dapat digunakan untuk mendukung strategi bisnis berbasis data (*data-driven decision making*).
