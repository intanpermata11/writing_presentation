# Summary <br> Front-End Bootcamp

<hr>

# Introduction ReactJS

### Apa itu ReactJS ?

> React JS merupakan sebuah framework view library Javascript yang berfungsi untuk membuat tampilan (user interface) pada website. React JS dibuat oleh tim engineer Facebook. React JS digunakan oleh facebook pada sisi Front-End.

### Kenapa menggunakan ReactJS ?

> - ReactJS is Fast <br>
>   React Js membuat aplikasi menjadi lebih cepat walaupun harus menghandle berbagai data
> - ReactJS is Modular <br>
>   React JS dapat membagi 1 tmapilan pada website menjadi komponen-komponen kecil.
> - React JS is Scalable <br>
>   React JS dapat digunakan pada aplikasi berskala kecil hingga berskala besar dan kompleks.
> - React JS is Popular <br>
>   Kebanyakan perusahan teknologi menggunakan React JS, sehingga dapat memudahkan mencari pekerjaan, freelance, bahkan startup jika menggunakan React JS.

### Instalasi ReactJS

> 1. Install Node JS [Download Here](https://nodejs.org/en/).
> 2. Use library `create-react-app` [Click Me](https://create-react-app.dev/).
> 3. Pada Git Bash, buat folder atau tempat untuk menginstall dan download ReactJS
> 4. Install react js dengan menggunakan: `npx create-react-app nama-file`
> 5. Masuk ke folder yang sudah kita buat, ketik `npm start` untuk menjalankan ReactJS, atau akses React menggunakan localhost:3000
> 6. Instalasi Berhasil
>    ![Instalasi ReactJS](https://i.ibb.co/TKZ1GBD/Screenshot-from-2021-02-05-17-46-04.png)
> 7. Struktur folder reactJS<br> >![Struktur Folder ReactJS](https://miro.medium.com/max/608/1*KnQegZWQurLlsLbVSjTzGQ.png)

### Perbandingan membuat UI Elements React JS vs Vanilla JS

> 1. Vanilla Javascript
>
> ```javascript
> // membuat DOM
> const rootElement = document.getElementById("root");
> // membuat element baru
> const element = document.createElement("div");
> // membuat content dan class
> element.textContent = "Hello World";
> element.className = "Container";
> //memanggil elemn baru dibawah rootElement
> rootElement.appenChild(element);
> ```
>
> 2. ReactJS
>
> - Membuat file HelloWorld.js di directory /src, dengan isi sebagai berikut:
>
> ```javascript
> import react from 'react';
> //membuat element UI komponen baru berisi text hello world
> function HelloWorld(){
>   return{
>       <h1>Hello World</h1>
>   }
> };
> //export element
> export default HelloWorld;
> ```
>
> - Edit file App.js dengan menambahkan panggilan untuk hello world
>
> ```javascript
> import react from "react";
> //import komponen elemen hello world
> import HelloWorld from "./HelloWorld";
> function App() {
>   return (
>     <div>
>       //memanggil elemen ke root App
>       <HelloWorld />
>     </div>
>   );
> }
> export default App;
> ```

### JSX (JavaScript Syntax Extension)

> **JSX** merupakan singkatan dari JavaScript Syntax Extension atau dikenal juga dengan Javascript XML. JSX adalah ekstensi React untuk Javasript. Sintaks JSX mirip seperti HTML, sehingga membuat kita lebih gampang menyusun elemen pada komponen React.
> <br> JSX memiliki beberapa peraturan, yaitu:
>
> 1. Setiap JSX hanya memiliki 1 parent element dan tidak boleh lebih.
> 2. Gunakan `<div>` sebagai parent dari element lain pada komponen
> 3. Bisa juga menggunakan tag fragment `<>`

### VIRTUAL DOM

> Virtual DOM adalah adalah sebuah konsep dalam pemrograman di mana representasi ideal atau “virtual” dari antarmuka pengguna disimpan dalam memori dan disinkronkan dengan DOM “yang sebenarnya” oleh library seperti ReactDOM. Proses ini disebut reconciliation.

### Class dan ClassName

> Pada JSX atribut class di tag element HTML harus menggunakan className

```javascript
import React from "react";

function HelloWorld() {
  return (
    <div>
      <h1 className="title">ReactJS</h1>
      <p className="description">
        A JavaScript library for building user interfaces
      </p>
    </div>
  );
}

export default HelloWorld;
```

### Curly Braces in JSX

> Curly Braces { } digunakan untuk membuat syntax JavaScript didalam element HTML.

```Javascript
   import React from 'react';

   function HelloWorld(){
    return (
      <div>
      <h1>{2 + 3}</h1>
      </div>
    );
   };

   export default HelloWorld; //output 5
```

```Javascript
   import React from 'react';

   function HelloWorld(){
    return (
      <div>
      <h1>2 + 3</h1>
      </div>
    );
   };

   export default HelloWorld; //output 2 + 3
```

```Javascript
   import React from 'react';

   function HelloWorld(){
    return (
      <div>
      <h1>{'INTAN'.tolowerCase()}</h1>
      </div>
    );
   };

   export default HelloWorld; //intan
```

### Variabel pada JSX

Gunakan Curly Braces untuk akses variabel pada JSX

```Javascript
   import React from 'react';

   function HelloWorld(){
    //Deklarasi Variabel
    const name = 'Intan Permatasari'
    return (
      <div>
      <h1>{name}</h1>
      <h1>{name.tolowerCase()}</h1>
      </div>
    );
   };

   export default HelloWorld;
   /*output
   Intan Permatasari
   intan permatasari*/
```

### Attribute pada JSX

```Javascript
   import React from 'react';

   function HelloWorld(){
    //Deklarasi Atribut
   const width = "500px";
    return (
      <div>
      <img src="image.jpg"
      alt = "image"
      width = {width}
      />
      </div>
    );
   };

   export default HelloWorld;
```

### Event pada JSX

```Javascript
   import React from 'react';

   function HelloWorld(){
    //Deklarasi Atribut
   const width = "500px";
   //function
   const onClickFunction = () => {
    alert('You Clicked Image');
   }
    return (
      <div>
      <img src="image.jpg"
      alt = "image"
      width = {width}
      onClick = {onClickFunction} //event in jsx
      />
      </div>
    );
   };

   export default HelloWorld;
```

### Conditional pada JSX

```Javascript
   import React from 'react';

   function HelloWorld() {
    let stopLight = 'yellow';
    let message;

    if (stopLight == 'red'){
      message = <h1>Stop!</h1>;
    } else if (stopLight == 'yellow'){
      message = <h1>Slow Down!</h1>;
    } else if (stopLight == 'green'){
      message = <h1>Go!</h1>;
    } else {
      message = <h1>unknown</h1>;
    }

    return(
      <div>
      {message}
      </div>
    );
   };

   export default HelloWorld; //output Slow Down!
```

### .map

`.map()` adalah metode nonmutasi yang menciptakan array baru, yang merupakan kebalikan dari metode mutasi, yang hanya membuat perubahan terhadap array yang memanggil.Fungsi .map() di JavaScript: memanggil fungsi elemen array, mengubah string menjadi array, merender daftar di dalam pustaka JavaScript, memformat ulang objek array.

```Javascript
   import React from 'react';

   function HelloWorld() {
    const numbers = [1,2,3,4,5];
    const listItems = numbers.map((number) => {
      return (
        <ul>
          <li>{number}</li>
        </ul>
      );
    });

    return(
      <div>{listItems}</div>
    );
   };

   export default HelloWorld;
```

# Component pada ReactJS

### Apa itu Component ?

> Component merupakan satu core dari React JS yang dapat membagi UI dalam satuan-satuan kecil, yang mana artinya dalam 1 page terdapat beberapa component yang dibuat.

> Component dibuat jika component tersebut bersifat reusabel code atau jika skala project, component tersebut dibutuhkan pada section atau page lain. Sehingga component yang dibuat dapat digunakan pada page lain juga.

### Bagaimana membuat Component ?

> - Menggunakan function
> - Menggunakan class <br>
>   Kebanyakan kasus dan dokumentasi resmi react JS dirokemendasikan menggunakan function.

### Memanggil CSS pada ReactJS

```javascript
import "./App.css";

function App(){
  return(
      <>
          <div className = "profile-container">
              <img src="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg" className="profile-img">
              <div>
              <h2>Intaan</h2>
              <h3>20 Tahun</h3>
              <p>Bootcamp FrontEnd Skilvul</p>
              </div>
          </div>
      </>
  );
};
```

> - Bisa dilihat pada code diatas, kita perlu membuat file css terlebih dahulu dan melakukan pemanggilan dengan menggunakan import "(alamat file css)"; <br>
> - Lalu juga yang membedakan dari react js dan html itu pada pemanggilan class css. Pada html memanggil dengan menggunakan class="..", sedangkan pada react berganti nama menjadi className=".."

### Cara membuat props menjadi static

> 1. buat file baru pada components, kali ini membuat MemberInfo.jsx
> 2. isi code memberinfo seperi dibawah ini:
>
> ```javascript
> function MemberInfo = ({name, age, info, imgUrl}) => {
>   return(
>       <>
>           <div className = "profile-container">
>               <img src={imgUrl} className="profile-img">
>               <div>
>               <h2>{name}</h2>
>               <h3>{age}</h3>
>               <p>{info}</p>
>               </div>
>           </div>
>       </>
>   );
> };
> export default MemberInfo;
> ```
>
> 3. Lalu pada App.jsx panggil MemberInfo dengan code seperti dibawah ini:
>
> ```javascript
> import "./App.css";
> import MemberInfo from "./components/MemberInfo";
>
> function App() {
>   return (
>     <>
>       <MemberInfo
>         name={"Intan"}
>         age={"20"}
>         info={"Peserta bootcamp FrontEnd Skilvul"}
>         imgUrl="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg"
>       />
>
>       <MemberInfo
>         name={"Permata"}
>         age={"20"}
>         info={"Peserta bootcamp FrontEnd Skilvul"}
>         imgUrl="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg"
>       />
>
>       <MemberInfo
>         name={"Sari"}
>         age={"20"}
>         info={"Peserta bootcamp FrontEnd Skilvul"}
>         imgUrl="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2022/03/08055643/Cari-Dokter-Umum-Terbaik-di-Yogyakarta_-Ini-5-Rekomendasinya.jpg"
>       />
>     </>
>   );
> }
> ```

### State & Props

> - State merupakan data lokal <br>
> - Props digunakan agar component memiliki data yang dinamis yang dikirim dari component lain.<br>
> - Stateless berarti tidak memiliki state, dan hanya memiliki props. <br>
> - Stateful berarti memiliki state dan dapat mengirim state tersebut ke component.

### Membuat fungsi decrement dan increment pada React JS

```javascript
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0); // --> useState itu isinya array [0,1,2,....dst]
  //let count = 0     ---> ini kalo tidak menggunakan state
  //state juga berfungsi agar isi dari variabel bisa berubah-ubah
  const increment = () => {
    setCount(count + 1); //benar
    //count = count + 1 //salah karena tidak menggunakan state.
  };
  const decrement = () => {
    setCount(count - 1);
  };

  return (
    <>
      <button onClick={decrement}> - </button>
      <p>{count}</p>
      <button onClick={increment}> + </button>
    </>
  );
}
export default Counter;
```

### Membuat fungsi looping di react js

```javascript
 import react from "react";
 import Card from "./Card";

 function ListUser(){
   const [users, setUsers] = useState([
       {name: "Ilham", umur: 20},
       {name: "Intan", umur: 20},
       {name: "Ujang", umur: 20},
   ])

 return(
   <>
      {users.map((item, index) =>(
       <Card key = {index} name = {item.name} umur = {item.umur} />
      ))}
   </>
 )
 }
 Export default ListUser
```

# ReactJS Hooks

### Apa itu Hooks

> - Hooks berfungsi untuk memudahkan penggunaan functional components agar bisa menggunakan state, lifecycle, dan lainnya.
> - Sebelumnya state dan lifecycle hanya bisa digunakan di class component, namun dengan hooks, kita dapat menggunakannya di functional component.
> - Hooks yang sering digunakan adalah useState dan useEffect (mirip seperti state dan lifecycle).

### Kelebihan penggunaan hooks

> Dengan menggunakan hooks, kode jadi terlihat lebih simple, clean, dan mudah dimengerti.

### Apa itu useState ?

> Adalah sama seperti dengan state biasa, tetapi penggunaannya sedikit berbeda dengan setState/ state di class component.<br>
> Structure dari useState, seperti dibawah ini:<br>
> ![Structure useState](https://freecontent.manning.com/wp-content/uploads/managing-component-state_04.png)

### Cara penggunaan useState

> 1. Import useState dari React
>
> ```javascript
> import { useState } from "react";
> ```
>
> 2. Menuliskan useState Hooks
>
> ```javascript
> const [nama, setName] = useState("Intan");
> ```
>
> 3. Pemanggilan data
>
> ```javascript
> <p>Halo, saya {nama}</p>
> ```
>
> 4. Update state
>
> ```javascript
> <button onClick={setNama("Permata")}> Ubah </button>
> ```

### Array dalam useState Hooks

> Kita dapat menyimpan data dalam state menggunakan array, kita tinggal menggunakan tanda [ ] dalam useState untuk menandakan
>
> ```javascript
> const [nama, setNama] = useState([]);
> ```

### Apa itu useEffect Hooks ?

> Merupakan hooks yang bisa digunakan untuk menggunakan lifecycle pada functional component dengan mudah.

### Apa itu lifeCycle ?

> - Jika dianalogikan bisa dianggap seperti lingkaran kehidupan selama 24 jam mulai dari bangun tidur hingga tidur lagi.
> - lifeCycle yang ada didalam hooks, hanya menggunakan useEffect yang mengsatukan componentDidMount, componentDidUpdate, dan componentWillMount.

### Penggunaan useEffect

> - Penggunaan useEffect, bisa dimasukan sebelum melakukan render, useEffect sendiri biasanya sendiri biasanya ditempatkan dibawah useState.
> - Nantinya, apa yang kita tuliskan dalam useEffect akan dijalankan setiap component baru di mount (componentDidMount), terjadi perubahan (componentDidUpdate), dan pada saat component akan ditinggalkan (componentWillMount).

### Cara penggunaan useEffect

> 1. import useEffect
>
> ```javascript
> import { useEffect } from "react";
> ```
>
> 2. Tuliskan penggunaan useEffect sebelum dirender
>
> ```javascript
> useEffect(() => {
>   console.log("telah terjadi perubahan");
> }, [nama]);
> ```

### Penggunaan useEffect Hooks

> Biasa digunakan ketika membuat suatu call API, karena API akan selalu dipanggil ketika komponen terbentuk, maka call API bisa dilakukan di dalam useEffect.
