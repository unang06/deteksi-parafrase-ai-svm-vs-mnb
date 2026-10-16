# Deteksi Teks Parafrase AI pada Jurnal Ilmiah Berbahasa Indonesia
### Perbandingan Multinomial Naïve Bayes vs Support Vector Machine

Project skripsi S1 Informatika, Universitas Gunadarma.

## Latar Belakang
Singkat 2–3 kalimat: kenapa deteksi parafrase AI pada teks ilmiah
berbahasa Indonesia penting, dan apa tujuan penelitian ini.

## Dataset
- 604 paragraf: 304 ditulis manusia (label 0), 300 hasil parafrase AI (label 1)
- Bahasa: Indonesia, domain: jurnal ilmiah
- (Jelaskan sumber & catatan ketersediaan data)

## Metodologi
1. Preprocessing: case folding, cleansing URL, tanda baca & angka, normalisasi spasi
   (tanpa stopword removal & stemming, karena fokus pada gaya penulisan)
2. Fitur: TF-IDF karakter n-gram (2–6), max 10.000 fitur
3. Pembagian data: StratifiedGroupKFold 5 fold (satu topik tidak terpecah
   antara data latih dan uji)
4. Model: Multinomial Naïve Bayes dan SVM (kernel linear)
5. Tuning: GridSearchCV (alpha untuk MNB, C untuk SVM)
6. Evaluasi: akurasi, precision, recall, F1 (rata-rata ± std 5 fold),
   confusion matrix, pengecekan overfitting


Kesimpulan singkat: model mana yang lebih baik dan kenapa.
(Opsional: tempel gambar confusion matrix)


## Teknologi
Python, scikit-learn, pandas, matplotlib, seaborn

