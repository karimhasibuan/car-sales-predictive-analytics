# Laporan Proyek Machine Learning

## Domain Proyek

Industri alat angkutan atau otomotif di Indonesia menunjukkan pertumbuhan yang positif berdasarkan data dari Badan Pusat Statistik (BPS). Pada tahun 2022, produk domestik bruto (PDB) industri otomotif atas dasar harga konstan (ADHK) mencapai Rp207,79 triliun, mengalami kenaikan sebesar 10,67% dibandingkan tahun sebelumnya yang sebesar Rp187,75 triliun. Setelah mengalami penurunan akibat pandemi Covid-19 pada tahun 2020, industri otomotif mulai pulih sejak tahun 2021 dan pertumbuhannya terus berlanjut pada tahun lalu. PDB industri otomotif juga menempati posisi ketiga terbesar di antara subsektor industri pengolahan lainnya, di bawah industri logam dasar yang tumbuh 14,8% dan industri mesin yang naik 11,37% [[1]](https://www.bps.go.id/indikator/indikator/view_data_pub/0000/api_pub/aDJqeEc4MTJlOWRaRWFOQ1Q4UE5UQT09/da_15/1).

Pertumbuhan industri otomotif didukung oleh kebijakan pemerintah dalam bentuk diskon pajak penjualan atas barang mewah (PPnBM) sepanjang tahun 2022. Kebijakan ini berhasil meningkatkan penjualan mobil sebesar 18,1%. Industri alat angkutan, sebagai bagian dari industri pengolahan, berkontribusi sebesar 8,67% terhadap PDB industri pengolahan pada tahun 2022 [[2]](https://kemenperin.go.id/artikel/22994/Produksi-Mobil-Lampaui-Target,-Penjualan-Naik-71-Persen). Data ini menunjukkan pentingnya industri otomotif dalam ekonomi nasional dan perannya dalam memulihkan pertumbuhan ekonomi setelah masa-masa sulit akibat pandemi [[3]](https://dataindonesia.id/sektor-riil/detail/kinerja-industri-otomotif-melonjak-1067-pada-2022).

Penjualan mobil adalah salah satu sektor bisnis yang memiliki peran penting dalam industri otomotif. Di tengah persaingan yang semakin ketat dan meningkatnya permintaan konsumen, strategi pemasaran yang tepat menjadi kunci keberhasilan dalam menjalankan bisnis penjualan mobil. Salah satu aspek penting dalam strategi pemasaran adalah menentukan harga yang tepat untuk mobil yang ditawarkan. Menetapkan harga yang ideal adalah suatu tantangan, mengingat perbedaan preferensi konsumen, persaingan pasar, dan faktor-faktor lainnya yang mempengaruhi harga mobil [[4]](https://ejournal.unsrat.ac.id/index.php/emba/article/view/21893).

Dalam upaya menentukan harga mobil yang realistis, diperlukan pendekatan yang dapat memberikan hasil prediksi yang akurat. Salah satu pendekatan yang dapat digunakan adalah penerapan teknik _machine learning_. Dengan menggunakan teknik _machine learning_, kita dapat memanfaatkan data historis penjualan mobil, variabel-variabel yang relevan, dan algoritma pembelajaran mesin untuk melakukan prediksi harga mobil yang lebih akurat [[5]](https://slims.ahmaddahlan.ac.id/index.php?p=fstream-pdf&fid=40&bid=3192).

Penerapan teknik _machine learning_ dalam menentukan harga mobil memiliki relevansi yang kuat dengan kebutuhan pasar dan preferensi konsumen. Konsumen sering kali ingin memiliki gambaran yang jelas tentang harga yang realistis sebelum mereka memutuskan untuk membeli mobil. Dengan adanya prediksi harga yang lebih akurat melalui teknik _machine learning_, konsumen dapat melakukan perencanaan keuangan dengan lebih baik, membandingkan harga dari berbagai pilihan mobil, dan membuat keputusan pembelian yang lebih informasional.

Oleh karena itu, penggunaan teknik _machine learning_ dalam menentukan harga mobil memberikan manfaat yang signifikan dalam meningkatkan keputusan bisnis, memberikan keuntungan kompetitif, dan memberikan kepuasan bagi konsumen.

## Business Understanding

### Problem Statements

- Faktor apa yang paling berpengaruh terhadap harga penjualan mobil?
- Bagaimana pendekatan _machine learning_ dapat digunakan untuk memprediksi harga mobil berdasarkan faktor-faktor yang berpengaruh tersebut?

### Goals

- Memahami faktor-faktor yang mempengaruhi harga penjualan mobil untuk dapat mengidentifikasi variabel yang paling signifikan dalam menentukan harga sehingga memberikan wawasan yang lebih baik dalam strategi penetapan harga, mendukung pengambilan keputusan yang lebih informasional, dan memperkuat strategi pemasaran dalam industri penjualan mobil.
- Memahami pendekatan _machine learning_ yang digunakan untuk prediksi harga mobil, sehingga melalui penerapan pendekatan _machine learning_ dalam prediksi harga mobil mampu meningkatkan efisiensi dan kecepatan dalam penentuan harga, meminimalkan kesalahan manusia, serta memberikan keunggulan kompetitif dalam bisnis penjualan mobil.

### Solution Approach

Berdasarkan pernyataan masalah dan tujuan yang telah disebutkan, maka terdapat solusi yang diberikan yaitu dengan menggunakan 3 algoritma Machine Learning pada kasus model regresi sebagai berikut:

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

[[1]](https://www.bps.go.id/indikator/indikator/view_data_pub/0000/api_pub/aDJqeEc4MTJlOWRaRWFOQ1Q4UE5UQT09/da_15/1) B. P. Statistik, “Laju Pertumbuhan Produk Domestik Bruto Atas Dasar Harga Konstan 2010 Menurut Lapangan Usaha (persen), 2022,” Badan Pusat Statistik, https://www.bps.go.id/indikator/indikator/view_data_pub/0000/api_pub/aDJqeEc4MTJlOWRaRWFOQ1Q4UE5UQT09/da_15/1 (accessed Jul. 5, 2023).

[[2]](https://kemenperin.go.id/artikel/22994/Produksi-Mobil-Lampaui-Target,-Penjualan-Naik-71-Persen) K. Perindustrian, “Kemenperin: Produksi Mobil Lampaui Target, Penjualan Naik 71 persen,” Kementerian Perindustrian, https://kemenperin.go.id/artikel/22994/Produksi-Mobil-Lampaui-Target,-Penjualan-Naik-71-Persen (accessed Jul. 5, 2023).

[[3]](https://dataindonesia.id/sektor-riil/detail/kinerja-industri-otomotif-melonjak-1067-pada-2022) S. Sadya, “Kinerja Industri Otomotif melonjak 10,67% PADA 2022,” Dataindonesia.id, https://dataindonesia.id/sektor-riil/detail/kinerja-industri-otomotif-melonjak-1067-pada-2022 (accessed Jul. 5, 2023).

[[4]](https://ejournal.unsrat.ac.id/index.php/emba/article/view/21893) G. A. Taroreh, L. Mananeke, and F. Roring, “ANALISIS STRATEGI PEMASARAN DALAM MENINGKATKAN VOLUME PENJUALAN MOBIL MITSUBISHI XPANDER PADA PT. BOSOWA BERLIANMOTOR KAIRAGI MARKETING STRATEGY ANALYSIS IN INCREASING THE SALES VOLUME OF MITSUBISHI XPANDER CARS AT PT. BOSOWA BERLIAN MOTOR KAIRAGI,” Analisis Strategi…… 3683 Jurnal EMBA, vol. 6, no. 4, pp. 3683–3692, 2018.

[[5]](https://slims.ahmaddahlan.ac.id/index.php?p=fstream-pdf&fid=40&bid=3192) I. Daqiqil, MACHINE LEARNING: Teori, Studi Kasus Dan Implementasi Menggunakan Python. Riau, Universitas Riau: UR Press, 2021.

Chris, S., & Susilawati, D. (2020). Analisis Perancangan Sistem untuk Kepuasan Pelanggan pada UD. Shinta Elektronic dengan Menggunakan Metode Algoritma C4. 5. ALGOR, 1(2), 52-58.

Munawar, Z., Muliantara, A., Kmurawak, R. M., Reba, F., Sroyer, A., Sukmawan, D., ... & Beno, I. S. (2023). Big Data Analytics: Konsep, Implementasi, dan Aplikasi Terkini. Kaizen Media Publishing.

Nikmatun, I. A., & Waspada, I. (2019). Implementasi data mining untuk klasifikasi masa studi mahasiswa menggunakan algoritma K-Nearest Neighbor. Simetris: Jurnal Teknik Mesin, Elektro dan Ilmu Komputer, 10(2), 421-432.

---Ini adalah bagian akhir laporan---
