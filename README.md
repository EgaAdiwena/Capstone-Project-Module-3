# **Capstone 3 Purwadhika**

Sebagai bagian dari tugas akhir program Data Science Purwadhika, notebook ini disusun untuk mengimplementasikan keterampilan analisis data dan machine learning. Dalam proyek ini, saya bersimulasi sebagai analis data yang ditugaskan untuk menggali *insights* dan menciptakan prediksi machine learning dari dataset yang disediakan, dengan tujuan menjawab permasalahan bisnis yang relevan.

by : Ega Adiwena

# **Saudi Arabia Used Cars**

# **Background**

Pasar mobil bekas di Arab Saudi sedang mengalami pertumbuhan yang signifikan. Diperkirakan bernilai USD 6,41 miliar pada tahun 2024, pasar ini diproyeksikan mencapai USD 9,03 miliar pada tahun 2029, dengan CAGR lebih dari 7,10% selama periode perkiraan.

Digitalisasi yang pesat di Arab Saudi, dengan penetrasi internet mencapai 98,6% populasi, telah mengubah lanskap pasar mobil bekas.. Transaksi peer-to-peer dan lelang online semakin populer, menyederhanakan proses jual beli.

https://www.mordorintelligence.com/industry-reports/saudi-arabia-used-car-market

**Problem Statement :**

Bagaimana cara melakukan valuasi yang akurat terhadap mobil bekas agar mendapatkan harga yang wajar dan tidak merugikan bagi pembeli maupun penjual?

**Objective :**

Diciptakan sebuah perangkat yang dapat memberikan prediksi harga yang tepat. Alat ini diharapkan dapat menjadi referensi bagi pembeli maupun penjual dalam proses transaksi.

Untuk menjawab permasalahan dan mengimplementasi tujuan yang didapat, saya mendeterminasi divisi *data engineer*, *software engineer*, *data analyst and machine learning*, dan *sales and marketing* sebagai *stakeholder*.

**Evaluation Matrix**

1.   MAE (Mean Absolute Error)
2.   RMSE (Root Mean Squared Error)
3.   R-Squared

# **Data Preprocessing**

1.   Column adjustment
2.   Missing value and duplicate checking
3.   Drop column
4.   Outliers checking
5.   Data distribution checking
6.   Data correlation checking

# **Data Modeling**

1.   Train and Splitting : Split data into train with testing proportion of 70 : 30
2.   Encoding : One Hot (Gear_type, Origin, Options) and Binary (Type, Region, Make)
4.   Modeling : Linear Regression, SVR, KNN, Decision Tree, Random Forest, Gradient Boost, XG Boost, LGBM Regressor

# **Conclusion**

1.   Hasil dari model menunjukkan bahwa performa terbaik pada test set dicapai oleh Base Model LightGBM, dengan nilai RMSE sebesar 29,339, MAE sebesar 13,771, dan R² sebesar 0.804. Evaluasi dilakukan menggunakan metrik RMSE (Root Mean Square Error), MAE (Mean Absolute Error), dan R² (Koefisien Determinasi).
2.   Nilai RMSE sebesar 29,339 mengindikasikan bahwa rata-rata kesalahan prediksi model berada pada selisih sekitar 29,339 satuan dari nilai sebenarnya. Nilai MAE sebesar 13,771 menunjukkan rata-rata kesalahan absolut prediksi model. Sedangkan R² sebesar 0.804 berarti model mampu menjelaskan 80,4% variabilitas data target pada test set, yang menunjukkan generalisasi model yang cukup baik.
3.   Meskipun performa test set Base Model lebih baik dibandingkan GridSearchCV dan RandomizedSearchCV, terdapat perbedaan cukup besar antara performa training (R²: 0.925) dan test set (R²: 0.804). Hal ini mengindikasikan model mungkin sedikit overfitting terhadap data training.
4.   Model saat ini sudah mencapai hasil yang cukup baik dalam memprediksi target pada test set. Namun, terdapat potensi peningkatan performa dengan melakukan eksplorasi fitur tambahan atau penyetelan hyperparameter yang lebih lanjut.

# **Recommendations**

1.   Penambahan Fitur Relevan : Menambahkan fitur tambahan yang dapat membantu model memahami lebih baik hubungan dengan target, seperti fitur interaksi antara spesifikasi tertentu (misalnya, lokasi atau kategori data tambahan yang relevan). Hal ini dapat membantu model menangkap pola-pola penting yang mungkin belum ditangkap sepenuhnya.
2.   Analisis Residual Error : Melakukan analisis pada residual error (selisih antara prediksi dan nilai aktual) untuk mengidentifikasi pola error, seperti underestimation atau overestimation, pada subkelompok tertentu. Dengan analisis ini, model dapat disesuaikan lebih baik untuk data tersebut.
3.   Cross-Validation yang Lebih Mendalam : Meningkatkan proses validasi dengan menggunakan teknik cross-validation yang lebih kuat, seperti k-fold dengan variasi stratifikasi, untuk mendapatkan estimasi performa model yang lebih stabil dan mengurangi kemungkinan hasil bias dari dataset.
4.   Eksplorasi Model Lain : Mencoba pendekatan algoritma lain yang mungkin lebih sesuai, seperti CatBoost, yang dapat menangani dataset dan hyperparameter dengan lebih efektif.
5.   Optimisasi Hyperparameter : Melakukan penyetelan hyperparameter lebih lanjut menggunakan pendekatan yang lebih luas, seperti Bayesian Optimization, untuk mengeksplorasi kombinasi hyperparameter terbaik tanpa overfitting.
