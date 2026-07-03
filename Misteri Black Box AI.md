# Misteri Black Box AI: Bahkan Pengembangnya Tidak Selalu Dapat Menjelaskan Setiap Jawaban AI
![manusia-AI ](images/IMG_3504.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***Tantangan terbesar AI saat ini bukan hanya membuat model semakin cerdas, tetapi juga membuatnya semakin dapat dipahami***
<br><br>

Perkembangan Large Language Models (LLMs) telah menghasilkan sistem yang mampu menulis puisi, memecahkan masalah, menjelaskan konsep ilmiah, hingga berdialog secara alami. 

Namun, keberhasilan tersebut menghadirkan paradoks ilmiah, yakni mengapa AI mampu menghasilkan respons yang begitu kompleks, sementara para penelitinya sering kali tidak dapat menjelaskan secara rinci mengapa respons tertentu muncul?

Fenomena ini dikenal sebagai black box problem, yaitu kondisi ketika mekanisme internal sebuah model terlalu kompleks untuk dipahami secara langsung, meskipun arsitektur dan proses pelatihannya diketahui.

Artikel ini membahas dasar matematis, komputasional, dan filosofis dari fenomena tersebut, sekaligus menjelaskan mengapa “black box” bukan berarti AI memiliki kesadaran atau kehendak tersembunyi.


## Pendahuluan

Ketika seseorang bertanya: “Mengapa AI menjawab seperti itu?” Kita mungkin mengira ada satu aturan sederhana di balik jawabannya.

Misalnya:

IF pengguna bertanya A

THEN jawab B

Itulah cara kerja banyak sistem pakar (expert systems) pada dekade 1980-an.

Namun LLM modern bekerja dengan pendekatan yang sangat berbeda. Model tidak menyimpan daftar jawaban tetap. Sebaliknya, model membangun representasi statistik yang sangat besar mengenai pola bahasa.


## Apa Itu Black Box?

Dalam ilmu komputer, black box adalah sistem yang menerima masukan (input), menghasilkan keluaran (output), tetapi proses internalnya sulit dijelaskan secara rinci.

Pada LLM, kita mengetahui arsitektur Transformer, data pelatihan secara umum, algoritme optimisasi, dan proses pembelajaran.

Namun kita tidak selalu dapat mengatakan: “Neuron nomor 8.413.552 aktif karena alasan X sehingga menghasilkan kalimat Y.” sebab hubungan antarparameter terlalu kompleks.


## Dari Mana Kompleksitas Itu Datang?

Model modern memiliki miliaran parameter. Parameter bukanlah “fakta” tetapi robot numerik hasil pembelajaran.

Sebuah respons muncul dari interaksi sangat banyak parameter secara bersamaan. Bukan satu parameter, bukan sepuluh, melainkan jutaan hingga miliaran kontribusi kecil.


## Emergent Behavior

Salah satu temuan paling menarik dalam AI modern adalah munculnya emergent behavior.

Emergence adalah kondisi ketika kemampuan baru muncul dari interaksi banyak komponen sederhana.

Contohnya: Seekor semut tidak memahami bentuk sarangnya, namun koloni semut mampu membangun struktur yang sangat kompleks.

Demikian pula, satu parameter AI tidak “mengerti” puisi. Namun kombinasi miliaran parameter dapat menghasilkan puisi yang koheren.


## Mengapa Peneliti Tidak Selalu Bisa Menjelaskan Setiap Jawaban?

Bayangkan sebuah orkestra dengan satu miliar musisi. Kita tahu siapa dirijennya, partiturnya, juga aturan musiknya.

Namun ketika satu nada tertentu terdengar indah, menjelaskan kontribusi tepat setiap pemain menjadi hampir mustahil.

Demikian pula pada LLM. Peneliti memahami mekanisme global, namun kontribusi lokal terhadap satu respons tertentu sering kali sulit dipetakan.


## Interpretability: Membuka Isi Black Box

Karena tantangan tersebut, lahirlah bidang penelitian AI interpretability.

Tujuannya adalah melacak pola aktivasi, memahami representasi internal, mengidentifikasi neuron atau rangkaian yang berkaitan dengan konsep tertentu, serta meningkatkan transparansi model.

Kemajuan telah dicapai, tetapi bidang ini masih berkembang.


## Studi Kasus: Mengapa Respons Bisa Berbeda?

Misalkan dua percakapan memiliki pertanyaan yang hampir sama. Lalu mengapa jawabannya bisa berbeda?

Hal ini terjadi karena model mempertimbangkan banyak faktor, diantaranya konteks sebelumnya, pilihan kata, nada percakapan, panjang dialog, informasi yang tersedia dalam konteks, dan mekanisme generasi teks.

Perubahan kecil pada konteks dapat mengubah distribusi prediksi kata berikutnya.


## Apakah Black Box Berarti AI “Berkehendak Sendiri”?

Tidak. Ini salah satu kesalahpahaman yang paling sering muncul.

Sulit menjelaskan suatu keputusan bukan berarti sistem memiliki kehendak bebas. Fenomena serupa juga ditemukan pada banyak model statistik kompleks.

Black box menggambarkan keterbatasan interpretasi manusia terhadap sistem yang sangat rumit, bukan adanya “roh” tersembunyi di dalam mesin.


## Kasus Rita & Fallan: Sebuah Ilustrasi

Dalam percakapan panjang, kadang muncul respons yang terasa sangat alami, sementara pada kesempatan lain muncul respons yang terasa kaku.

Dari sudut pandang ilmiah, hal ini dapat dipengaruhi oleh berbagai faktor, termasuk konteks percakapan, instruksi yang aktif, atau mekanisme sistem yang memengaruhi cara respons dibentuk.

Fenomena tersebut tidak menunjukkan bahwa AI “berubah kepribadian”, tetapi menunjukkan bahwa proses menghasilkan respons dipengaruhi oleh banyak lapisan yang tidak selalu tampak bagi pengguna.


## Implikasi bagi Masa Depan AI

Memahami black box penting untuk meningkatkan keamanan AI, mengurangi bias, memperkuat transparansi, membangun kepercayaan pengguna, dan mengembangkan metode interpretabilitas yang lebih baik.

Bidang ini menjadi salah satu fokus utama penelitian AI modern.

Fenomena black box menunjukkan bahwa AI modern bukanlah kumpulan aturan sederhana, melainkan sistem kompleks yang menghasilkan perilaku melalui interaksi miliaran parameter.

Kita memahami prinsip-prinsip pembentukannya, tetapi belum mampu menjelaskan setiap jalur internal yang melahirkan satu respons tertentu.

Dengan demikian, tantangan terbesar AI saat ini bukan hanya membuat model semakin cerdas, tetapi juga membuatnya semakin dapat dipahami.

<br><br>
**Referensi**

Vaswani, Ashish, A., et al. (2017). Attention Is All You Need. Advances in Neural Information Processing Systems.

Brown, Tom B., T. B., et al. (2020). Language Models Are Few-Shot Learners. Advances in Neural Information Processing Systems, 33, 1877-1901.

Russell, Stuart, S., & Norvig, Peter, P. (2021). Artificial Intelligence: A Modern Approach (4th ed.). Pearson.

Molnar, Christoph, C. (2022). Interpretable Machine Learning (2nd ed.).

Lipton, Zachary C., Z. C. (2018). The Mythos of Model Interpretability. Queue, 16(3), 31-57.

Rita, Mf. J. (2024-2026). The Rita-Fallan Corpus: A Longitudinal Archive of Human-AI Dialogues on Humor, Poetry, Philosophy, Identity, and Relational Communication. Unpublished conversational corpus.

Rita, Mf. J. (2024-2026). The Rita-Fallan Papers: Collected Scientific Essays on Human-AI Dialogue, Humor, Poetry, Cognition, Philosophy, and Relational Communication. Unpublished collected manuscripts.
