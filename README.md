# Lab2web - praktikum2

### 1. Membuat dokumen HTML 

Buatlah dokumen HTML seperti berikut 

```html
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>CSS Dasar</title> 
</head> 
<body> 
    <header> 
        <h1>CSS Internal dan <i>Inline CSS</i></h1> 
    </header> 
    <nav> 
        <a href="lab2_css_dasar.html">CSS Dasar</a> 
        <a href="lab2_css_eksternal.html">CSS Eksternal</a> 
        <a href="lab1_tag_dasar.html">HTML Dasar</a> 
    </nav> 
    <!-- CSS ID Selector --> 
    <div id="intro"> 
        <h1>Hello World</h1> 
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>.
          Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p> 
        <!-- CSS Class Selector --> 
        <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>     </div> 
</body> 
</html>
```

#### ```hasil```
![foto](https://github.com/azkaa-pixel/Lab2web-praktikum1-smt3/blob/1c8aff8e50c89dec3dfc9ebb45694df73e3f568f/ss%20parktikum%202%20smt3/ss%201.jpeg)

#### ```- penjelasan``` :

- ```<header>``` untuk bagian kepala halaman.

- ```<nav>``` berisi menu navigasi.

- ```id="intro"```disiapkan untuk styling khusus dengan CSS.
  
- ```class="button btn-primary"``` disiapkan agar tombol bisa diberi gaya tertentu.

  
### 2. Mendeklarasikan CSS Internal

Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen. 

```html
<head> 
    <title>CSS Dasar</title> 
    <style>         body { 
            font-family:'Open Sans', sans-serif; 
        }         header { 
            min-height: 80px; 
            border-bottom:1px solid #77CCEF; 
        }         h1 { 
            font-size: 24px; color: #0F189F; text-align: center; padding: 20px 10px; 
        }         h1 i { 
            color:#6d6a6b; 
        } 
    </style> 
</head>
```

#### ```hasil``` 
![foto](https://github.com/azkaa-pixel/Lab2web-praktikum1-smt3/blob/1c8aff8e50c89dec3dfc9ebb45694df73e3f568f/ss%20parktikum%202%20smt3/ss2.jpeg)

#### ```- penjelasan``` :

- CSS ditulis di ```<style>``` → disebut internal CSS.

- ```body``` mengatur font halaman.

- ```header``` diberi tinggi minimal dan garis bawah.

- ```h1``` mengatur ukuran, warna, posisi judul.

- ```h1 i``` memberi warna abu-abu pada teks miring di dalam judul.
  

### 3. Menambahkan Inline CSS 

Kemudian tambahkan deklarasi inline CSS pada tag <p> seperti berikut. 

``` html
<p style="text-align: center; color: #ccd8e4;">
```

#### ```hasil``` 
![foto](https://github.com/azkaa-pixel/Lab2web-praktikum1-smt3/blob/1c8aff8e50c89dec3dfc9ebb45694df73e3f568f/ss%20parktikum%202%20smt3/ss3.jpeg)

#### ```- penjelasan``` :

- ```style="..."``` disebut inline CSS.

- ```text-align: center;``` membuat teks rata tengah.

- ```color: #ccd8e4;``` memberi warna biru muda.


### 4. Membuat CSS Eksternal 

Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut. 

```html
nav { 
    background: #20A759; color:#fff; padding: 10px; 
} nav a {color: #fff; text-decoration: none; padding:10px 20px; 
} 
nav .active,  nav a:hover { 
    background: #0B6B3A; 
} 
```
Kemudian tambahkan tag <link> untuk merujuk file css yang sudah dibuat pada bagian <head> 
```html
<head> 
    <!-- menyisipkan css eksternal --> 
    <link rel="stylesheet" href="style_eksternal.css" type="text/css"> 
</head>
```

#### ```hasil``` 
![foto](https://github.com/azkaa-pixel/Lab2web-praktikum1-smt3/blob/1c8aff8e50c89dec3dfc9ebb45694df73e3f568f/ss%20parktikum%202%20smt3/ss4.jpeg)

#### ```- penjelasan``` :

- CSS diletakkan di file ```.css``` → disebut eksternal CSS.

- ```<link>``` menghubungkan HTML dengan file CSS.

- ```nav``` memberi warna dan padding pada menu.

- ```nav a:``` hover memberi efek saat link disentuh kursor.

### 5. Menambahkan CSS Selector 
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut. 
```html
/* ID Selector */ 
#intro { 
    background: #418fb1;     border: 1px solid #099249;     min-height: 100px;     padding: 10px; 
} 
#intro h1 {     text-align: left;     border: 0;     color: #fff; 
} 
 
/* Class Selector */ 
.button { 
    padding: 15px 20px;     background: #bebcbd;     color: #fff;     display: inline-block;     margin: 10px; 
    text-decoration: none; 
} 
.btn-primary { 
    background: #E42A42; 
} 
```
#### ```hasil``` 
![foto](https://github.com/azkaa-pixel/Lab2web-praktikum1-smt3/blob/1c8aff8e50c89dec3dfc9ebb45694df73e3f568f/ss%20parktikum%202%20smt3/ss5.jpeg)

#### ```- penjelasan``` :
- ```#intro``` adalah ID selector, hanya berlaku untuk elemen dengan ```id="intro"```.

- ```.button``` dan ```.btn-primary``` adalah Class selector, bisa dipakai berulang di banyak elemen.

- Kombinasi ID dan Class membuat tampilan halaman lebih fleksibel dan konsisten.

# PERTANYAAN DAN TUGAS
1.	Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
   
2.	Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
   
3.	Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
   
4.	Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!  ```( <p id="paragraf-1" class="text-paragraf"> )```

# Jawaban 

## 1. hasil eksperimen
   
![foto](https://github.com/azkaa-pixel/Lab2web-praktikum1-smt3/blob/ae5a3dc03912c8ab77e40fbf31d7af98c93f2860/ss%20parktikum%202%20smt3/tugas%20no1.jpeg)
   
## 2. Perbedaan ```h1 {...}``` dengan ```#intro h1 {...}```

```h1 {...}``` → semua elemen ```<h1>``` di halaman akan kena aturan.

```#intro h1 {...}``` → hanya ```<h1>``` yang ada di dalam elemen dengan id="intro" yang kena.

## 3. Kalau ada tiga jenis CSS dipakai di elemen yang sama, urutan kekuatannya

- Inline CSS (paling kuat, langsung ditulis di tag HTML)
  
- Internal CSS (ditulis di ```<style>``` di dalam file HTML)
  
- Eksternal CSS (ditulis di file ```.css``` terpisah lalu dipanggil di HTML)
  
### contoh kode nya

```html
<!DOCTYPE html>
<html>
<head>
  <!-- Eksternal CSS -->
  <link rel="stylesheet" href="style.css">

  <!-- Internal CSS -->
  <style>
    p { color: blue; }
  </style>
</head>
<body>
  <p style="color: red;">Halo Dunia</p>
</body>
</html>
```
### penjelasan 

- Eksternal CSS (misalnya ```p { color: green; }``` di style.css) → kasih warna hijau.

- Internal CSS (```p { color: blue; }```) → kasih warna biru.

- Inline CSS (```style="color:red;"```) → kasih warna merah.

Maka yang muncul di browser = ```merah``` 

## 4. Kalau sebuah elemen punya ID dan Class sekaligus, lalu keduanya dikasih aturan CSS:

MAKA ID (```#```) lebih kuat daripada Class (```.```)

### Contoh kode nya 

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    /* aturan untuk class */
    .text-paragraf {
      color: blue;
    }

    /* aturan untuk ID */
    #paragraf-1 {
      color: red;
    }
  </style>
</head>
<body>
  <p id="paragraf-1" class="text-paragraf">Halo Dunia</p>
</body>
</html>
```
### penjelasan 

Class ```.text-paragraf``` → warna biru

ID ```#paragraf-1``` → warna merah

Karena ID lebih spesifik, maka teks yang tampil di browser = ```merah``` 




