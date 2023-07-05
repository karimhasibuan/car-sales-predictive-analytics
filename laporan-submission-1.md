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
- **Commision Rate** merupakan Tarif komisi yang dibayarkan kepada tenaga penjual atas penjualan tersebut.
- **Commision Earned** merupakan Jumlah komisi yang diperoleh penjual atas penjualan tersebut.

Tahapan yang dilakukan dalam visualisasi data adalah melakukan visualisasi pada hasil exploratory data analysis seperti menemukan fitur-fitur yang relevan.

## REFERENSI

Chris, S., & Susilawati, D. (2020). Analisis Perancangan Sistem untuk Kepuasan Pelanggan pada UD. Shinta Elektronic dengan Menggunakan Metode Algoritma C4. 5. ALGOR, 1(2), 52-58.

Daqiqil, Ibnu. (2021). Machine Learning: Teori, Studi Kasus dan Implementasi Menggunakan Python (Vol. 1). Unri Press.

Lubis, A. N. (2004). Strategi Pemasaran dalam persaingan bisnis.

Munawar, Z., Muliantara, A., Kmurawak, R. M., Reba, F., Sroyer, A., Sukmawan, D., ... & Beno, I. S. (2023). Big Data Analytics: Konsep, Implementasi, dan Aplikasi Terkini. Kaizen Media Publishing.

Nikmatun, I. A., & Waspada, I. (2019). Implementasi data mining untuk klasifikasi masa studi mahasiswa menggunakan algoritma K-Nearest Neighbor. Simetris: Jurnal Teknik Mesin, Elektro dan Ilmu Komputer, 10(2), 421-432.
