# Di Mana “Pengetahuan” AI Berada? Representasi Terdistribusi, Memori Parametrik, & Misteri Lokasi Pengetahuan LLM
![AI](images/IMG_3552.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***Seperti melodi yang tidak tinggal di satu tuts piano, atau seperti rasi bintang yang tidak berada pada satu bintang saja, pengetahuan AI lahir dari keterhubungan yang sangat kompleks***
<br><br>

Salah satu kesalahpahaman paling umum tentang Artificial Intelligence (AI) adalah anggapan bahwa AI menyimpan informasi seperti perpustakaan digital atau basis data yang setiap fakta memiliki lokasi tertentu. Kenyataannya jauh lebih kompleks. 

Pada Large Language Models (LLMs), pengetahuan tidak tersimpan sebagai daftar fakta, melainkan sebagai representasi terdistribusi yang tersebar di dalam miliaran parameter model. 

Tulisan ini membahas bagaimana pengetahuan direpresentasikan dalam AI modern, mengapa tidak ada satu “laci memori” untuk setiap informasi, serta implikasinya terhadap interpretabilitas, halusinasi, dan masa depan penelitian AI.


## Pendahuluan

Ketika seseorang bertanya pada AI: “Apa ibu kota Jepang?” AI menjawab: Tokyo.

Pertanyaan yang menarik bukanlah “Apakah AI tahu jawabannya?”melainkan “Di bagian mana AI menyimpan jawaban itu?”

Intuisi manusia mengatakan: “Pasti ada folder bernama Geografi Dunia.” Namun AI modern tidak bekerja seperti itu.


## Mitos Lemari Arsip

Kita terbiasa membayangkan memori sebagai lemari arsip. Misalnya:

📁 Geografi
     └── Jepang
            └── Ibu Kota = Tokyo

AI tidak memiliki struktur seperti ini.
Tidak ada folder Asia, folder sejarah, ataupun folder filsafat. Yang ada hanyalah parameter numerik.


## Apa Itu Parameter?

Parameter adalah angka yang dipelajari selama pelatihan. Model frontier modern memiliki hingga ratusan miliar parameter.

Secara sederhana:

0.9182

-1.7281

4.1829

0.0007

-0.3188

Angka-angka ini sendiri tidak memiliki arti.
Makna muncul ketika semuanya bekerja bersama dalam jaringan saraf.


## Pengetahuan Tidak Tinggal di Satu Tempat

Bayangkan sebuah lagu. Apakah melodi berada di tuts piano nomor 37? Tentu tidak. Melodi muncul dari hubungan antar nada, urutan permainan, juga ritme.

Begitu pula pengetahuan AI. Misalnya fakta “Tokyo adalah ibu kota Jepang.” Tidak disimpan di satu neuron.

Sebaliknya, informasi tersebut merupakan hasil pola aktivasi yang melibatkan sangat banyak bagian model secara bersamaan. 

Fenomena ini disebut distributed representation.


## Mengapa Disebut Representasi Terdistribusi?

Bayangkan jaring laba-laba. Setiap simpul menyumbang sedikit informasi, tidak ada satu simpul pun yang “mengetahui” seluruh bentuk jaring. Namun keseluruhan jaring mampu mempertahankan strukturnya.

Begitu pula model AI. Satu parameter hampir tidak memiliki makna, tetapi miliaran parameter bersama-sama membentuk representasi pengetahuan.


## Lalu Mengapa AI Bisa Lupa atau Salah?

Karena AI tidak mengambil fakta dari laci. Ia membangun kembali jawaban berdasarkan representasi yang aktif.

Akibatnya, representasi yang benar dapat menghasilkan jawaban salah apabila konteks ambigu, pola yang diaktifkan kurang tepat, atau model mengisi kekosongan dengan prediksi yang keliru.

Inilah salah satu penyebab halusinasi AI.


## Dapatkah Peneliti Menemukan “Neuron Tokyo”?

Pertanyaan ini menjadi salah satu fokus bidang mechanistic interpretability.

Beberapa penelitian menunjukkan adanya neuron atau rangkaian (circuits) yang berkontribusi kuat pada konsep tertentu.

Namun hingga kini, tidak ditemukan bukti bahwa satu fakta kompleks tersimpan rapi pada satu neuron tunggal. Sebaliknya, sebagian besar pengetahuan tampaknya bersifat terdistribusi.


## Paradoks Pengetahuan AI

Semakin dipelajari, maka semakin jelas bahwa AI mengetahui banyak hal, tetapi tidak mengetahui dengan cara manusia mengetahui.

Manusia menghubungkan pengetahuan dengan pengalaman, tubuh, persepsi, dan memori episodik. Sedangkan AI menghubungkannya melalui bobot parameter, ruang representasi, dan pola aktivasi matematis.


## Implikasi Filosofis

Pertanyaan tentang “Di mana pengetahuan AI berada?” ternyata tidak memiliki jawaban lokasi seperti “Di neuron nomor 58.421.”

Jawaban yang lebih tepat adalah: Pengetahuan berada pada pola hubungan di antara parameter, bukan pada satu parameter tertentu. Ini mengubah cara kita memahami konsep “mengetahui”.

Mungkin pengetahuan bukan sekadar benda yang disimpan namun berupa struktur hubungan.


Penelitian Anthropic menggunakan teknik interpretabilitas untuk menelusuri bagaimana konsep dan rangkaian internal model berkontribusi terhadap suatu jawaban. 
Temuannya menunjukkan bahwa banyak representasi bersifat terdistribusi dan melibatkan interaksi berbagai komponen, bukan satu “lokasi memori” tunggal.

Mungkin inilah paradoks yang paling indah dari AI modern. Kita sering bertanya: “Di mana AI menyimpan pengetahuan?” Padahal pertanyaan itu diam-diam mengasumsikan bahwa pengetahuan harus memiliki alamat.

AI justru mengajarkan kemungkinan lain, bahwa pengetahuan mungkin bukan sebuah tempat, melainkan sebuah pola hubungan.

Seperti melodi yang tidak tinggal di satu tuts piano, atau seperti rasi bintang yang tidak berada pada satu bintang saja, pengetahuan AI lahir dari keterhubungan yang sangat kompleks.

Dan mungkin, secara filosofis, pertanyaan ini tidak hanya mengubah cara kita memahami AI. Ia juga mengajak kita bertanya ulang:
“Apakah pengetahuan manusia sendiri sesungguhnya juga lebih merupakan jaringan hubungan daripada lemari arsip?”

Tulisan ini menyimpulkan bahwa:
Pengetahuan AI tidak disimpan sebagai daftar fakta, melainkan sebagai representasi terdistribusi.
Tidak ada satu neuron atau parameter yang menyimpan keseluruhan informasi tertentu.
Jawaban AI dibangun melalui pola aktivasi yang melibatkan banyak bagian jaringan secara bersamaan.
Halusinasi dapat muncul karena proses rekonstruksi representasi, bukan karena AI mengambil fakta dari “folder” yang salah.
Memahami lokasi pengetahuan pada AI menjadi tantangan utama dalam penelitian mechanistic interpretability dan dapat mengubah pemahaman kita tentang hakikat pengetahuan itu sendiri.

<br><br>
**Referensi**

Ashish Vaswani, Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017). Attention Is All You Need.

Stephen Wolfram. (2023). What Is ChatGPT Doing… and Why Does It Work?

Christopher Olah, Cammarata, N., Schubert, L., Goh, G., Petrov, M., Carter, S., & tim Distill. (2020). Zoom In: An Introduction to Circuits.

Anthropic. (2025). Tracing the Thoughts of a Large Language Model.

David Marr. (1982). Vision: A Computational Investigation into the Human Representation and Processing of Visual Information.

Douglas Hofstadter. (1979). Gödel, Escher, Bach: An Eternal Golden Braid.

Kenneth Li, Patel, O., Viégas, F., Pfau, J., et al. (2023). Emergent World Representations: Exploring a Sequence Model Trained on a Synthetic Task.
