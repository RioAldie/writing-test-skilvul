# Writing Week 4

## Async dan Await

- **Async Await** adalah Fitur yang mempermudah kita dalam menangani proses asynchronous. Async/Await merupakan syntax khusus yang digunakan untuk menangani Promise agar penulisan code lebih efisien dan rapih.

- Async Await sering digunakan saat mengelola API

- **Struktur** dasar async await adalah async dan await itu sendiri, untuk menggunakan async await kita harus menuliskan async didepan function kita dan menuliskan await pada blok kode yang ingin kita tunggu prosesnya.

- contoh kode async await

  ```
      const getDataFromAPI = async () =>{
          const data = await getAllData();

          return data;
      }

  ```

## API

- **API atau Aplication User Interface** adalah mekanisme yang memungkinkan dua aplikasi saling berhubungan.
- API sendiri memiliki format Javascript Object Notation atau JSON.

## JSON

- **JSON atau Javascript Object Notation** adalah format yang digunakan untuk menyimpan dan mentransfer data.

- Berbeda dengan XML (extensive markup language) dan format lainnya yang memiliki fungsi serupa, JSON memiliki struktur data yang sederhana dan mudah dipahami. Itulah mengapa JSON sering digunakan pada API.
- **Struktur JSON** pada umumnya adalah Array of object atau object didalam array.

## Fecth API

- **Fetching API** adalah sebuah proses pengambilan data dari sebuah API.
- untuk melakukan fecthing data didalam javascript kita dapat menggunakan sebuah method bernama fecth dengan argumen url atau endpoint yang akan kita hit.

  ```
      const getMoviesBySearch = async (query) => {

          const data = await fetch(
              `https://api.themoviedb.org/3/search/movie?api_key=10badd151dbb806d6e12dd2bf5f10f9d&query=${query}&page=1`
          )
              .then((res) => res.json())
              .catch((err) => console.log(err))
              .finally((data) => {
              return data;
              });
          movies = data.results;
          renderMovies(movies);
          };

  ```

## Github Lanjutan

-**Git Clone** Untuk mengkloning repository didalam git hub
`git clone "url"`

### git pull

- Untuk mengambil data didalam repository

### git merge

- Untuk menggabungkan repositori

## Responsive Design

- Responsive web design adalah tampilan website yang bisa menyesuaikan dengan device pengguna.

- Ada beberapa cara untuk menerapkan responsive design didalam website
  - media query
  - flexbox
  - grid
- responsive design memiliki beberapa ukuran yang bisa digunakan
  - %
  - em
  - rem

### media query

    - untuk menggunakan media query kita membutuhkan sebuah breakpoints.
    - contoh penerapan media query didalam CSS
    ```
        @media screen and (min-width: 500px) and (max-width: 700px) {
            body {
            background-color: grey
            }
        }
    ```
    jika layar device berada diantara 500px dan 700px maka background dari body akan memiliki warna grey.

### Flexbox

- **Flexbox** merupakan konsep pengaturan layout yang mengatur ukuran elemen Child dari suatu Container untuk beradaptasi dengan Parent/Container-nya.

  - cara penggunaan flexbox adalah dengan menganti display menjadi display: flex;
  - beberapa property flexbox yang sering digunakan

    - **flex-direction** untuk mengatur penempatan elemen-elemen didalamnya yaitu secara horizontal atau vertikal
    - **justify-content** untuk mengatur jarak antar elemen secara otomatis
    - **align-items** untuk mengatur penempatan elemen-elemen
    - **flex-wrap** untuk membuat elemen-elemen dapat melakukan wrapping saat box berubah
    - contoh penggunaan flexbox

      ```
          div{
              display: flex;
              flex-direction: row;
              justify-self: start;
              flex-wrap: wrap;
              align-items: center;
          }

      ```

## Bootstrap

- **Bootsrap** adalah sebuah framework CSS yang dapat digunakan untuk mendesain sebuah halaman website dengan lebih mudah.

- untuk menggunakan bootstrap di website, kita dapat menggunakan beberapa cara

  - **NPM**
    dengan Node Package manager kita dapat menginstal boostrap di project kita
    `npm install bootstrap`
  - **CDN**
    dengan CDN kita tidak perlu mengisntall boostrap kita hanya tinggal menempel CDN yang telah disediakan kedalam project kita

    ```
     <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js">

    ```

- untuk penggunaan boostrap kita bisa menuliskan syntax atau kode bootstrap kedalam class di element kita
  `<button class="bg-danger"> Tombol Merah </button>`

- kelebihan dalam menggunakan boostrap adalah boostrap telah menyediakan css atau style yang dapat langsung kita gunakan seperti warna,ukuran font, layout dll

- untuk lebih lengkapnya kita bisa melihat dokumentasi dari penggunaan boostrap itu sendiri di link berikut
  https://getbootstrap.com/docs/5.0/getting-started/introduction/
