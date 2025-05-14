# Model Klasifikasi Buah Menggunakan MobileNetV2
Proyek ini adalah model klasifikasi gambar buah yang mampu mengenali 5 jenis buah menggunakan teknik Transfer Learning dengan arsitektur dasar MobileNetV2. Model ini telah diekspor ke berbagai format untuk mendukung implementasi di berbagai platform seperti web, mobile, dan desktop.

---

## Arsitektur Model
Model ini dibangun menggunakan MobileNetV2 sebagai feature extractor (tanpa layer fully connected di atasnya) dengan penambahan beberapa layer kustom sebagai classifier.

---

## Dataset
Dataset yang digunakan berasal dari Kaggle dengan topik Fruits Classification oleh Utkarsh Saxena (2021).

Dataset ini terdiri dari 10.000 gambar buah yang terbagi secara merata ke dalam 5 kategori, yaitu:
Apple: 2.000 gambar (20.00%)
Banana: 2.000 gambar (20.00%)
Grape: 2.000 gambar (20.00%)
Mango: 2.000 gambar (20.00%)
Strawberry: 2.000 gambar (20.00%)

Setiap kelas memiliki jumlah gambar yang seimbang, sehingga mendukung proses pelatihan model secara adil tanpa bias terhadap salah satu kelas. Total keseluruhan gambar dalam dataset ini adalah 10.000 gambar.

---

## Kelas Buah yang Dideteksi

Model ini dilatih untuk mengenali 5 jenis buah berikut:
1. Apple
2. Banana
3. Grape
4. Mango
5. Strawberry

Label dari masing-masing kelas disimpan dalam file `tflite/label.txt`.

---

## Format Model yang Disimpan

Model disimpan dalam tiga format berikut:

- SavedModel: disimpan di folder `saved_model/`, digunakan untuk keperluan pengembangan dan pelatihan lanjutan di TensorFlow.
- TFLite: disimpan di folder `tflite/`, digunakan untuk deployment model di perangkat mobile seperti Android.
- TensorFlow.js (TFJS): disimpan di folder `tfjs_model/`, digunakan untuk integrasi model di browser menggunakan JavaScript.

---

## Cara Menjalankan

1. Buka file `notebook.ipynb` di Google Colab atau Jupyter Notebook.
2. Jalankan seluruh sel pada notebook untuk melatih dan menyimpan model.
3. Gunakan model yang sudah diekspor sesuai dengan kebutuhan platform: TensorFlow untuk pengembangan lanjutan, TFLite untuk mobile, dan TFJS untuk browser.
