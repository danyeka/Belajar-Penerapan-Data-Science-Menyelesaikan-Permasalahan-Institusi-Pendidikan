# Menyelesaikan Permasalahan Institusi Pendidikan

## Business Understanding

Jaya Jaya Institute merupakan institusi pendidikan tinggi yang telah beroperasi sejak tahun 2000 dan memiliki rekam jejak yang baik dalam menghasilkan lulusan berkualitas. Namun, institusi ini menghadapi permasalahan serius berupa tingginya angka siswa yang tidak menyelesaikan studi atau putus sekolah (dropout). Masalah ini menjadi ancaman besar bagi reputasi institusi, sehingga diperlukan upaya untuk mengidentifikasi siswa yang berpotensi dropout sejak dini agar dapat diberikan pendampingan khusus.

### Business Problem

**Jaya Jaya Institute mengalami kendala signifikan akibat tingginya tingkat dropout mahasiswa, yang dapat berdampak negatif pada kredibilitas dan akreditasi institusi serta menurunkan kepercayaan publik terhadap standar pendidikan yang disediakan**. Keterbatasan dalam mendeteksi mahasiswa berisiko dropout secara dini menghalangi implementasi tindakan preventif dan bimbingan yang diperlukan, sehingga membahayakan eksistensi dan kompetitivitas institusi dalam persaingan pendidikan yang semakin kompetitif.

**Oleh karena itu, sangat penting untuk dapat mengenali dan memproyeksikan mahasiswa yang berpotensi dropout seawal mungkin** supaya institusi dapat melakukan intervensi yang efektif untuk meningkatkan angka kelulusan.

### Project Scope

- Persiapan dan pembersihan data awal
- Analisis Data Eksploratori (EDA) untuk mengidentifikasi faktor-faktor penyebab tingginya angka dropout melalui visualisasi data
- Pembuatan dashboard bisnis yang menampilkan faktor-faktor penyebab tingginya angka dropout
- Pengembangan model pembelajaran mesin untuk memprediksi status mahasiswa berdasarkan variabel-variabel penyebab tingginya dropout
- Implementasi model pembelajaran mesin untuk digunakan dalam prediksi status dropout atau kelulusan mahasiswa

### Preparation

**Data source:**
- [Students' Performance data](https://github.com/dicodingacademy/dicoding_dataset/tree/main/students_performance 'Dicoding GitHub - Students Performance data')
- [Predict Students' Dropout and Academic Success](https://doi.org/10.24432/C5MC89 'UCI Machine Learning - Predict Students Dropout and Academic Success')

**Setup environment:**

1. Clone this Repository
   ```bash
   git clone 
   ```

2. Create Python Virtual Environment
   ```bash
   virtualenv venv
   ```

2. Activate the Environment
   ```bash
   venv\Scripts\activate
   ```

4. Install All the Requirements Inside "requirements.txt"
   ```bash
   pip install -r requirements.txt
   ```

## Business Dashboard

[Jaya Jaya Institute Students Dashboard](https://link 'Tableau Public - Jaya Jaya Institute Students Dashboard'), Dashboard Siswa Jaya Jaya Institute telah dirancang secara optimal untuk memberikan wawasan kepada tenaga pengajar dan pihak internal institusi mengenai tingkat dropout siswa yang mencapai lebih dari 30%. Dashboard ini juga dibuat dengan mempertimbangkan aksesibilitas untuk individu dengan gangguan penglihatan warna.



![Jaya Jaya Maju Employees Dashboard]( 'Jaya Jaya Institute Students Dashboard')

Dashboard terdiri dari tiga bagian utama: bagian kiri menampilkan diagram lingkaran ringkasan data siswa, bagian tengah menunjukkan diagram sebar persebaran data siswa, dan bagian kanan berisi data numerik, diagram batang faktor dropout mahasiswa, serta filter dan legenda.
> Dari **pie chart jenis kelamin**, dapat dilihat bahwa populasi data lebih banyak berjenis kelamin perempuan, sebesar 2868 (64.83%), sedangkan laki-laki hanya 1556 (35.17%).  
> Dari **pie chart status siswa**, terdapat total 4424 siswa, di antaranya 794 (17.95%) yang saat ini sedang terdaftar, 2209 (49.93%) yang sudah lulus, dan 1421 (32.12%) yang dropout.  
> Dari **pie chart beasiswa**, hampir 1/4, yaitu sebesar  1099 (24.84%) siswa yang memperoleh beasiswa, sedangkan 3325 (75.16%) sisanya tidak.  
> Dari **pie chart debitur** sebanyak 503 (11.37%) adalah seorang debitur, dan 3921 (88.63%) sisanya tidak.  
> Dari **scatter plot status siswa berdasarkan umur dan nilai tes masuk**, dapat dilihat dengan jelas rata-rata siswa yang lulus sebagian besar berada pada usia di bawah 20 sampai 25 tahun, dengan rata-rata Nilai Penerimaan (Admission Grade) berkisar 120 sampai 160. Sementara itu, siswa yang berusia 30 sampai 40 tahun, bahkan 50 tahun memiliki rata-rata Nilai Penerimaan (Admission Grade) 100 sampai 140 dan berstatus dropout.  
> **Rata-rata umur** adalah 23.27 tahun, **rata-rata Nilai Penerimaan (Admission Grade)** adalah 127.0, dan sebanyak 110 siswa **internasional**, dan 4314 siswa lokal.  
> Dari **bar chart status siswa berdasarkan status debtor**, dapat dilihat siswa yang menjadi debitur jelas tergambar paling banyak adalah mereka yang berstatus dropout (312 siswa) dibandingkan dengan mereka yang lulus (101 siswa). Hal ini menggambarkan adanya faktor finansial yang sangat kuat terhadap tingkat kelulusan dan dropout siswa.  
> Dari **bar chart status siswa berdasarkan beasiswa**, terdapat 835 siswa lulus dengan beasiswa dan 1374 siswa yang lulus tanpa beasiswa, sebesar 37.79% berbanding 62.20%. Sedangkan siswa yang dropout dengan beasiswa sebanyak 134 dan siswa yang dropout tanpa beasiswa sebanyak 1287, sebesar 9.43% berbanding 90.57%.  
> Dari **bar chart distribusi jenis kursus dan jenis kelamin**, kursus dengan data terbanyak adalah Keperawatan dengan jenis kelamin dominan adalah Perempuan. Sementara kursus dengan data paling sedikit adalah Teknologi Produksi Buofuel dengan dominasi Laki-laki. Selain itu, mahasiswa Laki-laki terbanyak ada di Program Studi Teknik Informatika dan Manajemen.  


## Machine Learning Prediction System

Untuk dapat membantu institusi dalam memprediksi kemungkinan jika siswanya akan dropout dan mencegah hal tersebut lebih dini, dapat menggunakan sistem prediksi yang telah dibangun. Sistem dibangun menggunakan Streamlit dan untuk menjalankan sistem tersebut secara local, dapat menjalankan kode berikut pada Terminal,

```bash
streamlit run streamlit_app.py
```

Dan untuk menghentikan program aplikasi Streamlit dapat melalui `ctrl + c`.

Sistem prediksi tersebut juga dapat diakses secara langsung yang sudah di-deploy ke Streamlit Cloud melalui tautan [berikut ini](https://student-do-predict.streamlit.app 'Jaya Jaya Institute Students Dropout Prediction').

## Conclusion

Berikut adalah beberapa poin penting yang bisa ditarik menjadi kesimpulan:
- **Distribusi Demografi Siswa:** Mayoritas siswa berjenis kelamin perempuan (64.83%), dengan sebagian besar populasi total adalah siswa lokal (97.51%) dibandingkan siswa internasional (2.49%).
- **Status Siswa:** Dari total 4424 siswa, hampir sepertiga (32.12%) mengalami dropout. Sebagian besar siswa yang lulus berada pada usia muda (20–25 tahun) dengan nilai penerimaan yang relatif lebih tinggi (120–160), sementara siswa usia lebih tua dan dengan nilai lebih rendah cenderung mengalami dropout.
- **Pengaruh Beasiswa:** Siswa yang menerima beasiswa memiliki tingkat kelulusan yang lebih tinggi (37.79%) dibandingkan dengan tingkat dropout (9.43%), menunjukkan peran signifikan beasiswa dalam mendukung keberhasilan akademik.
- **Faktor Keuangan:** Sebagian besar siswa dropout (61.99%) adalah debitur, menandakan kemungkinan adanya tekanan finansial yang memengaruhi keberlanjutan studi mereka.
- **Distribusi Berdasarkan Kursus:** Kursus dengan jumlah siswa tertinggi adalah Keperawatan dengan dominasi perempuan, sementara Teknologi Produksi Biofuel memiliki jumlah siswa terendah dengan dominasi laki-laki.

### Recommended Action Items

Berikut beberapa rekomendai yang dapat diambil oleh institusi untuk mengatasi permasalahan tingkat dropout siswa:
- Perluasan program beasiswa, terutama untuk kategori siswa yang berisiko dropout berdasarkan status keuangannya.
- Penyediaan opsi pembayaran cicilan dengan bunga 0% atau program penghapusan sebagian utang/biaya kuliah yang menunggak bagi siswa berprestasi.
- Menyediakan opsi program gap year disertai orientasi khusus untuk siswa yang kembali dari gap year, guna membantu dalam penyesuaian diri dengan lingkungan, teknologi, atau kurikulum yang mungkin telah berubah.
- Mengadakan program bimbingan belajar khusus untuk siswa dengan nilai rendah, terutama yang berusia lebih tua dan yang sudah menikah.
- Mendirikan pusat dukungan psikologis dan konseling bagi siswa yang mengalami tekanan finansial atau akademik.
- Melakukan peninjauan dan pemantauan lebih lanjut terhadap siswa yang saat ini sedang terdaftar (enrolled), serta prediksi kemungkinan siswa untuk tidak lulus/dropout melalui sistem yang telah dibangun menggunakan teknologi machine learning melalui website prediksi [berikut ini](https://student-do-predict.streamlit.app 'Jaya Jaya Institute Students Dropout Prediction').
