# Laporan Proyek Machine Learning - Dinar Wahyu Rahman
## Domain Proyek

Proyek machine learning yang saya angkat adalah predictive analysis house rent prediction. Penggunaan machine learning yang tepat dalam memprediksi harga sewa rumah sangatlah membantu. Banyak platform sewa rumah yang menggunakan machine learning untuk memudahkan pekerjaan mereka dan para pelanggan. Para pelanggan bisa memilih rumah sesuai dengan kendisi dan pendapatan keuangan masing-masing. Sebab tantangan dalam penyewaan rumah di India ini ialah harganya yang semakin melonjak naik, seiring dengan kepadatan penduduknya yang semakin bertambah kian tahun ke tahun. Banyaknya penduduk tidak sebanding dengan banyaknya pemukiman yang layak huni, membuat harga house rent semakin mahal. Dengan penggunaan machine learning ini, seseorang bisa memperkirakan besarnya biaya pemukiman/house rent yang sesuai dengan kapasitas keuangannya dan sesuai dengan preferensi hunian terbaiknya, seperti besarnya rumah, banyaknya kamar, sudah dilengkapi perabotan atau tidak, dan sebagainya.

Referensi proyek: [Link jurnal](https://www.mdpi.com/2220-9964/8/8/349)

## Business Understanding
### Problem Statement
Bagaimana cara memperkirakan/memprediksi harga sewa rumah (dataset di India) dengan model machine learning kepada user?

### Goals
Dapat melakukan prediksi harga sewa rumah secara tepat. Dampak positif dari penggunaan machine learning untuk memperkirakan harga house rent ini ialah, memberikan gambaran secara garis besar berapa harga yang akan dikeluarkan untuk membeli satu unit rumah, dengan rincian seperti luas rumah, furniture, jumlah kamar, dan lainnya. 
### Solusion Statement
menggunakan model machine learning regresi linear berganda untuk memprediksi nilai numerik atau kontinu berdasarkan fitur atau variabel-variabel lainnya. 

## Data Understanding
dataset yang digunakan pada House Rent Predicion terdapat file csv yang di unduh di situs kaggle. Link dataset sebagai berikut: [Dataset](https://github.com/dinarrahman30/House_Rent_Prediction/blob/main/house_rent_prediction/House_Rent_Dataset.csv)

Untuk variable yang terdapat pada dataset antara lain sebagai berikut:

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

Tahapan yang digunakan mengenai data dengan melakukan eksploratory data analysis yaitu, melihat kondisi rumah yang akan disewa dengan variable Furnishing Status, Serta mengecek distribusi data rumah sewa yang ada di kota-kota India.

## Data Preparation
Data Preparation yang digunakan oleh saya adalah:
- mencari missing value
- mengecek duplicasi data
- melakukan encoding fitur kategori 
- Pembagian dataset dengan fungsi train_test_split dari library sklearn.

## Modeling

Model machine learning yang saya gunakan adalah model regresi linear untuk memprediksi nilai numerik atau kontinu berdasarkan fitur atau variabel-variabel lainnya. Model machine learning regresi yang dipakai ialah model regresi linear berganda. Model regresi linear sederhana ialah metode statistik yang digunakan untuk memodelkan hubungan antara satu variabel dependen dengan lebih dari dua variabel independen, yaitu variabel dependen (Y) dan independen (X1, X2,...). Model regresi linear berganda ini cocok untuk beberapa variabel independen yang mempengaruhi harga sewa secara linear misalnya, luas rumah, jumlah kamar, keberadaan perabotan, dan lainnya.

Berikut hasil dari model machine learning ini, 
![Cuplikan layar 2023-09-19 103051](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/cc85dedd-6db0-48be-8d94-ca4acc998bde)

Gambar 1. Define model

Pada gambar 1 menampilkan jenis model apa yang dipakai, yaitu LSTM.


## Evaluation
Untuk metrik evaluasi pada model house rent predictions ini adalah dengan metric='MSE' pada model compile, seperti, 
![Cuplikan layar 2023-09-19 102435](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/71c36f03-0553-4bd0-b296-fee46fd69cb8)

Gambar 2. Metrik evaluasi

Pada gambar 2 menampilkan metrik evaluasi yang dipakai ialah, mean_square_error. 


Hasil dari model compile tersebut, berikut adalah hasil prediksinya, ![Cuplikan layar 2023-09-17 223220](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/acdf58f2-293e-497f-ba98-d75e0a0f856b)

