# Submission 1: Real / Fake Job Posting Prediction

Nama: Cintha Hafrida Putri

Username dicoding: cintha_bang

| | **Deskripsi** |
| ----------- | ----------- |
| **Dataset** | [Real/Fake Job Posting Prediction](https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fshivamb%2Freal-or-fake-fake-jobposting-prediction)|
| **Masalah** |Penipuan lowongan pekerjaan telah menjadi masalah serius di era digital, dengan banyak individu tertipu oleh iklan pekerjaan palsu yang bertujuan mencuri informasi pribadi atau melakukan penipuan keuangan. Hal ini sangat berisiko bagi pencari kerja yang tidak berpengalaman. Seiring bertambahnya volume data digital, termasuk iklan pekerjaan di berbagai platform, metode verifikasi manual menjadi tidak efektif. Oleh karena itu, diperlukan metode yang efisien untuk memfilter informasi kredibel dan melindungi pengguna dari risiko penipuan online.|
| **Solusi machine learning** | Solusi ini menggunakan model klasifikasi untuk memprediksi keaslian iklan pekerjaan berdasarkan teks deskriptif dan fitur lain dalam postingan. Model dibuat dengan pipeline TFX untuk memproses data, melatih model, dan menyiapkan deployment. |
| **Metode pengolahan** | Proses pengolahan data meliputi penggabungan teks dari beberapa kolom menjadi satu, tokenisasi kata, penghapusan stop words menggunakan pustaka NLTK, dan lemmatization untuk mengonversi kata-kata ke bentuk dasar. Kolom yang tidak diperlukan seperti `job_id`, `telecommuting`, `has_questions`, `has_company_logo`, dan `salary_range` dihapus untuk menyederhanakan data. |
| **Arsitektur model** |Model ini dikembangkan menggunakan pipeline TFX (TensorFlow Extended) yang terdiri dari beberapa komponen utama. Pertama, komponen CsvExampleGen digunakan untuk mengimpor data dari file CSV ke dalam pipeline. Komponen ini mengkonversi data mentah menjadi format yang dapat diproses oleh TFX, sehingga data tersedia untuk analisis dan pemodelan lebih lanjut. Setelah data diimpor, komponen StatisticsGen digunakan untuk menghasilkan analisis statistik dari dataset. Komponen ini memberikan gambaran umum tentang distribusi dan karakteristik data, seperti mean, median, dan frekuensi nilai, yang membantu dalam memahami kualitas dan sifat data. Selanjutnya, SchemaGen berfungsi untuk menghasilkan skema data berdasarkan analisis statistik yang telah dilakukan. Skema ini mendefinisikan tipe dan struktur data yang diharapkan, termasuk validasi terhadap tipe data dan nilai yang mungkin. Dengan skema ini, proses validasi data dapat dilakukan dengan lebih efektif melalui komponen ExampleValidator. Komponen ini melakukan validasi terhadap data dengan membandingkan data yang ada dengan skema yang telah dihasilkan sebelumnya, memastikan bahwa data memenuhi kriteria yang telah ditetapkan, sehingga dapat menghindari masalah yang mungkin timbul akibat data yang tidak konsisten atau tidak valid. Setelah proses validasi, komponen Transform digunakan untuk preprocessing data, termasuk normalisasi, encoding, dan pengubahan format. Di sini, teknik-teknik transformasi diterapkan untuk mempersiapkan data agar sesuai dengan kebutuhan model, termasuk teknik seperti scaling dan augmentasi data. Terakhir, setelah data diproses, komponen Trainer bertanggung jawab untuk melatih model. Model ini menggunakan jaringan saraf sederhana sebagai arsitektur dasarnya untuk klasifikasi. Parameter yang digunakan dalam model ini, seperti jumlah layer, ukuran neuron per layer, dan fungsi aktivasi, dapat disesuaikan untuk mencapai performa yang optimal.|
| **Metrik evaluasi** | Evaluasi model dilakukan dengan metrik akurasi, presisi, recall, dan F1-score. Hasil evaluasi menunjukkan bahwa model memiliki **akurasi sekitar 85%**, yang menunjukkan model dapat memprediksi dengan baik antara iklan asli dan palsu. |
| **Performa model** | Model mencapai akurasi sebesar 85% pada dataset uji. Nilai ini menunjukkan kemampuan model dalam mengklasifikasikan iklan pekerjaan dengan cukup akurat, dan performa yang baik pada seluruh metrik evaluasi mengindikasikan bahwa model mampu mengenali pola iklan palsu dengan efektif. | 
