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
   git clone https://github.com/danyeka/Belajar-Penerapan-Data-Science-Menyelesaikan-Permasalahan-Institusi-Pendidikan.git
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

[Jaya Jaya Institute Students Dashboard](https://lookerstudio.google.com/reporting/78f7064e-e021-4899-8b32-ce21ccde5f26 'Tableau Public - Jaya Jaya Institute Students Dashboard'), Dashboard Siswa Jaya Jaya Institute telah dirancang secara optimal untuk memberikan wawasan kepada tenaga pengajar dan pihak internal institusi mengenai tingkat dropout siswa yang mencapai lebih dari 30%. Dashboard ini juga dibuat dengan mempertimbangkan aksesibilitas untuk individu dengan gangguan penglihatan warna.

**Dashboard Interaktif:** [Dashboard](https://lookerstudio.google.com/reporting/78f7064e-e021-4899-8b32-ce21ccde5f26) - Dashboard interaktif untuk analisis dan prediksi dropout siswa menggunakan Looker Studio yang dapat diakses secara online.



![Jaya Jaya Maju Employees Dashboard]( 'Jaya Jaya Institute Students Dashboard')

Dasbor ini tersusun dalam tiga bagian pokok: area kiri memperlihatkan diagram lingkaran yang merangkum informasi mahasiswa, area tengah menampilkan diagram pencar distribusi mahasiswa, dan area kanan berisi data angka, diagram batang faktor-faktor dropout mahasiswa, beserta filter dan keterangan.

> Berdasarkan **diagram lingkaran gender**, terlihat bahwa mayoritas mahasiswa adalah perempuan dengan jumlah 2.868 orang (64,83%), sementara mahasiswa laki-laki berjumlah 1.556 orang (35,17%).  

> Melalui **diagram lingkaran status mahasiswa**, tercatat total 4.424 mahasiswa, dengan rincian 794 orang (17,95%) masih aktif kuliah, 2.209 orang (49,93%) telah lulus, dan 1.421 orang (32,12%) mengalami dropout.  

> Pada **diagram lingkaran beasiswa**, hampir seperempat mahasiswa yakni 1.099 orang (24,84%) menerima beasiswa, sedangkan 3.325 orang (75,16%) tidak menerima beasiswa.

> **Diagram lingkaran debitur** menunjukkan 503 orang (11,37%) tercatat sebagai debitur, sementara 3.921 orang (88,63%) bukan debitur.  

> **Diagram pencar status mahasiswa berdasarkan usia dan nilai ujian masuk** memperlihatkan bahwa sebagian besar lulusan berusia antara 20-25 tahun dengan nilai masuk berkisar 120-160. Sebaliknya, mahasiswa berusia 30-40 tahun, bahkan mencapai 50 tahun, umumnya memiliki nilai masuk antara 100-140 dan cenderung mengalami dropout.

> Data menunjukkan **rata-rata usia** mahasiswa adalah 23,27 tahun, dengan **rata-rata Nilai Masuk** sebesar 127,0, serta terdapat 110 mahasiswa **internasional** dan 4.314 mahasiswa lokal.  

> **Diagram batang status mahasiswa berdasarkan status debitur** mengungkapkan bahwa mahasiswa debitur lebih banyak yang dropout (312 orang) dibandingkan yang lulus (101 orang). Hal ini mengindikasikan kuatnya pengaruh faktor keuangan terhadap tingkat kelulusan dan dropout.  

> Dari **diagram batang status mahasiswa berdasarkan beasiswa**, tercatat 835 penerima beasiswa berhasil lulus berbanding 1.374 lulusan non-beasiswa, dengan rasio 37,79% berbanding 62,20%. Sementara di kalangan mahasiswa dropout, 134 adalah penerima beasiswa dan 1.287 bukan penerima beasiswa, dengan perbandingan 9,43% berbanding 90,57%.  

> **Diagram batang distribusi program studi dan gender** menunjukkan bahwa Keperawatan memiliki peminat terbanyak dengan dominasi mahasiswa perempuan, sedangkan Teknologi Produksi Biofuel memiliki peminat paling sedikit dengan dominasi mahasiswa laki-laki. Selain itu, program studi Teknik Informatika dan Manajemen mencatat jumlah mahasiswa laki-laki terbanyak.


## Machine Learning Prediction System

Untuk dapat membantu institusi dalam memprediksi kemungkinan jika siswanya akan dropout dan mencegah hal tersebut lebih dini, dapat menggunakan sistem prediksi yang telah dibangun. Sistem dibangun menggunakan Streamlit dan dapat diakses secara online atau dijalankan secara lokal.

### Akses Online

**🌐 Live Demo:** [Jaya Jaya Institute Student Prediction](https://jayajaya-institute-student-prediction.streamlit.app/) - Aplikasi prediksi dropout mahasiswa yang dapat diakses langsung melalui browser tanpa instalasi.

### Menjalankan Secara Lokal

Untuk menjalankan sistem tersebut secara lokal, ikuti langkah-langkah berikut:

### Cara Menjalankan Aplikasi Streamlit

1. **Pastikan Environment Sudah Aktif**
   ```bash
   venv\Scripts\activate
   ```

2. **Jalankan Aplikasi Streamlit**
   ```bash
   streamlit run streamlit_app.py
   ```

3. **Akses Aplikasi**
   - Aplikasi akan terbuka secara otomatis di browser pada `http://localhost:8501`
   - Jika tidak terbuka otomatis, buka browser dan kunjungi alamat tersebut
   - 

4. **Menghentikan Aplikasi**
   - Tekan `Ctrl + C` di terminal untuk menghentikan server Streamlit

### Cara Melakukan Prediksi

#### Prediksi Data Tunggal:
1. Pilih tab **"Single Data Prediction"**
2. Isi semua field yang tersedia dengan data siswa:
   - **Data Demografis**: Gender, Age at enrollment, Nationality, dll.
   - **Data Akademik**: Course, Application mode, Previous qualification, dll.
   - **Data Keuangan**: Tuition fees up to date, Scholarship holder, Debtor status
   - **Data Kinerja**: Curricular units (semester 1 & 2), grades, evaluations
   - **Data Ekonomi**: GDP, Inflation rate, Unemployment rate
3. Klik tombol **"✨ Predict"**
4. Hasil prediksi akan muncul di bawah tombol:
   - **Graduate** (hijau): Siswa diprediksi akan lulus
   - **Dropout** (merah): Siswa diprediksi akan dropout

#### Prediksi Data Multiple (Batch):
1. Pilih tab **"Multiple Data Prediction"**
2. Download template Excel dengan klik **"📥 Download Student Data Template"**
3. Isi template Excel dengan data siswa (bisa multiple rows)
4. Upload file Excel yang sudah diisi
5. Klik tombol **"✨ Predict Data"**
6. Download hasil prediksi dalam format Excel

### Dashboard Bisnis

Selain sistem prediksi lokal, tersedia juga dashboard bisnis yang komprehensif untuk analisis pola dropout siswa. Dashboard ini menyediakan visualisasi interaktif dan insight mendalam tentang faktor-faktor yang mempengaruhi tingkat dropout.

Dashboard dapat diakses secara langsung melalui Looker Studio pada tautan [Dashboard](https://lookerstudio.google.com/reporting/78f7064e-e021-4899-8b32-ce21ccde5f26 'Jaya Jaya Institute Students Dropout Analysis Dashboard').

## Conclusion

Berdasarkan analisis data mahasiswa Jaya Jaya Institute, ditemukan beberapa temuan kritis yang memerlukan perhatian segera:

### 📊 **Gambaran Umum Dropout**
- **38.8%** mahasiswa mengalami dropout dari total 4.424 mahasiswa
- **61.2%** mahasiswa berhasil bertahan (Graduate/Enrolled)
- Tingkat dropout hampir 40% menunjukkan masalah serius yang perlu ditangani

### 🎯 **Faktor Risiko Utama Dropout**

#### 1. **Faktor Keuangan (Paling Kritis)**
- **61.99%** mahasiswa dropout adalah debitur
- Mahasiswa dengan status debtor memiliki risiko dropout **40-50x lebih tinggi**
- **95%** mahasiswa yang tidak dropout adalah non-debtor

#### 2. **Status Beasiswa**
- Mahasiswa **tanpa beasiswa** (~2.4K) memiliki tingkat dropout lebih tinggi
- Mahasiswa **penerima beasiswa** (~0.8K) menunjukkan tingkat retensi yang sangat baik
- Beasiswa terbukti sebagai **faktor protektif** yang efektif

#### 3. **Demografi dan Status Pernikahan**
- **Mahasiswa laki-laki** memiliki proporsi dropout lebih tinggi meskipun jumlah total lebih sedikit
- **Mahasiswa single** menunjukkan tingkat dropout **61.99%** vs married **38.01%**
- Mahasiswa yang sudah menikah cenderung lebih stabil secara akademik

### 📈 **Distribusi Program Studi**
- **Program Keperawatan**: Jumlah mahasiswa tertinggi dengan dominasi perempuan
- **Program Management, Tourism, Social Communication**: Tingkat dropout sangat tinggi
- **Variasi signifikan** tingkat dropout antar program studi menunjukkan perlunya evaluasi kurikulum

### 🚨 **Rekomendasi Strategis**

#### **Prioritas Tinggi:**
1. **Ekspansi program beasiswa** dan bantuan keuangan darurat
2. **Sistem early warning** untuk mahasiswa dengan masalah finansial
3. **Program mentoring khusus** untuk mahasiswa laki-laki dan single

#### **Prioritas Menengah:**
4. **Evaluasi dan restrukturisasi** program studi dengan dropout tinggi
5. **Konseling keuangan** dan manajemen hutang
6. **Program work-study** atau magang berbayar

#### **Prioritas Jangka Panjang:**
7. **Restrukturisasi sistem pembiayaan** pendidikan institusi
8. **Kemitraan dengan lembaga keuangan** untuk pinjaman pendidikan
9. **Pengembangan support system** yang komprehensif

### 💡 **Kesimpulan Utama**
**Faktor finansial** merupakan **predictor terkuat** untuk dropout, diikuti oleh **gender** dan **pilihan program studi**. Institusi harus mengadopsi pendekatan **multi-dimensional** yang mengatasi ketiga faktor ini secara simultan untuk mencapai penurunan tingkat dropout yang signifikan.

### Recommended Action Items

Berikut beberapa rekomendai yang dapat diambil oleh institusi untuk mengatasi permasalahan tingkat dropout siswa:
- Perluasan program beasiswa, terutama untuk kategori siswa yang berisiko dropout berdasarkan status keuangannya.
- Penyediaan opsi pembayaran cicilan dengan bunga 0% atau program penghapusan sebagian utang/biaya kuliah yang menunggak bagi siswa berprestasi.
- Menyediakan opsi program gap year disertai orientasi khusus untuk siswa yang kembali dari gap year, guna membantu dalam penyesuaian diri dengan lingkungan, teknologi, atau kurikulum yang mungkin telah berubah.
- Mengadakan program bimbingan belajar khusus untuk siswa dengan nilai rendah, terutama yang berusia lebih tua dan yang sudah menikah.
- Mendirikan pusat dukungan psikologis dan konseling bagi siswa yang mengalami tekanan finansial atau akademik.
- Melakukan peninjauan dan pemantauan lebih lanjut terhadap siswa yang saat ini sedang terdaftar (enrolled), serta analisis mendalam terhadap pola dropout melalui dashboard yang telah dibangun menggunakan Looker Studio melalui [Dashboard](https://lookerstudio.google.com/reporting/78f7064e-e021-4899-8b32-ce21ccde5f26 'Jaya Jaya Institute Students Dropout Analysis Dashboard').
