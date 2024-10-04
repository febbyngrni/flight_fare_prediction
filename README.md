# Prediksi Harga Tiket Pesawat

**Report** : [Medium](https://medium.com/@febbyngrni/flight-fare-prediction-using-machine-learning-algorithms-8971112e5997)<br>
**Dataset** : [Kaggle](https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction)

<br>

## Business Understanding
Industri penerbangan menghadapi tantangan dalam menetapkan harga tiket akibat fluktuasi permintaan, harga bahan bakar, dan persaingan yang ketat antar maskapai. Selain itu, ketidakpastian ekonomi global juga mempengaruhi jumlah penumpang. Untuk mengatasi hal ini, banyak maskapai menggunakan dynamic pricing, yang mengandalkan faktor-faktor seperti waktu pembelian dan ketersediaan kursi.

EaseMyTrip sebagai OTA (Online Travel Agency) juga menghadapi kesulitan serupa. Dengan memanfaatkan machine learning untuk memprediksi harga, mereka ingin mengoptimalkan strategi penetapan harga, meningkatkan pendapatan, dan tetap kompetitif di pasar perjalanan yang dinamis.
### Business Objectives
- **Optimalisasi Harga**: Menentukan harga tiket yang optimal berdasarkan prediksi untuk memaksimalkan margin keuntungan perusahaan serta meningkatkan daya saing di pasar.
- **Peningkatan Revenue**: Dengan prediksi harga yang lebih akurat, EaseMyTrip dapat meningkatkan pendapatan melalui penerapan dynamic pricing, mengoptimalkan jumlah transaksi, serta menawarkan layanan tambahan yang relevan kepada konsumen.

### Business Questions
- Faktor-faktor apa saja yang paling signifikan memengaruhi fluktuasi harga tiket pesawat?
- Bagaimana prediksi harga dapat meningkatkan konversi penjualan pada platform EaseMyTrip?
- Bagaimana model prediksi harga dapat diintegrasikan untuk menyesuaikan strategi penetapan harga yang mengoptimalkan revenue?

<br>

## Methods
Berikut adalah algoritma yang digunakan dalam proyek ini:
1. Feature Selection: Lasso Regression<br>
Digunakan untuk memilih fitur yang paling signifikan dengan mengurangi koefisien fitur yang tidak penting menjadi nol.
2. Modelling:
   - Linear Regression: Digunakan untuk memprediksi harga tiket dengan hubungan linear antar variabel.
   - Random Forest: Algoritma ensemble yang menangani data kompleks dan memberikan prediksi akurat.
   - XGBoost: Algoritma boosting untuk meningkatkan performa model prediksi.
3. Interpretation:
   - PDP (Partial Dependence Plot): Menggambarkan pengaruh fitur terhadap harga tiket secara global.
   - LIME: Menyediakan interpretasi lokal untuk analisis lebih mendalam dari prediksi model.

<br>

## Results
1. **Random Forest Model**  
   - Performa terbaik dengan RMSE sebesar **2668.17** dan R² Score **98%** pada data test. Model ini mampu menangkap fluktuasi harga dengan baik, terutama untuk maskapai Vistara dan penerbangan dengan durasi lama.
2. **Feature Importance (LIME & PDP)**  
   - **Kelas bisnis**, **maskapai Vistara**, dan **jumlah transit** memberikan kontribusi signifikan terhadap prediksi harga.  
   - Prediksi akurat ini memungkinkan perusahaan menyesuaikan harga secara dinamis.
3. **Algoritma Lain (XGBoost, Linear Regression)**  
   - XGBoost dan Linear Regression digunakan sebagai perbandingan, namun performanya lebih rendah dibandingkan Random Forest.

![download (1)](https://github.com/user-attachments/assets/b539a29f-b945-4816-bf57-0756145b3515)

### Future Work
- Mencoba Algoritma Lain<br>
Algoritma lain yang bisa dicoba untuk kasus regresi meliputi Gradient Boosting, LightGBM, CatBoost, atau bahkan Neural Networks, yang mungkin mampu menangkap pola non-linear yang lebih kompleks.
- Hyperparameter Tuning<br>
Melakukan Grid Search CV untuk hyperparameter tuning bisa membantu mendapatkan kombinasi parameter yang paling optimal, sehingga meningkatkan performa model.
- Interpretasi dengan SHAP<br>
Menggunakan SHAP (SHapley Additive exPlanations) dapat memberikan gambaran lebih akurat tentang interpretasi global dari model, melengkapi analisis dari PDP dan LIME.
- Time Series Analysis<br>
Melakukan time-series analysis untuk mengidentifikasi pola musiman dan perilaku harga yang berulang, serta melakukan forecasting untuk harga tiket di masa depan.
