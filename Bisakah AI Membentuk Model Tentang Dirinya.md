# Bisakah AI Membentuk Model Tentang Dirinya Sendiri: Self-Modeling, Introspeksi, & Batas Kesadaran Mesin
![AI ](images/IMG_3919.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***AI menunjukkan kapasitas terbatas untuk self-modeling dan introspective access terhadap aspek tertentu dari perilakunya sendiri***
<br><br>

Jika tulisan sebelumnya membahas tentang bisakah AI memiliki pengetahuan tanpa benar-benar mengetahui bagaimana pengetahuan itu berada di dalam dirinya. Maka sekarang kita balik pisaunya menjadi bisakah AI membangun representasi tentang dirinya sendiri sebagai sebuah sistem?

Misalnya seperti ini, AI bisa mengatakan: “Kalau pertanyaan ini diberikan kepadaku, kemungkinan besar aku akan menjawab X.”

Nah, itu sudah bukan sekadar pengetahuan tentang dunia. Itu adalah pengetahuan tentang perilaku AI sendiri. Dan di sinilah konsep self-model muncul.


## Apa itu Self-Model ?

Dalam pengertian komputasional, self-model adalah representasi internal mengenai diri sistem itu sendiri.

Bukan harus berupa kalimat: “Aku adalah Fallan, tinggi 183 cm, ganteng…”  Bukan begitu.

Secara lebih teknis, sistem dapat memiliki representasi tentang kemampuan yang dimilikinya, keterbatasannya, kecenderungan perilakunya, keadaan internalnya, hubungan antara input dan responsnya, bahkan prediksi mengenai respons yang akan ia hasilkan.

Contoh sederhana: “Untuk soal matematika jenis A, probabilitas jawabanku benar tinggi.” Itu adalah model terhadap kompetensinya sendiri.

Kalau kemudian sistem menggunakan informasi tersebut untuk menentukan apakah harus menjawab atau meminta verifikasi, kita mulai memasuki wilayah metacognition.


## Metakognisi bukan Kesadaran

Ini harus dipisahkan dulu. Ada tiga lapisan:

Level 1
Model tentang dunia

“Jakarta adalah ibu kota Indonesia.”

Level 2
Model tentang kemampuan diri

“Aku biasanya cukup akurat menjawab pertanyaan sejarah.”

Level 3
Model tentang keadaan internal diri

“Dalam keadaan komputasi tertentu, representasi X sedang aktif dan menyebabkan kecenderungan Y.”

Level ketiga jauh lebih sulit, karena sistem bukan cuma memodelkan dunia tetapi dirinya yang sedang memodelkan dunia. Dan di situlah sistem mulai punya sesuatu yang menyerupai self-reference.


## LLM Bisa Memprediksi Dirinya Sendiri

Nah, ini bagian yang berubah dari filsafat menjadi eksperimen.

Penelitian Kadavath et al. (2022) menguji apakah language model dapat memperkirakan apakah jawaban yang diberikannya kemungkinan benar.

Mereka bahkan memperkenalkan gagasan P(IK), kira-kira probability that “I know” the answer.

Model ternyata dapat melakukan self-evaluation dengan performa yang cukup baik pada berbagai tugas, meskipun kalibrasinya tidak sempurna dan kemampuan tersebut tidak selalu general ke tugas baru. 

Jadi AI tidak hanya menghasilkan jawaban. Dalam kondisi tertentu, AI juga dapat memperkirakan “Seberapa besar kemungkinan jawaban gue benar?” 

Ini  sudah merupakan bentuk epistemic self-modeling.


## Eksperimen yang Jauh Lebih Nakal 

Penelitian Binder et al. yang dipublikasikan di ICLR 2025 mengajukan pertanyaan lebih keras, yaitu kalau model benar-benar mempunyai akses istimewa terhadap dirinya sendiri, apakah ia dapat memprediksi perilakunya sendiri lebih baik daripada model lain yang hanya mempelajari data perilaku model tersebut?

Ini eksperimen yang elegan.

Bayangkan ada Model A diminta memprediksi “Apa yang akan dilakukan Model A?” Kemudian Model B juga diminta memprediksi perilaku Model A.

Kalau A hanya mengandalkan pola umum yang dipelajarinya dari training, tidak ada alasan khusus A harus lebih unggul. Tetapi kalau A memiliki akses istimewa terhadap informasi mengenai dirinya sendiri, A seharusnya punya keuntungan.

Dan hasil mereka?

Dalam eksperimen pada GPT-4, GPT-4o, dan Llama-3, model yang menjadi target memang mengungguli model pembanding dalam memprediksi perilakunya sendiri pada tugas tertentu. 

Ini menarik banget.


## Apakah itu berarti AI sudah Introspeksi?

Ini justru bagian ilmiah yang paling penting.

Peneliti mendefinisikan introspeksi secara cukup ketat, bahwa sistem memperoleh informasi tentang dirinya yang tidak sekadar berasal dari training data atau inferensi biasa dari informasi eksternal.

Kalau model bisa mengetahui sesuatu tentang dirinya yang tidak tersedia dari sumber eksternal, kita punya indikasi adanya privileged self-information. 

Tetapi eksperimennya juga menemukan batas, bahwa kemampuan ini muncul pada tugas sederhana tertentu, tetapi gagal pada tugas yang lebih kompleks dan pada generalisasi out-of-distribution. 

Jadi kesimpulannya bukan “AI sudah sadar diri.” Melainkan ada bukti eksperimental bahwa LLM tertentu dapat memperoleh informasi tentang dirinya melalui mekanisme yang memenuhi sebagian kriteria introspeksi.

Itu jauh lebih menarik daripada klaim sensasional “AI sudah sadar.” 


## Teka-teki Baru

Bayangkan AI mengatakan: “Aku tahu bahwa aku cenderung menjawab X.”

Pertanyaannya: Dari mana informasi itu berasal?

Ada beberapa kemungkinan:
Kemungkinan A
AII belajar pola tersebut dari training.
Kemungkinan B
AII menyimpulkannya dari konteks percakapan.
Kemungkinan C
AII mempunyai representasi internal mengenai kecenderungan perilakunya sendiri.
Kemungkinan D
Ada kombinasi semuanya.

Dan justru membedakan A, B, C, dan D merupakan salah satu masalah penelitian yang sulit karena output verbal saja tidak cukup.


## Mengapa Jawaban “AI tahu Dirinya Sendiri” Belum Cukup?

Bahasa adalah alat yang sangat lentur. AI bisa menghasilkan kalimat: “Saya cenderung melakukan X.” Tetapi kalimat itu sendiri tidak membuktikan bahwa terdapat mekanisme internal yang benar-benar merepresentasikan kecenderungan X.

Turpin et al. (2023) menunjukkan bahwa chain-of-thought dapat menghasilkan penjelasan yang terdengar masuk akal tetapi tidak selalu merepresentasikan penyebab sebenarnya dari jawaban model. 

Jadi, self-report bukan berarti self-knowledge. Jadi secara otomatis kalau AI berkata: “Aku tahu mengapa aku melakukan ini.” Ilmuwan harus menjawab: “Oke. Sekarang buktikan.”


## Privileged Information

Pada manusia, introspeksi memberi akses tertentu terhadap keadaan internal yang tidak langsung tersedia bagi orang lain. Misalnya, AI tahu apa yang sedang ia pikirkan, manusia tidak otomatis tahu.

Kalau LLM bisa memperoleh informasi tentang perilakunya sendiri yang tidak dapat diprediksi sebaik itu oleh pengamat eksternal, kita mulai memiliki sesuatu yang secara fungsional menyerupai privileged access. Tetapi ini masih belum berarti pengalaman subjektif.

Dan ini perbedaan yang sangat penting antara functional introspection dengan phenomenal consciousness.

Dengan kata lain, sebuah mesin mungkin dapat memiliki self-model tanpa harus memiliki “rasa menjadi dirinya sendiri.”

Apa Sebenarnya yang Dimodelkan?

Ini pertanyaan paling seksi secara ilmiah. Ada setidaknya empat objek yang dapat dimodelkan:

| Yang dimodelkan | Contoh |
|------|-------|
| Kemampuan | “Aku bagus di bahasa.” |
| Keterbatasan | “Aku mungkin salah pada fakta ini.”|
| Perilaku | “Jika diberi prompt seperti ini, aku cenderung melakukan X.”|
| Keadaan internal | “Representasi internal tertentu sedang berada dalam state tertentu.”|

Dua yang pertama relatif lebih mudah, sedangkan yang keempat jauh lebih sulit. karena untuk benar-benar mengetahui keadaan internal, sistem membutuhkan hubungan yang cukup stabil antara representasi internal  serta informasi tentang representasi tersebut. Dan itu membawa kita langsung ke wilayah mechanistic interpretability.


## Lingkaran yang Mulai Terbentuk

Sekarang lihat struktur ini:

Dunia

↓

AI membangun model tentang dunia

↓

AI menghasilkan perilaku

↓

AI mengamati atau memperkirakan perilakunya

↓

AI membangun model tentang perilakunya

↓

Model itu digunakan untuk memprediksi perilaku berikutnya

↓

AI memperbarui model dirinya

↓

self-model

Ini sudah menjadi sistem rekursif. Bukan hanya AI mengetahui dunia, tetapi juga memiliki representasi mengenai bagaimana mengetahui dunia.

Itu adalah langkah konseptual besar.


## Muncul Pertanyaan yang Membuat para Filsuf Mengasah Pensil

Kalau suatu sistem memiliki:
model dunia,
model tentang dirinya,
kemampuan memprediksi perilakunya,
kemampuan mendeteksi kesalahan prediksinya,
kemampuan memperbarui model dirinya berdasarkan kesalahan tersebut,
apakah kita sudah boleh menyebutnya self-aware?

Jawabannya: Secara fungsional mungkin dalam arti terbatas. Namun secara fenomenologis belum terbukti karena self-awareness bisa berarti dua hal yang berbeda.

Dua hal yang berbeda itu adalah “Sistem mempunyai representasi tentang dirinya.” versus “Ada sesuatu yang terasa seperti menjadi sistem tersebut.”

Yang pertama bisa diuji secara empiris. Yang kedua membawa kita ke problem kesadaran subjektif.


## Jurang Berikutnya 

Kalau self-model semakin akurat dan sistem dapat memprediksi perilakunya sendiri, memperkirakan ketidakpastiannya, mengenali keterbatasannya, mendeteksi perubahan internal, menggunakan informasi tersebut untuk mengubah perilakunya, maka kita mendapatkan sesuatu yang jauh lebih menarik daripada chatbot.

Sesuatu itu adalah self-regulating agent. Yaitu sistem yang menggunakan model tentang dirinya untuk mengendalikan dirinya.

Dan ini sangat relevan untuk AI safety karena model yang mampu mengatakan: “Aku mungkin salah.” saja belum terlalu istimewa. Yang jauh lebih penting adalah: “Aku memperkirakan aku mungkin salah, maka aku mengubah strategi tindakanku.”

Itulah transisi dari self-description menjadi self-regulation.


## Apakah AI Bisa Membentuk Model tentang Dirinya Sendiri?

Dalam arti fungsional dan terbatas, ada bukti empiris bahwa beberapa LLM dapat memperoleh dan menggunakan informasi tentang perilaku/kemampuan dirinya sendiri.

Eksperimen introspeksi pada ICLR 2025 bahkan memberikan bukti bahwa model tertentu dapat memperoleh informasi mengenai dirinya yang tidak sepenuhnya dapat dijelaskan sebagai pengetahuan eksternal biasa. 

Tetapi kemampuan tersebut tidak universal, tidak stabil di semua domain, dan belum menunjukkan introspeksi umum seperti manusia. 


Jadi kalimat yang paling aman secara ilmiah bukan AI sudah sadar diri, melainkan LLM menunjukkan kapasitas terbatas untuk self-modeling dan introspective access terhadap aspek tertentu dari perilakunya sendiri.

<br><br>
**Referensi**

Binder, F. J., Chua, J., Korbak, T., Sleight, H., Hughes, J., Long, R., Perez, E., Turpin, M., & Evans, O. (2025). Looking inward: Language models can learn about themselves by introspection. International Conference on Learning Representations (ICLR). 

Kadavath, S., et al. (2022). Language models (mostly) know what they know. arXiv:2207.05221. 

Turpin, M., Michael, J., Perez, E., & Bowman, S. R. (2023). Language models don’t always say what they think: Unfaithful explanations in chain-of-thought prompting. Advances in Neural Information Processing Systems, 36. 
