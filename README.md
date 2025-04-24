
#1. Pengolahan Data (Data Preprocessing)
•	Label Encoding:
o	Data yang digunakan mengandung fitur kategorikal (misalnya, Student dan Credit_rating), yang harus diubah menjadi format numerik agar bisa diproses oleh model machine learning.
o	Label Encoding digunakan untuk mengonversi nilai kategorikal menjadi angka. Setiap nilai kategori akan diberi label numerik yang unik. Misalnya, jika kolom Student memiliki dua kategori yaitu "yes" dan "no", mereka bisa diubah menjadi angka 1 dan 0.
o	Setiap kolom kategorikal memiliki encoder tersendiri, sehingga proses transformasi pada data baru tetap konsisten dengan data pelatihan.
#2. Pembagian Data (Train-Test Split)
•	Data dibagi menjadi dua set: data latih (training data) dan data uji (test data). Pembagian dilakukan dengan proporsi 80:20, yang berarti 80% data digunakan untuk melatih model dan 20% sisanya digunakan untuk menguji kinerja model.
•	train_test_split dari library sklearn.model_selection digunakan untuk melakukan pembagian ini secara acak.
#3. Pembangunan Model Decision Tree
•	Model Decision Tree dibangun menggunakan data latih yang telah diproses. Model ini memprediksi apakah seseorang akan membeli komputer atau tidak berdasarkan fitur yang ada.
•	Beberapa parameter yang digunakan untuk mengatur model Decision Tree:
o	criterion='entropy': Menggunakan entropy untuk mengukur kualitas pemisahan dalam pohon keputusan (menggunakan information gain).
o	max_depth=4: Membatasi kedalaman pohon menjadi 4, untuk menghindari model yang terlalu rumit (overfitting).
o	min_samples_leaf=10: Menentukan jumlah minimum sampel pada setiap daun pohon. Jika ada kurang dari 10 sampel di suatu daun, pohon tidak akan membagi lagi pada titik tersebut.
#4. Evaluasi Model
•	Classification Report:
o	Setelah model dilatih, performanya dievaluasi menggunakan metrik yang memberikan informasi tentang akurasi, precision, recall, dan f1-score dari setiap kelas (misalnya, "Membeli komputer" vs "Tidak membeli komputer").
•	Confusion Matrix:
o	Menampilkan matriks perbandingan antara prediksi model dan nilai asli (aktual). Matriks ini menunjukkan jumlah prediksi yang benar dan salah, baik positif maupun negatif.
•	Heatmap:
o	Untuk memudahkan interpretasi, confusion matrix divisualisasikan dengan heatmap. Ini memberikan gambaran yang jelas tentang seberapa baik model dalam memprediksi kelas yang benar.
#5. Visualisasi Pohon Keputusan
•	Plotting Tree Structure:
o	Struktur pohon keputusan divisualisasikan dengan menggunakan plot_tree dari sklearn.tree. Ini memungkinkan kita untuk melihat bagaimana model membuat keputusan berdasarkan fitur-fitur yang diberikan (misalnya, usia, penghasilan, dll).
o	Visualisasi ini penting untuk memahami bagaimana pohon membagi data pada setiap level.
#6. Prediksi pada Data Baru
•	Setelah model dilatih dan dievaluasi, dilakukan prediksi pada data baru. Data baru ini juga harus diubah menjadi format numerik menggunakan encoder yang sama dengan data pelatihan.
•	Model kemudian akan memberikan prediksi apakah seseorang dengan karakteristik tertentu akan membeli komputer atau tidak.
#Kesimpulan
Dengan langkah-langkah ini, algoritma Decision Tree digunakan untuk membuat prediksi keputusan pembelian komputer berdasarkan sejumlah fitur yang diberikan. Proses ini melibatkan pengolahan data, pelatihan model, evaluasi kinerja, dan visualisasi untuk interpretasi yang lebih baik.

