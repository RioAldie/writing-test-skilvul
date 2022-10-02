# Week And Presentation Week 2

<!-- scope and function -->

## Scope dan Function

### scope

- **scope** adalah konsep yang digunakan untuk membatasi pengaksesan sebuah variabel
- **block** adalah kode yang ada didalam curly bracket atau {}, block biasanya digunakan if,for,while dan lain-lain.
- **Global Scope** adalah variabel yang dapat diakses dimanapun

```
 let nama = 'Rio Aldi Erwanto'
 function(){
    console.log(nama)
 }

```

dikode diatas variabel nama merupakan global scope karena kita bisa mengaksesnya dimana pun.

- **Local Scope** adalah varibel yang aksesnya dibatasi didalam block tempat variabel tersebut dideklarasikan.

```

 function(){
  let nama = 'Rio Aldi Erwanto'

 }
  console.log(nama)
```

pada kode diatas kita memanggil variabel diluar block dan itu akan menyebabkan error karena local scope hanya dapat diakses didalam block itu sendiri.

### function

- **function** adalah sebuah blok kode yang dirancang untuk menyelesaikan tugas tertentu.

```
  function greeting(){
    console.log('halo dunia');
  }

```

- **membuat function** untuk membuat function kita perlu menuliskan syntax

  ```
    function namaFunction( parameter ){
      // isi function
    }

  ```

- **memanggil function** untuk memanggil function kita dapat menuliskan nama function ynag ingin dipanggil dan ().

```
  greeting();

```

- **parameter** adalah tempat untuk menerima data yang dikirim kedalam function

```
  function mahasiswa(nama){
    console.log(nama)
  }
  //nama adalah sebuah parameter
```

- **argumen** adalah data yang dikirimkan kedalam function.

```
  mahasiswa('aldi');

  //'aldi' adalah sebuah argumen
```

- **default parameter** adalah paramenter yang memiliki value default, value ini digunakan jika function tidak menerima sebuah argumen.

```
  function mahasiswa(nama = 'rio'){
    console.log(nama)
  }
  //nama adalah sebuah parameter dan 'rio' adalah nilai devault-nya
```

- **function helper** adalah funtion yang dipanggil didalam function lain.
- **arrow function** adalah cara penulisan function menggunakan () =>, arrow function merupakan syntax baru function didalam ES6.

```
const greeting = () =>{
  console.log('halo dunia');
}

```

- **return didalam function** kita tidak wajib menggunakan return didalam function akan tetapi dalam kasus tertentu return sangatlah dibutuhkan dan menurut saya return itu sangat penting untuk mengetahui nilai apa yang dihasilkan oleh function kita.

<!-- data type -->

## Data Type

- **tipe data** didalam javascript ada tipe data primitif dan non-primitif

### primitif

- **Tipe Data Primitif** adalah tipe data sederhana yang hanya mampu menampung satu jenis value

  - **String** adalah tipe data yang dapat menampung banyak karakter sekaligus.

  ```
        let nama = 'Rio Aldi';
  ```

- **Number** adalah tipe data yang menampung angka

  ```
        let umur = 21;

  ```

- **Boolean** adalah tipe data yang bernilai benar atau salah(true/false)

  ```
        let isLogin = false;

  ```

- **null** adalah tipe data yang memiliki nilai null / tidak ada

```
  let myMoney = null;
```

- **undefined** adalah tipe data yang memiliki nilai tetapi tidak terdefinisi;

### Non-Primitif

- **Tipe Data Non-Primitf** adalah tipe data yang didefinisikan sendiri oleh programer dan bisanya lebih dari satu nilai.

- contoh **Array** dan **Object**

  ```
    const hewanReptile = ['ular','buaya','kadal'];
    const mahasiswa = {
      nama: 'Rio Aldi E',
      umur: 21,
      Nim: '2013020017'
    }

  ```

<!-- dom dasar -->

## DOM(Document Object Model)

- **Definisi DOM** -DOM adalah sebuah API yang menyediakan fungsi-fungsi untuk memanipulasi dokumen,DOM bukanlah bagian dari javascript tapi DOM sangat berkaitan erat dengan javascript terumata untuk memanipulasi HTML.

### **Cara Penggunaan DOM**

-untuk menggunakan atau memamnggil elemen HTML dengan DOM ada beberapa cara, berikut cara yang paling sering digunakan

- `document.getElementById()`
  untuk memanggil element html berdasarkan id element
- `document.getElementsByClassName()`
  untuk memanggil element html berdasarkan class element
- `document.getElementsByName()`
  untuk memanggil element html berdasarkan atribut name pada element
- `document.getElementsByTagName()`
  untuk memanggil element html berdasarkan Tag element
- `document.querySelector()`
  untuk memanggil satu element html yang memiliki query yang kita inginkan
- `document.querySelectorAll()`
  untuk memanggil semua element html yang memiliki query yang kita inginkan
- selain cara diatas ada beberapa cara lain untuk memanggil element html didalam DOM.

### **Memanipulasi Element HTML dengan DOM**

- untuk memanipulasi element HTML kita dapat menggunakan

  - .innerHtml (menambahkan syntax html)
  - .innerText (menambahkan text)
  - .textContent (menambahkan text)
  - .writing (menambahkan syntarx html)
  - .createElement (membuat elemen baru)
  - .appendChild (menambahkan child baru)

- contoh kode mengubah elemen baru dihtml dengan DOM

  ```
      //kita buat element div untuk dijadikan parent terlebih dahulu

      <div id="parent"></div>

      //lalu kita panggil element tersebut menggunakan DOM

      document.getElementById('parent')

      //kita bisa menggunakan innerHTMl untuk menambahkan elemen baru didalam parent tadi

      document.getElementById('parent').innerHTML = "<h1>Belajar DOM Manipulation</h1>"

  ```

### **memanipulasi Style dengan DOM**

- untuk memanipulasi style dengan DOM kita dapat menggunakan .style.attribute = value;
- contoh manipulasi style

```
   // kita buat elemen yang akan kita styling
   <span id="redtext"> Text ini Merah </span>

   // lalu kita panggil elemennya menggunakan DOM
   document.getElemenById('redtext')

   // setelah itu kita gunakan style
   document.getElemenById('redtext').style.color = "red";


```

### **DOM Events**

- Events adalah interaksi elemen HTML dengan user.
- DOM Events adalah Object Model yang digunakan untuk menangkap interaksi user didalam elemen HTML
- berbagai HTML DOM Events yang sering digunakan

  - onclick
  - onsubmit
  - onchange
  - mouseenter
  - onfocus

- kita bisa langsung menggunakan Events dengan menggunakan element html

```
  <button onclick="submit()">tombol</button>

```

contoh dikode diatas adalah ketika button diclik kita akan memanggil function submit();

- kita juga bisa menambahkan event dengan menggunakan dom, yaitu menggunakan method addEventListener
- **addEventListener** adalah method untuk membuat event dan melakukan manipulasi didalam DOM.
  - addEventListener menerima argumen event dan function
  - ada beberapa eventListener
    - 'click'
    - 'mouseenter'
    - 'mousehover'
    - 'onfocus'
    - 'blur'
    - 'scroll'
    - dll
- berikut adalah syntax dasar eventListener dan cara menggunakannya.

```
  document.getQuerySelector('button').addEventListener('click',()=>{
    console.log('tombol diklik')
  });
  //output 'tombol diklik'

```

- pertama kita panggil element html terlebih dahulu
- lalu kita tambahkan addEventListener
- kita masukan event 'click' sebagai argumen pertama
- kita buat function sebagai argumen kedua
