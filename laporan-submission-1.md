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

Pada proyek ini, penulis menawarkan untuk menggunakan 3 algoritma dalam melakukan prediksi harga mobil dan menentukan algoritma yang paling baik prediksinya diantara lainnya. Adapun algoritma yang dipilih yaitu:

- Regresi Linear
- _Decision Tree_
- KNN (_K-Nearest Neighbors_)

Berikut adalah penjelasan yang lebih mendalam mengenai pemilihan ketiga algoritma (Regresi Linear, _Decision Tree_, KNN) sebagai solusi untuk memprediksi harga mobil dan bagaimana masing-masing algoritma dapat membantu menjawab pertanyaan masalah:

- Regresi Linear: Algoritma ini dipilih karena sederhana dan memiliki interpretabilitas tinggi. Regresi linear dapat memberikan pemahaman yang jelas tentang kontribusi setiap fitur (tipe, model, tahun mobil) terhadap prediksi harga mobil. Dengan demikian, kita dapat mengidentifikasi variabel yang paling signifikan dalam menentukan harga.

- _Decision Tree_: Algoritma ini dipilih karena kemampuannya untuk memodelkan hubungan yang kompleks antara fitur-fitur dan variabel target. _Decision tree_ membagi _dataset_ berdasarkan pemilihan fitur yang paling informatif pada setiap langkahnya. Hal ini memungkinkan pemodelan yang lebih kompleks dibandingkan dengan regresi linear. _Decision tree_ dapat membantu menggali hubungan non-linear antara fitur-fitur dan harga mobil.

- KNN (_K-Nearest Neighbors_): Algoritma ini dipilih karena sifatnya yang sederhana, intuitif, dan mampu menangani hubungan lokal antara fitur-fitur dan target. KNN mencari tetangga terdekat dari suatu data dan memprediksi berdasarkan mayoritas label atau rata-rata nilai tetangga terdekatnya. KNN dapat membantu dalam mengidentifikasi pola lokal yang mungkin terdapat dalam data, sehingga dapat memberikan prediksi yang lebih akurat dalam kasus harga mobil.

Pada proyek ini, matriks evaluasi yang digunakan adalah _Mean Absolute Error_ (MAE) dan _Mean Squared Error_ (MSE). Hal ini bertujuan untuk mengetahui kesalahan prediksi yang terkecil dari setiap algoritma yang digunakan.

## Data Understanding

_Dataset_ yang digunakan pada proyek _machine learning_ ini adalah [_Car Sales Data_](https://www.kaggle.com/datasets/suraj520/car-sales-data) yang bersumber dari situs Kaggle. _Dataset_ ini berisi 2.500.000 baris informasi tentang penjualan mobil dari _dealer_ mobil selama setahun. _Dataset_ mencakup sembilan kolom data untuk setiap penjualan mobil. Berikut penjelasan dari setiap kolom yang dimiliki oleh _dataset_ ini.

- **_Date_** merupakan data tanggal penjualan mobil dilakukan.
- **_Salesperson_** merupakan data nama penjual yang melakukan penjualan.
- **_Customer Name_** merupakan data nama pelanggan yang membeli mobil.
- **_Car Make_** merupakan data merk mobil yang dibeli seperti, Toyota, Honda, Ford, Chevrolet, atau Nissan.
- **_Car Model_** merupakan data model dari merk mobil yang dibeli seperti, Corolla, Civic, F-150, Silverado, atau Altima.
- **_Car Year_** merupakan data tahun pembuatan mobil yang dibeli, mulai dari tahun 2010 hingga 2022.
- **_Sale Price_** merupakan data harga mobil yang dijual dalam bentuk USD.
- **_Commission Rate_** merupakan tingkat komisi yang dibayarkan kepada penjual atas penjualan, nilainya berkisar 0,05-0,15.
- **_Commission Earned_** merupakan Jumlah komisi yang diperoleh penjual atas penjualan tersebut.

Kolom '_Car Make_', '_Car Model_' dan '_Car Year_' merupakan variabel yang berhubungan dengan mobil yang dijual.

Kumpulan data ini berguna untuk menganalisis tren penjualan mobil dari waktu ke waktu dan menganalisis dampak dari berbagai faktor pada penjualan mobil. Hal ini yang menjadikan penulis menggunakan _dataset_ ini sebagai sumber data yang digunakan pada proyek.

Contoh visualisasi data yang digunakan adalah diantaranya sebagai berikut:

- _Box Plot_, merupakan bentuk visualisasi statistik yang bertujuan untuk melihat adanya _outlier_ pada data.

[![boxplot.jpg](https://i.postimg.cc/fL7yPVdZ/boxplot.jpg)](https://postimg.cc/qhRphMQZ)

Gambar 1. Contoh bentuk _boxplot_ [[6]](https://eksplorasidatasaham.wordpress.com/2017/02/08/melihat-pola-sebaran-data-saham-analisa-boxplot/).

- Line Chart,merupakan bentuk visualisasi statistik yang bertujuan untuk menampilkan data yang berkelanjutan sepanjang waktu atau rentang nilai tertentu.

[![line-plot.png](https://i.postimg.cc/L4139Sd1/line-plot.png)](https://postimg.cc/rzqrjvwV)

Gambar 2. Contoh bentuk _line chart_ [[7]](https://ilmudatapy.com/membuat-line-plot-dengan-matplotlib-python/).

- Bar Chart, merupakan bentuk visualisasi statistik yang bertujuan untuk menampilkan perbandingan antara beberapa variabel.

[![barchart.png](https://i.postimg.cc/yx8M4Nd2/barchart.png)](https://postimg.cc/ZBX7646L)

Gambar 3. Contoh bentuk _bar chart_ [[8]](https://id.wikipedia.org/wiki/Templat:Vertical_bar_chart).

Grafik-grafik diatas akan digunakan dalam melakukan visualisasi pada hasil _Exploratory Data Analysis_ (EDA).

## DATA PREPARATION

Tahapan _data preparation_ dapat dilakukan sebagai berikut:

**1. Melakukan EDA (_Exploratory Data Analysis_)**, bertujuan untuk mendapatkan informasi fitur mengenai _dataset_ yang digunakan.

**1a. Menampilkan beberapa isi data yaitu dengan menampilkan 5 data teratas dan 5 data terakhir. Hasilnya dapat dilihat pada Tabel 1 berikut.**

Tabel 1. 5 data teratas dan terbawah dari _Car Sales Dataset_.

| Date       | Salesperson     | Customer Name   | Car Make  | Car Model | Car Year | Sale Price | Commission Rate | Commission Earned |
| ---------- | --------------- | --------------- | --------- | --------- | -------- | ---------- | --------------- | ----------------- |
| 2022-08-01 | Monica Moore MD | Mary Butler     | Nissan    | Altima    | 2018     | 15983      | 0.070495        | 1126.73           |
| 2023-03-15 | Roberto Rose    | Richard Pierce  | Nissan    | F-150     | 2016     | 38474      | 0.134439        | 5172.40           |
| 2023-04-29 | Ashley Ramos    | Sandra Moore    | Ford      | Civic     | 2016     | 33340      | 0.114536        | 3818.63           |
| 2022-09-04 | Patrick Harris  | Johnny Scott    | Ford      | Altima    | 2013     | 41937      | 0.092191        | 3866.20           |
| 2022-06-16 | Eric Lopez      | Vanessa Jones   | Honda     | Silverado | 2022     | 20256      | 0.113490        | 2298.85           |
| 2022-05-26 | Isabella Moore  | Shirley Lee     | Chevrolet | Silverado | 2021     | 49823      | 0.062977        | 3137.70           |
| 2022-10-03 | Kimberly Snow   | Tara Rodgers    | Ford      | F-150     | 2022     | 18803      | 0.068339        | 1284.97           |
| 2022-06-07 | Jessica Young   | Jennifer Moore  | Chevrolet | Civic     | 2010     | 30863      | 0.088915        | 2744.19           |
| 2023-02-15 | Donald Barber   | Ashley Diaz     | Honda     | Silverado | 2014     | 26125      | 0.088260        | 2305.80           |
| 2023-03-24 | Kayla Fowler    | Nathan Thompson | Honda     | Civic     | 2010     | 20762      | 0.137105        | 2846.57           |

Tabel 1 merupakan gabungan dari 5 data teratas dan 5 data terbawah. Hal ini bertujuan untuk mengetahui perwakilan isi data.

**1b. Melakukan pengecekan tipe data pada setiap kolom.**

Tabel 2. Nama kolom dan tipe data dari _dataset_ yang digunakan.
| # | Column | Dtype |
|-----|--------------------|-------------|
| 0 | Date | object |
| 1 | Salesperson | object |
| 2 | Customer Name | object |
| 3 | Car Make | object |
| 4 | Car Model | object |
| 5 | Car Year | int64 |
| 6 | Sale Price | int64 |
| 7 | Commission Rate | float64 |
| 8 |Commission Earned | float64 |

Tabel 2 memberikan informasi tentang struktur dataset yang terdiri dari 9 kolom. Kolom '_Date_', '_Salesperson_', '_Customer Name_', '_Car Make_' dan '_Car Model_' memiliki tipe data `object` yang merupakan tipe data kategori. Sedangkan, kolom '_Car Year_' dan '_Sale Price_' memiliki tipe data `int64` serta kolom '_Commission Rate_' dan '_Commission Earned_' memiliki tipe data `float64` yang merupakan tipe data numerik.

**1c. Menampilkan distribusi data pada kolom yang merupakan tipe data numerik.**

Tabel 3. Distribusi data pada kolom numerik.

|       | Car Year | Sale Price | Commission Rate | Commission Earned |
| ----- | -------- | ---------- | --------------- | ----------------- |
| count | 2.5e+06  | 2.5e+06    | 2.5e+06         | 2.5e+06           |
| mean  | 2015.996 | 30012.18   | 0.09998766      | 3001.005          |
| std   | 3.739    | 11545.14   | 0.02887202      | 1481.467          |
| min   | 2010     | 10000      | 0.05000014      | 501.34            |
| 25%   | 2013     | 20019      | 0.0749645       | 1821.71           |
| 50%   | 2016     | 30006      | 0.1000058       | 2741.91           |
| 75%   | 2019     | 40022      | 0.1250065       | 3978.142          |
| max   | 2022     | 50000      | 0.15            | 7494.53           |

Tabel 3 menyajikan informasi statistik tentang empat kolom numerik dalam _dataset_, yaitu '_Car Year_', '_Sale Price_', '_Commission Rate_', dan '_Commission Earned_'.

- **count**: Jumlah data yang ada dalam setiap kolom.
- **mean**: Nilai rata-rata dari setiap kolom, menunjukkan angka tengah atau pusat distribusi data.
- **std**: Standar deviasi, menggambarkan sejauh mana data tersebar di sekitar nilai rata-rata.
- **min**: Nilai terendah dalam setiap kolom, menunjukkan batas bawah data.
- **25%**: Kuartil pertama, nilai di mana 25% data terendah berada di bawahnya.
- **50%**: Kuartil kedua atau median, nilai di mana 50% data terletak di bawahnya.
- **75%**: Kuartil ketiga, nilai di mana 75% data terendah berada di bawahnya.
- **max**: Nilai tertinggi dalam setiap kolom, menunjukkan batas atas data.

Informasi ini memberikan gambaran tentang sebaran dan karakteristik data dalam kolom-kolom numerik seperti melihat nilai rata-rata, rentang nilai, dan deviasi standar dari '_Sale Price_', yang mengindikasikan variasi harga jual mobil dalam _dataset_.

**1d. Melakukan pengecekan terhadap data yang _null_ atau duplikat, yang bertujuan untuk mengidentifikasi data yang tidak lengkap atau mengandung duplikasi. Hasilnya dapat dilihat pada Tabel 4 berikut.**

Tabel 4. Jumlah data _null_ pada setiap kolom.

| Column            | Null Count |
| ----------------- | ---------- |
| Date              | 0          |
| Salesperson       | 0          |
| Customer Name     | 0          |
| Car Make          | 0          |
| Car Model         | 0          |
| Car Year          | 0          |
| Sale Price        | 0          |
| Commission Rate   | 0          |
| Commission Earned | 0          |

Informasi yang didapatkan dari Tabel 4 adalah bahwa tidak ada nilai _null_ (_missing value_) pada setiap kolom dalam _dataset_. Hal ini menunjukkan bahwa _dataset_ memiliki data lengkap untuk setiap kolom.

**1e. Memeriksa apakah terdapat nilai 0 pada kolom '_Car Year_' dan '_Sale Price_'. Hal ini dilakukan karena tidak mungkin tahun pembuatan dan harga mobil bernilai 0. Hasilnya dapat dilihat pada tabel 5 berikut.**

Tabel 5. Jumlah nilai 0 pada kolom '_Car Year_' dan '_Sale Price_'.

| Column     | Count of 0 |
| ---------- | ---------- |
| Car Year   | 0          |
| Sale Price | 0          |

Berdasarkan Tabel 5 dapat diketahui bahwa tidak ada nilai 0 pada kolom '_Car Year_' dan '_Sale Price_'. Hal ini menunjukkan bahwa dalam _dataset_ memiliki data yang rasional.

**1f. Memeriksa data _outlier_ menggunakan metode IQR (_Interquartile Range_) dan menghapus data yang _outlier_ pada data numerik yaitu '_Car Year_', '_Sale Price_', '_Commission Rate_', dan '_Commission Earned_'.**

[![boxplot-dataoutliers.png](https://i.postimg.cc/PrTvy9X8/boxplot-dataoutliers.png)](https://postimg.cc/XX1v72yV)

Gambar 4. Hasil visualisasi menggunakan _box plot_ untuk melihat data _outlier_.

Berdasarkan Gambar 4, dapat diketahui bahwa ternyata terdapat data _outlier_ pada kolom '_Commission Earned_'. Jumlah dari data _outlier_ dapat dilihat pada Tabel 6.

Tabel 6. Jumlah data _outlier_ pada data numerik.

| Column            | Count of Outliers |
| ----------------- | ----------------- |
| Car Year          | 0                 |
| Sale Price        | 0                 |
| Commission Rate   | 0                 |
| Commission Earned | 3432              |

Berdasarkan Tabel 6, dapat diketahui bahwa pada kolom '_Car Year_', '_Sale Price_' dan '_Commission Rate_' tidak terdapat _outlier_, sedangkan pada kolom '_Commission Earned_' terdapat 3432 data yang dianggap sebagai _outlier_. Hal ini menunjukkan bahwa nilai-nilai pada kolom '_Commission Earned_' memiliki variasi yang lebih besar dibandingkan dengan kolom lainnya. Data outlier tersebut akan dihapus untuk mengurangi bias pada data. Setelah data outlier dihapus maka total data saat ini adalah 2496568. Jumlah data saat ini akan digunakan untuk melihat distribusi data pada setiap kolom dan diteruskan ke tahap pembentukan model.

**1g. Melihat frekuensi data berdasarkan kolom '_Date_'.**

[![frequency-of-date.png](https://i.postimg.cc/fTTt6byf/frequency-of-date.png)](https://postimg.cc/YjZCFM1v)

Gambar 5. Grafik frekuensi data berdasarkan kolom '_Date_'.

Gambar 5 menunjukkan bahwa data yang digunakan memiliki pola data dengan gerakan musiman [[9]](https://amikjtc.com/jurnal/index.php/jurnal/article/view/91/85). Pola data musiman mengacu pada fluktuasi atau pola yang terulang dalam data dengan periode waktu yang tetap atau hampir tetap, yang terkait dengan faktor musiman atau perubahan berulang dalam suatu periode waktu tertentu.

Tabel 7. Frekuensi data berdasarkan tahun.

| Year | Frequency |
| ---- | --------- |
| 2022 | 1672227   |
| 2023 | 824341    |

Berdasarkan Tabel 7, dapat dilihat bahwa pada tahun penjualan lebih banyak terjadi pada tahun 2022 dengan frekuensi sebanyak 1.672.227 data dibandingkan dengan tahun 2023 dengan jumlah frekuensi sebanyak 824.341 data.

3. Melakukan drop pada kolom yang tidak relevan untuk diproses ke model seperti Date, Salesperson, Customer Name dan Year.
4. Melakukan Encoding pada variabel kategorikal yaitu kolom Car Make dan Car Model, bertujuan untuk mengkonversi variabel kategori menjadi angka atau vektor numerik yang mewakili kategori-kategori tersebut.
5. Melakukan Feature Scaling pada data numerik yaitu kolom Car Year, Commission Rate, dan Commission Earned menggunakan MinMaxScaler(), yang berfungsi untuk melakukan normalisasi dan standarisasi data.
6. Memisahkan kolom fitur dan target. Dalam hal ini, kolom fitur yaitu kolom selain Sale Price dan kolom target adalah Sale Price.
7. Membagi dataset yang telah melewati tahap preprocessing menjadi data latih dan data uji. Pembagian dibagi sebesar 80% untuk data latih dan 20% data uji.

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

[[6]](https://eksplorasidatasaham.wordpress.com/2017/02/08/melihat-pola-sebaran-data-saham-analisa-boxplot/) Ts. Priyadi, “Melihat Pola Sebaran data saham (Analisa Boxplot),” Perjalanan Menuju Happy Investing, https://eksplorasidatasaham.wordpress.com/2017/02/08/melihat-pola-sebaran-data-saham-analisa-boxplot/ (accessed Jul. 6, 2023).

[[7]](https://ilmudatapy.com/membuat-line-plot-dengan-matplotlib-python/) L. Afifah, “Membuat line plot Dengan Matplotlib Python,” IlmudataPy, https://ilmudatapy.com/membuat-line-plot-dengan-matplotlib-python/ (accessed Jul. 6, 2023).

[[8]](https://id.wikipedia.org/wiki/Templat:Vertical_bar_chart) W. Ensiklopedia, “Templat:Vertical Bar Chart,” Wikipedia, https://id.wikipedia.org/wiki/Templat:Vertical_bar_chart (accessed Jul. 6, 2023).

[[9]](https://amikjtc.com/jurnal/index.php/jurnal/article/view/91/85) K. Nugroho, “MODEL ANALISIS PREDIKSI MENGGUNAKAN METODE FUZZY TIME SERIES,” INFOKAM: Informasi Komputer Akuntansi dan Manajemen, vol. 12, no. 1, pp. 46–50, 2016.

---Ini adalah bagian akhir laporan---
