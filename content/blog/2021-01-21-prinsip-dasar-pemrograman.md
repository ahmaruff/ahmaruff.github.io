title: Prinsip Dasar Pemrograman  
date: 2021-01-21 18:05  
tags: programming, blogs, basic  
slug: prinsip-dasar-premrograman  
summary: Apa itu pemrograman? Apa saja prinsip dasarnya?.  

Apa yang membuat kalian tertarik dengan dunia IT?, Ingin menjadi hacker?, bekerja di startup ternama?, atau terinspirasi dengan Elon Musk?. Tentu setiap orang memiliki alasan dan motivasi masing-masing ketika terjun ke dunia IT. 

Didalam dunia IT yang sangat luas, terdapat satu hal yang harus dikuasai, yaitu kemampuan pemrograman. Bagi kalian yang baru memasuki dunia IT, mungkin masih bingung dengan konsep "pemrograman", dll. Pada artikel ini, kita akan membahas apa itu pemrograman, dan konsep dasar dari pemrograman. _check this out!_   

# Apa itu Pemrograman

Pengertian paling sederhana dari pemrograman adalah sekumpulan instruksi untuk menyelesaikan masalah yang spesifik. Dalam pengertian dini, banyak kegiatan sehari-hari dapat dikategorikan sebagai pemrograman; kegiatan tersebut memiliki instruksi spesifik yang dilakukan dalam urutan tertentu.

Contoh sederhananya adalah sebuah resep makanan. Kita bisa melihat resep sebagai sebuah program yang berfungsi untuk mereproduksi produk (makanan), tanpa harus dibantu oleh pembuat asli makanan tersebut. Ketika menjalankan instruksi pada resep dengan benar dan berurutan, maka hasil makanannya akan serupa dengan buatan si pembuat asli makanan tersebut (pembuat resep).

Dalam konteks komputasi, pemrograman merupakan suatu proses membuat sekumpulan (set) instruksi yang dimengerti oleh komputer dalam rangka untuk menyelesaikan suatu masalah spesifik. 

Karena komputer hanya mengenal angka 0 dan 1, maka akan sangat sulit bagi kita untuk menulis program komputer secara langsung menggunakan bilangan biner. Oleh karena itu, kita memerlukan alat bantu, yang bertugas menjadi jembatan komunikasi antara kita dengan komputer. Alat bantu tersebut dikenal sebagai “bahasa pemrograman”. Sebuah bahasa yang dimengerti oleh komputer dan programmer itu sendiri. melalui bahasa pemrograman, kita memberi instruksi kepada komputer untuk melakukan tugas tertentu.

Pada umumnya sebuah program untuk komputer dibuat untuk menyelesaikan masalah yang memiliki ciri-ciri sebagai berikut:

- Berulang. Sebuah masalah yang dilakukan berulang-ulang, yang melampaui kesabaran manusia jika dilakukan secara manual.

- Kontrol mesin pada kondisi yang tidak mungkin dilakukan oleh manusia karena keterbatasan fisik atau kondisi berbahaya.

- Sebuah masalah yang memerlukan akurasi dan konsistensi yang tinggi.

- Sebuah masalah yang memerlukan kecepatan pemrosesan yang tinggi.

---

# Konsep Dasar Pemrograman

Meskipun setiap bahasa pemrograman memiliki aturan dan keunikan masing-masing, terdapat beberapa konsep yang umum ditemukan di semua bahasa pemrograman tersebut, diantaranya:

1. **Urutan Instruksi/Perintah**

Membuat instruksi yang benar tentu sangat penting, akan tetapi instruksi tersebut juga harus disusun dengan urutan yang benar. Misal instruksi untuk membuat kopi,  apabila instruksi mengaduk kopi dilakukan terlebih dahulu sebelum kopi dan air dimasukkan kedalam gelas, tentu membuat instruksi tersebut ambigu dan hasil yang diinginkan tidak tercapai.

Pun begitu, dalam beberapa kasus, urutan instruksi bukan merupakan kewajiban. Sering kali dalam kasus tersebut, dibuat sebuah konvensi/urutan yang disepakati bersama untuk menghindari kerancuan. contohnya dalam penulisan alamat rumah yang biasanya memiliki urutan sebagai berikut:

```
Nama Lengkap
Jalan, RT/RW, No. rumah
Kelurahan,Kecamatan,
Kabupaten/kota, KODE POS
Provinsi
```

Urutan tersebut disepakati untuk mempermudah & mempercepat proses mengidentifikasi alamat seseorang.

2. **Struktur Percabangan/Kondisi Bersyarat**

Biasanya berupa pertanyaan kondisi. sekumpulan/blok instruksi akan dilakukan ketika kondisi tersebut terpenuhi. Dan apabila tidak terpenuhi, maka blok instruksi tersebut diabaikan dan lakukan instruksi lainnya.

Pada umumnya, struktur percabangan tersebut berupa **if**... **then**... **else**...

yang berarti**jika** ...(kondisi terpenuhi)... **maka**...(lakukan ini)... **atau jika tidak terpenuhi**...(lakukan itu)... 

contoh:

```python
if nilai >= 75:
    print("Kamu lulus")
else:
    print("Siap-siap remidial ya!")
```

_Penjelasan kode diatas:_  

`if nilai >=75` ini merupakan kondisi/syaratnya. jika (`if`) kondisi ini terpenuhi, maka komputer akan menjalankan perintah `print("Kamu lulus")`serta mengabaikan perintah dibawahnya. 

Sedangkan jika kondisi tidak terpenuhi (`else`), maka perintah diatas akan diabaikan, dan akan langsung menjalankan perintah `print("Siap-siap remidial ya!")`

3. **Struktur Perulangan/Loop**

Struktur ini dipakai agar komputer mengulang sekumpulan/blok instruksi yang sama. perulangan bisa dibuat dengan menentukan banyaknya perulangan yang diinginkan, atau selama sebuah kondisi tidak berubah/ masih bernilai benar. contoh:

```
Lakukan instruksi A sebanyak 10 kali
---
Lakukan instruksi B sebanyak jarak antara angka 1 sampai 5
---
Lakukan instruksi C secara terus menerus ketika waktu == jam makan siang
```



Konsep dasar pemrograman sangat penting untuk dipahami, karena mempermudah kita dalam mempelajari pemrograman. Konsep ini juga melatih logika dan kemampuan _computational thinking_ kita.

Selain itu, konsep dasar pemrograman ini muncul pada hampir semua bahasa pemrograman. Sehingga kita dapat memahami logika dari sebuah kode, meskipun kita belum menguasai bahasa pemograman yang digunakan pada kode tersebut.  

------  

Referensi:

[Programming Concepts](http://livecode.byu.edu/programmingconcepts/ControlStruct.php)


