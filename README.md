# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

Jaya Jaya Maju merupakan perusahaan multinasional yang telah berdiri sejak tahun 2000 dan memiliki lebih dari 1.000 karyawan yang tersebar di seluruh Indonesia. Dengan skala perusahaan yang besar dan cakupan operasional yang luas, Jaya Jaya Maju telah membuktikan diri sebagai pemain utama dalam industrinya. Namun, seiring dengan pertumbuhan perusahaan, tantangan internal khususnya dalam pengelolaan sumber daya manusia (SDM) semakin kompleks. Salah satu permasalahan yang ada adalah Jaya Jaya Maju menghadapi tingkat attrition (tingkat pengunduran diri karyawan) yang tinggi. Untuk mengatasi isu krusial ini, diperlukan analisis mendalam guna mengidentifikasi faktor-faktor kunci atau penyebab mendasar yang berkontribusi terhadap tingginya angka pengunduran diri karyawan, sehingga strategi retensi yang efektif dapat dirumuskan dan diimplementasikan.

---

### Permasalahan Bisnis

Meskipun telah memiliki sistem manajemen SDM yang mapan, Jaya Jaya Maju menghadapi tingkat attrition (tingkat pengunduran diri karyawan) yang cukup tinggi, yaitu lebih dari 10%. Angka ini berada di atas rata-rata industri dan berpotensi menimbulkan berbagai dampak negatif, seperti:
- Hilangnya talenta berpengalaman,
- Biaya rekrutmen dan pelatihan ulang yang tinggi,
- Gangguan terhadap produktivitas dan stabilitas tim,
- Penurunan moral dan keterlibatan karyawan lainnya.

Tingginya attrition ini menjadi sinyal bahwa ada faktor-faktor mendasar dalam lingkungan kerja atau manajemen karyawan yang perlu diidentifikasi dan diperbaiki.

---

### Tujuan Proyek

Dari permasalahan yang dihadapi oleh perusahaan, maka Departemen Human Resources (HR) Jaya Jaya Maju telah menginisiasi proyek analisis data dengan tujuan untuk:
1. Mengidentifikasi faktor-faktor utama yang berkontribusi terhadap keputusan karyawan untuk mengundurkan diri, berdasarkan data demografis dan metrik pekerjaan.
2. Membangun dashboard bisnis yang dapat memvisualisasikan metrik-metrik penting terkait attrition secara real-time, untuk mendukung pengambilan keputusan strategis oleh manajemen HR.
3. Memberikan rekomendasi berbasis data dalam upaya menurunkan attrition dan meningkatkan retensi karyawan.

---

### Cakupan Proyek

#### ✅ Data yang Digunakan
Dataset yang telah disediakan oleh PT Jaya Jaya Maju berisi informasi demografis, kondisi kerja, dan label attrition untuk masing-masing karyawan, termasuk fitur-fitur seperti:
1. Informasi demografi: Age, Gender, Education, MaritalStatus, dll.
2. Detail pekerjaan: Department, JobRole, JobLevel, JobSatisfaction, dll.
3. Kompensasi dan benefit: DailyRate, HourlyRate, MonthlyIncome, StockOptionLevel, dll.
4. Data lainnya: OverTime, WorkLifeBalance, YearsAtCompany, dll.
5. Target: Attrition (0 = tidak keluar, 1 = keluar)

#### ✅ Langkah-langkah Proyek
1. Data Understanding & Exploratory Data Analysis (EDA):
    Dalam tahap Data Understanding dan Exploratory Data Analysis (EDA), fokus utama adalah memperoleh pemahaman mendalam tentang data, dimulai dengan menganalisis distribusi setiap variabel. Proses ini juga melibatkan penanganan missing values dan outlier untuk memastikan kualitas dan kebersihan data, serta melakukan visualisasi awal guna mengidentifikasi pola-pola yang berpotensi memiliki pengaruh terhadap tingkat attrition.
2. Preprocessing Data:
    Tahapan preprocessing data krusial dilakukan dengan mengawali proses encoding variabel kategorikal, diikuti dengan standarisasi data numerik untuk memastikan skala yang seragam. Selanjutnya, dilakukan penyeimbangan kelas untuk mengatasi potensi imbalance data, sebelum akhirnya data dibagi menjadi set pelatihan dan pengujian untuk analisis lebih lanjut.
3. Pembuatan Model Prediksi:
    Dalam upaya membangun model prediksi, akan diimplementasikan algoritma klasifikasi XGBoost, kemudian mengevaluasi akurasi model secara komprehensif menggunakan metrik-metrik standar seperti precision, recall, F1-score, dan ROC AUC.
4. Pembuatan Dashboard Bisnis (Looker Studio):
    Dalam inisiatif ini, telah dilakukan pembuatan dashboard bisnis menggunakan Looker Studio untuk memvisualisasikan data kunci terkait distribusi attrition dan faktor-faktor yang memengaruhinya. 

**CATATAN: Tidak menggunakan Metabase dalam projek ini, sehingga tidak ada metabase.db.mv.db**

---

### Persiapan

#### ✅ Sumber data:

Sumber data yang digunakan berasal dari repository GitHub Dicoding Academy, yaitu `https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee`, dengan nama file `employee_data.csv`. Dataset ini berisi detail demografi karyawan, metrik terkait pekerjaan, dan penanda attrition.

Berikut adalah deskripsi fitur-fitur yang terdapat dalam dataset:
- `EmployeeId`: Pengidentifikasi karyawan.
- `Attrition`: Apakah karyawan mengalami attrition atau pengunduran diri? (0=tidak, 1=ya).
- `Age`: Usia karyawan.
- `BusinessTravel`: Komitmen perjalanan untuk pekerjaan.
- `DailyRate`: Gaji harian.
- `Department`: Departemen karyawan.
- `DistanceFromHome`: Jarak dari tempat kerja ke rumah (dalam km).
- `Education`: Tingkat pendidikan (1=Di Bawah Perguruan Tinggi, 2=Perguruan Tinggi, 3=Sarjana, 4=Master, 5=Doktor).
- `EducationField`: Bidang pendidikan.
- `EnvironmentSatisfaction`: Tingkat kepuasan terhadap lingkungan kerja (1=Rendah, 2=Sedang, 3=Tinggi, 4=Sangat Tinggi).
- `Gender`: Jenis kelamin karyawan.
- `HourlyRate`: Gaji per jam.
- `JobInvolvement`: Tingkat keterlibatan dalam pekerjaan (1=Rendah, 2=Sedang, 3=Tinggi, 4=Sangat Tinggi).
- `JobLevel`: Tingkat pekerjaan (1 sampai 5).
- `JobRole`: Peran pekerjaan.
- `JobSatisfaction`: Tingkat kepuasan kerja (1=Rendah, 2=Sedang, 3=Tinggi, 4=Sangat Tinggi).
- `MaritalStatus`: Status perkawinan.
- `MonthlyIncome`: Gaji bulanan.
- `MonthlyRate`: Tarif bulanan.
- `NumCompaniesWorked`: Jumlah perusahaan tempat pernah bekerja.
- `Over18`: Berusia di atas 18 tahun?
- `OverTime`: Lembur?
- `PercentSalaryHike`: Persentase kenaikan gaji tahun lalu.
- `PerformanceRating`: Peringkat kinerja (1=Rendah, 2=Baik, 3=Sangat Baik, 4=Luar Biasa).
- `RelationshipSatisfaction`: Tingkat kepuasan dalam hubungan (1=Rendah, 2=Sedang, 3=Tinggi, 4=Sangat Tinggi).
- `StandardHours`: Jam kerja standar.
- `StockOptionLevel`: Tingkat opsi saham.
- `TotalWorkingYears`: Total tahun bekerja.
- `TrainingTimesLastYear`: Jumlah pelatihan yang diikuti tahun lalu.
WorkLifeBalance: Keseimbangan kehidupan kerja (1=Rendah, 2=Baik, 3=Sangat Baik, 4=Luar Biasa).
- `YearsAtCompany`: Jumlah tahun di perusahaan.
- `YearsInCurrentRole`: Jumlah tahun dalam peran saat ini.
- `YearsSinceLastPromotion`: Jumlah tahun sejak promosi terakhir.
- `YearsWithCurrManager`: Jumlah tahun dengan manajer saat ini.

#### ✅ Setup environment:

Dengan Menggunakan Anaconda
```
# Ke folder proyek
cd C:\Users\Windows 10\Studpen_DataSains

# Buat environment baru
conda create -n attrition-env python=3.9

# Aktifkan environment
conda activate attrition-env

# Install library dari requirements.txt
pip install -r requirements.txt

# Jalankan jupyter notebook
pip install notebook
jupyter notebook
```

---

## Business Dashboard

Dashboard bisnis dibuat dengan Looker Studio untuk memvisualisasikan dan menganalisis secara mendalam fenomena attrition karyawan. Dashboard ini menyajikan beberapa perspektif kunci, termasuk distribusi attrition secara keseluruhan, dampak lembur terhadap tingkat pengunduran diri, hubungan antara kepuasan kerja dan attrition, rentang usia dominan karyawan yang mengundurkan diri, serta pengaruh tingkat pendidikan terhadap keputusan pengunduran diri. Tampilan visual yang jelas dan ringkas ini memungkinkan pemangku kepentingan untuk dengan cepat mengidentifikasi pola dan faktor-faktor yang berkontribusi pada attrition karyawan di Jaya Jaya Maju. Akses dashboard dapat melalui tautan berikut:[Dashboard](https://lookerstudio.google.com/reporting/6d8b83ea-9f95-4b11-b2f5-6f836737f4fb)

---

## Conclusion

![Visualisasi Dashboard]("TampilanDashboard.png")
Berdasarkan visualisasi pada dashboard yang telah dibuat, dapat disimpulkan beberapa temuan kunci terkait attrition karyawan. Mayoritas karyawan (sekitar 59.8%) tidak mengalami pengunduran diri, namun terdapat persentase signifikan sekitar 40% yang menunjukkan adanya attrition. Analisis menunjukkan bahwa lembur memiliki dampak yang relatif kecil terhadap keputusan resign dibandingkan faktor lainnya. Terdapat indikasi bahwa semakin rendah tingkat kepuasan kerja, semakin tinggi potensi attrition. Selain itu, rentang usia 30-an (terutama 35-36 tahun) menunjukkan angka pengunduran diri tertinggi, dan karyawan dengan tingkat pendidikan menengah (level 3 dan 4) lebih sering terlibat dalam keputusan resign dibandingkan dengan mereka yang berpendidikan sangat rendah atau sangat tinggi.

![Korelasi Fitur dengan Attrition](https://github.com/salsarzkm/Sub1_DataSains/blob/main/CorrelationOfFeaturesWithAttrition.png)
Namun, berdasarkan hasil analisis korelasi fitur dengan attrition yang dilakukan selama tahap Eksplorasi Data (EDA), dapat disimpulkan bahwa faktor-faktor yang berkaitan dengan pengalaman, stabilitas kerja, dan kompensasi finansial memiliki korelasi negatif yang paling signifikan dengan tingkat pengunduran diri karyawan. Secara spesifik, karyawan dengan TotalWorkingYears yang lebih tinggi, Age yang lebih matang, MonthlyIncome yang lebih besar, StockOptionLevel yang lebih tinggi, serta YearsInCurrentRole dan YearsWithCurrManager yang lebih lama, menunjukkan kemungkinan attrition yang lebih rendah. Sementara itu, fitur-fitur seperti PercentSalaryHike, PerformanceRating, dan HourlyRate menunjukkan korelasi yang sangat lemah atau tidak signifikan dengan attrition, mengindikasikan bahwa pengaruhnya tidak sekuat faktor-faktor utama yang telah disebutkan.

![Heatmap Korelasi](https://github.com/salsarzkm/Sub1_DataSains/blob/main/heatmap.png)
Berdasarkan heatmap korelasi antar fitur numerik yang dihasilkan selama fase Eksplorasi Data (EDA), dapat disimpulkan adanya korelasi positif yang kuat antara beberapa variabel yang mencerminkan jenjang karir, pengalaman, dan pendapatan. Sebagai contoh, MonthlyIncome sangat erat kaitannya dengan JobLevel dan TotalWorkingYears, yang mengindikasikan bahwa semakin tinggi tingkat pekerjaan dan pengalaman kerja, semakin besar pendapatan bulanan karyawan. Demikian pula, YearsAtCompany, YearsInCurrentRole, dan YearsWithCurrManager menunjukkan korelasi positif yang kuat satu sama lain, menunjukkan konsistensi karyawan dalam peran dan manajer mereka seiring dengan lama bekerja di perusahaan. Temuan lain yang signifikan adalah korelasi positif yang kuat antara PercentSalaryHike dan PerformanceRating, menegaskan bahwa kenaikan gaji mayoritas didasarkan pada evaluasi kinerja. Sementara itu, fitur StandardHours menunjukkan korelasi nol dengan semua fitur lain, mengindikasikan bahwa variabel ini kemungkinan merupakan konstanta dan dapat dihapus dari analisis lebih lanjut. Pemahaman terhadap interkorelasi ini penting untuk strategi seleksi fitur dan mitigasi masalah multikolinearitas dalam pembangunan model

![Attrition Rate By Dummy Variabel](https://github.com/salsarzkm/Sub1_DataSains/blob/main/AttritionRateByDummyVariables.png)
Berdasarkan analisis tingkat attrition berdasarkan variabel dummy, dapat disimpulkan bahwa faktor-faktor seperti peran pekerjaan, intensitas kerja, dan status perkawinan memiliki pengaruh signifikan terhadap keputusan karyawan untuk mengundurkan diri. Secara spesifik, karyawan dengan peran Sales Representative menunjukkan tingkat attrition tertinggi, sementara peran manajerial seperti Manager, Research Director, dan Manufacturing Director memiliki tingkat attrition yang sangat rendah. Selain itu, bekerja lembur (OverTime) dan sering melakukan perjalanan bisnis (BusinessTravel_Travel_Frequently) berkorelasi kuat dengan tingkat attrition yang lebih tinggi. Penting juga dicatat bahwa karyawan dengan status perkawinan Single memiliki tingkat attrition yang jauh lebih tinggi dibandingkan dengan mereka yang sudah menikah.

---

### Rekomendasi Action Items (Optional)

Berdasarkan temuan yang telah disampaikan dari dashboard, berikut adalah rekomendasi action item yang dapat dilakukan oleh departemen HR untuk menurunkan tingkat attrition di Jaya Jaya Maju:

1. **Evaluasi dan Perbaiki Beban Kerja pada Peran Tertentu**

   Temuan: Peran dengan tingkat turnover tinggi, yaitu Laboratory Technician, Sales Executive, Research Scientist, dan Sales Representative. Posisi-posisi tersebut meenjadi fokus dalam evaluasi dan perbaikan beban kerja
   
    Action Items:
    - Lakukan job audit dan workload analysis untuk posisi-posisi tersebut.
    - Tinjau ulang job description dan realokasi tugas bila diperlukan.
    - Sediakan dukungan tambahan seperti asisten atau teknologi pendukung.

3. **Kelola Kebijakan Lembur dengan Lebih Baik**

   Temuan: 54.7% dari karyawan yang resign melakukan lembur.
   
    Action Items:
    - Tetapkan batas maksimal lembur yang lebih ketat.
    - Wajibkan kompensasi lembur baik secara finansial maupun waktu cuti tambahan (compensatory time-off).
    - Lakukan survei rutin mengenai persepsi terhadap beban kerja dan lembur.
    
5. **Tingkatkan Retensi pada Karyawan Pendidikan Menengah**

   Temuan: Pendidikan level 3 (42.5%) dan 4 (24.6%) mendominasi pengunduran diri.
   
    Action Items:
    - Sediakan jalur karier dan program pelatihan profesional yang jelas.
    - Dorong pengembangan keterampilan
    - Buat program mentoring untuk jenjang pendidikan menengah agar merasa dihargai dan punya prospek.

7. **Fokus pada Usia Rentan Mengundurkan Diri (29–33 Tahun)**

   Temuan: Mayoritas pengunduran diri terjadi pada usia awal 30-an.
   
    Action Items:
    - Lakukan stay interview dan mentoring untuk kelompok usia ini.

9. **Tingkatkan Kepuasan Kerja Terutama bagi Karyawan yang Lembur**

   Temuan: Karyawan yang lembur cenderung memiliki kepuasan kerja rendah (tingkat 1 dan 2).
   
    Action Items:
    - Evaluasi faktor-faktor yang menyebabkan rendahnya kepuasan kerja pada karyawan lembur (misalnya gaji, manajemen, workload, pengakuan).
    
