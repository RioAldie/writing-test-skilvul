# Week And Presentation Week 2

## Array

- **Array** adalah truktur data yang digunakan untuk menyimpan sebuah kelompok data dalam satu tempat, array di javascript dapat menampung berbagai tipe data yang berbeda.

### **Cara Penggunaan Array**

- untuk membuat array kita perlu menggunakan square bracket atau kurung siku []
- setiap data didalam array memiliki index, index didalam array dimulai dari 0

  ```
      let buah = ['mangga','anggur','jeruk'];
      //  index :   0     ,   1    ,   2
      console.log(buah)

  ```

- untuk menampilkan atau mengambil isi didalam array kita dapat menggunakan index value

  - contoh kode untuk mendaptkan anggur dari array buah

  ```
      let buah = ['mangga','anggur','jeruk'];

      console.log(buah[1]);
      //Output 'anggur'

  ```

- untuk menampilkan/mengambil seluruh isi dari array kita dapat menggunakan perulangan for
  -contoh kode untuk menampilkan seluruh isi array buah

  ```
  let buah = ['mangga','anggur','jeruk'];

  for(let i=0; i< buah.lenght; i++){
      console.log(buah[i])
  }

  ```

- menganti isi array atau mengupdate array dapat mencari terlebih dahulu array indexnya dan kita masukan value yang baru

  - contoh kode untuk mengupdate array buah

  ```
  let buah = ['mangga','anggur','jeruk'];

  buah[1] = 'pisang';
  console.log(buah);

  ```

### Array Property

- **Array Property** adalah fitur yang sudah disediakan atau bawaan didalam javascript untuk membantu developer menggunakan array

        - constructor
        - length
        - index
        - input
        - prototype

  - contoh kode penggunaan property length

  ```
    let buah = ['mangga','anggur','jeruk'];
    console.log(buah.length)

    //output: 3

  ```

### Array Method

- **Array Method** adalah built-in-method yang disediakan oleh javascript untuk memanipulasi array
- contoh array built-in-methods yang sering digunakan

  - **push()** untuk menambahkan item baru kedalam array pada urutan terakhir

    ```
       let buah = ['mangga','anggur','jeruk'];

       buah.push('manggis')

       console.log(buah);

       // output : 'mangga','anggur','jeruk','manggis'

    ```

  - **pop()** untuk menghapus item array di index paling akhir

    ```
       let buah = ['mangga','anggur','jeruk'];

       buah.pop()

       console.log(buah);

       // output : 'mangga','anggur'

    ```

  - **shift()** untuk menghapus item array paling awal

    ```
       let buah = ['mangga','anggur','jeruk'];

       buah.shift()

       console.log(buah);

       // output : 'anggur','jeruk'

    ```

  - **sort()** untuk mengurutkan array

    ```
       let angka = ['2','1','5']

       angka.sort()

       console.log(angka);

       // output : '1','2','5'

    ```

  - **map** untuk melakukan looping dengan membuat sebuah array baru

    ```
       let buah = ['mangga','anggur','jeruk'];

       buah.map((b,i) =>{
        //b adalah item dan i adalah index
        return console.log(i, b)
       })

       console.log(buah);

    ```

### Array Looping

- **forEach()** untuk melakukan looping pada setiap elemen array
- perbedaan map() dan forEach() adalah konsep mereka hampir sama akan tetapi map dapat menghasilkan array baru sedangkan forEach() hanya dapat mengubah array.

- **Array Multi dimensi** adalah array yang didalamnya terdapat array sehingga membentuk kelompok dan dimensi

  - contoh array multidimensi

  ```
      const buah = [
          ['jambu biji', 'jambu air',],
          ['jeruk peras', 'jeruk bali'],
          ['durian aceh', 'durian musangking']
      ]

  ```

## Object

- **Object** adalah tipe data non-primitid yang digunakan untuk menyimpan sebuah property dan method.
  - struktur object dibuat dengan menggunakan curly bracket "{}".

### Property Object

- **Property** adalah data lengkap dari sebuah object yang menyimpan sebuah data.
  - property dibuat dengan menggunakan key dan value
  - key adalah nama dari property
  - value adalah isi atau nilai dari property.

### Method Object

- **Method** adalah action dari sebuah object, method menyimpan sebuah function didalam object
  - property dibuat dengan menggunakan key dan value
  - key adalah nama dari method / nama function
  - value adalah function itu sendiri
- contoh kode object

  ```
      let state = {
        nama: "rio aldi erwanto",
        umur: "21",
        salam: () =>{
          console.log("halo, perkenalkan saya rio")
        }
      }

  ```

### Manipulasi Object

- **Mengakses Object**
  untuk mengakses property atau method kita dapat menggunakan namaObject.property

  ```
    console.log(state.nama)
    console.log(state.salam)

  ```

- **Menambahkan Properti baru**
  untuk menambahkan property baru kita dapat menggunakan assigment "=" dan spread operator "{...}

  ```
    state = {...state, nim: '2013020017'}

  ```

- **Mengupdate sebuah Object**
  untuk menguptade kita perlu memanggil properti terlebih dahulu lalu kita gunakan assignment "=" dan value baru.

  ```
    state.umur = 22;

  ```

- **menghapus sebuah Object**
  untuk menghapus object kita dapat menggunakan delete operator.
  ```
    delete state.nim;
  ```

### Nested Object

- **Nested Object** adalah sebuah object yang berada didalam object
  ```
        let state = {
          nama: "rio aldi erwanto",
          umur: "21",
          keluarga:{
            adik: "rahma"
          }
        }
  ```

### Looping Object

- **Lopping Object** untuk melakukan sebuah perulangan pada object kita dapat menggunakan method bawaan js yaitu "for in"
  ```
    for(let key in object){
      //console.log(key)
    }
  ```

### Array Of Object

- sebuah array yang menyimpan object didalamnya, konsep aof ini sangat berkaitan erat dengan JSON dan akan kiat jumpai nanti saat bermain dengan API.

## Module

- **javacript module** adalah file Javascript yang di dalamnya terdapat value dari objects, functions, dan variables. Kemudian file tersebut dapat diexport dan diimport oleh file lain. Yang mana file lain yang mengimportnya dapat menggunakan values yang ada di file tersebut.
- **export** adalah sebuah metode dimana kita memberikan akses pada kode kita agar dapat digunakan oleh file js lainnya.

  - pada versi nodejs 14 kebawah untuk melakukan export kita perlu menuliskan
    module.exports = namavariabel;
    `module.exports = state;`
  - sedangakan ada cara yang lebih baru jika kita menggunakan node versi 14 keatas
    `export state;`

- **import** adalah sebuah metode untuk menerima/memanggil sebuah variabel dari file lain.
  - pada versi nodejs 14 kebawah untuk melakukan import kita perlu menuliskan
    require('file.js')
    `const state = require('file.js')`
  - sedangakan ada cara yang lebih baru jika kita menggunakan node versi 14 keatas
    `import state from 'file.js'`

## Rekursive Function

- **Rekursif** adalah sebuah function yang memanggil dirinya sendiri.
- rekursif kebanyakan digunakan untuk kasus yang berkaitan dengan perhitungan.
- contoh function rekursif

  ```
      function rekursif(n){
          if(n === 9){
            return n;
          }
          x = x + 1;
          return rekursif(x);
      }

  ```

## Web Storage API

- salah satu Web API yang dapat menyimpan data secara lokal pada sisi client. Berbeda dengan objek atau array, data yang disimpan pada objek atau array JavaScript bersifat sementara, dan akan hilang jika terjadi reload atau pergantian URL pada browser,data yang disimpan didalam webstore akan tetap ada walaupun website di reload maupun diclose.

### Local storage

- Local storage adalah sebuah penyimpanan data di local browser dan data tersebut tidak akan terhapus walaupun browser diclose dan direload, local storage seringkali digunakan untuk menyimpan session login.
- **setItem** untuk menyimpan data kelocal storage

```
  localStorage.setItem(key, 'value');

```

- **getItem** untuk mengambil data di local storage

```

  const dataLocal = localStorage.getItem(key);

  console.log(dataLocal);

```

### Cookies

- Cookie adalah file yang dibuat oleh situs yang Anda kunjungi. Cookie membuat kegiatan online Anda jadi lebih mudah dengan menyimpan informasi browsing. Dengan cookie, situs membuat Anda tetap login, mengingat preferensi situs Anda, dan memberikan konten lokal yang sesuai dengan Anda.

## Asyncrhonous

**Syncronous** adalah eksekusi code secara berurutan dimana eksekusi akan menunggu sampai kode selesai sebelum lanjut ke kode slanjutnya.
**Asyncronus** adalah eksekusi code tanpa menunggu eksekusi code lain selesai, dimana kode dibawahnya akan tetap dieksekusi walaupun kode diatas belum dieksekusi

### Callback

- **Callback** adalah sebuah parameter yang merupakan function
- contoh callback

  ```
    function intro(nama){
      consolee.log('Halo saya', nama);
    }

    function getNama(){
      const nama = prompt('masukan nama anda');
      intro(nama);
    }

    getNama();

  ```

### Promise

- **Promise** Sebuah mekanisme baru pada fitur javascript / ES6 yang merepresentasikan sebuah object request pengolahan data yang dilakukan secara asynchronous seperti ajax.
- promise digunakan untuk mendapatkan hasil yang masih belum selesai atau masih diharapkan.
- promise memiliki 2 paramaeter utama yaitu resolve dan reject
- resolve adalah instan object yang mengembalikan nilai kedalam then()
- reject adalah instan object yang mengembalikan error kedalam catch()

  ```
    const myPromise = new Promise((resolve, reject) => {
                  if(login){
                    return resolve("Login berhasil");
                  }else{
                    return reject("login gagal");
                  }
               });
    myPromise.then((res)=>{
        console.log(res);
    }).catch((err) =>{
        console.log(err);
    })

  ```
