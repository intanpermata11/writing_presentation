# Web Development Basic

<hr>

# JS Dasar - Scope dan Function <br>

## 1. Scope

Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

### Blocks

> Blocks adalah code yang berada didalam curly braces {}.Conditional, function, dan looping menggunakan blocks.

### Global Scope

> Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks. <br>

Variabel myName dideklarasikan secara global scope

```JAVASCRIPT
let myName = 'Intan';
function greeting() {
    return myName;//Intan
}
console.log(myName);//Intan
```

### Local Scope

> Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.<br>

Mendeklarasikan variabel secara local scope

```JAVASCRIPT
function greeting() {
    let myName = 'Intan';
    return myName;
}
console.log(greeting()) //Intan
console.log(myName); //Uncaught ReferenceError : myName is not defined because local scope
```

## 1. Function

Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.

### Membuat Function

```JAVASCRIPT
function greeting() {
    return 'Hello World';
};
```

### Memanggil Function

```JAVASCRIPT
greeting () //panggil nama fungsinya
console.log(greeting())//Hello World
```

### Parameter dan Argumen

> Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.<br>
> Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.

```JAVASCRIPT
function penambahan (a,b) {
    return a+b;
}
```

> Argumen adalah nilai yang digunakan saat memanggil function.
> Jumlah argumen harus sama dengan jumlah parameternya
> Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.

```JAVASCRIPT
function penambahan (a,b) {
    return a+b;
}
console.log(penambahan(5,5))//Output : 10
```

### Default Parameter

> Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.
> Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen

```JAVASCRIPT
function greetOnWebsite (name = 'Intan') {
    return 'Hello' + name;
}
console.log(greetOnWebsite('Permata'));//Output : Hello Permata
console.log(greetOnWebsite()); //Output :Hello Intan
```

### Function Helper

> Kita bisa menggunakan function yang sudah dibuat pada function lain.

```JAVASCRIPT
function multipleByNineFifths (number) {
    return number * (9/5);
};
function getFahrenheit(celcius){
    return multipleByNineFifths(celcius) + 32;
};
getFahrenheit(15);//returns 59
```

### Arrow Function

> Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)

```JAVASCRIPT
const greeting = () => {
    return 'Hello World';
};
const penambahan = (a,b) => {
    return a+b;
};
```

### Short Syntax Function

Zero Parameters

```JAVASCRIPT
const functionName = () => {};
```

One Parameters

```JAVASCRIPT
const functionName = paramOne => {};
```

Two or more Parameters

```JAVASCRIPT
const functionName = (paramOne, paramTwo) => {};
```

Single Line Block

```JAVASCRIPT
const sumNumbers = number => number+number;
```

Multi Line Block

```JAVASCRIPT
const sumNumbers = number => {
    const sum = number+number;
    return sum; //return statement
};
```

<hr>

# JS Dasar - Data Type Built in Prototype & Method <br>

Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.

> Tipe data pada javacript terdiri dari tipe data primitive dan object.

## Tipe Data Primitive

Semua jenis tipe data kecuali objek mendefinisikan nilai yang tidak dapat diubah. Misalnya, String tidak dapat diubah. Ini disebut sebagai tipe data primitive.

> Tipe data primitive terdiri dari : Boolean, Null, Undefined, Number, BigInt, String, Symbol.

1. **Boolean** mewakili entitas logis dan dapat memiliki dua nilai: benar dan salah.
2. Tipe data **null** adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
3. Tipe data **undefined** adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Undefined berbeda dengan null.
4. Tipe data **number** adalah tipe data yang mengandung semua angka termasuk angka desimal.
5. **BigInt** : Tipe BigInt adalah primitif numerik dalam JavaScript yang dapat mewakili bilangan bulat dengan presisi arbitrer. Dengan BigInts, kita dapat dengan aman menyimpan dan mengoperasikan bilangan bulat besar bahkan di luar batas bilangan bulat aman untuk Numbers.
6. Tipe data **string** adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.
7. **Simbol** adalah nilai primitif yang unik dan tidak dapat diubah dan dapat digunakan sebagai kunci dari properti Object . Dalam beberapa bahasa pemrograman, Simbol disebut "atom".

### Transformasi Tipe Data String

> - toUpperCase() <br> Transform ini berfungsi untuk merubah nilai string yang ada pada sebuah variabel menjadi kapital semua. <br>

Contoh

```javascript
let string_upper = "intan";
console.log(string_upper.toUpperCase()); // Output : INTAN
```

> - toLowerCase() <br> Transform ini berfungsi untuk merubak nilai string pada sebuah variabel menjadi huruf kecil semua.

Contoh

```javascript
let string_lower = "Intan";
console.log(string_lower.toUpperCase()); // Output : intan
```

### MATH

> - Math merupakan method yang memiliki properti yang biasa digunakan untuk matematika constant dan function. Math dapat digunakan dengan tipe data Number dan tidak dapat digunakan dengan tipe data BigInt.
> - Terdapat beberapa Math properties, contohnya
>   <br>Math.E; Math.LN2; Math.LN10; Math.LOG2E; Math.LOG10E; Math.PI; Math.SQRT1_2; Math.SQRT2
> - Pada Math juga terdapat method, contohnya seperti
>   <br> Math.abs(); Math.acos(); Math.acosh(); Math.asin(); Math.asinh(); Math.atan(); Math.atanh(); Math.atan2(); Math.cbrt(); Math.ceil(); Math.clz32(); Math.cos(); Math.cosh(); Math.exp(); Math.expm1(); Math.floor(); Math.fround(); Math.hypot(); Math.imul(); Math.log(); Math.max(); Math.min(); Math.pow(); Math.random(); Math.round(); Math.sqrt();

## Object (NON- Primitive)

> Tipe data non-primitive adalah tipe data yang dapat menyimpan lebih dari satu nilai pada satu waktu dan dapat diubah. Tipe data non-primitif akan dianggap berbeda meskipun nilainya sama dan dalam urutan yang sama. Tipe data Non-Primitive adalah Object.

### JSON

> JSON (JavaScript Object Notation) adalah format pertukaran data ringan, berasal dari JavaScript, tetapi digunakan oleh banyak bahasa pemrograman. JSON membangun struktur data universal.

<hr>

# JS DOM : Introduction <br>

## Apa itu DOM ?

DOM merupakan singkatan dari Document Object Model. Artinya, dokumen (HTML) yang dimodelkan dalam sebuah objek.
DOM adalah jembatan agar bahasa pemrograman dapat berinteraksi dengan dokumen HTML. Objek document adalah model dari dokumen HTML. Objek ini berisi kumpulan fungsi dan atribut berupa objek dari elemen HTML

> DOM bukan bagian dari JavaScript, melainkan browser (Web API).

Objek dari dokumen ini menyediakan sekumpulan fungsi dan atribut/data yang bisa kita manfaatkan dalam membuat program Javascript. Inilah yang disebut API (Application Programming Interface).

## Mencari Element HTML dengan DOM

### TRAVERSING

- Traversing kebawah : <br>
  - Mengembalikan object yang merepresentasikan elemen yang ditangkap dan properti id-nya cocok dengan tag HTML yang dituju. Cara menangkap element id :
    ```JAVASCRIPT
    document.getElementByID(id);
    ```
  - Mengembalikan HTMLCollection dari seluruh elemen yang memiliki class name sesuai. Mencari element berdasarkan element Class, dengan cara seperti dibawah ini :
    ```JAVASCRIPT
    document.getElementByClass(name);
    ```
  - Mengembalikan HTMLCollection of object dari seluruh elemen dengan nama elemen (tag element) yang sesuai. Mencari element berdasarkan element tag name, dengan cara seperti dibawah ini :
    ```JAVASCRIPT
    document.getElementByTagName(name);
    ```
  - Mengembalikan elemen pertama di dalam dokumen yang cocok dengan selector spesifik. Jika tidak, akan mengembalikan nilai null. Cara akses :
    ```JAVASCRIPT
    querySelector(<query_selector>);
    ```
- Traversing ke atas : <br>
  Untuk mengakses parent dapat menggunakan:
  `itemQuery.parentElement`; <br> `itemQuery.closest(". ")`;
- Traversing ke samping : <br>
  Untuk mengakses sibling dapat menggunakan:
  `itemQuery.previousElementSibling`; <br> `itemQuery.nextElementSibling`;

<hr>

# JS DOM : Manipulation <br>

DOM atau Document Object Model merupakan objek JavaScript spesial yang hanya ada di environment Browser. Objek ini digunakan untuk mendapatkan struktur dokumen website, bahkan memanipulasinya.

> method `createElement()` dari objek document digunakan untuk membuat elemen baru dengan menyertakan nama tag spesifik yang dituju sebagai parameter.

> Method `append()` yang menerima argument bertipe Node atau string, sedangkan jika kita ingin menyematkan elemen lain sebagai child dari elemen tersebut, gunakanlah `appendChild()`.

contoh kasus pembuatan dan penyematan elemen baru.

```JAVASCRIPT
const newParagraph = document.createElement('p');
const newContent = document.createTextNode('Hallo!');
newParagraph.appendChild(newContent);
document.body.appendChild(newParagraph);
```

Jika kita menggunakan .appendChild, kita dapat menggunakan .append tetapi tidak sebaliknya.

> `element.innerHTML` fungsinya adalah untuk menentukan dan mengembalikan nilai konten dari suatu element dalam bentuk text atau string berikut dengan tag html didalamnya nya. <br>

> `element.innerText` fungsinya adalah untuk menentukan dan mengembalikan nilai konten dari suatu element dalam bentuk text atau string.

> `element.textContent` dapat kita gunakan untuk mengubah teks di dalam sebuah element

> `Remove()` akan menghapus element node dari dokumen.

> Fungsi `getAttribute()` akan mengembalikan nilai atribut tertentu pada element HTML. Contoh data atribut data-color pada button.

> Fungsi `setAttribute()` metode menambahkan specified atribut elemen, dan memberikan nilai yang ditentukan.

<hr>

# JS DOM : Event and Forms <br>

Event = kejadian/kegiatan/interaksi yang terjadi pada website.

> HTML DOM Event : `Focus; Click; Change; Hover; Blur; Scroll; Submit.`

3 cara memberikan event : `HTML Attribute`; `event property`; `addEventListener()`

1. HTML Attribute
   ```html
   <h1 onclick="alert('Selamat Datang')">Hallo</h1>
   ```
2. Event Property
   ```javascript
   paragraf.onclick = function () {
     alert("Ini adalah paragraf");
   };
   function tampilkanAlert() {
     alert("ini alert ya ges ya");
   }
   ```
3. addEventListener()
   ```JAVASCRIPT
   let button = document.getElementById("btn")
   button.addEventListener("click", function(){
       alert("ini dari button")
   })
   ```

### EventListener
- Click
  ```html
  <input id="”user-input”" /> dan <button id="alert-button”">show</button>.
  ```
- Blur<br>
  “Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)
  ```javascript
  // cari dulu element tersebut berdasarkan id-nya
  const input = document.getElementById(“username”)
  // tambahkan event listener
  input.addEventListener(“blur”, () => {
    if(input.value.length < 6) alert(“Panjang username minimal 6”)
  })
  ```
- Form Submission
  ```html
  <input name="”email" /> dan <input type="”password”" name="”password”" />
  ```
  Bagaimana caranya kita mendapatkan isi dari kedua input tersebut saat submit form? Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input.

> `onclick` adalah atribut HTML untuk menentukan aksi saat event klik pada sebuah elemen.

> Event `onmouseover` dan `onmouseout` dapat digunakan untuk memicu fungsi ketika pengguna mengarahkan mouse ke atas, atau keluar dari elemen HTML
