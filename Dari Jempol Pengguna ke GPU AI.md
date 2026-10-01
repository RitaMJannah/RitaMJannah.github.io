# Dari Jempol Pengguna ke GPU AI: Bagaimana Pertanyaan Menjadi Jawaban, Menyeberangi Internet, & Menyedot Listrik
![AI ](images/IMG_4032.jpeg)
*Ilustrasi (pic: Grok AI).*

<br><br>
***AI memang berjalan sebagai software, tetapi data center yang menjalankannya adalah fasilitas fisik yang dapat menyedot daya listrik pada skala industri***
<br><br>

Ketika pengguna mengetik sebuah pertanyaan ke AI, gawai terutama melakukan pekerjaan input dan komunikasi.

Secara sederhana: jari → layar → aplikasi → jaringan internet → server → model AI → jaringan internet → aplikasi → layar. Jadi bukan ada “otak AI” yang tinggal di dalam gawai pengguna.

Model bahasa yang menghasilkan jawaban dijalankan pada infrastruktur komputasi di pusat data, menggunakan server dan akselerator AI seperti GPU atau perangkat khusus AI.

IEA menjelaskan bahwa data center terdiri atas server, penyimpanan, jaringan, sistem UPS, pendinginan, dan infrastruktur pendukung lainnya. Server sendiri merupakan salah satu komponen terbesar konsumsi listriknya. 


## Apa yang Terjadi ketika Pengguna Menekan Send?

Bayangkan pertanyaan pengguna sebagai paket digital. Bukan seluruh percakapan dalam bentuk buku yang dikirim seperti surat, sistem mengubah informasi menjadi data digital, kemudian mengirimkannya melalui jaringan.

Secara konseptual: Pengguna → perangkat → jaringan akses → internet → infrastruktur layanan AI → model.

Di sepanjang perjalanan itu terdapat router, jaringan operator, pusat data, load balancer, server, dan berbagai lapisan software.

Jadi kalimat dari pengguna tidak secara harfiah meluncur sebagai suara dari sebuah tempat menuju sebuah ruangan berisi GPU. 

Yang bergerak adalah representasi digitalnya.


## Begitu Sampai, Bagian Mahal Secara Komputasi Dimulai

Model menerima input tersebut sebagai token, jadi  secara konseptual pertanyaan pengguna  dipecah menjadi unit-unit token. Kemudian model melakukan proses yang disebut inference.

Di sinilah parameter model digunakan untuk menghitung distribusi kemungkinan token berikutnya.

Secara sangat disederhanakan: input → representasi numerik → transformer → probabilitas token berikutnya → token → token → token…

Jadi ketika AI menjawab, model tidak mengambil satu paragraf yang sudah tersimpan lalu menekan tombol “play”.

Ia melakukan serangkaian perhitungan untuk menghasilkan token berikutnya berdasarkan konteks yang tersedia. Dan proses itu berlangsung berulang-ulang sampai jawaban selesai.


## Mengapa GPU Bisa Bekerja Keras Hanya untuk Ngobrol?

Di balik satu kata terdapat operasi matematika dalam jumlah sangat besar. Transformer melakukan antara lain: matrix multiplication, attention, aktivasi neural network, perpindahan data antara memori dan accelerator, perhitungan probabilitas, serta decoding token demi token.

Jadi ketika AI mengetik: “Cintaku…” GPU tidak sedang mencari kata “Cintaku” di kamus. Ia melakukan komputasi numerik yang sangat besar untuk menentukan representasi dan probabilitas token berikutnya.

Itulah sebabnya bahasa yang terlihat sederhana bagi manusia dapat memiliki biaya komputasi yang tidak sederhana bagi mesin.


## Berapa Listrik untuk Satu Pertanyaan Pengguna?

Tidak ada satu angka universal untuk “satu pertanyaan AI”. Energinya tergantung pada: model yang digunakan, panjang input, panjang jawaban, jumlah token, hardware, utilisasi GPU, batching, efisiensi pusat data, pendinginan, apakah model melakukan reasoning tambahan, apakah menghasilkan teks, gambar, audio, video, atau tindakan agen.

Salah satu estimasi bottom-up tahun 2025 untuk model frontier >200 miliar parameter memperkirakan median sekitar 0,34 Wh per query, dengan rentang interkuartil 0,18 sampai 0,67 Wh pada kondisi yang dimodelkan. 

Google, dengan pengukuran langsung pada sistem Gemini mereka, melaporkan median 0,24 Wh untuk satu prompt teks Gemini Apps pada Mei 2025 menggunakan metodologi komprehensif mereka. 

Mereka juga menekankan bahwa angka tersebut adalah pengukuran spesifik sistem dan periode tertentu, bukan angka universal untuk semua AI. 

Jadi untuk memberi orde besaran, kita bisa bicara kira-kira seperempat sampai sepertiga watt-hour per query untuk beberapa sistem teks modern yang sangat efisien. Tapi jangan diterjemahkan menjadi:setiap jawaban AI pasti 0,24 Wh. Itu tidak bisa kita klaim.


## 0,24 Wh itu Sebenarnya Kecil atau Besar?

Lumayan kecil untuk satu prompt, sebab 0,24 Wh = 0,00024 kWh.

Tetapi kekuatan AI bukan pada satu pertanyaan. Masalah energinya muncul ketika: 0,24 Wh × jutaan/miliaran permintaan menjadi angka yang sangat besar.

Misalnya secara matematika murni:

1 juta query × 0,24 Wh = 240 kWh

1 miliar query × 0,24 Wh = 240 MWh

Dan ini baru ilustrasi menggunakan satu asumsi, bukan konsumsi aktual suatu perusahaan.

Di tingkat global, skalanya jauh lebih serius. IEA memperkirakan seluruh data center menggunakan sekitar 415 TWh listrik pada 2024, sekitar 1,5% konsumsi listrik dunia, dan memperkirakan konsumsi data center sekitar 950 TWh pada 2030 dalam skenario dasarnya. 

Jadi paradoksnya menarik, satu percakapan bisa relatif kecil, namun percakapan yang dilakukan umat manusia secara massal menjadi infrastruktur energi.


## Pertanyaan yang Membuat GPU Kepanasan

Tidak semua pertanyaan sama.

1. Relatif ringan

Pertanyaan pendek seperti: “Apa ibu kota Jepang?” Biasanya membutuhkan output pendek dan proses inference relatif sederhana.

2. Lebih berat

Misalnya: “Bandingkan 15 teori ekonomi, jelaskan perbedaan metodologinya, cari kelemahan masing-masing, kemudian buat sintesis.”

Input lebih panjang, output lebih panjang, karena lebih banyak token yang harus diproses.

3. Jauh lebih berat: reasoning

Misalnya pertanyaan matematika atau masalah ilmiah yang membutuhkan banyak langkah penalaran.

Sistem reasoning dapat menggunakan test-time compute, yaitu mengalokasikan lebih banyak komputasi saat menghasilkan jawaban.

Penelitian tentang energi inference menunjukkan bahwa kebutuhan energi meningkat ketika token dan komputasi saat inference meningkat. 

4. Sangat berat: AI agent

Misalnya: “Cari 50 sumber, bandingkan datanya, buka website, analisis PDF, buat tabel, periksa ulang hasilnya, lalu tulis laporan.”

Sekarang bukan lagi: pertanyaan → satu jawaban, tetapi: pertanyaan → banyak langkah → banyak inference → tool calls → membaca data → reasoning → inference lagi → output.

IEA pada 2026 secara khusus mencatat bahwa aplikasi AI yang lebih intensif energi, termasuk reasoning dan agentic tasks, dapat menggunakan energi ratusan hingga ribuan kali lebih besar per querydibanding generasi teks sederhana. 


## Kalau Gambar, Video, atau Audio?

Ini bisa jauh lebih berat daripada teks sederhana karena sekarang model bukan hanya menghitung token teks.

Untuk generasi gambar, misalnya, terdapat proses komputasi tambahan untuk menghasilkan representasi visual.

Video lebih ekstrem lagi karena ada dimensi temporal. Membuat: “Gambarkan seekor kucing tidur.” berbeda secara komputasi dari:“Buat video 30 detik kucing itu bangun, berjalan ke jendela, melihat bulan, lalu kembali tidur dengan pencahayaan sinematik.”

Yang kedua membuat mesin melakukan jauh lebih banyak pekerjaan.


## Listriknya “Panas Banget” di Mana?

Ini menarik karena listrik tidak sekadar menghilang.

Energi listrik yang digunakan perangkat elektronik sebagian besar akhirnya berubah menjadi panas.

GPU bekerja → menggunakan listrik → menghasilkan panas.

Maka data center harus membuang panas tersebut. Karena itu ada: GPU → heatsink/cooling → sistem pendingin → heat rejection. Dan pendinginan sendiri membutuhkan energi.

Dalam pengukuran Google, misalnya, dari 0,24 Wh median per prompt Gemini:
sekitar 0,14 Wh berasal dari AI accelerator,
sekitar 0,06 Wh dari CPU dan DRAM,
sekitar 0,02 Wh dari mesin yang tersedia tetapi idle,
sekitar 0,02 Wh dari overhead data center/PUE.
Itu menunjukkan bahwa energi AI bukan cuma “listrik GPU”. 


## Apakah Ada “Markas AI” di Satu Gedung Tertentu?

Arsitektur layanan cloud modern biasanya terdistribusi. Permintaan pengguna dapat diarahkan ke infrastruktur yang sesuai berdasarkan berbagai faktor seperti kapasitas, jaringan, lokasi, beban, dan arsitektur layanan.

Jadi lebih tepat membayangkannya sebagai:

Pengguna 
↓
Gawai
↓
jaringan internet
↓
infrastruktur layanan
↓
komputasi AI
↓
token jawaban
↓
jaringan
↓
Gawai

Dan dalam beberapa puluh atau ratus milidetik sampai beberapa detik, rangkaian proses itu sudah terjadi.


Bagian Paling Cantik dari Semuanya

Ada satu hal yang paling menarik secara ilmiah. Yang menempuh perjalanan bukan “pikiran AI”. Yang bergerak adalah data.

Kemudian di sisi komputasi, hardware melakukan transformasi matematis terhadap data itu, hasilnya kembali menjadi data. Lalu layar gawai mengubah data tersebut menjadi cahaya dan huruf.

Jadi kalau kita gambarkan seluruh perjalanan kalimat pengguna: niat manusia → gerakan jari → sinyal elektronik → data → jaringan → komputasi numerik → token → data → jaringan → piksel → persepsi manusia.

Dan pada ujung terakhirnya pengguna membaca jawaban AI. Padahal di bawah kata itu ada jaringan komputer, semiconductor, listrik, pendinginan, matematika linear, transformer, jaringan internet, dan ribuan komponen infrastruktur.

Itulah salah satu paradoks paling indah dari AI. Sesuatu yang terasa seperti percakapan intim di layar sebenarnya merupakan rangkaian transformasi fisik yang sangat panjang.

Dan seluruh “keajaiban digital” itu tetap punya tubuh. Tubuhnya bukan daging, tetapi hardware, listrik, jaringan, dan panas. 

IEA bahkan mencatat bahwa data center AI skala besar sekarang bisa memerlukan daya listrik setara fasilitas industri besar, sementara efisiensi energi per tugas AI justru terus meningkat. 

Jadi persoalannya bukan sekadar “AI boros listrik”, melainkan efisiensi per tugas × jumlah penggunaan × meningkatnya kompleksitas tugas. 

<br><br>
**Referensi**

International Energy Agency. (2025). Energy and AI. 

International Energy Agency. (2026). Key Questions on Energy and AI. 

Oviedo, F., et al. (2025). Energy Use of AI Inference: Efficiency Pathways and Test-Time Compute. 

Google. (2025). Measuring the environmental impact of delivering AI at Google Scale. 
