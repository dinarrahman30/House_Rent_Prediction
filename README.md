# Laporan Proyek Machine Learning - Dinar Wahyu Rahman
## Domain Proyek

Proyek machine learning yang saya angkat adalah predictive analysis house rent prediction. Penggunaan machine learning yang tepat dalam memprediksi harga sewa rumah sangatlah membantu. Banyak platform sewa rumah yang menggunakan machine learning untuk memudahkan pekerjaan mereka dan para pelanggan. Para pelanggan bisa memilih rumah sesuai dengan kendisi dan pendapatan keuangan masing-masing.

Referensi proyek: [Link jurnal](https://www.mdpi.com/2220-9964/8/8/349)

## Business Understanding
### Problem Statement
Bagaimana cara memperkirakan/memprediksi harga sewa rumah (dataset di India) dengan model machine learning kepada user?

### Goals
Dapat melakukan prediksi harga sewa rumah secara tepat.
### Solusion Statement
menggunakan model machine learning regresi untuk memprediksi nilai numerik atau kontinu berdasarkan fitur atau variabel-variabel lainnya.

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

Model machine learning yang saya gunakan adalah model regresi untuk memprediksi nilai numerik atau kontinu berdasarkan fitur atau variabel-variabel lainnya.
Berikut hasil dari model machine learning ini,
![Cuplikan layar 2023-09-11 222329](https://github.com/dinarrahman30/House_Rent_Prediction/assets/68122380/836b7299-b1d3-48bb-9795-b9591bc28bea)


## Evaluation
Untuk metrik evaluasi pada model house rent predictions ini adalah dengan metric='acc' pada model compile, seperti,

Hasil dari model compile tersebut, dimana accuracy sebesar 
