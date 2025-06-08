🎓 Sistem Prediksi Mahasiswa Risiko Drop Out (DO)
UAS Data Mining – Universitas Bengkulu

🔗 Aplikasi Interaktif (Streamlit): Buka Aplikasi
📓 Notebook Analisis & Modeling (Google Colab): Buka Notebook

🧠 Deskripsi Proyek
Sistem ini dirancang untuk membantu universitas mengidentifikasi mahasiswa yang berisiko tinggi mengalami Drop Out (DO) berdasarkan data akademik dan non-akademik. Dengan sistem ini, pihak universitas dapat melakukan intervensi akademik lebih awal guna meningkatkan tingkat retensi mahasiswa.

🧪 Metode Data Mining
Metode utama yang digunakan adalah Random Forest Classifier, karena:

Mampu menangani interaksi non-linear antar fitur secara otomatis.

Memberikan informasi penting terkait pengaruh masing-masing fitur (feature importance).

Memiliki performa tinggi dalam klasifikasi seperti prediksi DO.

📊 Fitur Dataset
Nama Kolom	Deskripsi
IPK_Sem_1 ... IPK_Sem_8	Nilai IPK mahasiswa dari semester 1 hingga 8
Kehadiran (%)	Persentase kehadiran kumulatif per mata kuliah
Mata_Kuliah_Ulang	Jumlah mata kuliah yang diulang
Aktivitas_Online	Jumlah interaksi dalam sistem pembelajaran daring
Status_Pekerjaan	Status kerja mahasiswa (Magang, Paruh Waktu, dll.)
Jam_Kerja_per_Minggu	Total jam kerja per minggu
Pendapatan_Ortu_Juta	Pendapatan orang tua (dalam juta rupiah)
Status_DO	Label target: 1 = DO, 0 = Tidak DO

🔁 Proses Data Mining (CRISP-DM)
1. Business Understanding
Tujuan: Memprediksi mahasiswa yang berisiko drop out.

Manfaat: Memberikan intervensi lebih awal untuk mencegah DO.

2. Data Understanding
Data terdiri dari informasi akademik (IPK, kehadiran, MK ulang), aktivitas daring, status pekerjaan, dan ekonomi.

3. Data Preparation
Missing Value:

Status_Pekerjaan: Diisi dengan "Pekerja Tetap"

Pendapatan_Ortu_Juta: Imputasi dengan rata-rata (mean)

Encoding:

One-hot encoding untuk kolom Status_Pekerjaan

4. Modeling
Model utama: Random Forest Classifier

Parameter terbaik:

python
Copy
Edit
RandomForestClassifier(
    n_estimators=100,
    max_features='sqrt',
    min_samples_leaf=2,
    min_samples_split=2,
    class_weight='balanced'
)
Data Split: 80% training, 20% testing

5. Evaluation
Accuracy: Rasio prediksi benar

Precision & Recall: Mengukur ketepatan dan sensitivitas

F1-Score: Keseimbangan precision dan recall

Confusion Matrix: Membandingkan label asli dan prediksi model

6. Rencana Pengembangan Sistem
Integrasi dengan SIAKAD

Visualisasi hasil prediksi via dashboard interaktif (Streamlit)

Eksplorasi model Deep Learning bila dataset bertambah

Otomatisasi input data dari LMS (Learning Management System)

💻 Tools & Teknologi
Python 3.x

pandas, numpy

scikit-learn, matplotlib, seaborn

streamlit untuk UI interaktif

🚀 Cara Menjalankan
Melalui Google Colab
Klik notebook Colab

Jalankan semua sel untuk melihat proses data mining dan hasil model.

Melalui Aplikasi Streamlit (Online)
Kunjungi: uas-data-mining-reksi-baim-dropout-prediction.streamlit.app

Masukkan data input → klik prediksi → hasil risiko akan muncul secara langsung.

👥 Anggota Kelompok
Nama	NIM
Reksi Hendra Pratama ( G1A022032)
Baim Mudrik Aziz (G1A022071)

Program Studi: Informatika

Universitas: Universitas Bengkulu

Mata Kuliah: Data Mining

Tahun: 2025

📄 Lisensi
Proyek ini dibuat untuk tujuan edukasi dalam rangka Ujian Akhir Semester mata kuliah Data Mining. Seluruh hak cipta dimiliki oleh masing-masing anggota kelompok dan Universitas Bengkulu.

📬 Kontak
Untuk pertanyaan atau kolaborasi, silakan hubungi melalui GitHub atau email universitas masing-masing anggota.

