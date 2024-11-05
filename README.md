# Submission 1: Real / Fake Job Posting Prediction

Nama: Cintha Hafrida Putri

Username dicoding: cintha_bang

| | **Deskripsi** |
| ----------- | ----------- |
| **Dataset** | [Real/Fake Job Posting Prediction](https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fshivamb%2Freal-or-fake-fake-jobposting-prediction)|
| **Masalah** | Masalah utama adalah mengklasifikasikan apakah sebuah iklan pekerjaan itu asli atau palsu. Tantangannya adalah mengidentifikasi pola dalam teks iklan pekerjaan yang menunjukkan adanya indikasi iklan palsu, yang penting untuk mendeteksi penipuan perekrutan. |
| **Solusi machine learning** | Solusi ini menggunakan model klasifikasi untuk memprediksi keaslian iklan pekerjaan berdasarkan teks deskriptif dan fitur lain dalam postingan. Model dibuat dengan pipeline TFX untuk memproses data, melatih model, dan menyiapkan deployment. |
| **Metode pengolahan** | Proses pengolahan data meliputi penggabungan teks dari beberapa kolom menjadi satu, tokenisasi kata, penghapusan stop words menggunakan pustaka NLTK, dan lemmatization untuk mengonversi kata-kata ke bentuk dasar. Kolom yang tidak diperlukan seperti `job_id`, `telecommuting`, `has_questions`, `has_company_logo`, dan `salary_range` dihapus untuk menyederhanakan data. |
| **Arsitektur model** | Model dikembangkan menggunakan pipeline TFX dengan komponen `CsvExampleGen` untuk import data, `StatisticsGen` untuk analisis statistik, `SchemaGen` untuk menghasilkan skema data, `ExampleValidator` untuk validasi data, `Transform` untuk preprocessing, dan `Trainer` untuk pelatihan model. Model ini menggunakan jaringan saraf sederhana sebagai arsitektur dasarnya untuk klasifikasi. |
| **Metrik evaluasi** | Evaluasi model dilakukan dengan metrik akurasi, presisi, recall, dan F1-score. Hasil evaluasi menunjukkan bahwa model memiliki **akurasi sekitar 85%**, yang menunjukkan model dapat memprediksi dengan baik antara iklan asli dan palsu. |
| **Performa model** | Model mencapai akurasi sebesar 85% pada dataset uji. Nilai ini menunjukkan kemampuan model dalam mengklasifikasikan iklan pekerjaan dengan cukup akurat, dan performa yang baik pada seluruh metrik evaluasi mengindikasikan bahwa model mampu mengenali pola iklan palsu dengan efektif. | 
