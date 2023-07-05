# Laporan Proyek Machine Learning

## Domain Proyek

Penjualan mobil merupakan salah satu bisnis di dunia industri. Dalam menjalankan bisnis tersebut, diperlukan strategi pemasaran yang tepat dalam menentukan harga produk agar dapat memberikan harga yang ideal bagi konsumen (Lubis, 2004). Konsumen sering kali ingin mengetahui harga yang realistis sebelum membeli mobil, hal ini membantu mereka dalam melakukan perencanaan keuangan dan pengambilan keputusan pembelian yang lebih baik.

Dalam menentukan harga mobil dapat dilakukan dengan berbagai cara diantaranya melakukan pendekatan machine learning. Machine learning merupakan salah satu teknik yang dapat membantu dalam melakukan prediksi (Daqiqil, 2021).

## Business Understanding

### Problem Statements

- Faktor apa yang mempengaruhi harga penjualan mobil?
- Bagaimana pendekatan machine learning yang digunakan untuk prediksi harga mobil?

### Goals

- Mengetahui faktor yang mempengaruhi harga penjualan mobil.
- Mengetahui pendekatan machine learning yang digunakan untuk prediksi harga mobil.

### Solution Approach

Berdasarkan peryantaan masalah dan tujuan yang telah disebutkan, maka terdapat solusi yang diberikan yaitu dengan menggunakan 3 algoritma Machine Learning pada kasus model regresi sebagai berikut:

- Regresi Linear

  Regresi linear adalah salah satu algoritma yang paling sederhana dan paling umum digunakan dalam prediksi variabel kontinu. Keuntungan utama regresi linear adalah interpretabilitas yang tinggi. Model regresi linear memberikan pemahaman yang jelas tentang bagaimana setiap fitur (tipe, model, tahun mobil) berkontribusi terhadap prediksi harga mobil. Selain itu, regresi linear bekerja dengan baik ketika ada hubungan linier yang kuat antara fitur-fitur independen dan variabel dependen (Munawar et al., 2023).

- Decision Tree

  Decision tree adalah algoritma yang dapat memodelkan hubungan yang lebih kompleks antara fitur-fitur dan variabel target. Decision tree membagi dataset berdasarkan pemilihan fitur yang paling informatif pada setiap langkahnya, dan ini memungkinkan pemodelan yang lebih kompleks dibandingkan dengan regresi linear ( Chris & Susilawati, 2020).

- KNN (K-Nearest Neighbors)

  KNN (K-Nearest Neighbors) adalah algoritma machine learning yang digunakan untuk klasifikasi dan regresi. Algoritma ini bekerja dengan mencari tetangga terdekat dari suatu data dan memprediksi berdasarkan mayoritas label atau rata-rata nilai tetangga terdekatnya. KNN dipilih karena kemampuannya yang sederhana, intuitif, dan mampu menangani hubungan lokal antara fitur dan target (Nikmatun & Waspada, 2019).

Berdasarkan algoritma yang digunakan diatas, maka akan dilakukan evaluasi dan pengujian model menggunakan metrik evaluasi yang tepat seperti Mean Squared Error (MSE).

## Data Understanding

Dataset yang digunakan pada proyek machine learning ini adalah [Car Sales Data](https://www.kaggle.com/datasets/suraj520/car-sales-data) yang bersumber dari Kaggle. Dataset ini berisi informasi tentang penjualan mobil dari dealer mobil selama setahun.

Berdasarkan dataset diatas, maka dapat diketahui variabel-variabel pada dataset tersebut yaitu sebagai berikut:

- **Date** merupakan tanggal penjualan mobil.
- **Salesperson** merupakan nama penjual yang melakukan penjualan.
- **Customer Name** merupakan nama pelanggan yang membeli mobil.
- **Car Make** merupakan merk mobil yang dibeli.
- **Car Model** merupakan model dari merk mobil yang dibeli.
- **Car Year** merupakan tahun pembuatan mobil yang dibeli.
- **Sale Price** merupakan harga mobil yang dijual dalam bentuk USD.
- **Commission Rate** merupakan Tarif komisi yang dibayarkan kepada tenaga penjual atas penjualan tersebut.
- **Commission Earned** merupakan Jumlah komisi yang diperoleh penjual atas penjualan tersebut.

Tahapan yang dilakukan dalam visualisasi data adalah melakukan visualisasi pada hasil exploratory data analysis seperti menemukan fitur-fitur yang relevan.

## DATA PREPARATION

Pada project ini, terdapat beberapa teknik data preparation yang digunakan, yaitu:

- Melakukan EDA (Exploratory Data Analysis), bertujuan untuk mendapatkan informasi fitur mengenai dataset yang digunakan.
- Melakukan pengecekan terhadap data yang null atau duplikat.
- Melakukan drop pada kolom yang tidak relevan untuk diproses ke model seperti Date, Salesperson, Customer Name dan Year.
- Melakukan Encoding pada variabel kategorikal yaitu kolom Car Make dan Car Model, bertujuan untuk mengkonversi variabel kategori menjadi angka atau vektor numerik yang mewakili kategori-kategori tersebut.
- Melakukan Feature Scaling pada data numerik yaitu kolom Car Year, Commission Rate, dan Commission Earned menggunakan MinMaxScaler(), yang berfungsi untuk melakukan normalisasi dan standarisasi data.
- Memisahkan kolom fitur dan target. Dalam hal ini, kolom fitur yaitu kolom selain Sale Price dan kolom target adalah Sale Price.
- Membagi dataset yang telah melewati tahap preprocessing menjadi data latih dan data uji. Pembagian dibagi sebesar 80% untuk data latih dan 20% data uji.

## MODELLING

Pada project ini, menggunakan 3 algoritma yaitu Regresi Linear, Decision Tree dan KNN (K-Nearest Neighbors). Kelebihan dan Kekurangan Algoritma tersebut adalah sebagai berikut:

Berikut adalah kelebihan dan kekurangan dari tiga algoritma tersebut:

1. Regresi Linear:
   Kelebihan:

   - Sederhana dan mudah diinterpretasikan.
   - Cocok untuk memodelkan hubungan linier antara variabel dependen dan independen.
   - Cocok untuk memprediksi nilai kontinu.

   Kekurangan:

   - Tidak bisa menangkap hubungan non-linier antara variabel.
   - Rentan terhadap asumsi yang tidak terpenuhi, seperti asumsi keterikatan linieritas dan independensi error.

2. Decision Tree:
   Kelebihan:

   - Mudah dipahami dan diinterpretasikan.
   - Mampu menangani data dengan jenis variabel campuran (numerik dan kategorikal).
   - Tidak memerlukan preprocessing data yang rumit.

   Kekurangan:

   - Cenderung overfitting terhadap data pelatihan jika tidak diatur dengan baik.
   - Tidak stabil terhadap perubahan kecil pada data pelatihan.

3. KNN (K-Nearest Neighbors):
   Kelebihan:

   - Sederhana dan mudah diimplementasikan.
   - Tidak mengasumsikan distribusi data tertentu.
   - Mampu menangani data dengan variasi tinggi dan tidak memerlukan asumsi yang kuat tentang data.

   Kekurangan:

   - Memerlukan komputasi yang lebih tinggi karena melibatkan perhitungan jarak antara data.
   - Sensitif terhadap skala data dan pemilihan parameter K yang tepat.
   - Tidak memberikan interpretasi yang jelas tentang hubungan antara variabel.

Berdasarkan hasil modelling dari 3 algoritma yang digunakan diatas, algoritma Decision Tree membutuhkan lebih banyak waktu dibandingkan algoritma lainnya.

## EVALUATION

Pada project ini, matriks evaluasi yang digunakan dalam proyek ini adalah Mean Squared Error (MSE). MSE digunakan sebagai ukuran kesalahan antara nilai prediksi dan nilai sebenarnya dalam kasus regresi. Semakin kecil nilai MSE, semakin baik model dalam melakukan prediksi yang akurat. Dalam kasus ini, tiga algoritma telah dievaluasi yaitu Regresi Linear, Decision Tree, dan KNN.

[![mse-reports.png](https://i.postimg.cc/5Nw2y7fn/mse-reports.png)](https://postimg.cc/ZC5SDLBd)

Berdasarkan hasil diatas, dapat diketahui bahwa Decision Tree maupun KNN memberikan hasil prediksi yang lebih baik dengan nilai MSE yang lebih rendah dibandingkan Regresi Linear. Oleh karena itu, untuk dataset ini, model Decision Tree dan KNN lebih disarankan untuk digunakan dalam melakukan prediksi Sale Price.

[![sale-predict.png](https://i.postimg.cc/J4TdNm7n/sale-predict.png)](https://postimg.cc/6yv0KkvJ)

Berdasarkan hasil pengujian prediksi diatas, memang hasil pada algoritma Decision Tree yang paling mendekati kemudian disusul oleh KNN dan ada algoritma Regresi Linear. Meski begitu, hasil prediksi masih jauh dari nilai asli.

[![important-feature.png](https://i.postimg.cc/BZPxY0Cb/important-feature.png)](https://postimg.cc/kD96GLzP)

Hasil yang didapatkan menunjukkan skor pentingnya fitur dalam menentukan Sale Price. Setiap fitur memiliki skor penting yang dinyatakan sebagai angka.

Misalnya, "Commission Earned" memiliki skor penting sebesar 0.7083596164141285, yang berarti fitur tersebut memiliki pengaruh yang paling signifikan dalam menentukan Sale Price. Skor penting ini dapat diinterpretasikan sebagai persentase kontribusi fitur tersebut dalam mempengaruhi Sale Price.

Selanjutnya, "Commission Rate" memiliki skor penting sebesar 0.2916393396038089, yang menunjukkan bahwa fitur ini juga memiliki pengaruh yang cukup signifikan dalam menentukan Sale Price, meskipun tidak sebesar "Commission Earned".

Fitur-fitur lainnya, seperti "Car Year", "Car Make_Nissan", "Car Make_Toyota", dan seterusnya, memiliki skor penting yang sangat kecil, bahkan mendekati nol. Hal ini menunjukkan bahwa fitur-fitur tersebut memiliki pengaruh yang relatif kecil atau kurang signifikan dalam memprediksi Sale Price.

Dalam konteks ini, skor penting yang lebih tinggi menandakan bahwa fitur tersebut memiliki pengaruh yang lebih besar dalam menentukan Sale Price, sedangkan skor penting yang lebih rendah menandakan pengaruh yang lebih kecil.

Dalam beberapa kasus, komisi yang diperoleh dan tingkat komisi yang diterapkan dapat mencerminkan karakteristik penjualan mobil tertentu. Misalnya, mobil dengan harga jual yang lebih tinggi mungkin memiliki komisi yang lebih besar, atau komisi yang diberikan untuk penjualan mobil tertentu mungkin lebih tinggi dibandingkan dengan mobil lainnya. Oleh karena itu, fitur-fitur ini dapat memberikan informasi penting dalam memprediksi Sale Price.

## REFERENSI

Chris, S., & Susilawati, D. (2020). Analisis Perancangan Sistem untuk Kepuasan Pelanggan pada UD. Shinta Elektronic dengan Menggunakan Metode Algoritma C4. 5. ALGOR, 1(2), 52-58.

Daqiqil, Ibnu. (2021). Machine Learning: Teori, Studi Kasus dan Implementasi Menggunakan Python (Vol. 1). Unri Press.

Lubis, A. N. (2004). Strategi Pemasaran dalam persaingan bisnis.

Munawar, Z., Muliantara, A., Kmurawak, R. M., Reba, F., Sroyer, A., Sukmawan, D., ... & Beno, I. S. (2023). Big Data Analytics: Konsep, Implementasi, dan Aplikasi Terkini. Kaizen Media Publishing.

Nikmatun, I. A., & Waspada, I. (2019). Implementasi data mining untuk klasifikasi masa studi mahasiswa menggunakan algoritma K-Nearest Neighbor. Simetris: Jurnal Teknik Mesin, Elektro dan Ilmu Komputer, 10(2), 421-432.

---Ini adalah bagian akhir laporan---
