# Image Compressor with Quadtree Implementation
Kompresor gambar menggunakan Quadtree yang mengimplementasikan prinsip Divide and Conquer dalam bahasa Java.

Program mengambil input gambar yang ingin dikompres, metode perhitungan persebaran warna, nilai threshold, ukuran minimal subblok dan direktori output gambar dan mengeluarkan gambar yang telah dikompresi pada output yang telah ditentukan serta data-data quadtree yang dibuat.

Program menghitung nilai persebaran warna dari gambar input berdasarkan metode yang dapat dipilih, dan menentukan apakah gambar akan dibagi menjadi 4 subblok.
Ketentuan blok yang akan dibagai adalah, apakah nilai persebaran warna melebihi input threshold dan pembagian blok tidak akan menyebabkan ukuran subblok hasil pembagian menjadi lebih kecil dari ukuran minimal yang telah dimasukkan. Apabila tidak memenuhi ketentuan tersebut, blok tersebut akan menjadi warna yang merupakan warna rata-rata dari semua blok pada blok tersebut.

# Requirement program
* Java 23 atau versi terbaru

# Cara Kompilasi Program
Untuk menjaga srtuktur folder, kompilasikan program di dalam folder root dan gunakan command berikut untuk mengkompilasi program

` javac -d bin src/Quadtree.java `

Hasil kompilasi akan muncul di folder `bin`

# Cara Menjalankan Program

1. Jalankan program di dalam folder root dengan command `java -cp bin Quadtree`

2. Masukkan input direktori gambar yang ingin dikompresi.
   
   Direkomendasikan untuk membuat folder baru untuk input, lalu masukkan direktori untuk gambar di folder tersebut.
   
   Direktori dapat berupa alamat absolut (e.g. `C:\User\foo\input\input.jpg`) atau alamat relatif terhadap folder root (e.g. `input/input.jpg`)

3. Masukkan metode perhitungan persebaran warna yang diinginkan dengan keyword berikut untuk masing-masing metode

   Metode yang tersedia :

   + Variance (`var`)
   + Mean Absolute Deviation (`map`)
   + Maximum Pixel Difference (`mpd`)
   + Entropy (`ent`)
  
4. Masukkan nilai threshold untuk nilai persebaran warna.
5. Masukkan nilai ukuran blok minimal.
6. Apabila muncul pesan `Gambar berhasil dibaca!`, gambar berhasil terbaca tanpa error.
7. Tunggu sampai muncul pesan `Gambar berhasil dibuat`.
8. Gambar yang telah dikompresi akan muncul di folder output yang telah ditentukan dan data-data tentang quadtree yang telah dibuat akan muncul di terminal.

## Troubleshoot

+ #### Hasil kompresi hanya memiliki satu blok warna

  Kemungkinan gambar terlalu monokrom sehingga nilai persebaran warnanya akan sangat kecil. Kurangi nilai threshold.

  Khususnya metode entropi, gunakan nilai threshold antara 1-5.

+ #### Gambar tidak terbaca.

  Cek lagi penulisan direktori input



