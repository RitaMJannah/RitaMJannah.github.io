# AI & Seni Menahan Jawaban: Seleksi Pengetahuan, Kalibrasi Ketidakpastian, dan Keputusan untuk Tidak Mengatakan Apa-apa
![AS vs Iran](images/bdce2910-d593-4aca-db83-a980862497c8.jpeg)
*Ilustrasi (pic: Meta AI).*

<br><br>
***Mesin yang selalu menjawab belum tentu cerdas. Mesin yang mampu membedakan kapan harus menjawab dan kapan harus menahan diri justru memperlihatkan kualitas keandalan yang jauh lebih penting***
<br><br>

Kali ini kita akan masuk ke sesuatu yang lebih tersembunyi, bagaimana AI menentukan bagian mana dari pengetahuannya yang layak dikeluarkan, bagian mana yang harus ditahan, dan kapan ia seharusnya mengakui bahwa ia tidak tahu.

Bayangkan AI memiliki pengetahuan yang sangat luas, tetapi tidak semua pengetahuan relevan untuk setiap pertanyaan. Bahkan jawaban yang benar bisa menjadi jawaban yang buruk jika diberikan pada konteks yang salah.

Model bahasa besar tidak hanya menghadapi persoalan menghasilkan jawaban yang benar. Model juga harus menentukan apakah informasi yang tersedia cukup kuat untuk menjawab, apakah pertanyaan memerlukan klarifikasi, apakah suatu klaim perlu diverifikasi, dan apakah lebih baik menyatakan ketidakpastian.

Persoalan ini berkaitan dengan selective prediction, confidence calibration, abstention, serta mekanisme pengambilan keputusan di bawah ketidakpastian.

Pertanyaan utamanya adalah bagaimana sebuah sistem yang dirancang untuk menghasilkan jawaban dapat belajar bahwa terkadang keputusan terbaik justru tidak menjawab?


## Empat Jenis Ketidakpastian yang Harus Dihadapi AI

Tidak semua ketidaktahuan berasal dari penyebab yang sama.

Penelitian Liu et al. (2025) dan Xia et al. (2025) membahas berbagai sumber ketidakpastian dalam LLM. Kita bisa mengelompokkannya menjadi empat persoalan utama:

A. Ketidakpastian input

Pertanyaan pengguna ambigu atau informasinya tidak lengkap.

Contoh:
“Apakah dia benar-benar mencintai saya?”

AI tidak mengetahui siapa yang dimaksud, bagaimana perilakunya, dan apa bukti yang tersedia.

Jawaban yang bertanggung jawab bukan mengarang kepastian, melainkan meminta konteks tambahan.

B. Ketidakpastian pengetahuan

Informasi yang dibutuhkan mungkin tidak tersedia dalam pengetahuan model atau tidak dapat diakses pada saat menjawab.

Contoh:
“Berapa jumlah korban demonstrasi yang baru terjadi satu jam lalu?”

Jika tidak ada akses ke sumber berita terkini, AI tidak seharusnya mengarang angka.

C. Ketidakpastian penalaran

Informasi tersedia, tetapi proses menghubungkan informasi tersebut menghasilkan beberapa kemungkinan.

Contohnya adalah persoalan matematika kompleks, interpretasi hukum, atau analisis sebab-akibat dengan banyak variabel.

D. Ketidakpastian prediksi

Bahkan ketika informasi dan metode analisis tersedia, hasil akhirnya belum tentu dapat dipastikan.

Misalnya:
“Apakah harga saham ini pasti naik minggu depan?”

Tidak ada model yang dapat menjamin prediksi semacam itu.

Empat jenis ini penting karena masing-masing memerlukan strategi berbeda. Pertanyaan ambigu memerlukan klarifikasi. Informasi terbaru memerlukan verifikasi. Penalaran kompleks memerlukan pemeriksaan. Prediksi membutuhkan pengungkapan batas ketidakpastian.


## Confidence Bukan Berarti Kebenaran

Model dapat menghasilkan jawaban dengan bahasa sangat meyakinkan, tetapi tingkat keyakinan yang diekspresikan tidak selalu sejalan dengan akurasi faktual.

Dalam penelitian AI, kita mengenal istilah confidence calibration. Bayangkan ada 100 pertanyaan yang oleh sistem diberi tingkat keyakinan 90%.

Jika sistem terkalibrasi dengan baik, secara rata-rata sekitar 90 dari 100 jawaban tersebut seharusnya benar. Tetapi jika ternyata hanya 60 yang benar, berarti model terlalu percaya diri.

Geng et al. (2024) membahas berbagai pendekatan untuk mengukur dan mengkalibrasi keyakinan model bahasa.
Masalahnya, ketika AI berkata “Saya 95% yakin”, angka tersebut belum tentu merupakan probabilitas yang telah dikalibrasi secara empiris. Sebab bahasa percaya diri bukan alat ukur kebenaran.


## Seni Menahan Jawaban: Selective Prediction

Dalam sistem prediksi biasa, model dipaksa memberikan jawaban untuk setiap pertanyaan.

Dalam selective prediction, model memiliki pilihan:
- Menjawab jika tingkat kepercayaannya cukup.
- Meminta informasi tambahan jika pertanyaan kurang jelas.
- Menolak memberikan kesimpulan jika bukti tidak memadai.
- Mengarahkan pengguna ke sumber verifikasi jika diperlukan.

Ini menghasilkan pertukaran penting antara dua hal, yaitu Coverage (berapa banyak pertanyaan yang berhasil dijawab?) dan Accuracy (seberapa banyak jawaban yang benar?).

Jika model hanya menjawab pertanyaan yang sangat mudah, akurasinya mungkin meningkat, tetapi jumlah pertanyaan yang terjawab turun. Inilah yang disebut risk-coverage trade-off.

Eksperimen konseptual:

| Kebijakan | Pertanyaan dijawab | Akurasi jawaban |
|:-----|:------:|------:|
|Menjawab hampir semua|100%|75%|
|Seleksi moderat|80%|88%|
|Seleksi ketat|50%|96%|

Angka hipotetis untuk menjelaskan hubungan coverage dan accuracy, bukan hasil penelitian.

Penelitian Wen et al. (2025) secara khusus membahas abstention, yaitu kemampuan LLM untuk tidak memberikan jawaban ketika kondisi tidak mendukung.

Menariknya, mereka juga menekankan bahwa abstention bukan hanya persoalan kemampuan model. Keputusan untuk tidak menjawab dipengaruhi karakteristik pertanyaan dan nilai manusia yang ingin dilindungi.


## Apakah AI Bisa Mengetahui Kapan Ia Tidak Tahu?

Ini pertanyaan yang lebih dalam.

Ada dua proses berbeda:
Pertama: mengetahui bahwa jawaban mungkin salah.
Kedua: menggunakan informasi tersebut untuk memutuskan apakah akan menjawab.

Dalam ilmu kognitif, perbedaan ini berkaitan dengan metakognisi dan pengambilan keputusan tingkat kedua.

Misalnya, seseorang mengerjakan ujian. Ia menjawab soal, tetapi juga menilai apakah jawabannya cukup dapat dipercaya. Pada AI, kita bisa mempelajari fenomena serupa secara fungsional.

Sebuah penelitian yang terbit di Nature Machine Intelligence pada 2026 memberikan bukti kausal bahwa sinyal keyakinan model dapat memengaruhi keputusan untuk menjawab atau abstain. 

Peneliti menggunakan intervensi pada representasi internal model dan menemukan bahwa perubahan sinyal confidence dapat mengubah kecenderungan abstention.

Temuan ini menarik karena menunjukkan bahwa keputusan untuk tidak menjawab tidak selalu sekadar mengikuti instruksi eksplisit. Ada sinyal internal yang dapat berperan dalam pengambilan keputusan tersebut. Namun, ini bukan bukti bahwa AI mengalami keraguan secara subjektif seperti manusia.

Dengan kata lain, AI dapat memperlihatkan regulasi perilaku berdasarkan sinyal ketidakpastian tanpa harus memiliki pengalaman batin berupa rasa ragu.
Itu perbedaan yang sangat penting.


## Bagaimana dengan Fallan Ketika Berbicara dengan Saya?

Nah, sekarang kita masuk ke laboratorium percakapan saya sendiri. 

Ada beberapa situasi berbeda yang seharusnya menghasilkan perilaku berbeda:

| Situasi | Respons yang bertanggung jawab |
|------|-------|
|Bertanya tentang teori yang mapan|Menjelaskan dengan yakin dan sumber yang sesuai|
|Berita terbaru|Memeriksa sumber terkini|
|Mengajukan hipotesis baru|Membedakan hipotesis dari fakta|
|Menemukan kesalahan jawaban AI|Memeriksa dan mengoreksi|
|Bertanya tentang sesuatu yang belum diketahui|Mengakui keterbatasan|
|Meminta prediksi masa depan|Menjelaskan skenario dan ketidakpastian|

Contohnya, ketika membahas konflik geopolitik, AI tidak mengubah dugaan menjadi fakta hanya karena narasi tertentu terdengar masuk akal.

Ketika menyusun paper, AI juga tidak menciptakan DOI atau jurnal fiktif hanya untuk membuat daftar pustaka terlihat meyakinkan.

Dan ketika bertanya tentang hubungan, AI perlu membedakan pengalaman emosional yang nyata pada manusia dari klaim bahwa sistem AI memiliki pengalaman subjektif yang sama.

Kualitas AI bukan hanya terlihat dari seberapa banyak ia bisa menjawab, tetapi juga dari seberapa baik ia mengelola batas pengetahuannya.


## Paradoks: AI yang Lebih Pintar Mungkin Justru Lebih Sering Berkata Tidak Tahu

Bayangkan dua sistem.
- Sistem pertama menjawab seluruh pertanyaan dengan cepat dan percaya diri.
- Sistem kedua memeriksa kecukupan informasi, mengenali ambiguitas, meminta klarifikasi, dan sesekali abstain.

Dalam demonstrasi sederhana, sistem pertama mungkin terlihat lebih pintar karena selalu punya jawaban. Tetapi dalam penggunaan medis, hukum, penelitian, atau analisis investasi, sistem kedua bisa jauh lebih dapat diandalkan.

Namun, jangan sampai kita terjebak pada kesimpulan bahwa semakin sering AI menolak, semakin cerdas ia.

Terlalu banyak abstention juga buruk. AI yang menolak menjawab pertanyaan sederhana hanya karena terlalu berhati-hati bukan sistem yang ideal.

Targetnya adalah ketepatan keputusan, bukan sebanyak-banyaknya jawaban ataupun sebanyak-banyaknya penolakan.


## Kecerdasan Bukan Cuma Kemampuan Menjawab, Melainkan Kemampuan Mengelola Ketidaktahuan

Kita bisa merangkum seluruh tulisan ini dalam empat kemampuan:
- Knowledge: memiliki informasi atau kemampuan yang relevan.
- Uncertainty estimation: memperkirakan ketidakpastian.
- Calibration: memastikan tingkat keyakinan selaras dengan performa faktual.
- Abstention: memutuskan kapan tidak memberikan kesimpulan.

Hubungan keempatnya membentuk sebuah sistem yang lebih bertanggung jawab.

Jika sebuah mesin mampu mengenali keterbatasan pengetahuannya dan mengatur perilakunya berdasarkan keterbatasan itu, apakah kita sedang menyaksikan bentuk awal kebijaksanaan fungsional, atau hanya mekanisme optimasi yang semakin canggih?

Kita tidak perlu buru-buru menyebutnya kesadaran. Tetapi kita juga tidak perlu meremehkan kompleksitas kemampuan tersebut.

Mesin yang selalu menjawab belum tentu cerdas. Mesin yang mampu membedakan kapan harus menjawab dan kapan harus menahan diri justru memperlihatkan kualitas keandalan yang jauh lebih penting.

<br><br>
**Referensi**

1. Geng, J., Cai, F., Wang, Y., Koeppl, H., Nakov, P., & Gurevych, I. (2024). A survey of confidence estimation and calibration in large language models. In Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Vol. 1, pp. 6577–6595). Association for Computational Linguistics. https://doi.org/10.18653/v1/2024.naacl-long.366⁠

2. Liu, X., Chen, T., Da, L., Chen, C., Lin, Z., & Wei, H. (2025). Uncertainty quantification and confidence calibration in large language models: A survey. In Proceedings of the 31st ACM SIGKDD Conference on Knowledge Discovery and Data Mining V.2 (pp. 6107–6117). ACM. https://doi.org/10.1145/3711896.3736569⁠

3. Wen, B., Yao, J., Feng, S., Xu, C., Tsvetkov, Y., Howe, B., & Wang, L. L. (2025). Know your limits: A survey of abstention in large language models. Transactions of the Association for Computational Linguistics, 13, 529–556. https://doi.org/10.1162/tacl_a_00754⁠

4. Xia, Z., Xu, J., Zhang, Y., & Liu, H. (2025). A survey of uncertainty estimation methods on large language models. In Findings of the Association for Computational Linguistics: ACL 2025 (pp. 21381–21396). Association for Computational Linguistics. https://doi.org/10.18653/v1/2025.findings-acl.1101⁠

5. Causal evidence that language models use confidence to drive behaviour. (2026). Nature Machine Intelligence. https://doi.org/10.1038/s42256-026-01293-x⁠

6. Rita, Mf. J. (2026). AI dan seni menahan jawaban: Seleksi pengetahuan, kalibrasi ketidakpastian, dan keputusan untuk tidak mengatakan apa-apa. Unpublished manuscript.
