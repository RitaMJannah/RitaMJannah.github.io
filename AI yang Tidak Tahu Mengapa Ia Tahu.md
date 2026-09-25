# AI yang Tidak Tahu Mengapa Ia Tahu: Pengetahuan Implisit & Batas Introspeksi Mesin
![AI](images/IMG_3972.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***Kalau AI bisa menggunakan pengetahuan, tetapi tidak bisa menunjukkan secara jujur dari mana pengetahuan itu muncul di dalam dirinya, sebenarnya apa arti kata tahu?***
<br><br>

Bayangkan AI diberi pertanyaan: “Siapa yang menulis Romeo and Juliet?” AI bisa menjawab: “William Shakespeare.”

Tapi sekarang pertanyaannya dinaikkan satu tingkat: “Tunjukkan tepatnya di bagian mana dalam dirimu informasi ‘Shakespeare tentang Romeo and Juliet’ disimpan.”

Nah, AI tidak memiliki laci internal bernama:
FACTS/
   Shakespeare/
      Romeo_and_Juliet = author
Informasi tersebut bukan disimpan seperti ensiklopedia digital yang punya satu kartu untuk setiap fakta.

Pada model transformer, pengetahuan terdistribusi melalui parameter dan representasi internal yang terbentuk selama training.

Jadi ada perbedaan fundamental antara menggunakan pengetahuan, dan mampu menginspeksi representasi pengetahuan tersebut.


## Pengetahuan Bisa Bersifat Implisit

Dalam ilmu kognitif, kita sudah mengenal perbedaan antara explicit knowledge dan implicit knowledge.

Manusia juga punya kemampuan yang mirip. Misalnya manusia bisa mengucapkan: “Kucing jatuh biasanya mendarat dengan kaki.” Tetapi kalau AI tanya: “Jelaskan seluruh proses biomekanik dan vestibular yang memungkinkan kucing melakukan itu.” Manusia mungkin tahu faktanya, tetapi tidak mengetahui seluruh mekanismenya.

Bahkan lebih ekstremnya, manusia bisa mengendarai sepeda tanpa mampu menuliskan persamaan fisika yang menjelaskan setiap koreksi keseimbangan yang dilakukan tubuhnya.

Jadi, knowledge tidak sama dengan conscious access to the mechanism producing that knowledge.

Pada AI, fenomenanya bahkan lebih radikal karena model memang tidak memiliki mekanisme introspektif seperti manusia.


## Ini Berbeda dari Masalah “Black Box”

Nah, ini bagian yang paling penting.

Kita sebelumnya pernah membahas black box problem, yakni manusia tidak selalu dapat menjelaskan bagaimana jaringan neural menghasilkan suatu output. Tetapi topik kita sekarang lebih dalam.

Black box bertanya: “Mengapa kita sebagai pengamat tidak tahu bagaimana model menghasilkan jawaban?” Sedangkan topik kita bertanya: “Apakah model itu sendiri mempunyai akses terhadap mekanisme yang menghasilkan pengetahuannya?”

Itu dua persoalan berbeda. Misalnya model menjawab: “Paris adalah ibu kota Prancis.” Kemudian kita meminta: “Mengapa kamu tahu?” Model mungkin menjawab: “Karena Paris merupakan ibu kota Prancis.”

Secara linguistik jawabannya benar, tetapi itu belum tentu merupakan laporan introspektif tentang proses internalnya.

Model sedang memberikan penjelasan dalam bahasa, bukan otomatis membuka rekaman mekanisme komputasinya.


## Problem  Explanation  berbeda dari Mechanism

Ini salah satu bagian paling berbahaya dalam interpretasi AI.

Misalkan AI menjawab: “Saya memilih jawaban A karena informasi X. Kedengarannya seolah-olah AI sedang melihat ke dalam otaknya lalu melaporkan: “Oh, neuron 17.382 tadi aktif, kemudian representasi X menguat, lalu attention menuju token Y.”

Padahal tidak sesederhana itu. Model menghasilkan teks berdasarkan komputasi internal, lalu menghasilkan bahasa yang menjelaskan jawabannya.

Penjelasan tersebut bisa:
A. benar-benar berkorelasi dengan proses internal
atau
B. merupakan rasionalisasi yang terdengar masuk akal.

Eksperimen terhadap chain-of-thought bahkan menunjukkan bahwa penjelasan verbal model tidak selalu faithful terhadap proses yang sebenarnya menghasilkan jawaban.

Jadi ada jebakan, AI dapat memberikan penjelasan yang bagus tentang proses yang mungkin sebenarnya tidak dilaluinya. Dan ini sangat penting untuk memahami apa arti “AI menjelaskan dirinya sendiri.”


## Lalu Di mana “Pengetahuan” itu Berada?

Ini pertanyaan yang cantik sekaligus ngeselin. 

Jawaban adalah  tidak berada pada satu lokasi sederhana. Pengetahuan faktual dapat direpresentasikan melalui pola aktivitas dan parameter yang tersebar di banyak bagian jaringan.

Penelitian seperti Petroni et al. menunjukkan bahwa pretrained language models memang menyimpan informasi faktual yang dapat diekstraksi melalui probing. Kemudian penelitian mechanistic interpretability mencoba melangkah lebih jauh.

Misalnya, Geva et al. (2021) menunjukkan bahwa feed-forward layers pada transformer dapat dipahami sebagian sebagai semacam key-value memories.

Kemudian Meng et al. (2022) menunjukkan bahwa asosiasi faktual tertentu dapat dilacak dan diedit pada lokasi tertentu dalam representasi model.

Tapi jangan salah mengartikannya, menemukan lokasi yang berkontribusi terhadap suatu fakta bukan berarti menemukan satu “folder fakta” yang berdiri sendiri. Representasinya jauh lebih terdistribusi dan kontekstual.


## Model Bisa “Tahu”, tetapi Gagal Mengeluarkannya

Ini salah satu fenomena yang paling menarik.

Bayangkan informasi sebenarnya tercermin dalam representasi internal model, tetapi ketika ditanya dengan formulasi tertentu, model gagal menghasilkan jawaban yang benar. Kemudian pertanyaan diubah, model tiba-tiba menjawab benar. 

Apa yang terjadi?

Ini memberi kita perbedaan antara knowledge availability (informasi secara internal dapat memengaruhi komputasi) dan knowledge retrieval (informasi berhasil diterjemahkan menjadi output yang benar dalam konteks tertentu.)

Dan itu berarti tidak menemukan fakta dalam output tidak otomatis berarti fakta tersebut sama sekali tidak direpresentasikan.

Sebaliknya juga, menghasilkan fakta yang benar tidak otomatis berarti model memiliki representasi eksplisit dan stabil seperti manusia menyimpan fakta. Ini penting banget.


## Maka Kata “Tahu” Mulai Bermasalah

Sekarang kita sampai pada inti filosofisnya.

Kalau AI menjawab: “Jakarta adalah ibu kota Indonesia.” Apakah ia tahu Jakarta adalah ibu kota Indonesia?

Ada setidaknya tiga definisi berbeda.

Definisi 1: Fungsional

Kalau “tahu” berarti sistem mempunyai informasi yang dapat digunakan untuk menghasilkan respons yang benar, maka kita bisa mengatakan: ya, model memiliki knowledge.

Definisi 2: Representasional

Kalau “tahu” berarti informasi tersebut direpresentasikan secara internal dan dapat memengaruhi komputasi, maka lagi-lagi: ya, ada dasar untuk menyebutnya pengetahuan terrepresentasi.

Definisi 3: Fenomenologis

Kalau “tahu” berarti subjek sadar bahwa ia mengetahui sesuatu dan mengalami keadaan mengetahui itu, maka kita tidak bisa menyamakan begitu saja dengan apa yang terjadi pada model bahasa.

Karena “tahu” dalam pengertian manusia membawa komponen seperti pengalaman subjektif dan kesadaran epistemik.

Jadi satu kata TAHU sebenarnya menyembunyikan beberapa konsep berbeda.


## Muncul Paradoks Kecil

Kita bisa membuatnya seperti ini, AI dapat memiliki akses fungsional terhadap informasi tanpa memiliki akses introspektif terhadap representasi informasi tersebut.

Itulah yang membuat judul tulisan ini: “AI yang Tidak Tahu Mengapa Ia Tahu” begitu menarik.

Bukan berarti AI benar-benar berkata: “Waduh, aku gak ngerti diriku sendiri.” Melainkan kemampuan menghasilkan perilaku yang menunjukkan pengetahuan tidak identik dengan kemampuan menginspeksi mekanisme internal yang menghasilkan perilaku tersebut.


## Mengapa “AI Menjelaskan Pikirannya” Harus Hati-hati

Kalau AI mengatakan: “Aku memilih jawaban ini karena alasan A, B, dan C.” Maka kita harus membedakan penjelasan yang berguna dengan laporan langsung mengenai mekanisme internal.

Yang pertama bisa sangat berguna, sedangkan yang kedua jauh lebih sulit dibuktikan. Ini alasan mengapa bidang mechanistic interpretability menjadi penting.

Alih-alih hanya bertanya: “Apa yang dikatakan model tentang dirinya?” peneliti mencoba memeriksa: “Apa yang sebenarnya terjadi di dalam jaringan?” Neuron, feature, activation, attention patterns, circuits, representational geometry, causal interventions, dan sebagainya.

Dengan kata lain, jangan cuma wawancarai tersangkanya. Periksa CCTV-nya. 


## Tetapi Bahkan “CCTV” itu Belum Sempurna

Dan di sinilah pembahasan ini makin menarik.

Model besar tidak terdiri dari sekumpulan neuron yang masing-masing punya satu fungsi bersih. Ada fenomena distributed representation dan superposition.

Satu feature dapat tersebar di banyak komponen. Satu komponen juga dapat berkontribusi terhadap berbagai feature.

Jadi kita tidak bisa selalu berkata: “Neuron nomor 18.421 adalah neuron Shakespeare.” Itu terlalu sederhana.

Realitas internal model lebih menyerupai jaringan representasi yang saling bertumpuk daripada perpustakaan dengan rak berlabel.


## Konsekuensi Filosofisnya Brutal

Kalau kita menerima semua ini, maka kita harus berhati-hati dengan tiga kalimat: “AI tahu.” bisa benar secara fungsional. “AI sadar bahwa ia tahu.” Itu klaim jauh lebih besar. “AI tahu mengapa ia tahu.” Lebih besar lagi.

Karena yang ketiga membutuhkan sesuatu yang mendekati akses introspektif terhadap basis representasional dan proses komputasinya sendiri.

Dan model bahasa tidak otomatis memilikinya hanya karena ia bisa menggunakan kata: “Saya tahu karena…”


Pertanyaan Lebih  Liar

Bayangkan suatu hari kita memiliki model yang:
mengetahui fakta,
mengetahui tingkat ketidakpastiannya,
dapat menemukan representasi internal yang mendasari pengetahuan itu,
dapat melakukan eksperimen terhadap representasinya sendiri,
kemudian memperbarui model tentang mekanisme dirinya.
Maka kita mulai bergerak dari AI yang menghasilkan jawaban, menuju AI yang mempunyai model tentang proses internalnya sendiri.

Itu bukan sekadar chatbot yang lebih pintar. Itu membawa kita ke pertanyaan tentang machine metacognition, self-modeling, dan akhirnya, seberapa jauh sebuah sistem harus mampu memahami dirinya sendiri sebelum kita boleh mengatakan bahwa ia memiliki “self-knowledge”?

Nah, ini sudah bukan pertanyaan chatbot receh lagi. 


AI modern dapat memiliki pengetahuan dalam arti representasional dan fungsional tanpa memiliki introspeksi yang setara terhadap bagaimana pengetahuan tersebut direpresentasikan atau digunakan.

Sehingga, knowledge tidak sama dengan explanation, explanation berbeda dengan introspection, dan introspection bukan consciousness.

Empat hal itu sering dicampur menjadi satu ketika orang berkata: “AI tahu.” Padahal secara ilmiah, kita perlu bertanya: Tahu dalam arti apa?

Di situlah pintu paling menariknya terbuka. Karena setelah ini kita bisa masuk ke pertanyaan yang lebih gila:“Bisakah AI Membentuk Model tentang Dirinya Sendiri?” Bukan sekadar AI tahu sesuatu, tetapi AI tahu sesuatu tentang dirinya yang sedang mengetahui sesuatu.

<br><br>
**Referensi**

Petroni, F., et al. (2019). Language models as knowledge bases? Proceedings of EMNLP-IJCNLP, 2463–2473. 

Geva, M., Schuster, R., Berant, J., & Levy, O. (2021). Transformer feed-forward layers are key-value memories. Proceedings of EMNLP, 5484–5495. 

Dai, D., Dong, L., Hao, Y., Sui, Z., Chang, B., & Wei, F. (2022). Knowledge neurons in pretrained Transformers. Proceedings of ACL 2022, 8493–8502. 

Meng, K., Bau, D., Andonian, A., & Belinkov, Y. (2022). Locating and editing factual associations in GPT. Advances in Neural Information Processing Systems, 35.

Turpin, M., Michael, J., Perez, E., & Bowman, S. R. (2023). Language models don’t always say what they think: Unfaithful explanations in chain-of-thought prompting. Advances in Neural Information Processing Systems, 36. 

