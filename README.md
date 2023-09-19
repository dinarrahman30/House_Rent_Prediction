# Laporan Proyek Machine Learning - Dinar Wahyu Rahman
## Domain Proyek
Proyek machine learning yang saya angkat adalah predictive analysis house rent prediction. Penggunaan machine learning yang tepat dalam memprediksi harga sewa rumah sangatlah membantu. Banyak platform sewa rumah yang menggunakan machine learning untuk memudahkan pekerjaan mereka dan para pelanggan. Para pelanggan bisa memilih rumah sesuai dengan kendisi dan pendapatan keuangan masing-masing. Sebab tantangan dalam penyewaan rumah di India ini ialah harganya yang semakin melonjak naik, seiring dengan kepadatan penduduknya yang semakin bertambah kian tahun ke tahun. Banyaknya penduduk tidak sebanding dengan banyaknya pemukiman yang layak huni, membuat harga house rent semakin mahal. Dengan penggunaan machine learning ini, seseorang bisa memperkirakan besarnya biaya pemukiman/house rent yang sesuai dengan kapasitas keuangannya dan sesuai dengan preferensi hunian terbaiknya, seperti besarnya rumah, banyaknya kamar, sudah dilengkapi perabotan atau tidak, dan sebagainya.


## Business Understanding
### Problem Statement
1. Bagaimana cara memperkirakan/memprediksi harga sewa rumah (dataset di India) dengan model machine learning kepada user?
2. jenis model machine learning apa yang cocok digunakan untuk memprediksi harga sewa rumah di India?
### Goals
1. Dapat melakukan prediksi harga sewa rumah secara tepat. Caranya penggunaan machine learning untuk memperkirakan harga house rent ini ialah, memasukkan data-data rincian ruma sewa yang ingin disewa, dengan isi rincian seperti luas rumah, kelengkapan furniture, jumlah kamar, dan lainnya.
2. Dengan menggunakan model machine learning regresi linear berganda untuk memprediksi nilai numerik atau kontinu berdasarkan fitur atau variabel-variabel lainnya. Model regresi linear sederhana ialah metode statistik yang digunakan untuk memodelkan hubungan antara satu variabel dependen dengan lebih dari dua variabel independen, yaitu variabel dependen (Y) dan independen (X1, X2,...). Model regresi linear berganda ini cocok untuk beberapa variabel independen yang mempengaruhi harga sewa secara linear misalnya, luas rumah, jumlah kamar, keberadaan perabotan, dan lainnya.

## Data Understanding
dataset yang digunakan pada House Rent Predicion terdapat file csv yang di unduh di situs kaggle. Link dataset sebagai berikut: [Dataset](https://github.com/dinarrahman30/House_Rent_Prediction/blob/main/house_rent_prediction/House_Rent_Dataset.csv)

Untuk keterangan variable yang terdapat pada dataset antara lain sebagai berikut:

- BHK: Number of Bedrooms, Hall, Kitchen.
- Rent: Rent of the Houses/Apartments/Flats.
- Size: Size of the Houses/Apartments/Flats in Square Feet.
- Floor: Houses/Apartments/Flats situated in which Floor and Total Number of Floors (Example: Ground out of 2, 3 out of 5, etc.)
- Area Type: Size of the Houses/Apartments/Flats calculated on either Super Area or Carpet Area or Build Area.
- Area Locality: Locality of the Houses/Apartments/Flats.
- City: City where the Houses/Apartments/Flats are Located.
- Furnishing Status: Furnishing Status of the Houses/Apartments/Flats, either it is Furnished or Semi-Furnished or Unfurnished.
- Tenant Preferred: Type of Tenant Preferred by the Owner or Agent.
- Bathroom: Number of Bathrooms.
- Point of Contact: Whom should you contact for more information regarding the Houses/Apartments/Flats.

Tahapan yang digunakan mengenai data dengan melakukan eksploratory data analysis yaitu, melihat kondisi rumah yang akan disewa dengan variable Furnishing Status, Serta mengecek distribusi data rumah sewa yang ada di kota-kota India. Untuk ukuran dataset yang dipakai sebesar (4746, 12). Sementara untuk lisensi dari dataset ialah bersifat publik dan berkatogori dummies, namun dataset ini tetap dapat dijadikan preferensi simulasi dari prediksi harga sewa rumah di India. Untuk teknik visualisasi data apda bagian EDA, lebih bayak menggunakan visualisasi diagram batang dan pie, sepeti,

![diagram 1](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/fb0ab42b-5fea-4fcd-8881-22f11912c290)

Gambar Diagram Batang 1. Bar Plot for Number of House in Each City which is Available for Rent.

![diagram 2](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/4d639094-cdc8-48d8-81cb-d8aa226944e9)

Gambar Diagram Batang 2. look at the rent of the houses in different cities according to the furnishing status of the house.

![diagram 3](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/55608920-fc48-4572-aed1-15954d59b640)

Gambar Diagram Pie. Pie Plot on Cities to check the distribution.


## Data Preparation
Data Preparation yang digunakan oleh saya adalah:
- mencari data missing value atau data dengan isi 0 atau null dengan kode house_rent.isnull().sum(). Dimaksudkan agar data yang kosong atau null ini tidak mengganggu kita saat train dataset. Mencegah bias data yang mengakibatkan pada kesalahan prediksi harga sewa rumah.
- mengecek duplicasi data. dengan kode house_rent.duplicated().sum() duplikasi data dapat menyebabkan overfitting pada saat train model, menghasilakn bias pada hasil prediksi.

## Modeling

Model machine learning yang saya gunakan adalah model regresi linear untuk memprediksi nilai numerik atau kontinu berdasarkan fitur atau variabel-variabel lainnya. Model machine learning regresi yang dipakai ialah model regresi linear berganda. Model regresi linear sederhana ialah metode statistik yang digunakan untuk memodelkan hubungan antara satu variabel dependen dengan lebih dari dua variabel independen, yaitu variabel dependen (Y) dan independen (X1, X2,...).

Kelebihan dari model regresi linear berganda ini ialah,
- Model regresi linear berganda ini cocok untuk beberapa variabel independen yang mempengaruhi harga sewa secara linear misalnya, luas rumah, jumlah kamar, keberadaan perabotan, dan lainnya.
- Modelnya juga sederhana dan mudah untuk dipahami. Model ini cocok untuk mereka yang belajar machine learning awal.

Kekurangan dari model regresi berganda ini adalah,

- Terlalu sederhana, hasil yang didapat tidak sekompleks model machine learning lainnya.
- Model ini juga sensitif terhadap adanya outlier dalam data. Poin data yang ekstrem dapat memengaruhi koefisien regresi dan kinerja model secara signifikan.
- Rentan akan overfitting dan underfitting hasil. Resiko ini juga dapat ditemui di hampir semua model machine learning.

Berikut hasil dari model machine learning ini, 
![Define Model](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/cc85dedd-6db0-48be-8d94-ca4acc998bde)

Gambar 2. Define model

Pada gambar 2 menampilkan jenis model apa yang dipakai, yaitu LSTM. Model LSTM atau Long Short-Term Memory untuk memprediksi harga sewa rumah atau house rent adalah pendekatan yang unik, tetapi bisa menjadi fitur yang menarik jika kita ingin memperhitungkan urutan waktu dalam data atau jika kita memiliki data historis yang berkaitan dengan harga sewa rumah.

## Evaluation
Untuk metrik evaluasi pada model house rent predictions ini adalah dengan metric='MSE' pada model compile, seperti, 
![Metrik Evaluasi](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/71c36f03-0553-4bd0-b296-fee46fd69cb8)

Gambar 3. Metrik evaluasi

Pada gambar 3 menampilkan metrik evaluasi yang dipakai ialah, mean_squared_error atau MSE. MSE mengukur rata-rata dari kuadrat selisih antara nilai prediksi dan nilai sebenarnya.

#### Rumus: MSE = Σ (y_pred - y_true)^2 / n

Dan untuk optimizernya menggunakan 'Adam'. Optimizer 'Adam' adalah salah satu metode optimasi yang sering digunakan dalam pembuatan model regresi, termasuk model untuk memprediksi harga sewa rumah atau house rent, dan merupakan kombinasi dari metode-metode optimasi lain yang efektif.


Berikut adalah hasil prediksi dari sewa rumah dengan memasukkan variabel-variabel yang menentukan harga sewa rumah, 

![Prediksi Harga Sewa Rumah](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/c154b817-471d-43aa-8415-ecf074e53547)

Gambar. 4 Prediksi Harga Sewa Rumah.

## Kesimpulan
tujuan utama dari penggunaan machine learning yang tepat dalam memprediksi harga sewa rumah sangatlah membantu. Banyak platform sewa rumah yang menggunakan machine learning untuk memudahkan pekerjaan mereka dan para pelanggan. Para pelanggan bisa memilih rumah sesuai dengan kendisi dan pendapatan keuangan masing-masing.

## Referensi 
Zhou, X., Tong, W., & Li, D. (2019). Modeling housing rent in the Atlanta metropolitan area using textual information and deep learning. ISPRS International Journal of Geo-Information, 8(8), 349.

Referensi proyek: [Link jurnal](https://www.mdpi.com/2220-9964/8/8/349)
