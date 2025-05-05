# Decision Tree

Proyek ini adalah implementasi klasifikasi trafik jaringan berbasis machine learning dengan menggunakan algoritma **Decision Tree** untuk mendeteksi dan membedakan jenis trafik normal dan berbahaya berdasarkan data numerik dari paket jaringan.

## Dataset
Dataset yang digunakan berisi data dari serangkaian serangan siber berbasis jaringan yang melibatkan protokol MQTT dan teknik man-in-the-middle. Dataset yang digunakan **MITM ARP Spoofing.csv**, **MQTT DoS Publish Flood.csv**, **MQTT Malformed.csv**.

Ketiga dataset ini digabungkan menjadi satu kumpulan data yang dianalisis lebih lanjut.

## Pra-Pemrosesan Data
Langkah-langkah yang dilakukan sebelum pelatihan model:

1. Menggabungkan ketiga dataset.
2. Menghapus nilai kosong (NaN) dan data duplikat.
3. Memilih kolom numerik dari posisi kolom ke-7 hingga ke-75 untuk digunakan sebagai fitur (**X**).
4. Menetapkan kolom **Label** sebagai target (**y**), yang menunjukkan apakah sebuah flow merupakan serangan atau tidak.

## Model Decision Tree Classifier
Model yang digunakan adalah **Decision Tree** dari pustaka **scikit-learn**, karena mudah dipahami dan mampu menangani data numerik dengan baik. Model dilatih menggunakan data latih dan diuji menggunakan data uji, dengan metrik evaluasi sebagai berikut:

- Akurasi
- Confusion Matrix sebagai visualisasi performa model

## Hasil Analisis
Model **Decision Tree** berhasil memetakan jenis-jenis serangan berdasarkan pola trafik jaringan, dengan identifikasi trafik sebagai berikut:

- MITM ARP Spoofing
- MQTT DoS Publish Flood
- MQTT Malformed
- Benign (trafik normal)

## Library yang Digunakan
- **pandas, numpy** digunakan untuk Manipulasi dan analisis data.
- **matplotlib, seaborn** digunakan untuk Visualisasi data dan hasil klasifikasi.
- **sklearn** digunakan untuk Machine learning, evaluasi model, dan preprocessing.
