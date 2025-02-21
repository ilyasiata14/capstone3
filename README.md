🚴‍♂️ Capstone 3: Bike Sharing Demand Prediction

📌 Project Overview
Sistem bike-sharing semakin populer di kota-kota besar, tetapi salah satu tantangan utamanya adalah mengoptimalkan jumlah sepeda yang tersedia di berbagai lokasi. Proyek ini bertujuan untuk memprediksi jumlah peminjaman sepeda berdasarkan berbagai faktor seperti cuaca, waktu, dan hari kerja/libur.

🎯 Business Problem
Stakeholder: Operator bike-sharing, pemerintah kota, pengguna layanan.
Tantangan: Menyediakan jumlah sepeda yang cukup tanpa kelebihan atau kekurangan di tiap lokasi.
Solusi: Model Machine Learning yang dapat memprediksi jumlah peminjaman sepeda berdasarkan faktor eksternal.
🗂 Dataset
Sumber: Capital Bikeshare Data
Fitur Utama:
Datetime: dteday, hr, season
Weather: temp, atemp, hum, weathersit
Kondisi Operasional: holiday, workingday
Target: cnt (jumlah total peminjaman sepeda)
🛠 Data Processing & Feature Engineering
Data Cleaning: Menangani missing values, duplikasi, dan format data.
Feature Engineering:
hourly_bin: Mengelompokkan waktu dalam beberapa kategori (pagi, siang, malam).
day_of_week: Menambahkan informasi hari dalam seminggu.
is_weekend: Menandai apakah hari tersebut akhir pekan atau bukan.
Feature Selection: Menggunakan korelasi & feature importance untuk memilih fitur terbaik.
📊 Model Development
Beberapa model Machine Learning yang diuji:

Baseline Model: Linear Regression
Tree-Based Models: Random Forest, XGBoost, LightGBM
Hyperparameter Tuning: Menggunakan GridSearchCV untuk optimasi parameter.
📏 Evaluation Metrics
Model dievaluasi menggunakan:

MAE (Mean Absolute Error)
MSE (Mean Squared Error)
RMSE (Root Mean Squared Error)
R² (R-squared Score)
Model	MAE	MSE	RMSE	R²
Linear Regression	143.6	10025	100.2	0.6775
XGBoost (Final)	66.4	9729.9	98.6	0.6877
📌 Key Insights
✔ XGBoost menghasilkan performa terbaik dengan RMSE lebih rendah & R² lebih tinggi dibanding model lainnya.
✔ Faktor waktu & cuaca sangat berpengaruh terhadap jumlah peminjaman sepeda.
✔ Model ini dapat digunakan untuk membantu operator bike-sharing dalam pengelolaan inventaris sepeda.

🚀 Deployment & Next Steps
Model disimpan dalam format Pickle (.pkl).
Rekomendasi untuk bisnis:
Tambah sepeda saat jam sibuk berdasarkan prediksi model.
Optimalkan lokasi stasiun berdasarkan pola peminjaman.
Pengembangan lebih lanjut:
Integrasi dengan data lalu lintas & event kota.
Eksperimen dengan Time Series Forecasting.

🚀 Project by: Ilya Aryaputra
Untuk detail lebih lanjut, cek notebook Jupyter dan presentasi PPT. 🚴‍♂️✨
