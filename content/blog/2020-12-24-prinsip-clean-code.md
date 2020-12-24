title: Prinsip Clean Code  
date: 2020-12-24 18:25  
tags: clean-code, programming, tips, blogs  
slug: prinsip-clean-code  
summary: Prinsip clean code dalam pemrograman.

> Ketika kita mulai belajar pemograman, apa yang kita pelajari pertama kali?, pasti `syntax` bahasa pemrograman. Ketika kita menemukan `error/bugs`, apa yang pertama kali kita lihat?, pasti kode kita. Ketika kita diskusi di forum programmer, apa yang paling sering menjadi topik pembahasan?, Jawabannya `best practice programming`, `library/framework` yang sendang tenar, update IDE terbaru, dsb.  


Semua hal diatas tak lepas dari yang namanya “kode”. Bahkan sudah tertanam di alam bawah sadar kita, definisi programmer adalah orang yang menulis kode alias *“tukang ngoding”*. Pernyataan Itu tidaklah salah, tetapi juga tidak sepenuhnya benar. Banyak kemampuan lain  yang harus diasah agar menjadi programmer yang handal. Salah satunya adalah kemampuan menulis dan bercerita.  

# Loh, buat apa programmer bercerita?.  

Saya ambil quotes yang cukup terkenal di dunia pemrograman, **_“Code is read more often that it is written”_**. Yang maksudnya adalah, sebagai programmer kita akan lebih sering membaca (dan memahami) kode daripada menulisnya. Ketika kita membangun sebuah software, kita akan berulang kali membaca kode kita. Entah itu karena terdapat error, mengecek konsistensi kode kita atau bahkan ketika kita lupa tugas apa yang dikerjakan kode tersebut. oleh karena itu, lahirlah prinsip `“clean code”`, yang pada intinya kita harus mengikuti prinsip ini agar kode kita mudah dipahami oleh orang lain. Ketika kode kita mudah dipahami, disitulah kode kita mampu "bercerita".

Berikut beberapa aspek penting dalam penerapan prinsip clean code:

## Sistem Penamaan yang Baik.  
Dalam menentukan nama variabel dan function, kita sebaiknya mengikuti konvensi/acuan umum yang berlaku pada bahasa/framework yang digunakan. Selain itu, pastikan namanya tidak ambigu dan mewakili tugas apa yang dilakukannya.  
  
**DO's**  

```python
def harga_tanah(luas_tanah):
    return luas_tanah*500000
```  


**DON'Ts**  

```python
def hrgTnh(l):
    return l*500000
```

## Menuliskan Komentar Secara efisien  
Mungkin kita pernah berpikir, semakin banyak komentar yang kita tulis pada kode kita, maka semakin jelas & mudah dipahami kode tersebut. _well_, sebenarnya tidak juga. Ketika kita menulis kode kita dengan baik (sistem penamaan yang baik, indentasi yang rapi, dsb), kita tidak perlu menuliskan banyak komentar. Jadi, dalam menuliskan komentar, pastikan komentar itu dibuat karena bagian itu memerlukan penjelasan ekstra. Bukan karena penulisan kode yang buruk.  

  
**DO's**  

```python
# Menghitung harga tanah dan mengembalikan (return) hasilnya
def harga_tanah(luas_tanah):
    return luas_tanah*500000
```  


**DON'Ts**  

```python
# menghitung hrg tanah
def hrgTnh(l):
    return l*500000 # 'l' adalah variabel luas tanah
```  
> kita tak perlu lagi memberi komentar untuk variabel l ketika kita sudah menggunakan sistem penamaan yang baik.  

---

## **_Best Practice_ dalam menulis komentar**  


- Tuliskan outline/gambaran umum kegunaan dari kode tersebut. sehingga kita mendapat gambaran fungsi kode tersebut secara cepat tanpa harus memahaminya secara mendetail (code skimming)    

- tuliskan komentar pendek pada function/method yang kompleks, yang menggambarkan kegunaannya.  
**P.S.** Untuk function yang bersifat publik, wajib menuliskan docstring yang sesuai pada **semua** function       

- Jangan menggunakan kata-kata kasar. Sering kali kode kita dilihat/review orang lain. Tentu sebagai orang waras, kita tidak ingin mempermalukan diri kita dengan komentar bernada kasar.    

- Hindari komentar "WET", alias Wrote everything twice. maksudnya, apabila kode kita sudah clear & mudah dipahami, kita tidak perlu menuliskan komentar lagi.    

contoh:  

```python
return hasil # return hasil
```     
> komentar pada kode diatas tidak berguna dan hanya buang-buang waktu karena sama sekali tidak membantu (hanya ditulis ulang kodenya)    


## Penulisan Function yang efektif  
Dalam bebeberapa kasus mungkin kita ingin memasukkan beberapa perhitungan/tugas dalam sebuah function sekaligus. Hal ini sebaiknya dihindari, karena dapat menimbulkan kerancuan dan berpotensi menghasilkan bugs. Pastikan satu function hanya mengerjakan satu tugas saja. 

**DO's**  

```python
# Menghitung harga tanah dan mengembalikan (return) hasilnya
def harga_tanah(luas_tanah):
    return luas_tanah*500000

# menghitung persentase makelar
def makelar(harga_tanah):
    return 0.05*harga_tanah # 0.05 sama dengan 5%

harga_tanah_ali = harga_tanah(2000)
uang_makelar = makelar(harga_tanah_ali).

```  


**DONT's**  

```python
# menghitung harga tanah dan makelar
def harga_tanah_dan_makelar(luas_tanah):
    harga_tanah = luas_tanah*500000
    uang_makelar = 0.05*harga_tanah
    return [harga_tanah,uang_makelar] 
```  

> Kode diatas tidak efisien,karena apabila kita kita hanya memerlukan salah satu output saja, kode tersebut tetap melakukan dua kali perhitungan. Selain itu, return yang dihasilkan berupa list, sehingga kita perlu menentukan secara spesifik return mana yang ingin kita gunakan. Hal ini tentu membingungkan dan berpotensi menghasilkan bugs pada kode kita.  

## Exception Handling   
Ketika kode kita semakin banyak dan kompleks, potensi menghasilkan bugs/error juga semakin besar. Sebagai programmer kita tentu tidak ingin menghabiskan waktu mencari bugs yang _“tidak terlihat”_. Kita tentu ingin ada warning yang jelas mengenai bugs/error tersebut. disinilah exception handling berperan. Dengan exception handling, kita bisa memprediksi error yang berpotensi muncul, dan cara mengatasinya, sehingga software/kode kita tetap bisa berjalan.  

**DO's**  

```python
def harga_tanah(luas_tanah):
    try:
        return float(luas_tanah*500000)
    except Exception as e:
        if ValueError:
            print('Inputan Harus Berupa Angka!')
        else:
            print(e)
```  


**DONT's**  

```python
def harga_tanah(luas_tanah):
    try:
        return float(luas_tanah*500000)
    except Exception as e:
        print('aku ngga tau harus ngapain')
```  

## Don't Repeat Yourself (DRY)  

Ketika kita berulang kali menulis kode dengan logika yang sama, ada baiknya kita mempertimbangkan untuk membuat function untuk melakukan tugas tersebut. hal ini supaya tidak terdapat duplikasi kode serta membuat kode kita lebih modular dan terstruktur.  


**Daripada Seperti ini**  

```python
harga_tanah_ali = 2000*500000
print(harga_tanah_ali)

harga_tanah_budi = 1000*500000
print(harga_tanah_budi)

harga_tanah_cici = 3500*500000
print(harga_tanah_cici)
```  


**lebih Baik Seperti Ini**  

```python
def harga_tanah(luas_tanah):
    return luas_tanah*500000  

harga_tanah_ali = harga_tanah(2000)
harga_tanah_budi = harga_tanah(1000)
harga_tanah_cici = harga_tanah(3500)

print(f'{harga_tanah_ali}\n{harga_tanah_budi}\n{harga_tanah_cici}')
```  
> dengan menggunakan function seperti diatas, kita tidak perlu menuliskan kode yang sama berulang kali. selain itu, kita juga bisa menggunakannya di tempat lain atau bahkan di project lain (modular). hal ini tentu sangat berguna untuk meningkatkan efisiensi kita sebagai programmer.  

## Keep It Simple St*pid (KISS)  

Prinsip ini pada dasarnya memaksa kita untuk menuliskan kode sesederhana mungkin. Prinsip KISS mengharuskan kita untuk memikirkan `logic` kode kita sebelum kita tulis. pastikan logic tersebut sederhana dan mudah dipahami. Prinsip ini juga mengharuskan kita memisahkan function-function dengan logic yang berbeda. Hal ini agar kode kita tidak menjadi _"spaghetti code"_ serta mudah dalam menemukan dan mengatasi bugs yang muncul.  


## Penutup  
Sebagai programmer, kita akan sering bekerja sama dengan programmer lain. kita akan sering memodifikasi kode yang dibuat orang lain. Tanpa prinsip clean code, kita tentu akan kesulitan memahami kegunaan kode tersebut. Sehingga proses pembangunan software tersendat. Dengan penerapan clean code, komunikasi dan kolaborasi antar programmer menjadi lebih baik.

Prinsip clean code juga memastikan software yang kita bangun lebih mudah dipelihara. Selain itu dengan penerapan clean code, kita akan lebih mudah dalam menambah fitur dan lebih mudah dalam mengatasi bugs. yang pada akhirnya efisiensi dan produktivitas kita sebagai programmer meningkat.
