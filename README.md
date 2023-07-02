
# Laporan Proyek _Machine Learning_ Oleh Candra Burhanudin

> ## Analisis Sentimen Ulasan Pengguna Aplikasi LIVIN by Mandiri menggunakan Algoritma Support Vector Machine

# 🕸️ Domain Proyek

## **Latar Belakang**

Dalam pengembangan aplikasi, penting bagi pengembang untuk memahami sentimen pengguna terhadap aplikasi mereka. analisis sentimen digunakan untuk mengidentifikasi dan memahami sentimen dalam teks. dalam konteks penggunaan Aplikasi LIVIN by Mandiri pengembang ingin memahami sentimen pengguna terhadap penggunaan aplikasi tersebut untuk dapat menjadi evaluasi peningkatan produk. Dengan menggunakan analisis sentimen pada dataset Livin' by Mandiri App Reviews_ dengan jumlah review sampel 20000, pengembang dapat mengidentifikasi lebih cepat terkait kekurangan, masalah, atau peningkatan yang dialami pengguna dengan mengidentifikasi _review_ dengan rentang 1 sampai 5 yang dapat membantu pengembang untuk meningkatkan pengalaman pengguna melalui perbaikan yang sesuai. Analisis sentimen memberikan wawasan objektif berdasarkan data. pengembang dapat membuat keputusan yang lebih objektif dan logis berdasarkan temuan analisis sentimen sehingga dapat meningkatkan kepuasan pengguna dan meningkatkan proses pelayanan ,perbaikan dan daya saing aplikasi LIVIN di pasaran.

- **Penyelesaian**
  berdasarkan hasil review aplikasi LIVIN dengan jumlah sampel sebanyak 20000 untuk mengatasi tantangan dalam menganalisis sentimen dari review pengguna aplikasi LIVIN, metode yang digunakan adalah SVM (_Support Vector Machine_) untuk melakukan klasifikasi. SVM adalah algoritma pembelajaran mesin yang efektif dalam memisahkan dan mengklasifikasikan data berdasarkan fitur-fitur yang relevan. dalam konteks ini untuk SVM digunakan untuk mengklasifikasikan review pengguna LIVIN MANDIRI. Hasil list review dari rentang 1 sampai 5 dibagi 2 sentimen dimana hasil *review* dengan rating 1 - 3 dikategorikan menjadi sentimen negatif dan review dengan rating 4 sampai 5 dikategorikan menjadi sentimen positif.

# 💼 _Business Understanding_

Untuk Membantu Proses Identifikasi Permasalahan dan untuk kepentingan pelayanan pengguna aplikasi LIVIN yang masih memiliki beberapa kendala saat menggunakan aplikasi LIVIN, pengembangan analisis sentimen diperlukan untuk membantu identifikasi masalah agar dapat mempercepat perbaikan pelayanan pengguna dengan mengumpulkan data ulasan aplikasi dan memproses klasifikasi sentimen positif dan negatif yang akan memberikan informasi untuk memfokuskan pengembang atas permasalahan yang dimiliki untuk menjadi pertimbangan prioritas untuk proses perbaikan pelayanan. Klasifikasi adalah proses pengkategorian terhadap sekumpulan dokumen ke dalam kategori tertentu[1].

## _Problem Statement_

- **Masalah 1 : Bagaimana cara mengetahui ulasan dalam dataset aplikasi menjadi sebuah informasi untuk memahami area yang perlu dipertimbangkan untuk pengembangan pelayanan dan peningkatan pengalaman pengguna ?**
- **Masalah 2 : Bagaimana mengimplementasikan metode analisis sentimen yang efektif untuk memfilter ulasan positif dan negatif pada aplikasi LIVIN by Mandiri?**
- **Masalah 3 : Bagaimana cara mengidentifikasi ulasan positif dan negatif dalam dataset ulasan aplikasi LIVIN untuk meningkatkan pengalaman pengguna ?**

## _Goals_

- **Jawaban Pernyataan Masalah 1**
  Untuk mengetahui informasi penting yang terdapat pada dataset ulasan dapat menggunakan cara analisis sentimen, pengembang dapat mengidentifikasi *review* yang mengandung sentimen negatif atau kritik terhadap aplikasi. Ini membantu pengembang untuk mengetahui kekurangan atau masalah yang dialami pengguna, seperti bug, kinerja yang lambat, antarmuka yang rumit, atau fitur yang kurang memuaskan. Dengan menemukan pola dan tren dalam sentimen negatif, pengembang dapat fokus pada peningkatan yang sesuai untuk meningkatkan pengalaman pengguna.

- **Jawaban Pernyataan Masalah 2**
  Untuk mengimplementasikan metode analisis sentimen yang efektif dalam memfilter ulasan positif dan negatif pada aplikasi LIVIN by Mandiri, dapat melalui langkah dengan mengumpulkan sejumlah besar ulasan pengguna aplikasi LIVIN by Mandiri, lalu pemilihan algoritma analisis sentimen yang cocok seperti algoritma _Naive Bayes_, _Support Vector Machines_, _Recurrent Neural Networks_. setelah melakukan pemilihan metode lalu latih model dengan dataset yang sudah diberi label dan lakukan evaluasi serta uji coba model.

- **Jawaban Pernyataan Masalah 3**
  Dengan dibuatnya analisis sentimen untuk mengidentifikasi ulasan positif dan negatif dapat melalui Identifikasi tren dan masalah dengan meninjau hasil analisis sentimen dan identifikasi tren umum dalam ulasan positif dan negatif. Dengan memperhatikan masalah yang sering muncul dalam ulasan negatif dapat memahami area yang perlu diperbaiki atau ditingkatkan dalam aplikasi LIVIN.

## _Solution Statements_

dari permasalahan yang dialami, solusi yang dapat diterapkan dalam proses analisis sentimen dapat menggunakan beberapa metode yaitu :

1.  _Naive Bayes_: Algoritma _Naive Bayes_ adalah metode klasifikasi yang sering digunakan dalam analisis sentimen. Algoritma ini menggunakan teorema Bayes untuk memprediksi sentimen berdasarkan kata-kata atau fitur-fitur dalam teks review. _Naive Bayes_ cocok untuk analisis sentimen karena efisien dan mampu mengatasi data yang besar.

2.  _Support Vector Machines (SVM)_: SVM adalah metode klasifikasi yang dapat diterapkan dalam analisis sentimen. SVM mencari garis atau hiperplane yang dapat memisahkan kelas positif dan negatif berdasarkan fitur-fitur teks. Dalam konteks analisis sentimen, SVM dapat mempelajari pola dan memprediksi sentimen berdasarkan teks _review_ dan _rating_ yang diberikan.

3.  Metode Deep Learning: Metode deep learning, seperti _Recurrent Neural Networks (RNN)_, _Convolutional Neural Networks (CNN)_, dan _Transformer-based models_ (misalnya, BERT atau GPT), juga dapat digunakan dalam analisis sentimen. Metode ini memanfaatkan kemampuan jaringan saraf dalam memahami dan memodelkan hubungan kompleks dalam teks. Dengan melatih model _deep learning_ pada dataset _review_ dan _rating_, model dapat mempelajari representasi teks yang kaya dan menghasilkan prediksi sentimen.

> **Pemilihan metode untuk penelitian ini menggunakan metode SVM _Support Vector Machines_. SVM dapat mengatasi dataset yang memiliki banyak fitur (kata-kata) dalam ruang berdimensi tinggi, yang umum terjadi dalam analisis sentimen pada ulasan teks. SVM dapat membangun batas keputusan yang kompleks dan memisahkan dengan baik kelas positif dan negatif dalam ruang fitur yang kompleks. dan dengan SVM dalam dataset ulasan pengguna, biasanya terjadi ketidakseimbangan antara jumlah ulasan positif dan negatif. SVM memiliki kemampuan untuk mengatasi masalah ini dan memberikan penanganan yang baik terhadap data yang tidak seimbang, sehingga mencegah pemodelan yang bias terhadap kelas mayoritas.**

# 🧷 _Data Understanding_

## _Overview Dataset_

Dataset yang digunakan pada penelitian ini yaitu **_Livin' by Mandiri App Reviews_**. Livin' by Mandiri adalah platform layanan keuangan digital yang dikembangkan oleh Bank Mandiri, salah satu bank terbesar di Indonesia. Platform ini dirancang untuk menyediakan berbagai layanan dan fitur keuangan bagi pengguna, termasuk kemampuan untuk melakukan pembayaran, transfer uang, dan mengelola keuangan mereka melalui perangkat mobile. variabel pada dataset dapat dilihat pada **Tabel 1**.

> **Link _Dataset_ : [Livin' by Mandiri App Reviews](https://www.kaggle.com/datasets/itanium/livin-by-mandiri-app-reviews)** 
> **Jumlah _Record_ : 155.188** 
> **_Data Source_ : Google Play Store** 
> **_Usage Ideas_ : _EDA and Sentiment Analysis_**

**Tabel 1 Variabel Pada Livin**
| index | date | review | rating | thumbs_up | version |
| ----- | ------------------- | ----------------------------------------------------------------------------- | ------ | --------- | ------- |
| 0 | 2021-09-30 06:12:53 | Udah dicoba, keren dan responsive, dengan tampilan yang makin segar pastinya! | 5 | 36 | 1.0.0 |

Keterangan :

> - ***Index* :** Berisi identifikasi unik untuk mengidentifikasi dan mengakses item atau elemen dalam koleksi data dengan cara yang efisien.
> - ***Review* :** Berisi Ulasan pengguna terhadap pengalaman penggunaan aplikasi.
> - ***Date* :** keterangan tanggal dan waktu ulasan pengguna saat proses posting ulasan.
> - ***Rating* :** penilaian yang diberikan pengguna terhadap pengalaman saat menggunakan aplikasi. penilaian berupa angka 1 hingga 5 dimana angka 1 memberikan ulasan paling rendah dan 5 adalah ulasan paling tinggi
> - ***thumbs_up* :** jumlah acungan jempol dari beberapa netizen terhadap ulasan yang diberikan
> - ***Version* :** Versi Aplikasi Livin App By Mandiri

## _exploratory data analysis_

### _Preview Dataset_

**Tabel 2 Preview Dataset**
|index|date|review|rating|thumbs_up|version|
|---|---|---|---|---|---|
|0|2021-09-30 06:12:53|Udah di coba, keren dan responsive, dengan tampilan yang makin segar pastinya\!|5|36|1\.0\.0|
|1|2021-09-30 06:33:15|Excellent|5|0|1\.0\.0|

### Perubahan Nilai Rating Mejadi Nilai Sentimen Positif dan Negatif

> ***rating* (*rating* 1 sampai 3 menjadi label negatif & *rating* 4 sampai 5 menjadu positif)**  
> **positif (1) dan negatif (0)**
>
> *Output* :

**Tabel 3 Perubahan Nilai Rating Menjadi Sentimen Positif dan Negatif**
|index|date|review|rating|thumbs_up|version|sentiment|
|---|---|---|---|---|---|---|
|0|2021-09-30 06:12:53|Udah di coba, keren dan responsive, dengan tampilan yang makin segar pastinya\!|5|36|1\.0\.0|1|
|1|2021-09-30 06:33:15|Excellent|5|0|1\.0\.0|1|
|2|2021-09-30 06:48:30|Keren\. Cakep benar semakin canggih\. Terdepan terpercaya tumbuh bersama anda\.|5|22|1\.0\.0|1|
Field Sentiment akan terbuat dengan asumsi bahwa *rating* positif bernilai 1 dan *rating* negatif bernilai 0

### Jumlah Pembagian Data Training & Data Testing

> Visualisasi pembagian data dan perbandingan jumlah data dapat dilihat pada `Tabel 1`. Data yang paling banyak digunakan adalah data *training* sebanyak 80% sedangkan untuk data *testing* digunakan sebanyak 20%.

**Tabel 1 Diagram Pembagian Dataset Dan Perbandingan Jumlah data**

| Jenis Diagram | Keterangan |
| ------------- | ---------- |
|![pie chart](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/abe1863d-ebed-467f-8fc3-7691e728c342)**Gambar 1 Diagram Lingkaran Perbandingan Data _Training_ Dan _Testing_**| Pada **Gambar 1** Dataset dibagi menjadi Data Training Dan Data Testing dengan perbandingan 80 : 20 	|
|![diagram batang perbandingan jumlah data](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/307eaee8-cba2-4ccd-9c64-6bd4f56818ae) **Gambar 2 Diagram Batang Perbandingan Jumlah Data _Training_ Dan _Testing_**					|	Pada **Gambar 2** Jumlah _Data training_ yang digunakan sebanyak 16000 dan untuk data testing sebanyak 4000 dari jumlah total dataset yang digunakan berjumlah 20000. |	 

### Jumlah Sentimen Positif Dan Negatif 
![diagram batang jumlah sentimen negatif positif](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/341191c5-0090-4b94-a48b-10a14431676f)
 
 **Gambar 3 Jumlah Perbandingan Sentimen Negatif Dan Positif**
 
>Dari total 20000 data yang digunakan jumlah sentimen negatif mencapai total 6012 Data dan untuk jumlah sentimen positif mencapai total sebanyak 9988. diagram batang perbandingan jumlah sentimen negatif dan positif dapat dilihat pada **Gambar 3**

### Diagram Jumlah Panjang Teks Data Latih Dan Data Uji ![diagram batang jumlah panjang teks](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/a1c6e8f2-ff5e-4634-a380-6a8650fe3c71)

**Gambar 4 Diagram Perbandingan Jumlah Panjang Teks**
> Pada Proses perhitungan panjang teks, jumlah panjang teks tertinggi pada data train berjumlah 387 karakter sedangkan jumlah panjang teks tertinggi pada data test berjumlah 402 karakter. Diagram Perbandingan Jumlah Panjang Teks Data Training dan Data Testing dapat dilihat pada **Gambar 4**

### WordCloud Kumpulan Ulasan Kata Pada Dataset

![wordcloud kumpulan kata](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/b7d18d6a-3fcc-43db-aa71-b7e7966e4fe0)

**Gambar 5 Pemetaan Intensitas kemunculan kata menggunakan WordCloud**

> Dari 20000 Ulasan pada Dataset dengan WordCloud dapat memetakan kata-kata dengan menyusun dari kata yang memiliki intensitas tinggi sampai intensitas rendah. output dapat dilihat pada **Gambar 5** .

### WordCloud Kumpulan Kata Ulasan Sentimen Positif

![wordcloud kumpulan kata positif](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/9eeb465a-f31d-423f-acc1-0e23da44ecff)

**Gambar 6 Pemetaan Intensitas kata dengan sentimen Positif Menggunakan WordCloud**

> Untuk dapat melihat Ulasan Pengguna yang memiliki sentimen Positif dengan mengelompokan output yang hanya memiliki nilai sentimen 1. hasil output dapat dilihat pada **Gambar 6**. terlihat bahwa beberapa ulasan memiliki kata yang memiliki intensitas tinggi seperti bagus, mudah, _good_, keren, membantu, terimakasih yang sudah sesuai dengan data yang bersifat sentimen positif

### WordCloud Kumpulan Kata Ulasan Sentimen Negatif

![wordcloud kumpulan kata negatif](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/0693fed2-b9b9-4f1f-8625-ec6590d850c2)

**Gambar 7 Pemetaan Intensitas kata dengan sentimen Positif Menggunakan WordCloud**

> Untuk dapat melihat Ulasan Pengguna yang memiliki sentimen Positif dengan mengelompokan output yang hanya memiliki nilai sentimen 1. hasil output dapat dilihat pada **Gambar 6**. Terlihat bahwa beberapa ulasan memiliki kata yang memiliki intensitas tinggi seperti ribet, login, update, gagal, susah, transaksi yang sudah sesuai dengan data yang bersifat sentimen negatif yang berhubungan dengan ulasan pengguna yang memiliki masalah dalam proses didalam aplikasi.

# 🧮 Data Preparation

**Proses yang dilakukan pada data preparation yaitu :**

1.  _Encoding_ FItur _Rating & Review_
2.  Standarisasi Data
3.  NLTK _Stopword_
4.  _Train Test Split_
5.  _Feature Engineering_ dengan TF-IDF

**Alasan Dilakukan Data Preparation :**

1.  *Encoding* pada fitur *rating & review* dilakukan untuk mendapatkan fitur baru yang sesuai sehingga dapat mewakili variabel sentimen positif (1) dan negatif (0). 2, Dengan menerapkan standarisasi terutama mengubah semua kata ke huruf kecil membantu dalam pemrosesan teks dan pengolahan data yang melibatkan perbandingan atau pencarian berdasarkan teks tanpa memperhatikan perbedaan huruf besar dan kecil.
2.  NLTK *Stopword* dilakukan untuk menghilangkan kata-kata, simbol yang tidak diinginkan untuk mendapatkan data output yang lebih relevan
3.  *Train Test Split* dilakukan untuk proses evaluasi kinerja, menghindari overfitting, serta mempermudah dalam tuning parameter
4.  TF-IDF membantu dalam mengidentifikasi kata-kata yang unik dan memberikan informasi penting dalam teks.

## Encoding Fitur Sentiment

> pada field rating memiliki nilai 1-5 yang merepresentasikan nilai rating. untuk mengubah label rating menjadi positif (1) dan negatif (0) dengan ketentuan rating 1-3 negatif & 4-5 positif dilakukan proses pembuatan _field_ baru bernama `sentiment`. proses dilakukan dengan menggunakan _library_ pandas

    df['sentiment'] = df['rating'].apply(lambda x: 1 if x >= 4 else  0)

## Standarisasi Fitur Sentiment

> Dalam penelitian ini, peneliti hanya menggunakan 20000 Data ulasan untuk digunakan sebagai analisis sentimen dan dilakukan standarisasi data dengan merubah gaya huruf menjadi huruf kecil seluruhnya.

    new_df = df[:20000]
    new_df['review'] = new_df['review'].str.lower()

## NLTK Stopword

*Stopword Removal* merupakan proses untuk menghilangkan kata yang dianggap tidak berpengaruh terhadap kalimat[2]. Penerapan *stopword* dilakukan dengan library NLTK Indonesia dengan menambahkan kustomisasi kata pengecualian. selain itu dilakukan proses penghapusan simbol dan tanda baca pada *field* review_filtered. output dapat dilihat pada **Tabel 4**.

> **list kata penambahan _stop word_ :**
> yg, dg, rt, dgn, ny, d, klo, kalo, amp, biar, bikin, bilang, gak, ga, gk, krn, nya, nih, sih, si, tau, tdk, tuh, utk, ya, jd, jgn, sdh, aja, n, t, nyg, hehe, pen, u, nan, loh, rt, &, yah, mandiri, aplikasi, livin, aplikasinya, udah, pake, apk.

***Output* :**
**Tabel 4 Penerapan NLTK *Stopword***
|index|sentiment|review_filtered|
|---|---|---|
|0|1|coba keren responsive tampilan segar pastinya|
|1|1|excellent|
|2|1|keren cakep canggih terdepan terpercaya tumbuh anda|
|3|1|mantap|
|4|1|mantap|

## *Train-Test-Split*

> Data yang diproses yaitu pada kolom , `review_filtered` sebagai fitur dan label dan melakukan proses pemisahan data antara data latih dan data uji secara acak dengan perbandingan 80:20 dengan menggunakan `library sklearm` . Jumlah data latih sebanyak `16000` dan data uji sebanyak `4000`. lalu data latih dan data uji disimpan pada variabel `train_data` dan`test_data`

    train_data = pd.concat([X_train, y_train], axis=1)
    test_data = pd.concat([X_test, y_test], axis=1)

## *Feature Engineering* dengan TF-IDF

Setelah semua data sudah melewati tahap preprocessing, maka Langkah selanjutnya adalah pembuatan fitur untuk mempermudah proses klasifikasi. Pada tahap ekstraksi fitur dilakukan dua proses yaitu pembuatan *word vector* dimana dilakukan pengubahan fitur teks menjadi representasi *vector* dari pembobotan kata dengan TF-IDF[3]. TFIDF (_Term Frequency-Inverse Document Frequency_) adalah metode yang digunakan dalam pemrosesan teks dan pemodelan tematik untuk mengevaluasi pentingnya sebuah kata dalam suatu dokumen atau korpus teks. Parameter yang digunakan pada penelitian ini yaitu :

- **min_df** untuk menghilangkan istilah yang terlalu jarang muncul. variabel **min_df = 5**
- **max_df** untuk menghilangkan term yang terlalu sering muncul. variabel **max_df = 0,8**
- **sublinear_tf** akan mengubah vektor frekuensi menjadi bentuk logaritma ( 1+log(tf)). variabel sublinear bernilai Boolean **True**
- **use_idf** untuk menggunakan inverse document frequency. variabel use_idf bernilai bboolean **True**

# 🛠️ Modeling

Dari permasalahan tersebut metode yang digunakan pada penelitian ini adalah Support Vector Machine. penelitian ini menggunakan SVM untuk menyelesaikan permasalahan klasifikasi. SVM termasuk dalam kategori supervised learning yang termasuk metode populer dalam machine learning.

> Kelebihan Dan Kekurangan SVM
> - dengan SVM data review yang memiliki jumlah ulasan positif dan negatif tidak sama mampu diatasi oleh metode SVM dalam proses analisis sentimen
> - Dengan SVM mampu mengatasi masalah klasifikasi linear dan nonlinear karena memiliki fleksibilitas untuk menangani masalah klasifikasi linear dan non-linier. SVM dapat menggunakan kernel untuk mengubah data ke dalam bentuk yg memungkinkan pemisah garis atau permukaan yang kompleks
> - Kekurangan SVM jika jumlah fitur dalam dataset sangat besar, SVM menghadapi tantangan kinerja dengan waktu eksekusi yang lebih lama
> - Sensitif terhadap pemilihan parameter yang apabila tidak tepat dapat mengakibatkan kinerja yang buruk atau overfitting pada model

## Klasifikasi Sentimen dengan *Support Vector Machine*

### klasifikasi menggunakan *library* `sklearn` dengan konfigurasi kernel = linear

Dengan menggunakan kernel linear, yang berarti SVM mencoba memisahkan kelas dengan garis linear. Dalam dimensi rendah, SVM dengan kernel linear biasanya efisien dan mudah diinterpretasikan. Namun, jika data tidak terpisah secara linier, kernel linear mungkin tidak mampu memisahkan dengan baik. pada dataset yang peneliti gunakan beberapa ulasan mengatakan positif namun memberikan ulasan yang rendah dengan asumsi bahwa pemisahan data tidak secara linear. namun untuk mencoba pertama kali peneliti menggunakan kernel linear

### Klasifikasi dengan *Hyperparameter* kernel RBF

Percobaan kedua dengan kernel RBF menggunakan fungsi basis radial sebagai kernel. Kernel RBF memetakan data ke dimensi ruang yang lebih tinggi, sehingga memungkinkan SVM untuk memisahkan data yang tidak terpisah secara linier di ruang fitur yang lebih kompleks. Kernel RBF secara efektif dapat menangani data yang memiliki pola yang rumit dan tidak linier. Namun, penggunaan kernel RBF dapat lebih rumit dalam pengaturan parameter dan lebih memakan waktu dalam pelatihan model. parameter yang digunakan pada penelitian ini yaitu :

1.  Cost. Parametrer C mengotrol trade-off antara penyebaran margin dan jumlah kesalahan klasifikasi
2.  Gamma. parameter ini mengontrol sejauh mana pengaruh suatu titik data dalam perhitungan fungsi kernel. nilai gamma yang besar menyebabkan fungsi kernel memiliki jangkauan yang lebih sempit
3.  Kernel. di gunakan untuk menangani ketidakseimbangan kelas dalam dataset

    param_grid = {'C': [0.1, 1, 10, 100, 1000], 'gamma': [1, 0.1, 0.01, 0.001, 0.0001]}
    svm_model = svm.SVC(kernel='rbf')

Saat melakukan *hyperparameter tuning* dengan kernel RBF (*radial basic function)* hasil beberapa matriks telah mengalami peningkatan dengan menerapkan RBF pada dataset non-linear dimana hubungan antara fitur-fitur dengan sentimen tidak dapat dinyatakan secara linier. adanya kemungkinan bahwa beberapa fitur yang muncul dalam *review* positif juga muncul dalam review negatif, atau ada kompleksitas dalam hubungan antara fitur-fitur dengan sentimen. untuk itu *hyperparameter* yang digunakan adalah RBF

# 📋*Evaluation*

> pada percobaan pertama tanpa melakukan *hyperparameter tuning* dengan kernel linear hasil metrik yang dihasilkan berupa *precision, recall, f1-score*, support dapat dilihat pada **Tabel 5**.

## Hasil Matriks Awal

**Tabel 5 Hasil Matrik Menggunakan Kernel Linear**
| | precision | recall | f1-score | support |
| ------------ | --------- | ------ | -------- | ------- |
| Negatif | 0.83 | 0.84 | 0.84 | 1490 |
| Positif | 0.90 | 0.90 | 0.90 | 2510 |
| Accuracy | | | 0.88 | 4000 |
| macro avg | 0.87 | 0.87 | 0.87 | 4000 |
| weighted avg | 0.88 | 0.88 | 0.88 | 4000 |

> hasil dengan Kernel Linear mendapat akurasi yang cukup tinggi sebesar 88% dengan `f1-score` kelas negatif sebesar 84% dan kelas positif sebesar 90%. hasil menggunakan kernel linear sudah cukup baik

## Hasil Metrik Setelah *Hyperparameter Tuning*

**Tabel 6 Hasil Matrik Kernel RBF Serta Menggunakan *Hyperparameter Tuning***
| | precision | recall | f1-score | support |
| ------------ | --------- | ------ | -------- | ------- |
| Negatif | 0.83 | 0.90 | 0.86 | 1490 |
| Positif | 0.94 | 0.89 | 0.91 | 2510 |
| Accuracy | | | 0.89 | 4000 |
| macro avg | 0.88 | 0.90 | 0.89 | 4000 |
| weighted avg | 0.90 | 0.89 | 0.90 | 4000 |

> setelah melakukan *hyperparameter* nilai akurasi meningkat menjadi 89% diikuti dengan nilai `f1-score` pada kelas negatif sebesar 86% dan kelas positif mendapat 91%. hasil lengkap dapat dilihat pada **Tabel 6**. untuk itu Model yang akan digunakan untuk proses analisis sentimen menggunakan kernel RBF.

### Keterangan Metrik

1.  *Precision: Precision* mengukur sejauh mana hasil positif yang diprediksi oleh model adalah benar. Ini merupakan rasio dari true positive (TP) dibagi dengan jumlah total prediksi positif (TP + FP).

2.  *Recall: Recall* (sensitivitas atau true positive rate) mengukur sejauh mana model dapat mengidentifikasi dengan benar contoh positif. Ini merupakan rasio dari true positive (TP) dibagi dengan jumlah total contoh positif (TP + FN).

3.  *F1-score: F1-score* merupakan rata-rata harmonik antara precision dan recall. Ini memberikan nilai keseimbangan antara precision dan recall. F1-score sering digunakan sebagai metrik evaluasi yang lebih baik ketika kelas-kelas yang dihasilkan tidak seimbang.

4.  *Support: Support* adalah jumlah kemunculan aktual dari setiap kelas dalam data uji. Ini memberikan informasi tentang seberapa banyak contoh yang termasuk dalam setiap kelas.

5.  *Macro Avg: Macro average* adalah rata-rata aritmatik dari metrik evaluasi (precision, recall, F1-score) dihitung secara terpisah untuk setiap kelas. Setiap kelas memiliki bobot yang sama dalam perhitungan rata-rata.

6.  *Weighted Avg: Weighted average* adalah rata-rata tertimbang dari metrik evaluasi (precision, recall, F1-score) dihitung dengan mempertimbangkan proporsi contoh dalam setiap kelas. Kelas yang lebih banyak contohnya memiliki bobot yang lebih besar dalam perhitungan rata-rata.

### Kernel RBF Formula

$$K(x, x') = \exp \left( -\frac{\|x - x'\|^2}{2\sigma^2} \right)$$
Keterangan:

- `K(x, x')` merupakan fungsi kernel RBF antara vektor `x` dan `x'`.
- `\exp` adalah fungsi eksponensial.
- `\|x - x'\|^2` menghitung jarak euclidean kuadrat antara vektor `x` dan `x'`.
- `\sigma` adalah parameter lebar kernel (scale parameter).

### Kernel Linear Formula

$$K(x, x') = x \cdot x'$$
Keterangan:

- `K(x, x')` merupakan fungsi kernel linear antara vektor `x` dan `x'`.
- `\cdot` merupakan simbol untuk perkalian dot antara vektor `x` dan `x'`.

### *Accuracy*

Nilai akurasi didapatkan dari jumlah data bernilai positif yang diprediksi positif dan data bernilai negatif yang diprediksi negatif dibagi dengan jumlah seluruh data di dalam dataset.

$$Accuracy = \frac{True\ Positives + True\ Negatives}{True\ Positives + True\ Negatives + False\ Positives + False\ Negatives}$$

### *Precision*

$$Precision = \frac{True\ Positives}{True\ Positives + False\ Positives}$$
Nilai Precision adalah peluang kasus yang diprediksi positif yang pada kenyataannya termasuk kasus kategori positif.

### *Recall*

Nilai Recall adalah peluang kasus dengan kategori positif yang dengan tepat diprediksi positif.
$$Recall = \frac{True\ Positives}{True\ Positives + False\ Negatives}$$

### *F1 Score*

Nilai _F1-Score_ atau dikenal juga dengan nama _F-Measure_ didapatkan dari hasil _Precision_ dan _Recall_ antara kategori hasil prediksi dengan kategori sebenarnya.
$$F1\text{-}score = 2 \cdot \frac{Precision \cdot Recall}{Precision + Recall}$$

> Keterangan :
>
> - ***True Positive* (TP)** : Jumlah data yang bernilai Positif dan diprediksi benar sebagai Positif.
> - **F*alse Positive* (FP)** : Jumlah data yang bernilai Negatif tetapi diprediksi sebagai Positif.
> - ***False Negative* (FN)** : Jumlah data yang bernilai Positif tetapi diprediksi sebagai Negatif.
> - ***True Negative* (TN)** : Jumlah data yang bernilai Negatif dan diprediksi benar sebagai Negatif.

# Hasil Uji Coba

![Hasil Uji Coba Model](https://github.com/candraburhanudin15/analisis-sentimen-Review-Livin-By-Mandiri/assets/62823773/25d8c5c7-d63a-4e77-8354-bbef32cdcce3)

Dari Hasil Uji Coba 7 Ulasan Yang dibuat hasil sudah sesuai . Dari beberapa Ulasan Negatif Terkait, Login, Update, Verifikasi Wajah yang sering gagal menjadi sebuah prioritas utama dalam penunjang keputusan untuk meningkatkan pelayanan aplikasi LIVIN kepada pengguna.

# Kesimpulan

Pembuatan Analisis Sentimen menggunakan metode SVM Dalam beberapa kasus, penggunaan kernel RBF dapat menghasilkan metrik yang lebih baik dalam metrik evaluasi seperti akurasi, presisi, dan _recall_ dibandingkan dengan kernel linear. Namun, pemilihan kernel yang tepat bergantung pada karakteristik data dan kompleksitas masalah yang sedang diselesaikan. Oleh karena itu, penting untuk melakukan eksperimen dan evaluasi yang cermat untuk menentukan kernel yang paling sesuai untuk kasus yang spesifik. pada dataset _LIVIN By Mandiri App Review_ yang bersifat non-linear dimana data ulasan positif atau negatif terkadang memiliki makna yang tidak sesuai dengan rating yang diberikan seharusnya, maka dari itu menggunakan kernel RBF lebih cocok di aplikasikan kepada dataset ini. Model pelatihan menggunakan metode RBF mendapatkan nilai yang lebih baik dengan akurasi mencapai 89%.

# Daftar Pustaka

[1] A. Novantika, “Analisis Sentimen Ulasan Pengguna Aplikasi Video Conference Google Meet menggunakan Metode SVM dan Logistic Regression,” _PRISMA, Prosiding Seminar Nasional Matematika_, vol. 5, pp. 808–813, 2022, [Online]. Available: https://journal.unnes.ac.id/sju/index.php/prisma/

[2] M. Diki Hendriyanto, A. A. Ridha, and U. Enri, “Analisis Sentimen Ulasan Aplikasi Mola Pada Google Play Store Menggunakan Algoritma Support Vector Machine Sentiment Analysis Of Mola Application Reviews On Google Play Store Using Support Vector Machine Algorithm” _Journal of Information Technology and Computer Science (INTECOMS)_, vol. 5, no. 1, 2022.

[3] A. Muhammadin and I. A. Sobari, “Analisis Sentimen Pada Ulasan Aplikasi Kredivo Dengan Algoritma SVM Dan NBC,” _Jurnal Rekayasa Perangkat Lunak_, vol. 2, no. 2, 2021, [Online]. Available: http://jurnal.bsi.ac.id/index.php/reputasi

**---Ini adalah bagian akhir laporan---**
