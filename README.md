# Soal test maggang Quality Assurance engineer

Berikut adalah soal/pertanyaan yang perlu dijawab oleh peserta

## knowledge base

1. Apa yang anda ketahui tentang Rest API?
Jawab : Jenis API layanan web yang menggunakan permintaan HTTP untuk melakukan operasi CRUD. Rest API memungkinakn sistem untuk berkomunikasi melalui protocol HTTP (Hypertext Transfer Protocol) dengan memanfaatkan metode seperti GET, POST, PUT, DELETE, dll.

2. Apa yang anda ketahui tentang Server side and Client side processing?
Jawab : Server side processing adalah pemrosesan data dan logika aplikasi terjadi di server tempat aplikasi web di host. Sedangkan Client side processing adalah pemrosesan data dan logika aplikasi terjadi di perangkat client (seperti browser) setelah mendapatkan halaman web dari server.

3. Apa yang anda ketahui tentang Monolith dan Microservices, berikan contohnya?
Jawab : Microservices adalah sebuah pendekatan arsitektur perangkat lunak di mana sebuah aplikasi besar dibangun sebagai kumpulan layanan kecil yang independen. Setiap layanan memiliki fokus pada satu tugas atau fungsionalitas spesifik dalam aplikasi dan berkomunikasi dengan layanan lainnya melalui antarmuka jaringan.

4. Apa yang anda ketahui tentang Automation testing serta sebutkan contohnya?
Jawab : Biasa disebut juga automation testing atau automated QA testing, praktik yang menjalankan pengujian perangkat lunak secara otomatis untuk memeriksa bug,Berkaitan dengan proses mengeksekusi test case, memelihara test data, menganalisis test result dengan menggunakan alat khusus yang memungkinkan pembuatan skenario pengujian dan eksekusinya secara otomatis. Beberapa contoh alat test automation populer termasuk Katalon, Selenium, Appium, Cucumber, dan Robot Framework. Automation testing adalah proses penggunaan tools dan skrip otomatis untuk melakukan pengujian perangkat lunak secara otomatis, tujuannya adalah untuk meningkatkan efisiensi, konsistensi, dan akurasi pengujian perangkat lunak dengan manual testing. Contoh jenis-jenis dari automation testing seperti unit testing, integration testing, functional testing, load testing, performance testing, regression testing, smoke testing, API testing.

5. Dengan menggunakan tools automation testing tersebut, biasanya menggunakan bahasa/tools apa?
Jawab : Tools yang biasa digunakan Ketika melakukan automation testing yaitu katalon dan selenium dengan menggunakan bahasa pemrograman java.


## Use cases

Suppose there was a transaction that had been done in tokopedia.com , the transaction
id should be available on the screen alongside with the address of shipment, date of
order, seller’s name, and delivery service (JNE/POS/REX/others). 
The transaction id (TRX_ID) should also be available on the database which again supposedly there was a simple table containing all the transaction data.

![success notif](imgs/trx-notif.png)

![tabel transaksi](imgs/table-trx.png)

Apparently, the order `01023A9AC` seems to have different Delivery Service on the UI and the
database record. How do you, as automation test developers develop such test scenario so that
this kind of error does not occur?

Jawab :
Use Case 1 : Menampilkan Detail Transaksi di Halaman Tokopedia

Aktor Utama : Pengguna
Deskripsi : Pengguna ingin melihat detail transaksi yang telah dilakukan di tokopedia.com

Langkah-langkah :
1. Pengguna membuka situs tokopedia.com dan masuk ke akunnya.
2. Pengguna mengklik menu "Transaksi"
3. Sistem menampilkan daftar transaksi yang telah dilakukan pengguna.
4. Pengguna memilih salah satu transaksi untuk melihat detailnya.
5. Sistem menampilkan detail transaksi yang terdiri dari:
a. Transaction ID (TRX_ID)
b. Alamat pengiriman (Address_Ship)
c. Tanggal pemesanan (Date_Order)
d. Nama penjual (Seller_Name)
e. Layanan pengiriman (Delivery_Service) (JNE/POS/REX/dll)

Use Case 2 : Memeriksa Ketersediaan TRX_ID di Database

Aktor Utama : Sistem
Deskripsi : Sistem harus memastikan bahwa Transaction ID (TRX_ID) dan transaksi yang ditampilkan di halaman Tokopedia juga ada dalam database.

Langkah-Langkah :
1. Sistem mengakses database transaksi.
2. Sistem mengambil TRX_ID dari transaksi yang ditampilkan di halaman tokopedia.
3. Sistem memeriksa apakah TRX_ID tersebut ada dalam tabel database.
4. Jika TRX_ID ditemukan, sistem melanjutkan operasi berikutnya. Jika tidak, sistem menampilkan pesan kesalahan.