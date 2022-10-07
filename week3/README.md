# Week And Presentation Week 2

## Array

- **Array** adalah truktur data yang digunakan untuk menyimpan sebuah kelompok data dalam satu tempat, array di javascript dapat menampung berbagai tipe data yang berbeda.
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

  - **forEach()** untuk melakukan looping pada setiap elemen array
  - perbedaan map() dan forEach() adalah konsep mereka hampir sama akan tetapi map dapat menghasilkan array baru sedangkan forEach() hanya dapat mengubah array.
