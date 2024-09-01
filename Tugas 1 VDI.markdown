Dwi Ratna Anggraeni
122450008
RB

**RESUME ARTIKEL**

# **Making data visualization more efficient and effective: a survey**

> Penulis : Xuedi Qin, Yuyu Luo, Nan Tang, Guoliang Li

> Nama Jurnal : The VLDB Journal

> Tanggal Terbit : 19 November 2019

Dunia bisnis berbasis data saat ini membutuhkan visualisasi data untuk membantu pengambilan keputusan perusahaan industri. Namun, karena tingginya permintaan pemrosesan jumlah data, kecepatan, dan kebenaran data, ada kebutuhan yang muncul untuk ahli basis data untuk membantu agar efisien dan visualisasi data yang efektif. Artikel ini mensurvei teknik-teknik yang membuat visualisasi data menjadi lebih efisien dan efektif.
1. Spesifikasi Visualisasi
2. Pendekatan Efisien untuk Visualisasi Data
3. Rekomendasi Visualisasi Data

## **1. Pendahuluan**

Visualisasi data adalah mengubah data abstrak menjadi visi fisik (misalnya, panjang, posisi, bentuk, warna, dan dan sebagainya), untuk menyajikan cerita yang menarik dari data kepada publik yang lebih berorientasi pada visual.  visualisasi data banyak digunakan di berbagai aplikasi yang berhubungan dengan database, seperti Excel, Google Sheets, Oracle Data Visualization Desktop, IBM DB2, Amazon Quicksight, Microsoft Power BI, dan lain sebagainya.
Alur visualisasi data yaitu:
1. Impor 
2. Persiapan data 
3. Manipulasi data 
4. Pemetaan
5. Rendering 

Berdasarkan alur tersebut, ada tiga arah yang membuat visualisasi data lebih efisien dan efektif yaitu:
1. Spesifikasi Visualisasi: menyediakan berbagai cara agar pengguna dapat menentukan apa yang diinginkan.
2. Pendekatan yang Efisien untuk Visualisasi Data: proses pembuatan visualisasi data harus efisien dan terukur, terutama untuk dua komponen, “Data Manipulation” dan “Mapping”. 
3. Rekomendasi Visualisasi Data: Menentukan visualisasi dengan tepat seperti tentang data apa yang akan divisualisasikan, cerita apa yang yang harus diceritakan, dan bagaimana memvisualisasikannya hal tersebut memerlukan latihan.

## **2. Spesifikasi Visualisasi** 

**2.1 Spesifikasi visualisasi data**

Secara umum, bahasa visualisasi data terdiri dari tiga bagian: data, tanda (atau isyarat visual), dan pemetaan diantara keduanya.

**2.2 Kategorisasi bahasa visualisasi data**

Bahasa visualisasi data dikategorikan  tingkat terendah yaitu pengguna harus menentukan fungsi pemetaan dan tingkat tinggi yaitu merangkum detail konstruksi visualisasi, seperti fungsi pemetaan,beberapa properti untuk ggplot2, serta pengguna hanya perlu menentukan jenis tanda dan tidak perlu menentukan fungsi pemetaan antara data dan tanda.

**2.3 Operasi visual berbasis GUI**

Dibandingkan dengan menggunakan bahasa visualisasi deklaratif untuk menspesifikasikan visualisasi  yang lebih mudah adalah dengan mengikuti “prinsip manipulasi langsung”, sebuah konsep yang digunakan secara luas dalam aspek interaksi manusia dan komputer menggunakan  alat bantu berbasis GUI yang canggih (Tableau, Qlik, Excel, Google Spreadsheet], Amazon Quicksight, Microsoft Power BI, Google Fusion Tables, iVisDesigner, Lyra, Keshif, Data Illustrator).

**2.4 Spesifikasi yang kurang spesifik**

Visualisasi tidak ada artinya jika tidak dapat memberikan wawasan dari data. Namun, ada banyak kasus, pengguna tidak mengetahui semua aspek dari data yang ada, karena data mungkin besar dan sering diperbarui. Sehingga menimbulkan spesifikasi yang kurang spesifik. 

## **3. Pendekatan yang efisien untuk visualisasi data**

**3.1 Visualisasi data yang tepat**

Banyak sistem visualisasi data membaca data dari database. Mereka juga dapat memanipulasi data dengan pernyataan SQL dan kemudian menggunakan alat visualisasi untuk membuat visualisasi. Ermac adalah sebuah Data Visualization Management System (DVMS), Sistem ini mendukung dua relasi: data dan skala, di mana data relasi meliputi catatan data yang akan divisualisasikan dan referensi ke elemen visual yang diberikan; skala relasi menunjukkan pemetaan dari rentang data ke rentang pengkodean visual. Beberapa teknik optimasi untuk visualisasi interaktif dalam DVMS.
-Column Store

-Indexes

-Parallel Computation

-Prediction and Prefetching

**3.2 Perkiraan visualisasi data**

Ketika jumlah data tumbuh secara eksponensial, maka modul pemrosesan data tradisional tidak dapat memberikan hasil pemrosesan yang cepat dan interaktif. Untuk mengatasi masalah antara jumlah data dan interaktivitas, banyak penelitian yang mempercepat tahap pemrosesan data dengan memanfaatkan pemrosesan kueri perkiraan (AQP) yang memberikan hasil visualisasi perkiraan. Pangloss menyediakan visualisasi perkiraan kepada pengguna dengan cepat berdasarkan teknik AQP, pengguna dapat memperoleh wawasan awal dari hasil perkiraan dan kemudian memverifikasi pengamatan mereka pada hasil yang tepat. 
-Berbasis Sampling Tambahan, Pengguna biasanya dapat memperoleh beberapa wawasan awal dari perkiraan visualisasi dan memutuskan untuk menghentikannya jika kualitas visualisasi cukup untuk memverifikasi wawasan ini.

-Berbasis Persepsi Manusia, Pendekatan berbasis persepsi manusia menghentikan pengambilan sampel ketika tidak ada perbedaan yang jelas pada persepsi manusia antara visualisasi perkiraan saat ini dan visualisasi yang akan didapat dengan pengambilan sampel lebih lanjut.

**3.3 Visualisasi data progresif**
Banyak hasil penelitian dalam visualisasi data perkiraan menghasilkan hasil visualisasi yang progresif kepada pengguna, selain visualisasi data progresif berbasis pengambilan sampel tambahan di atas, ada juga banyak hasil penelitian  yang menyediakan visualisasi progresif dengan agregasi hirarki.
-Range-Based Binning: imMens menyediakan visualisasi resolusi yang berbeda dengan mengubah ukuran bin. Bin dengan resolusi yang sama memiliki rentang yang sama.

-Range and Content-Based Binning: Menyediakan dua struktur pohon untuk eksplorasi hirarki: HETree-R (HETree berbasis rentang) dan HETree-C (HETree berbasis konten)

## **4. Rekomendasi Visualisasi**

Proses visualisasi data bersifatiteratif, dan letak kesulitan utama para praktisi adalah mereka harus terlibat dalam setiap langkah modifikasi. Tentu saja, diharapkan adanya solusi rekomendasi visualisasi pengguna lebih mudah, dengan merekomendasikan visualisasi yang baik.

**4.1 Rekomendasi berdasarkan spesifikasi**

- Spesifikasi yang tidak lengkap: Sistem rekomendasi visualisasi dengan spesifikasi kosong tidak memerlukan masukan dari pengguna, sedangkan sistem rekomendasi dengan spesifikasi parsial menerima masukan spesifikasi sebagian elemen visualisasi dari pengguna untuk visualisasi yang diinginkan. 

- Spesifikasi berbasis referensi: Beberapa sistem rekomendasi visualisasi merekomendasikan visualisasi berdasarkan data referensi atau visualisasi referensi. Biasanya, sistem akan merekomendasikan visualisasi yang mirip atau berbeda dengan referensi yang diberikan dalam aspek-aspek tertentu.

**4.2 Rekomendasi berbasis perilaku**

Sistem rekomendasi berbasis perilaku menangkap perilaku pengguna saat ini sebagai input, kemudian menyimpulkan apa yang diinginkan pengguna dan merekomendasikan visualisasi yang berguna berdasarkan tugas mereka. HARVEST adalah sistem rekomendasi visualisasi berbasis perilaku. Sistem ini merekomendasikan visualisasi berdasarkan tugas pengguna yang disimpulkan dari perilaku mereka.

**4.3 Rekomendasi personalisasi**

Sistem rekomendasi personalisasi menangkap perilaku historis pengguna sebagai masukan untuk merekomendasikan visualisasi menarik yang dipersonalisasi.

## **5. Arah Penelitiannya lainnya**

**5.1 Persiapan data untuk visualisasi data**

Sebelum memvisualisasikan, data harus dibersihkan seperti normalisasi nilai, deduplikasi, imputasi nilai yang hilang, dan deteksi pencilan. Tableau telah mengintegrasikan Trifacta untuk persiapan data di seluruh dataset. Karena memvisualisasikan data yang belum siap olah dapat menyesatkan pengguna.

**5.2 Tolak ukur visualisasi data**

**5.3 Visualisasi data untuk aplikasi yang berhubungan dengan database**

visualisasi data juga memainkan peran penting dalam aplikasi yang berhubungan dengan basis data, seperti Excel, Google Spreadsheet, Oracle Data Visualization Desktop, IBM Db2, Amazon Quicksight, dan lain-lain.  Perkembangan teknik visualisasi cukup pesat, membuat  lebih banyak peluang tentang penggunaan visualisasi data untuk aplikasi yang berhubungan dengan database.
- Visualisasi data untuk penemuan data.
  
- Visualisasi data untuk debugging data.

## **6. Kesimpulan**
Visualisasi data adalah bidang yang berkembang pesat dengan banyaknya hasil penelitian baru dan sistem baru yang dikembangkan baru-baru ini. Penelitian dan praktisi dari berbagai bidang telah berkontribusi pada keberhasilan visualisasi data yang luar biasa, yang didorong oleh sebagian besar (jika tidak semua) domain dan aplikasi. Artikel ini mensurvei hasil visualisasi data terbaru, dari perspektif manajemen data.Namun, banyak praktisi yang masih mengalami masalah efisiensi dan rekomendasi dari sistem-sistem ini. 
