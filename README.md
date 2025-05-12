# RupaID

**RupaID** adalah aplikasi berbasis Python yang digunakan untuk mengidentifikasi nilai mata uang Rupiah dari citra gambar menggunakan metode ekstraksi ciri **Local Binary Pattern (LBP)** dan klasifikasi **Naïve Bayes**. Akurasi model diuji menggunakan teknik **K-Fold Cross Validation**.

## Fitur
- Identifikasi citra uang Rupiah berbagai nominal (1K hingga 100K)
- Ekstraksi fitur menggunakan Local Binary Pattern (LBP)
- Klasifikasi menggunakan Naïve Bayes
- Evaluasi performa model menggunakan K-Fold Cross Validation
- Antarmuka pengguna berbasis GUI (Tkinter)

## Cara Menjalankan
1. Clone repositori ini:
   ```bash
   git clone https://github.com/username/rupaid.git
   cd rupaid
2. Install dependensi:
  pip install -r requirements.txt
3. Jalankan aplikasi:
  python Program_Identifikasi_MataUang.py

Dataset
Dataset terdiri dari 120 citra uang Rupiah berbagai nominal. Gambar diambil dengan kamera di atas kertas HVS.

Lisensi
Proyek ini menggunakan lisensi MIT.
