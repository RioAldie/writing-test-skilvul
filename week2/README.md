# Week And Presentation Week 2

<!-- scope and function -->
<!-- data type -->
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

- untuk memanipulasi element HTML baru kita dapat menggunakan

  - .innerHtml (menambahkan syntax html)
  - .innerText (menambahkan text)
  - .textContent (menambahkan text)
  - .writing (menambahkan syntarx html)

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
