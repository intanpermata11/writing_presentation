# Web Development Basic

<hr>

# Unix Command Line ,Git & Github Dasar <br>

### Objectives Learning

> - Command Line Interface (CLI)
> - Shell
> - File System
> - Command untuk melihat current working directory
> - Command untuk melihat isi sebuah direktori
> - Command untuk berpindah direktori
> - Command untuk melihat isi dari files
> - Command untuk membuat file & direktori baru
> - Command untuk menyalin file & direktori
> - Command untuk memindahkan atau me-rename file & direktori
> - Command untuk menghapus file & direktori

### Command Line Interface (CLI)

> CLI adalah singkatan dari Command Line Interface. Singkatnya, dengan CLI sebagai program, pengguna bisa memberikan perintah dalam bentuk teks, kemudian memberikan instruksi dan melakukan tugas tertentu.

### Shell

> Saat kita menyebut "command line" atau "command line interface", sebenarnya yang dimaksud adalah shell yang berbasis teks. Shell ini adalah program yang menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi. Selain command line, kita juga punya shell berbasis grafis yang lebih dikenal dengan nama GUI atau graphical user interface.

### File System

> - Sebuah filesystem mengatur bagaimana data disimpan di dalam sebuah system
> - Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree

### Command untuk Navigasi

> - pwd : (Print working directory) Command untuk melihat current working directory
> - ls : (lists) Command untuk melihat isi file yang ada di sebuah direktori
> - cd <nama_direktori> : (change directory) Command untuk berpindah direktori.

### Membuat files & direktori

> - touch : Command untuk membuat sebuah file
> - mkdir : Command untuk membuat sebuah direktori

### Melihat isi files

> - head : Command untuk melihat beberapa line awal dari sebuah file text
> - tail : Command untuk melihat beberapa line awal dari sebuah file text
> - cat : Command untuk melihat isi sebuah file

### Menyalin, memindahkan, dan menghapus files & directory

> - cp : Command “cp” untuk menyalin file, “cp -R” untuk menyalin directory
> - mv : (move) Command “mv” untuk memindahkan file, “mv -R” untuk memindahkan directory
> - rm : (remove) Command “rm” untuk menghapus file, “rm -R” atau “rm -d” untuk menghapus directory

<hr>

# HTML (Hypertext Markup Language ) <br>

### Objectives Learning

> - Mengetahui dan memahami kegunaan HTML pada web development
> - Mengetahui cara menggunakan tools pendukung dalam HTML Development
> - Mengetahui cara membuat HTML sederhana
> - Mengetahui cara menjalankan HTML secara manual dan menggunakan live server
> - Mengetahui cara membaca dokumentasi HTML melalui w3schools
> - Mengetahui cara penggunaan Tag HTML yang populer
> - Mengetahui dan memahami semantic HTML
> - Mengetahui cara deployment HTML ke Netlify

### Overview

> - HTML adalah singkatan dari Hypertext Markup Language.
> - HTML digunakan untuk menampilkan konten pada browser.
> - Contoh konten yang dapat ditampilkan seperti Text, Image, Video, Link, dan masih banyak lainnya.
> - HTML bersifat statis. HTML hanya bertugas menampilkan konten yang diminta oleh developer.
> - HTML bukanlah sebuah bahasa pemrograman, artinya HTML tidak bisa dinamis mengolah data.
> - Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML : Browser dan Code Editor
> - Recommended Code Editor : Visual Studio Code
> - Visual Studio Code adalah code editor yang dikembangkan oleh tim engineer Microsoft.
> - Visual Code Studio merupakan paket all in one. Kamu bisa menggunakan ini untuk bahasa pemrograman apapun.

### HTML Structure

> - Kita bisa menuliskan HTML tanpa structure dan kita bisa tetap menjalankan nya tetapi untuk menjalankannya dengan baik kita perlu HTML Structure
> - Structure HTML

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hello World</h1>
</body>
</html>
```

### HTML Element

> - HTML element didefinisikan dengan opening tag, content, dan closing tag.
> - Contoh element HTML

```HTML
<body>
    <div>
        <!-- Element Heading  -->
        <h1>ini HTML</h1>

        <!-- Element Paragraph -->
        <p>Ini Content</p>

        <!-- Element hyperlink -->
        <a href="https://kampusmerdeka.kemdikbud.go.id/"> menuju website kampus merdeka</a>
    </div>
</body>
```

### HTML Attributes

> - Attribute adalah properties dari sebuah HTML Element.
> - Semua HTML Element memiliki attribute.

```HTML
<body>
    <div>
        <!-- Element Heading dengan atribut ID -->
        <h1 id="header">ini HTML</h1>

        <!-- Element image dengan atribut src -->
       <img src="image.png">

        <!-- Element hyperlink dengan atribut href -->
        <a href="https://kampusmerdeka.kemdikbud.go.id/"> menuju website kampus merdeka</a>
    </div>
</body>
```

### HTML Comment

> - Comment tidak akan dieksekusi oleh sistem.
> - Comment hanya untuk dibaca oleh sesama programmer.

```HTML
<body>
    <div>
     <!-- INI COMMENT -->
    </div>
</body>
```

### Cara menjalankan HTML

> - Kita bisa menjalankan HTML dengan mencari lokasi file HTML kita lalu membukanya via browser. Contoh : file:///C:/xampp/htdocs/STUPEN/summary.html
> - Kekurangan menggunakan cara ini kita perlu refresh halaman jika ada perubahan content. Gunakan Extension live server agar perubahan terjadi secara realtime.
> - Jika sudah selesai install “Live Server” kita bisa klik kanan pada file HTML kita dan ada pilihan open with “Live Server” maka HTML kita sudah auto reload.

### Cara membaca dokumentasi

> - Untuk melihat seluruh element yang disediakan oleh HTML, kita bisa cek dokumentasi yang disediakan.
> - [Resource by Mozilla](https://developer.mozilla.org/ "Pergi ke Resouce by Mozilla")
> - [Documentation by W3schools](https://www.w3schools.com/ "Pergi ke W3schools ")

### HTML Tag Populer

> - IMG : Tag img untuk menampilkan gambar. Src atau source adalah attribute untuk memberitahukan sumber gambar

```HTML
<img src="image.png" alt="profile">
```

> - Alt adalah alternative. Jika gambar tidak berhasil dimunculkan kita bisa memberi tahu ke user di tag img kita menampilkan gambar apa
> - Video : tag video untuk menampilkan video

```HTML
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

> - Video merupakan double closing tag sehingga kita menaruh konten di antara opening dan closing
> - controls berguna untuk kita bisa mengatur videonya di play / pause dan indikator menit
> - Table :

```HTML
<table>
    <!-- baris table  -->
    <tr>
        <!-- data table -->
        <th>nama</th>
        <th>npm</th>
        <th>jurusan</th>
    </tr>

    <!-- baris table  -->
    <tr>
         <!-- data table -->
        <td>Intan</td>
        <td>202210011</td>
        <td>S1 Sistem Informasi</td>
    </tr>
</table>
```

### Semantic HTML

> - Semantic artinya kita menggunakan element html yang sesuai dengan kebutuhan konten
> - Jadi daripada kita menuliskan

```HTML
<div class=”header”>
```

> - Kita menuliskan

```HTML
<header>
```

> - Kegunaan Semantic :
>   - Meningkatkan Accessibility ,
>   - Meningkatkan SEO ,
>   - Lebih mudah di maintain

### Deploy HTML

> - Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang
> - Sedangkan jika aplikasi kita mobile seperti Android Atau IOS kita bisa deploy ke Google Play Store atau App Store
> - Kita gunakan tools bernama Netlify untuk proses deployment
> - Kita tinggal masuk ke netlify.com lalu register seperti biasa menggunakan email atau github
> - Setelah itu masuk ke tab Sites lalu drag and drop seluruh folder html kalian
> - Setelah itu masuk ke tab Sites lalu drag and drop seluruh folder html kalian

<hr>

# CSS (Cascading Style Sheets) <br>

### Objectives Learning

> - Apa itu CSS
> - Struktur CSS
> - CSS Comment
> - 3 Cara menggunakan CSS
> - Linking the CSS Files with HTML
> - Tag Name
> - Class Name
> - Multiple Classes
> - ID Name
> - Perbedaan Class Name dan ID Name
> - Chaining Selectors
> - Nested Element
> - !important pada CSS
> - Multiple Selector

### Overview

> - CSS adalah bahasa yang digunakan untuk mendesain halaman website
> - Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.

### Stucture CSS

```CSS
.elementHTML {
    property : value
}
```

### CSS Comment

> - Comment tidak akan dieksekusi oleh sistem.
> - Comment hanya untuk dibaca oleh sesama programmer.

```CSS
/*ini comment*/
.elementHTML {
    property : value
}
```

### 3 Cara Menggunakan CSS

> - Inline Style : menambahkan CSS pada attribute element HTML

```HTML
<p style="text-align: justify"> paragraf rata kanan kiri</p>
```

> - Internal

```HTML
<style>
    P {
        color : coral;
        font-size : 36px;
    }
</style>
```

> - File External : Jika kita membutuhkan banyak code pada CSS, direkomendasikan untuk memisahkan code CSS di file tersendiri (extension .css) dan terpisah dari file HTML.

```HTML
<link href="style.css" type="text/css" rel="stylesheet">
```

### CSS - Tag Name

> - Kita bisa menggunakan Tag Elemen HTML secara langsung pada CSS. Jika menggunakan Tag Element, maka ini bersifat global.
> - Global artinya akan mempengaruhi seluruh Tag Elemen HTML yang ada pada file tersebut

### CSS - Class Name

> - Kita bisa menggunakan attribute class pada elemen HTML lalu memanggil nama class tersebut pada CSS
> - HTML yang memiliki class yang sama, akan mempunyai styling yang sama saat digunakan pada CSS.
> - Gunakan (.) saat memanggil class pada CSS

### CSS - ID Name

> - Biasanya digunakan jika hanya ada 1 element pada 1 page. Contohnya navigation header dan footer.
> - Gunakan (#namaID) saat memanggil element ID HTML pada CSS

### Chaining Selectors

> - Chaining selector dapat kita gunakan pada case/kasus berikut :<br> Jika kita memiliki 3 tag elemen HTML pada CSS namun kita ingin ada 1 elemen HTML yang memiliki styling berbeda.

### !important CSS

> - !important CSS berada di level paling atas dari ID dan Class.<br>Maksudnya adalah jika pada styling CSS kita menggunakan !important, maka styling sebelumnya baik itu ID Name atau Class Name akan di override.

### Multiple Selector

Pada CSS kita bisa membuat code lebih efisien dan tidak repetitive (melakukan hal yang sama berulang-ulang).

```CSS
h1, p {
    color : pink;
    font-family : 'Nunito', sans-serif;
}
```

<hr>

# Algoritma dan JavaScript Dasar <br>

### Objectives Learning

> - Pengertian algoritma
> - Pentingnya Algoritma
> - Ciri-ciri algoritma
> - Proses Algoritma
> - Penyajian Algoritma

### Apa itu Algoritma ?

> Algoritma adalah metode atau langkah yang direncanakan secara tersusun dan berurutan untuk menyelesaikan atau memecahkan permasalahan dengan sebuah intruksi atau kegiatan

### Kenapa Algoritma itu penting ?

> Programming itu identik dengan memecahkan suatu permasalahan, maka dari itu algoritma merupakan pemeran utamanya bahasa pemrograman hanyalah pemeran pendamping.<br>
> Belajar algoritma sama aja dengan mengingat kembali alur berfikir yg terstruktur

### Ciri Ciri Algoritma

> - Memiliki 0 atau lebih inputan. Contoh : Kopi Sachet
> - Memiliki min 1 buah output. Contoh : Segelas kopi hangat
> - Instruksi jelas tidak ambigu. Contoh : mulai dari menyiapkan kopi sampai ke tahap pembuatannya
> - Memiliki titik berhenti (stop). Contoh : Kopi selesai dibuat
> - Sebisa mungkin tepat sasaran dan efisien

### Jenis Proses Algoritma

> - Sequence : Instruksi yg dijalankan secara berurutan.<br>Contoh : Gelas diisi dengan air, lalu air siap utk diminum.
> - Selection : Instruksi yg dijalankan jika memenuhi suatu kondisi. <br>Contoh : Jika lampu merah, saya akan berhenti.
> - Iteration : Instru,brksi yg berulang kali dijalankan selama memenuhi suatu kondisi.<br>Contoh : Selama belum sampai rumah, saya akan terus menyetir.
> - Concurrent : Instruksi yg dijalankan secara bersamaan.<br>Contoh : Ibu mencuci baju sambil membersihkan rumah.

### Penyajian Algoritma

#### Algoritma Deskriptif

Penulisan algoritma dengan cara deskriptif seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari

> Contoh <br>
> Menukar isi dari 2 gelas:<br>
>
> - Terdapat gelas A isi kopi dan gelas B isi teh<br>
> - Siapkan gelas C yg masih kosong<br>
> - Gelas A dituang ke dalam gelas C<br>
> - Gelas B dituang ke dalam gelas A<br>
> - Gelas C dituang ke dalam gelas B<br>
> - Isi gelas A dan B sudah ditukar

#### Flowchart

Flow chart atau diagram alir, penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual. Flow chart menggunakan simbol bangun datar sebagai representasi dari proses yg dilakukan.

> ![Flowchart Lampu Lalu Lintas](https://i.ibb.co/yVkHyL1/Picture1.png)

Simbol Flowchart

> ![Flowchart membuat kopi](https://1.bp.blogspot.com/-v7vOWxeLis8/XjFjO0KyqhI/AAAAAAAACT4/x5rs2eXYJCciwgXtBupewTBNimKl3v6IgCLcBGAsYHQ/s640/simbol%2Bsimbol%2Bflowchart.png)

### Pseudo Code.

Penulisan algoritma yg hampir menyerupai penulisan pada kode pemrograman disebut dengan pseudo code.<br>

> Pada umumnya pseudocode memiliki 3 bagian:
>
> - Judul : Penjelasan dari algoritma yg dibuat
> - Deklarasi : Mendefinisikan/menyiapkan semua nama (variabel) yg akan digunakan
> - Deskripsi : langkah-langkah penyelesaian masalah

Contoh : <br>
Algoritma Deskriptif nya

```
1. Terdapat lampu
2. Apakah lampu berwarna hijau?
3. Jika ya, jalan lalu ke no 9
4. Apakah lampu berwarna kuning?
5. Jika ya, hati-hati lalu ke no 9
6. Apakah lampu berwarna merah?
7. Jika ya, berhenti lalu ke no 9
8. Jika tidak, lampu rusak lalu ke no 9
9. selesai 
```

Pseudo Code nya

```Pseudocode
deklarasi
	lampu ← text (hijau/kuning/merah)
deskripsi
	if lampu is hijau
		cetak “jalan”
	else if lampu is kuning
		cetak “hati-hati”
	else if lampu is merah
		cetak “berhenti”
	else
		cetak “lampu rusak”
	end
```

<hr>

# JavaScript : Introduction <br>

### Objectives Learning

> - Apa itu Javascript
> - Bagaimana menjalankan Javascript
> - Syntax dan Statement
> - Tipe Data
> - Variable
> - Operator
>   - Arithmetic Operator
>   - Assignment Operator
>   - Comparison Operator
>   - Conditional Operator
> - Pengenalan Conditional

### Apa itu Javascript ?

> Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website. Javascript juga dapat membuat website menjadi interaktif dan dinamis

### Bagaimana menjalankan Javascript ?

> Javascript dijalankan melalui browser pada device setiap user. Umumnya browser Chrome dan Mozilla yang sudah support untuk semua fitur Javascript.

### Syntax dan Statement

> Syntax bisa dianalogikan seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemograman. <br>
> Kita menggunakan syntax tertentu untuk membuat statement program, instruksi untuk djalankan/dieksekusi oleh web browser, compiler, ataupun intrepreter

### Contoh Syntax JavaScript

```JAVASCRIPT
alert()
```

![Alert Javascript](https://www.jquery-az.com/wp-content/uploads/2015/12/2..0_3-JavaScript-alert-success.png)

```JAVASCRIPT
Prompt()
```

![Prompt Javascript](https://1.bp.blogspot.com/-cmEyJNKro8Q/X5tupvJKGrI/AAAAAAAAK74/GL0q_m6intkHYX-jCbq0P1GKqpG8zbMdwCLcBGAsYHQ/s346/niguru%2B%25287%2529.png)

```JAVASCRIPT
Confirm()
```

![Confirm Javascript](https://support.pega.com/sites/default/files/collaboration/inline-images/Modaldialog%2528Window.confirm%2529.png)

### Console Log

> Console log adalah tempat kita untuk cek logic pemograman web yang kita kembangkan. Console log juga tempat kita untuk melakukan debugging (mengetahui error pada code) pada pemograman web. <br>
> ![Console Log](https://media.geeksforgeeks.org/wp-content/uploads/6-50.png)

### Comments

Comments adalah sintaks yang digunakan untuk memberi keterangan tentang suatu statement. Menggunakan bahasa inggris atau bahasa indonesia.
Comments tidak akan dijalankan oleh program karena hanya untuk dibaca oleh sesama programmer ataupun diri sendiri untuk memahami maksud dan tujuan sebuah statement/syntax.

> Single Comments
>
> ```JAVASCRIPT
>   //ini single comment
>   console.log(5);
> ```
>
> Multiline Comments
>
> ```JAVASCRIPT
>   /* ini multiline comment.
>   terdiri dari beberapa line */
>   console.log(5);
> ```

### Tipe Data (Data Types)

Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming. <br>

Ada 6 tipe data fundamental pada Javascript :

1. **Number** : tipe data yang mengandung semua angka termasuk angka desimal.<br>
   Contoh : 2, 4, 1200, 23.42

```JAVASCRIPT
let number1 = 11;
let number2 = 12;
let number3 = 13;
```

2. **String** : Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.<br>
   Harus diawali dan diakhiri dengan single quotes ‘ … ‘ ataupun double quotes “ … “.

```JAVASCRIPT
let string = "Intan Permatasari";
```

3. **Boolean** : Tipe data boolean adalah tipe data yang hanya mempunyai 2 buah nilai.
   2 buah nilai tersebut adalah TRUE (benar) or FALSE (salah).

```JAVASCRIPT
let benar = true;
let salah = false;
```

4. **Null** : Tipe data null adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
   Null berbeda dengan string kosong. String kosong masih memiliki tipe data string.

```JAVASCRIPT
let datapertama = null;
let datakedua = null;
let dataketiga = "";

console.log(datapertama);
console.log(datakedua);
console.log(dataketiga);
```

Hasil <br>
![Outpul Tipe Data Null](https://i.ibb.co/qJcxtm8/Capture2.png) <br> <br>

5. **Undefined** : Tipe data undefined adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai.
Undefined berbeda dengan null.<br>

Undefined didapat dari hasil berikut:<br>
- Nilai dari pemanggilan variabel yang belum didefinisikan
- Nilai dari pemanggilan element array yang tidak ada
- Nilai dari pemanggilan property objek yang tidak ada
- Nilai dari pemanggilan fungsi yang tidak mengembalikan nilai (return)
- Nilai dari parameter fungsi yang tidak memiliki argumen <br>

Tipe data null biasanya diperoleh dalam kondisi normal dan sudah kita rencanakan.
Tipe data undefined biasanya didapat dari hasil kesalahan program (error), kelalaian programmer, dan tidak direncanakan.

```JAVASCRIPT
let a = "Intan"
let b = "Permata"
let peserta = ["Ilhamsyah","Maulana"];

console.log(c); //undefined
console.log(a); //Intan
console.log(peserta.length)//2
console.log(peserta.panjangkarakter)//undefined
```

6. **Object** : Tipe data object adalah koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya).
   Tipe data object mempunyai key dan value.

```JAVASCRIPT
var person {
    firstName:"Intan",
    lastName:"Permatasari",
    age:20,
    eyeColor:"black"
};
```

### VARIABEL

Variable adalah container/tempat untuk menyimpan sebuah nilai. <br>

**3 hal yang dapat dilakukan pada variabel :**

> 1.  Membuat variabel dengan nama yang jelas dan menggambarkan tentang data tersebut
> 2.  Menyimpan dan mengupdate informasi/data yang disimpan
> 3.  Mendapatkan/menampilan data yang tersimpan

**Aturan Penamaan Variabel :**

> 1.  Harus mendeskripsikan tentang data yang disimpan
> 2.  Tidak bisa menggunakan number pada awal nama variabel
> 3.  Gunakan camelcase untuk penamaan yang lebih dari 1 kata. <br>
>     Contoh: myName, myAge

**Ada 3 cara mendefinisikan sebuah variabel :**

1. var

```Javascript
var myName = "Intan";
console.log(myName);
//output : Intan
```

2. let :
   dianjurkan untuk menggunak let untuk variabel yang dinamis/dapat diubah.

```Javascript
var myName = "Intan";
console.log(myName); //output : Intan
myName = "Permatasari"
console.log(myName); //output : Permatasari
```

3. Const : Gunakan const jika variabel tidak dapat diubah nilainya.
   Biasanya digunakan untuk menggambarkan konstanta sebuah nilai. Seperti konstanta pi = 3.14.

```Javascript
const phi = 3.14;
console.log(phi); //output : 3.14
phi = 10;
console.log(phi); //Uncaught TypeError: Assignment to constant variable.
```

### OPERATOR

#### Assignment Operator (=)

> Assignment operator digunakan untuk menyimpan sebuah nilai pada variabel.
>
> ```JAVASCRIPT
> let myName = "Intan";
> ```

#### Mathematical Assignment Operator

> Assignment operator digunakan untuk menyimpan sebuah nilai pada variabel.
>
> ```JAVASCRIPT
> let a = 5;
> a = a + 1;
> console.log(a);//output 6
> //atau
> let a = 5;
> a += 1;
> console.log(a);//output 6
> ```

#### Increment dan Decrement

> Gunakan increment atau decrement untuk menambah atau mengurangi sebesar 1 nilai.
>
> ```JAVASCRIPT
> let a = 10;
> let b = 11;
> a++; //increment
> b--; //increment
> console.log(a); //output : 11
> console.log(b); //output : 10
> ```

#### Arithmetic Operator

> Arithmetic operator adalah operator yang melibatkan operasi matematika.
>
> - Tambah (+)
> - Kurang (-)
> - Pembagian (/)
> - Perkalian (\*)
> - Modulus (%)
>
> ```JAVASCRIPT
> console.log(2 + 3)//print 5;
> console.log(7 - 5 )//print 2;
> console.log(10 / 2 )//print 5;
> console.log(7 * 5 )//print 35;
> console.log(11 % 3 )//Modulus adalah sisa hasil bagi = 2
> ```

#### Comparison Operator

> Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya.
> Hasil operasi yang melibatkan comparison operator adalah antara true or false <br>

> Simbol :
>
> - lebih kecil dari : <
> - lebih besar dari : >
> - lebih kecil sama dengan : <=
> - lebih besar sama dengan : >=
> - sama dengan : ===
> - tidak sama dengan : !==
>
> ```JAVASCRIPT
> 8 < 10 //menghasilkan true;
> 8 > 10 //menghasilkan false;
> ```

#### Logocal Operator

> Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman.
> Menghasilkan nilai BOOLEAN yaitu TRUE or FALSE.
>
> - AND operator : && <br>
>   akan menghasilkan nilai true jika kedua atau semua premis bernilai TRUE
> - OR operator: || <br>
>   akan menghasilkan nilai true jika salah satu premis mengandung nilai TRUE
> - NOT operator: !<br>
>   akan membalikkan sebuah nilai BOOLEAN. TRUE menjadi FALSE dan sebaliknya.

<hr>

# JavaScript : Conditional <br>

### Apa Itu Conditional

> Conditional merupakan statement percabangan yang menggambarkan suatu kondisi.<br>
> Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut.<br>
> Yang dicek adalah apakah kondisi tersebut TRUE (benar). Jika TRUE maka code didalam kondisi tersebut dijalankan.

### Contoh Conditional di kehidupan sehari-hari

> Jika cuaca cerah hari ini, maka kita akan pergi keluar<br>
> Jika alarm berbunyi, maka kita akan bangun dari tidur<br>
> Jika lelah, maka kita akan istirahat<br>
> Jika lapar, kita akan makan<br>

### IF Statement

```JAVASCRIPT
let say = true;
if (say) {
    console.log("great!"); //print great!
}
```

### IF...ELSE Statement

Else akan mengeksekusi sebuah statement/code jika suatu kondisi bernilai FALSE

```JAVASCRIPT
let say = false;
if (say) {
    console.log("great!"); //tidak akan menampilkan ini
} else {
    console.log("shut up");//akan menampilkan ini
}
```

### IF...ELSE IF Statement

Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.

```JAVASCRIPT
let say = great!;
if (say == "great") {
    console.log("you are great!"); //akan menampilkan ini
} else if (say == "good") {
    console.log("you are good!"); //tidak akan menampilkan ini
} else {
    console.log("shut up");//
}
```

### Truthy and Falsy

> Truthy and falsy digunakan untuk mengecek apakah variabel telah terisi namun tidak mementingkan nilainya.
> Truthy and Falsy Assignment : Analoginya adalah jika kita memiliki sebuah website dan meminta inputan username lalu menampilkannya. Jika usernamenya kosong kita bisa isi nilai tersebut.

### Switch Case Contidional

> Gunakan switch case jika kondisi dan percabangan terlalu banyak

```JAVASCRIPT
swicth (expression) {
    case value1 :
        statement1;
        break;
    case value2 :
        statement2;
        break;
    case value3 :
        statement3;
        break;
    default :
        default_statement;
}
```

### Ternary Operator

> Ternary operator merupakan short-syntax dari statement if … else.

```JAVASCRIPT
let isNowSale = true;
isNowSale ? console.log('lets shopping now') : console.log('shopping latter');
```

<hr>

# JavaScript : Looping <br>

### Apa itu Looping ?

> Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.

### Manual Looping

```JavaScript
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
console.log(6);
```

### FOR LOOP

> FOR LOOP merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan.
> Gunakan FOR LOOP jika kita tahu seberapa banyak nilai pasti untuk pengulangannya<br>

> FOR LOOP PARAMETER
>
> - Inisialisasi: Sebagai inisialisasi awal dari mana mulainya sebuah pengulangan. Kita memberikan nilai awal/default pada parameter ini
> - Condition: For loop akan terus berjalan selama kondisi ini terpenuhi. Selama kondisi bernilai TRUE.
> - Post-expression (Increment/Decrement): Iterasi statement yang digunakan untuk mengupdate variabel yang menjadi kontrol pada pengulangan

```JAVASCRIPT
let angka = 1;
for (angka; angka <= 10; angka++){
    console.log(angka);
}
```

```JAVASCRIPT
let angka = 10;
for (angka; angka > 0; angka--){
    console.log(angka);
}
```

### WHILE LOOP

> WHILE LOOP akan menjalankan instruksi pengulangan kondisi bernilai TRUE.
> Gunakan WHILE LOOP jika kita tidak mengetahui jumlah pasti pengulangan.

```JAVASCRIPT
let angka = 1;
while (angka <= 10) {
    console.log(angka);
    angka++;
}
```

### DO WHILE

> Terkadang kita ingin setidaknya menjalankan pengulangan 1 kali sebelum dilakukan pengecekan kondisi

```JAVASCRIPT
var bensin = 9;

//perularangan while-do
while (bensin > 0) {
    console.log("Masih ada bensin, nyalakan mesin!");
    bensin--;
}

//perulangan do-while
do {
    console.log("nyalakan mesin!");
    bensin--;
} while (bensin > 0);
```

### NESTED LOOP

> Jika kita membuat looping didalam looping. Maka ini dinamakan Nested Loop.
> Looping pertama dianalogikan sebagai baris.
> Looping kedua dianalogikan sebagai kolom

```JAVASCRIPT
for (let angka = 1; angka > 10; angka++){
    for (let nomor = 1; nomor > angka; nomor++){
        document.write('<br/>')
        document.write('Baris', +angka);
        document.write('<br/>')
        document.write('Kolom', +nomor);
    }
}
```
