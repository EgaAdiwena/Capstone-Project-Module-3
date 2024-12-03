# **Capstone 3 Purwadhika**

Sebagai bagian dari tugas akhir program Data Science Purwadhika, notebook ini disusun untuk mengimplementasikan keterampilan analisis data dan machine learning. Dalam proyek ini, saya bersimulasi sebagai analis data yang ditugaskan untuk menggali *insights* dan menciptakan prediksi machine learning dari dataset yang disediakan, dengan tujuan menjawab permasalahan bisnis yang relevan.

by : Ega Adiwena

# **Saudi Arabia Used Cars**

Pasar mobil bekas di Arab Saudi sedang mengalami pertumbuhan yang signifikan. Diperkirakan bernilai USD 6,41 miliar pada tahun 2024, pasar ini diproyeksikan mencapai USD 9,03 miliar pada tahun 2029, dengan CAGR lebih dari 7,10% selama periode perkiraan.

Digitalisasi yang pesat di Arab Saudi, dengan penetrasi internet mencapai 98,6% populasi, telah mengubah lanskap pasar mobil bekas.. Transaksi peer-to-peer dan lelang online semakin populer, menyederhanakan proses jual beli.

https://www.mordorintelligence.com/industry-reports/saudi-arabia-used-car-market

# **Background**

**Problem Statement :**

Bagaimana cara melakukan valuasi yang akurat terhadap mobil bekas agar mendapatkan harga yang wajar dan tidak merugikan bagi pembeli maupun penjual?

**Objective :**

Diciptakan sebuah perangkat yang dapat memberikan prediksi harga yang tepat. Alat ini diharapkan dapat menjadi referensi bagi pembeli maupun penjual dalam proses transaksi.

Untuk menjawab permasalahan dan mengimplementasi tujuan yang didapat, saya mendeterminasi divisi *data engineer*, *software engineer*, *data analyst and machine learning*, dan *sales and marketing* sebagai *stakeholder*.

**Evaluation Matrix**

1.   MAE (Mean Absolute Error)
2.   MAPE (Mean Absolute Percentage Error)
3.   RMSE (Root Mean Squared Error)
4.   R-Squared

# **Data Preprocessing**

1.   Column adjustment
2.   Missing value and duplicate checking
3.   Drop column
4.   Outliers checking
5.   Data distribution checking
6.   Data correlation checking

# **Data Modeling**

1.   Encoding : One Hot (Gear_type, Origin, Options) and Binary (Type, Region, Make)
2.   Train and splitting : Split data into train with testing proportion of 70 : 30
3.   Modeling : Linear Regression, KNN Regressor, Decision Tree Regressor, Random Forest Regressor, and XG Boost Regressor

# **Conclusion**

1.   Model prediksi yang kami kembangkan telah berhasil memetakan harga mobil bekas dalam rentang 11.000 - 185.000 SAR. Model ini dapat digunakan sebagai input dalam sistem pendukung keputusan untuk transaksi jual beli mobil bekas.
2.   Besarnya nilai RMSE menunjukkan tingkat ketidakpastian model dalam memprediksi harga mobil bekas. Rata-rata, prediksi model dapat menyimpang sebesar 17.532 SAR dari harga sebenarnya.
3.   Analisis terhadap hasil model menunjukkan bahwa fitur 'Make', 'Engine Size', dan 'Year' memiliki kontribusi signifikan terhadap akurasi prediksi harga mobil bekas. Setelah dilakukan tuning hyperparameter, model berhasil mencapai nilai RMSE sebesar 17.523, MAE sebesar 11.476, dan MAPE sebesar 0,1937. 
4.   Nilai-nilai tersebut mengindikasikan performa model yang cukup baik.

# **Recommendations**

1.   Ana
