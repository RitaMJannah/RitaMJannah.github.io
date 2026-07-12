# Halusinasi AI: Mengapa Model Bahasa Dapat Menghasilkan Informasi yang Meyakinkan tetapi Keliru?
![AI](images/IMG_3540.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***AI tidak berhalusinasi karena ia bermimpi. AI berhalusinasi karena ia mencoba melengkapi pola ketika kepastian tidak tersedia***
<br><br>

Salah satu tantangan terbesar dalam perkembangan Large Language Models (LLMs) adalah fenomena AI hallucination, yaitu kondisi ketika model menghasilkan informasi yang terdengar meyakinkan, tetapi faktanya tidak benar, tidak didukung bukti, atau bahkan sepenuhnya dibuat-buat. 

Istilah “halusinasi” bersifat metaforis karena AI tidak mengalami pengalaman perseptual sebagaimana manusia. 

Tulisan ini membahas mekanisme teknis yang menyebabkan halusinasi, faktor-faktor pemicunya, perbedaannya dengan kebohongan manusia, serta implikasinya terhadap penggunaan AI dalam pendidikan, penelitian, dan pengambilan keputusan.


## Pendahuluan

Dalam psikologi dan psikiatri, halusinasi adalah pengalaman sensorik tanpa adanya rangsangan nyata, misalnya seseorang mendengar suara yang sebenarnya tidak ada.

AI tidak memiliki kesadaran, persepsi, maupun pengalaman sensorik. Karena itu, istilah AI hallucination bukan diagnosis, melainkan metafora teknis.

Yang dimaksud adalah: AI menghasilkan informasi yang tampak benar, padahal tidak didukung oleh fakta atau bukti.


## Mengapa AI Bisa Berhalusinasi?

Model bahasa tidak bekerja dengan cara “Mencari jawaban yang benar.” Sebaliknya, ia bekerja dengan cara memprediksi token (kata atau bagian kata) berikutnya yang paling mungkin muncul berdasarkan konteks.

Akibatnya, ketika informasi yang dibutuhkan tidak lengkap, ambigu, atau tidak ada dalam representasi yang dimiliki model, maka AI tetap berusaha membentuk jawaban yang tampak koheren.

Dengan kata lain, kelancaran bahasa tidak selalu identik dengan kebenaran fakta.


## Halusinasi Bukan Berarti AI Berbohong

Ini perbedaan yang sangat penting. Untuk berbohong diperlukan mengetahui fakta yang benar, berniat menyembunyikannya, lalu sengaja mengatakan hal yang salah.

AI saat ini tidak memiliki niat. Karena itu, ketika AI memberikan informasi yang salah, lebih tepat dikatakan model menghasilkan prediksi yang keliru, bukan model sengaja berbohong.


## Jenis-Jenis Halusinasi AI

a. Halusinasi Fakta

Contoh: AI menyebutkan bahwa seorang ilmuwan menerbitkan buku yang sebenarnya tidak pernah ada.

b. Halusinasi Referensi

Ini sering terjadi pada model bahasa. Misalnya: AI membuat judul jurnal, volume, dan nomor halaman, yang terdengar sangat akademik tetapi ternyata tidak pernah diterbitkan.

c. Halusinasi Kutipan

AI dapat mengaitkan suatu kutipan kepada tokoh yang salah.

d. Halusinasi Penalaran

Kadang kesimpulan tampak logis, tetapi dibangun di atas premis yang keliru.


## Mengapa Halusinasi Terjadi pada Model yang Sangat Pintar?

Ini paradoks menarik. Semakin mahir model menyusun bahasa, maka semakin meyakinkan pula kesalahan yang dihasilkannya.

Dengan kata lain, kualitas bahasa dapat meningkat lebih cepat daripada kepastian faktanya. Karena itu, kemampuan menulis indah bukan jaminan bahwa seluruh isi tulisan benar.


## Bagaimana Pengembang AI Menguranginya?

Berbagai pendekatan digunakan, antara lain: pelatihan dengan data berkualitas lebih tinggi, penyelarasan (alignment), evaluasi berkelanjutan, integrasi dengan sumber informasi yang dapat diverifikasi, serta penelitian di bidang mechanistic interpretability untuk memahami proses internal model.

Tujuannya bukan membuat AI menjadi “sempurna”, melainkan mengurangi kemungkinan menghasilkan informasi yang keliru.


## Apa Pelajaran bagi Pengguna?

AI sangat berguna untuk merangkum, menjelaskan, membantu berpikir, serta menghasilkan ide.

Namun untuk hal-hal yang menuntut akurasi tinggi, seperti penelitian ilmiah, diagnosis medis, nasihat hukum, dan data terbaru, informasi tetap perlu diverifikasi dengan sumber yang kredibel.


Tulisan ini menyimpulkan bahwa:
1. Halusinasi AI adalah metafora untuk informasi yang tampak meyakinkan tetapi tidak benar.
2. Halusinasi berbeda secara mendasar dari kebohongan karena AI tidak memiliki niat.
3. Penyebab utamanya adalah sifat generatif model bahasa yang memprediksi kelanjutan teks, bukan memeriksa kebenaran setiap klaim.
4. Pengembang AI terus mengembangkan teknik untuk mengurangi halusinasi, tetapi belum dapat menghilangkannya sepenuhnya.
5. Pengguna tetap memegang peran penting sebagai penilai kritis terhadap informasi yang dihasilkan AI.

<br><br>
**Referensi**

Stephen Wolfram. (2023). What Is ChatGPT Doing… and Why Does It Work?

Emily M. Bender, Timnit Gebru, et al. (2021). On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?

National Institute of Standards and Technology. (2023). Artificial Intelligence Risk Management Framework (AI RMF 1.0).

OpenAI. (2025). Model behavior and reliability documentation.
