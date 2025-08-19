# Capstone-Project-Hactivb-IBM
Melakukan analisis fraud/kecurangan terhadap dataset yang berisi profil nasabah dengan judul 

## 🚀 "ANALISIS KLASIFIKASI RISIKO POTENSIAL FRAUD BERDASARKAN PROFIL NASABAH MENGGUNAKAN RANDOM FOREST PADA DATASET BANK MARKETING"

## 📌 PROJECT OVERVIEW
Penelitian ini bertujuan untuk mendeteksi potensi fraud atau kecurangan berdasarkan profil nasabah dengan menggunakan dataset Bank-Full. Dataset ini berisi data nasabah yang mencakup informasi seperti:
1. Demografi: umur (age), pekerjaan (job), status pernikahan (marital), tingkat pendidikan (education).
2. Finansial: saldo rekening (balance), pinjaman perumahan (housing), pinjaman pribadi (loan).
3. Interaksi Marketing: durasi panggilan terakhir (duration), jumlah kontak kampanye (campaign), hasil kampanye sebelumnya (poutcome).
Permasalahan utama yang diangkat adalah adanya potensi imbalance pada data target (jumlah nasabah yang melakukan transaksi tertentu jauh lebih sedikit dibanding yang tidak), yang dapat memengaruhi kinerja model prediksi. Dalam artian ketidakseimbangan kelas (imbalanced data) pada variabel target class (yes/no).
Penelitian ini akan mengimplementasikan SMOTE (Synthetic Minority Over-sampling Technique) untuk mengatasi ketidakseimbangan kelas, sehingga model dapat belajar lebih baik dari data minoritas. Dan juga Metode yang digunakan adalah Random Forest Classifier yang dikenal andal dalam menangani data dengan banyak variabel kategorikal maupun numerik, serta mampu memberikan interpretasi melalui feature importance.

## 📂 RAW DATASET LINK
1. Sumber == https://zenodo.org/records/14636312
2. Record == 45211 (baris) & 17 (kolom)
3. Class == 'no' (39922) & 'yes' (5289)

## 📊 Insight & findings
- Dataset awal sangat imbalance, jumlah transaksi fraud jauh lebih sedikit dibanding non-fraud.  
- Transaksi fraud cenderung terjadi pada jumlah transfer yang besar.  
- Setelah balancing dengan **SMOTE**, distribusi kelas menjadi seimbang.
![alt text](https://github.com/Nursam442/Capstone-Project-Hactivb-IBM/blob/main/sebelum%20smote.png?raw=true)
![alt text](https://github.com/Nursam442/Capstone-Project-Hactivb-IBM/blob/main/setelah%20smote.png?raw=true)
- Model **Random Forest** mencapai hasil evaluasi:  
  - Accuracy: ~88%
![alt text](https://github.com/Nursam442/Capstone-Project-Hactivb-IBM/blob/main/confusion%20matrix.png?raw=true)
  - ROC-AUC: ~0.91
![alt text](https://github.com/Nursam442/Capstone-Project-Hactivb-IBM/blob/main/ROC.png?raw=true)
- Feature paling berpengaruh: `duration`, `housing`, dan `contact`.
![alt text](https://github.com/Nursam442/Capstone-Project-Hactivb-IBM/blob/main/FI.png?raw=true)

## 🤖 AI support explanation
Dalam penelitian ini, AI digunakan pada beberapa tahap:
  1. Random Forest sebagai algoritma klasifikasi berbasis machine learning.
  2. SMOTE untuk menyeimbangkan distribusi kelas target.
  3. Visualization tools (matplotlib & seaborn) untuk membantu memahami pola data.
  4. LLM (ChatGPT) digunakan untuk:
    -. Merancang alur penelitian.
    -. Menjelaskan hasil model dan interpretasi variabel.
    -. Membantu menyusun insight, rekomendasi, dan perapihan laporan agar lebih sistematis.

