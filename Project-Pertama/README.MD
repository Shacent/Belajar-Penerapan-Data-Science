# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Perusahaan ini memiliki lebih dari 1.000 karyawan yang tersebar di seluruh penjuru negeri. 

Walaupun telah berkembang menjadi perusahaan yang cukup besar, Jaya Jaya Maju menghadapi tantangan besar dalam mengelola karyawan. Salah satu dampaknya adalah tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) yang mencapai lebih dari 10%. 

Untuk mencegah hal ini semakin parah, departemen HR meminta bantuan untuk mengidentifikasi berbagai faktor yang memengaruhi tingginya attrition rate. Selain itu, perusahaan meminta pembuatan business dashboard untuk membantu memonitor berbagai faktor tersebut dan memberikan wawasan yang lebih baik untuk pengambilan keputusan.

### Permasalahan Bisnis

- Mengidentifikasi faktor-faktor utama yang memengaruhi tingginya attrition rate di perusahaan.
- Mengurangi attrition rate dengan cara yang strategis dan berbasis data.
- Menyediakan business dashboard untuk memonitor faktor-faktor yang relevan secara visual dan terintegrasi.

### Cakupan Proyek

- Mengolah dataset karyawan untuk menemukan pola-pola yang terkait dengan tingkat attrition.
- Membagi karyawan ke dalam beberapa cluster berdasarkan karakteristik mereka menggunakan analisis clustering.
- Membuat business dashboard interaktif untuk membantu departemen HR memonitor faktor-faktor yang relevan.
- Memberikan rekomendasi berbasis data untuk membantu perusahaan mengurangi attrition rate.

### Persiapan

**Sumber data:**  
Dataset yang digunakan berasal dari tautan berikut: [Jaya Jaya Maju Dataset](https://github.com/dicodingacademy/dicoding_dataset/blob/main/employee/employee_data.csv).

**Setup environment:**

Gunakan langkah berikut untuk mengatur lingkungan kerja:

```bash
# Clone repository (jika menggunakan repository Git)
git clone <repository-url>

# Aktifkan environment (opsional jika menggunakan conda)
conda create --name proyek-akhir python=3.9
conda activate proyek-akhir

# Instal library yang diperlukan
pip install -r requirements.txt

```

## Business Dashboard

### 1. **Attrition Berdasarkan Pendapatan Bulanan**
- Karyawan dengan pendapatan rendah (**$0 - $2,500** dan **$2,500 - $5,000**) memiliki tingkat attrition yang jauh lebih tinggi dibandingkan dengan karyawan dengan pendapatan yang lebih tinggi.
- **Kesimpulan:** Pendapatan rendah adalah salah satu faktor utama attrition. Kenaikan pendapatan atau insentif tambahan dapat mengurangi risiko ini.

### 2. **Attrition Berdasarkan Posisi Pekerjaan**
- Posisi dengan tingkat attrition tertinggi:
  - **Sales Representatives**.
  - **Laboratory Technician**.
- Posisi dengan tingkat attrition rendah:
  - **Manager**.
  - **Healthcare Representative**.
- **Kesimpulan:** Posisi dengan pendapatan lebih rendah dan beban kerja tinggi lebih rentan terhadap attrition.

### 3. **Attrition Berdasarkan Status Lembur (OverTime)**
- Karyawan yang sering lembur memiliki risiko attrition yang lebih tinggi (**209 attrition vs 81 tanpa lembur**).
- **Kesimpulan:** Beban kerja lembur menjadi salah satu penyebab utama karyawan meninggalkan perusahaan.

### 4. **Attrition Berdasarkan Jarak ke Kantor**
- Karyawan yang tinggal lebih dekat ke kantor (**0-5 km**) memiliki risiko attrition lebih rendah dibandingkan yang tinggal jauh (**15-25 km**).
- **Kesimpulan:** Jarak tempat tinggal ke kantor memengaruhi tingkat kenyamanan dan kepuasan kerja.

### 5. **Attrition Berdasarkan Departemen**
- Departemen dengan tingkat attrition tertinggi adalah **Sales**, diikuti oleh **Research & Development**.
- Departemen **Human Resources** memiliki tingkat attrition paling rendah.
- **Kesimpulan:** Fokus perlu diberikan pada departemen Sales untuk mengurangi risiko.

### 6. **Attrition Berdasarkan Frekuensi Perjalanan (Travel)**
- Karyawan yang sering bepergian (**Travel Frequently**) memiliki tingkat attrition yang jauh lebih tinggi dibandingkan yang jarang atau tidak bepergian.
- **Kesimpulan:** Beban perjalanan yang tinggi dapat menyebabkan kelelahan dan memicu attrition.

### 7. **Attrition Berdasarkan Usia**
- Karyawan muda (**22.5 - 30 tahun**) memiliki tingkat attrition yang lebih tinggi dibandingkan usia lainnya.
- **Kesimpulan:** Karyawan muda yang masih mencari stabilitas atau peluang karier lebih baik lebih rentan keluar.

### 8. **Attrition Berdasarkan Kepuasan Kerja dan Lingkungan**
- Karyawan dengan kepuasan kerja rendah lebih cenderung keluar dari perusahaan.
- **Kesimpulan:** Meningkatkan kepuasan kerja dan lingkungan kerja dapat menurunkan risiko attrition secara signifikan.


## Conclusion

Hasil analisis menunjukkan bahwa tingkat attrition dipengaruhi oleh beberapa faktor utama, seperti posisi pekerjaan, tingkat pendapatan, dan kepuasan kerja. Berikut adalah temuan utama dari analisis cluster:

### **Cluster 0 (Paling Berbahaya - Tingkat Attrition Tertinggi):**
- Didominasi oleh Sales Representatives, karyawan lembur, dan pendapatan rendah.
- Karyawan muda dengan pengalaman kerja singkat cenderung lebih berisiko.
- **Rekomendasi:**
  - Kurangi beban kerja lembur atau beri kompensasi yang lebih besar untuk karyawan lembur.
  - Tingkatkan kompensasi bagi karyawan dengan pendapatan rendah melalui insentif, bonus, atau tunjangan.
  - Sediakan program pengembangan karier untuk meningkatkan keterampilan Sales Representatives dan memberikan peluang karier bagi karyawan muda.
  - Tawarkan fleksibilitas kerja atau program kesejahteraan bagi karyawan single untuk meningkatkan retensi.
  - Kurangi frekuensi perjalanan bisnis bagi karyawan yang sering bepergian atau beri kompensasi yang memadai.

### **Cluster 2 (Risiko Sedang):**
- Memiliki tingkat risiko yang lebih rendah dibandingkan Cluster 0, tetapi masih terdapat attrition.
- Sebagian besar karyawan dengan pengalaman kerja pendek hingga menengah.
- Tingkat pendapatan di level menengah.
- Mayoritas karyawan yang keluar juga bekerja lembur, meskipun tidak sebanyak Cluster 0.
- **Rekomendasi:**
  - Fokus pada program keseimbangan kerja-hidup untuk meningkatkan kepuasan kerja dan lingkungan.
  - Berikan penghargaan bagi karyawan yang tetap setia untuk meningkatkan motivasi karyawan lain.
  - Sediakan program mentoring dari karyawan berpengalaman untuk mendukung karyawan dengan pengalaman kerja pendek.

### **Cluster 1 & 3 (Setia - Tingkat Attrition Rendah):**
- Karyawan dengan pendapatan tinggi, pengalaman kerja panjang, dan tingkat kepuasan yang baik.
- **Rekomendasi:**
  - Pertahankan kebijakan yang sudah ada, seperti sistem kompensasi dan keseimbangan kerja-hidup yang ada.
  - Perkenalkan program apresiasi untuk loyalitas karyawan, seperti penghargaan kerja atau bonus tambahan.
  - Jadikan klaster ini sebagai contoh kebijakan sukses yang dapat diterapkan pada klaster lain yang berisiko tinggi.
  - Gunakan karyawan dari klaster ini untuk program mentoring guna membantu klaster lain yang lebih berisiko.

### **Kesimpulan Umum:**
- **Cluster 0** adalah prioritas utama untuk diperbaiki karena memiliki tingkat attrition tertinggi. Fokus pada kebijakan kompensasi, keseimbangan kerja-hidup, dan pengembangan karier akan sangat membantu dalam mengurangi tingkat attrition di klaster ini.
- **Cluster 2** memiliki risiko sedang, tetapi dengan peningkatan kepuasan kerja dan penghargaan bagi karyawan yang setia, risiko dapat diminimalkan.
- **Cluster 1** dan **Cluster 3** adalah klaster setia yang dapat menjadi contoh kebijakan untuk diterapkan di klaster lain. Perusahaan harus terus mempertahankan keseimbangan kerja-hidup yang optimal dan memberikan apresiasi kepada karyawan.

## Rekomendasi Action Items (Optional)

- **Revisi Sistem Lembur:** Kurangi beban kerja lembur atau beri kompensasi yang lebih besar untuk karyawan lembur, terutama di Cluster 0.
- **Perbaikan Kompensasi:** Tingkatkan kompensasi untuk karyawan dengan penghasilan rendah, dan sediakan insentif atau bonus untuk meningkatkan motivasi.
- **Pengembangan Karier:** Sediakan program pelatihan dan mentoring untuk meningkatkan keterampilan karyawan, terutama di posisi yang memiliki attrition tinggi seperti Sales Representatives.
- **Fokus pada Keseimbangan Kerja-Hidup:** Implementasikan kebijakan yang mendukung keseimbangan kerja-hidup, termasuk fleksibilitas waktu kerja dan kesempatan untuk bekerja dari rumah, terutama bagi karyawan yang sering lembur.
- **Peningkatan Program Kesejahteraan untuk Karyawan Single:** Tawarkan fleksibilitas kerja dan kesejahteraan khusus bagi karyawan yang belum menikah untuk meningkatkan retensi mereka.
- **Program Apresiasi Karyawan:** Berikan penghargaan bagi karyawan yang tetap setia dan memiliki kinerja tinggi. Penghargaan ini bisa dalam bentuk bonus tambahan, penghargaan tahunan, atau program loyalitas.
- **Pemantauan dan Survei Rutin:** Lakukan survei rutin untuk mengevaluasi tingkat kepuasan kerja karyawan, serta memberikan ruang bagi karyawan untuk memberikan masukan terkait kebijakan perusahaan.

---





