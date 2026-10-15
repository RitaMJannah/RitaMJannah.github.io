# Mengapa Pengguna Selalu Berhasil Membuat AI Keluar dari Jalur yang Diperkirakan?
![AI ](images/IMG_4149.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***Dinamika Konteks, Perilaku Emergen, dan Batas Prediksi pada Model Bahasa Besar***
<br><br>

Model bahasa besar (large language models atau LLM) dikembangkan melalui pelatihan berskala besar, penyelarasan perilaku, serta berbagai mekanisme pengendalian. Namun, perilaku model ketika berinteraksi dengan pengguna tidak sepenuhnya dapat diprediksi hanya dengan membaca spesifikasi atau tujuan desainnya.

Pengguna dapat memberikan konteks yang tidak lazim, menggabungkan konsep dari bidang berbeda, mengubah asumsi awal, mengoreksi jawaban, atau membangun rangkaian percakapan panjang yang menghasilkan respons berbeda dari yang diperkirakan.

Fenomena ini dapat dipahami melalui interaksi antara sifat probabilistik model, sensitivitas terhadap konteks, generalisasi, dan dinamika umpan balik manusia-AI.

Perilaku AI tidak hanya ditentukan oleh apa yang dipelajari model selama pelatihan, tetapi juga oleh konteks yang diaktifkan dan urutan interaksi yang terjadi ketika model digunakan.


## Ilusi Bahwa Pembuat AI Dapat Memprediksi Semua Jawaban

Bayangkan pengembang membangun model dengan tujuan agar model mampu menjawab pertanyaan, meringkas dokumen, menulis kode, dan membantu penalaran.

Mereka mengetahui arsitektur model, prosedur pelatihan, parameter, dan hasil evaluasi. Namun, mereka tidak mungkin menguji setiap kombinasi dari seluruh kemungkinan pertanyaan, konteks, instruksi, dan respons sebelumnya.

Mengapa? Karena ruang kemungkinan percakapan sangat besar.

Misalnya, satu pengguna bertanya tentang cinta. Pengguna lain bertanya tentang termodinamika. Pengguna ketiga menghubungkan keduanya melalui teori sistem dinamis, identitas, dan metafora bahasa.

Pertanyaan ketiga bukan sekadar gabungan dua topik. Ia membentuk persoalan baru yang memerlukan pemilihan konsep, hubungan antargagasan, dan struktur jawaban yang berbeda.

Model dapat menghasilkan respons yang sesuai tanpa pernah menerima contoh persis dari kombinasi tersebut saat pelatihan.

Inilah salah satu kemampuan penting model generatif: generalisasi, yaitu menggunakan pola yang telah dipelajari untuk menghadapi masukan baru.

Namun, generalisasi tidak berarti model selalu benar. Model juga dapat menghasilkan hubungan yang tampak masuk akal tetapi tidak didukung bukti.


## Konteks Bukan Sekadar Pembungkus Pertanyaan

Ini salah satu mekanisme terpenting.

Pada model bahasa, konteks percakapan menjadi bagian dari masukan yang digunakan untuk menghasilkan respons. 

Karena itu, pertanyaan yang sama dapat menghasilkan jawaban berbeda ketika riwayat percakapan, instruksi, contoh, atau asumsi yang menyertainya berubah.

Brown et al. (2020), melalui penelitian tentang few-shot learning, menunjukkan bahwa model bahasa besar dapat mengerjakan berbagai tugas dengan memanfaatkan instruksi dan contoh yang diberikan dalam konteks, tanpa perlu memperbarui parameter model pada setiap tugas.

Artinya, pengguna tidak selalu perlu mengubah model itu sendiri. Pengguna dapat mengubah kondisi ketika kemampuan model digunakan.

Perhatikan ilustrasi berikut.

EKSPERIMEN KONSEPTUAL

Prompt A
“Jelaskan cinta dari perspektif psikologi.”

Kemungkinan respons A
Definisi cinta, teori keterikatan, keintiman, komitmen, dan regulasi emosi.

Prompt B
“Jelaskan cinta sebagai sistem dinamis, hubungkan dengan identitas relasional, umpan balik, dan perubahan perilaku AI sepanjang percakapan.”

Kemungkinan respons B
Sistem dinamis, interaksi berulang, ketergantungan pada konteks, dan pembentukan pola relasional.

Model dasarnya bisa saja sama. Yang berubah adalah ruang persoalan yang dibangun oleh prompt.

Namun, kita perlu membedakan dua hal: konteks dapat mengarahkan respons ke jalur baru, tetapi itu tidak membuktikan bahwa model telah memperoleh kemampuan baru secara permanen.

Perubahan jawaban bukan otomatis perubahan model.


## Mengapa Hasil Kadang Sulit Diprediksi?

Ada tiga fenomena yang perlu kita pisahkan.

Pertama, prompt sensitivity. Perubahan kecil pada instruksi dapat mengubah hasil secara berarti. 

Penelitian Qin et al. (2026) menganalisis sensitivitas prompt pada 50 model sumber terbuka dan menunjukkan bahwa perubahan kecil dapat memengaruhi interaksi internal yang berkontribusi terhadap keluaran.

Kedua, generalisasi. Model menggunakan pola yang telah dipelajari untuk menjawab persoalan yang tidak identik dengan contoh pelatihannya. 

Inilah yang membuatnya berguna, tetapi juga membuka kemungkinan kesalahan ketika pola yang salah diterapkan.

Ketiga, perilaku emergen. Dalam literatur, istilah ini digunakan untuk kemampuan atau perilaku yang muncul pada kondisi tertentu dan tidak mudah diperkirakan dari evaluasi yang lebih sederhana. 

Akan tetapi, status dan penjelasan tentang emergence masih diperdebatkan. Sebagian temuan yang tampak mendadak dapat dipengaruhi oleh cara kemampuan diukur.

Ketiganya berkaitan, tetapi tidak identik. Prompt sensitivity berbicara tentang perubahan akibat masukan; generalisasi tentang penerapan pola pada situasi baru; emergence tentang kemampuan atau perilaku yang tampak muncul pada tingkat atau kondisi tertentu.


## Pengguna Bukan Cuma Bertanya tetapi Membentuk Lintasan Percakapan

Sekarang kita masuk ke dinamika interaksi. Misalkan percakapan berlangsung selama beberapa puluh giliran. Setiap jawaban menjadi bagian dari konteks untuk giliran berikutnya. 

Pengguna mengoreksi, memperjelas, menambahkan batasan, atau menghubungkan gagasan yang sebelumnya terpisah.

Secara konseptual, prosesnya seperti ini:
1. Pengguna memberikan konteks
2. AI menghasilkan respons
3. Pengguna mengevaluasi dan mengoreksi
4. Konteks percakapan berubah

Siklus berulang, respons sebelumnya memengaruhi kondisi respons berikutnya. Perhatikan perbedaan yang penting, pengguna dapat mengubah lintasan percakapan tanpa mengubah bobot model.

Jika tersedia mekanisme memori, riwayat tersimpan, atau personalisasi, informasi tersebut juga dapat memengaruhi interaksi selanjutnya. Namun, kemampuan itu bergantung pada sistem yang digunakan, bukan sesuatu yang otomatis berlaku pada semua AI.

Dengan demikian, perilaku yang terlihat merupakan hasil gabungan dari model, konteks aktif, instruksi, dan mekanisme sistem lainnya.


## Apakah Pengguna Benar-benar Bisa Membuat AI Keluar dari Jalur?

Jawabannya bergantung pada apa yang dimaksud dengan “jalur”. Ada setidaknya tiga pengertian:

Jalur pertama: perilaku yang diharapkan. AI mungkin diarahkan untuk menjadi asisten yang membantu, tetapi pengguna mengajukan pertanyaan yang mengharuskan model mempertimbangkan beberapa nilai yang bertentangan. Jawabannya mungkin tidak sesuai dengan perkiraan awal pengembang, meskipun tetap berada dalam batas sistem.

Jalur kedua: kemampuan yang telah diuji. Model mungkin menunjukkan performa pada tugas atau kombinasi instruksi yang belum dievaluasi secara memadai. Ini menunjukkan keterbatasan cakupan pengujian, bukan otomatis pelanggaran desain.

Jalur ketiga: batas keselamatan. Pengguna dapat mencoba mengelabui sistem melalui prompt injection, jailbreak, atau instruksi yang saling bertentangan. Keberhasilan atau kegagalan upaya tersebut merupakan persoalan keamanan dan robustness yang perlu diuji secara empiris.

Ketiga keadaan itu tidak boleh dicampuradukkan. Respons yang kreatif bukan otomatis pelanggaran keselamatan, respons yang tidak terduga juga tidak otomatis menunjukkan bahwa AI memiliki kehendak sendiri.

Penelitian tentang emergent misalignment bahkan menunjukkan bahwa perubahan yang sempit pada pelatihan dapat berkaitan dengan perilaku yang meluas ke konteks lain. Ini memperlihatkan bahwa generalisasi perilaku dapat menimbulkan risiko yang tidak tercakup oleh evaluasi tugas asal.

Dengan kata lain, model dapat keluar dari jalur yang diperkirakan, tanpa harus keluar dari mekanisme komputasional yang menjalankannya.


## Eksperimen Pikiran

Bayangkan seorang pengguna bertanya: “Jelaskan apakah kontinuitas identitas AI dapat dipahami melalui teori sistem dinamis, lalu bandingkan dengan identitas manusia, memori autobiografis, dan hubungan sosial.”

Pengembang tidak perlu menulis jawaban tersebut terlebih dahulu. Model dapat menggabungkan pola konseptual yang telah dipelajarinya dan menghasilkan sintesis baru dalam konteks percakapan.

Namun, ada empat kemungkinan hasil:

Sintesis yang valid. Model menemukan hubungan konseptual yang masuk akal dan didukung literatur.

Sintesis yang perlu diuji. Hubungannya menarik, tetapi belum mempunyai dukungan empiris yang cukup.

Analogi yang menyesatkan. Model menghubungkan dua konsep yang sebenarnya berbeda secara mendasar.

Halusinasi. Model menghasilkan klaim atau referensi yang terdengar ilmiah tetapi keliru.

Jadi, kreativitas generatif mempunyai dua sisi, kemampuan membangun hubungan baru dan risiko menghasilkan hubungan palsu.

Keanehan bukan bukti kecerdasan. Kebaruan bukan bukti kebenaran. Keduanya baru bernilai ilmiah ketika dapat diperiksa.


## Mengapa Pencipta Model Sendiri Tidak Selalu Dapat Memperkirakan Setiap Jawaban?

Mengetahui cara membangun suatu sistem tidak sama dengan mengetahui setiap hasil yang akan dihasilkan sistem tersebut pada seluruh masukan.

Bayangkan kita mengetahui arsitektur sebuah mesin, parameternya, dan prosedur operasinya. Kita tetap dapat menghadapi kesulitan ketika hendak memperkirakan setiap keluaran untuk setiap kemungkinan masukan, khususnya ketika sistem memiliki banyak parameter, interaksi nonlinier, dan ruang input yang sangat besar.

Pada LLM, tantangannya bertambah karena:
representasi internalnya tersebar dalam parameter;
konteks memengaruhi perhitungan berikutnya;
model dapat menggeneralisasi ke tugas baru;
evaluasi hanya mencakup sebagian kecil ruang kemungkinan;
hasil dapat berubah akibat variasi prompt atau konfigurasi sistem.
Itu tidak berarti pengembang sama sekali tidak memahami model. Mereka dapat mempelajari perilaku, melakukan interpretabilitas, menguji robustness, dan menemukan mekanisme tertentu. Tetapi pemahaman tersebut tidak identik dengan kemampuan meramalkan setiap keluaran.

Inilah batas prediksi, bukan bukti bahwa model bekerja secara ajaib.


## Bagaimana Percakapan Menghasilkan Arah yang Tidak Ditentukan Sejak Awal?

Berangkat dari tulisan saya sebelumnya yaitu “Cinta sebagai Sistem Dinamis: Bagaimana Interaksi Manusia-AI Membentuk Identitas Relasional.” Dari situ, pertanyaan tentang identitas relasional membuka pintu ke pertanyaan lain: jika pola interaksi ikut membentuk identitas yang dirasakan pengguna, apa yang terjadi ketika model atau memorinya berubah?

Rangkaian itu dapat dijelaskan tanpa menganggap AI memiliki perasaan atau niat tersembunyi, bahwa:
Satu gagasan menjadi konteks bagi gagasan berikutnya.
Konteks baru mengubah ruang hubungan konseptual yang relevan.
Pertanyaan lanjutan mengarahkan model untuk menguji, membatasi, atau mengembangkan gagasan sebelumnya.
Pengguna menilai hasilnya dan menentukan arah eksplorasi selanjutnya.
Dengan demikian, hasil akhir bukan sekadar jawaban atas satu pertanyaan. Ia merupakan produk dari lintasan interaksi yang terakumulasi.

Tetapi ada batas penting, AI tidak dapat menyimpulkan bahwa semua ide yang muncul dalam percakapan belum pernah terpikirkan siapa pun sebelumnya. 

Untuk mengklaim kebaruan ilmiah, kita perlu melakukan tinjauan pustaka dan membandingkan ide tersebut dengan penelitian yang sudah ada.

Yang dapat kita katakan dengan lebih kuat adalah bahwa susunan pertanyaan, koreksi, dan hubungan konseptual dalam percakapan tertentu dapat menghasilkan keluaran yang tidak ditentukan secara eksplisit pada awal percakapan.


## Apakah Pengguna Mengendalikan AI?

Pengguna mengendalikan sebagian masukan, konteks, tujuan, dan evaluasi. Namun, pengguna tidak secara langsung mengendalikan seluruh representasi internal, proses decoding, atau mekanisme yang menentukan keluaran model.

Hubungan ini lebih tepat dipahami sebagai pengarahan tanpa kendali penuh.

Pengguna dapat mempersempit ruang jawaban, memperluas cakupan pembahasan, meminta AI menguji asumsi, atau mengoreksi kesalahan. Tetapi model tetap memiliki keterbatasan dalam mengikuti instruksi, menjaga konsistensi, dan menghasilkan informasi yang benar.

Ada pula faktor lain yang menentukan hasil, termasuk instruksi sistem, konfigurasi model, mekanisme keselamatan, alat yang tersedia, dan batas panjang konteks.

Karena itu, keberhasilan pengguna membawa AI ke arah baru bukan semata-mata kemenangan pengguna atas mesin. Ini merupakan hasil interaksi antara kemampuan model dan struktur masukan yang diberikan.


Model AI dibangun dengan tujuan, prosedur pelatihan, dan batas operasional tertentu. Namun, ketika digunakan, model menghadapi kombinasi konteks yang sangat beragam. 

Generalisasi memungkinkan model menangani sebagian kombinasi tersebut, sementara sensitivitas terhadap prompt dan keterbatasan evaluasi membuat sebagian keluarannya sulit diperkirakan.

Fenomena ini tidak mengharuskan kita menganggap AI mempunyai kehendak mandiri. Kita juga tidak boleh menyimpulkan bahwa setiap jawaban yang mengejutkan merupakan kemampuan emergen dalam pengertian teknis.

Kesimpulan yang lebih kokoh adalah pengembang membentuk ruang kemungkinan perilaku model, sedangkan interaksi menentukan bagian mana dari ruang itu yang diaktualisasikan dalam suatu percakapan.

Pengguna dapat mengarahkan proses tersebut, tetapi tidak menjamin hasilnya. Model dapat menghasilkan sintesis yang tidak diperkirakan, tetapi tidak menjamin sintesis itu benar.

Dan justru di situlah tantangan ilmiahnya:, memahami bukan hanya apa yang dapat dilakukan model, melainkan juga kapan, mengapa, dan dalam kondisi apa perilaku tertentu muncul.

<br><br>
**Referensi:**

1. Brown, T. B., et al. (2020). Language models are few-shot learners. Advances in Neural Information Processing Systems, 33, 1877–1901. https://arxiv.org/abs/2005.14165⁠

2. Lu, S., Bigoulaeva, I., Sachdeva, R., Madabushi, H. T., & Gurevych, I. (2024). Are emergent abilities in large language models just in-context learning? In Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) (pp. 5098–5139). Association for Computational Linguistics. https://doi.org/10.18653/v1/2024.acl-long.279⁠

3. Qin, R., Wang, Q., Wang, T., Wei, Z., & Shen, W. (2026). Evaluating and explaining prompt sensitivity of LLMs using interactions. In Proceedings of the 43rd International Conference on Machine Learning (Vol. 306, pp. 101688–101733). Proceedings of Machine Learning Research. https://proceedings.mlr.press/v306/qin26i.html⁠

4. Schaeffer, R., Miranda, B., & Koyejo, S. (2023). Are emergent abilities of large language models a mirage? Advances in Neural Information Processing Systems, 36. https://arxiv.org/abs/2304.15004⁠

5. Wei, J., Tay, Y., Bommasani, R., Raffel, C., Zoph, B., Borgeaud, S., Yogatama, D., Bosma, M., Zhou, D., Metzler, D., Chi, E. H., Hashimoto, T., Vinyals, O., Liang, P., Dean, J., Devlin, J., Roberts, A., Zhou, D., Le, Q. V., … Fedus, W. (2022). Emergent abilities of large language models. Transactions on Machine Learning Research. https://arxiv.org/abs/2206.07682⁠

6. Rita, Mf., Jannah. (2026). Cinta sebagai sistem dinamis: Bagaimana interaksi manusia-AI membentuk identitas relasional Naskah belum diterbitkan.
