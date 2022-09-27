# Week And Presentation Week 1

## Unix Command Line

#### **Shell**

- Shell adalah user interface yang bertugas untuk memproses semua perintah yang diketik di CLI.
- Terdapat 2 jenis shell yaitu Command Line Interface (CLI) dan Graphical User Interface (GUI).

#### **Command Line Interface**

- Command Line Interface atau CLI adalah program yang memungkinkan pengguna mengetik perintah teks yang memerintahkan komputer untuk melakukan tugas tertentu.
- Ada Beberapa CLI Shell contoh:

  - bash
  - zsh
  - fish
  - dash

- Cara mengakses cli dikomputer untuk windows adalah menggunakan command promt, yaitu Buka menu pada ❖ atau Windows Logo 🡒 ketik “Command Prompt” 🡒 pilih Command Prompt.
- berikut adalah tampilan awal dari command-prompt, cli bawaan dari windows.
- ![image info](./asset/command-prompt.png)
- didalam CLI kita bisa melakukan berbagai perintah seperti
  -membuat file
  -menghapus file
  -menganti nama sebuah file
  -dll.

#### **Graphic User Interface**

- GUI merupakan bentuk antarmuka yang memungkinkan pengguna untuk menggunakan elemen grafis dalam berinteraksi dengan komputer atau sistem operasi.
- ini adalah tampilan GUI yang ada di Windows
- ![image info](./asset/Gui.png)
  didalam GUI kita juga bisa melakukan beberapa hal seperti di CLI, GUI juga memiliki kelebihannya sendiri yaitu didalam GUI kita mampu menampilkan media visual seperti Image, Poto dan Video.

#### **File System**

- Pengertian File System itu adalah suatu cara untuk memisahkan data yang ada pada disk/drive dan dibagi menjadi beberapa bagian.
- semua disk atau penyimpanan yang ada dikomputer pasti menggunakan file system tertentu.
  - windows menggunakan **NTFS(New Technology File System)**
  - Mac menggunakan **HFS+(Hierarchical File System+)**
  - Linux menggunakan file system yang berbeda-beda karena Linux memiliki banyak sistem operasi dan distro,tapi umumnya Linux menggunakan **EXT(EXTended File System)**
- **pwd**
- command pwd berfungsi untuk melihat current working directory
- untuk menggunakan pwd cukup mengetikan pwd di shell cli.
- ![image info](./asset/pwd.png)

#### **ls**

- command ls berfungsi untuk menampilkasn list isi di sebuah directory
- untuk menggunakan ls cukup mengetikan ls di shell cli.
- ![image info](./asset/ls.png)

#### **cd**

- command cd berfungsi untuk berpindah directory
- untuk masuk kedalam sebuah directory dapat menggunakan

```
  cd namadirektori

```

- ![image info](./asset/cd-in.png)
- untuk keluar dari directory dapat menggunakan

```
  cd ..

```

- ![image info](./asset/cd-out.png)

#### **head,tail,cat**

- head, tail dan cat sama-sama berfungsi untuk menampilkan isi dari sebuah files, walaupun memiliki fungsi yang sama mereka memiliki kemampuan yang berbeda-beda seperti head hanya akan menampilkan bagian kepala atau atas dari sebuah file, sedangkan tail adalah kebalikan head tail akan menampilkan bagian akhir dari sebuah file, sedangkan cat berfungsi untuk menampilkan seluruh isi dari file karena itulah cat jauh lebih sering digunakan.
- contoh penggunaan cat
- ![image info](./asset/cat.png)

#### **mkdir**

- command mkdir berfungsi untuk membuat atau menambah sebuah direktori atau folder baru
- cara penggunaan mkdir

```
- mkdir (spasi) nama direktori

```

- ![image info](./asset/mkdir.png)

#### **Touch**

- Touch berfungsi membuat file baru dapat menggunakan Touch
- cara menggunakan touch

```
- touch (spasi) nama file yang akan dibuat

```

- ![image info](./asset/touch.png)

#### **cp**

- cp adalah command untuk menyalin atau mencopy direktori dan file
- cara menyalin direktori menggunakan cp adalah mengetikan cp -r (nama direktori yang akan dicopy) (nama direktori baru)

```
- cp -r direktori_baru direktori_copian

```

- - ![image info](./asset/cpr.png)

- cara menyalin file menggunakan cp adalah mengetikan cp (nama file yang akan dicopy) (nama file baru)

```
- cp file_baru file_copian

```

- ![image info](./asset/cp.png)

#### **mv**

- command mv berfungsi untuk memindahkan atau rename file dan direktori
- cara penggunaan mv sebagai berikut

  - untuk memindahkan file caranya adalah mengetikan mv (nama file yang akan dipindahkan) (direktori yang dituju)

  ```
    mv file.html direktori/

  ```

  - hasil ![image info](./asset/mv-file.png)
  - untuk memindahkan direktori caranya adalah mengetikan mv (nama direktori yang akan dipindahkan) (direktori yang dituju)

  ```
    mv directori_satu/ direktori_dua/

  ```

  - hasil ![image info](./asset/mv-r.png)
  - untuk menganti nama file/direktori adalah mengetikan mv (nama file sebelumnya) (nama file baru)

  ```
    mv nama_lama nama_baru

  ```

  - hasil ![image info](./asset/mv-rename.png)

#### **rm**

- command rm berfungsi untuk menghapus direktori dan file
- untuk menghapus file/direktori cukup menuliskan rm (nama file yang akan dihapus)
- hasil ![image info](./asset/rm.png)

## Git dan Github Dasar

<!-- Peserta mampu memahami kenapa Git dan Github tools yang wajib digunakan -->

#### **Git**

- Git adalah sebuah version control system pada perangkat lunak yang berfungsi untuk menyimpan setiap perubahan pada file maupun direktori pada suatu project.
- kenapa kita harus menggunakan Git pada project kita, karena dengan git kita bisa mengetahui perubahan apa saja yang terjadi.

#### **Github**

- Github adalah sebuah website untuk manajemen project entah itu menyimpan maupun megelola, github juga merupakan platform jejaring sosial bagi software developer diseluruh dunia.
- kenapa kita harus menggunakan Github, karena Github memudahkan kita untuk menyimpan kode yang telah kita buat dan Github juga membantu kita untuk berkolaborasi dengan orang lain, Github juga bisa kita gunakan sebagai portfolio kita.
  <!-- Peserta mampu memahami perbedaan antara Git dan Github -->
  <!-- Peserta mampu memahami alur kerja dari Git dan Github -->

#### **Alur Kerja**

- Alur kerja untuk penggunaan Git dan Github adalah
  1. buat sebuah repositori baru diwebsite github
  2. buka file project kita diterminal
  3. lakukan inisiasi dengan git init
  4. buat remote baru
  5. masukan file dengan git add ./ git \* (setalah melakukan git add . file perubahan akan tersimpan di lokal kita)
  6. lakukan commit pada file yang telah ditambahkan dengan git commit (setelah melakukan commit perubahan akan tersimpan secara permanen dilokal)
  7. lakukan push untuk mengirim file kedalam repositori kita (setelah push dilakukan file kita akan otomatis tersimpan di github secara permanen)
  <!-- Peserta mampu memahami dan membuat Repository Git -->

#### **Repositori**

- Repositori adalah sebuah direktori untuk menyimpan files didalam github, repositori biasanya disebut repo.
- cara membuat repo adalah
- .masuk kedalam platform github
- .klik tombol new repositori
- .masukan nama repositori dan pilih public atau private
- .untuk pengaturan lainnya adalah opsional
- .setelah itu tekan tombol create repository
- jika berhasil kita akan diarahkan ke halaman repositori dengan tampilan seperti ini
  ![image info](./asset/repo.png)
- kenapa muncul tampilan seperti itu, karena repositori tersebut masih kosong
<!-- Peserta mampu melakukan commit pada Git -->

#### **Add dan Commit**

- git Add berfungsi untuk menambahkan file atau perubahan file kita kedalam repositori.
- git Commit berfungsi untuk menyimpan file yang ditambahkan kedalam local.
- cara melakukan add adalah dengan mengetikan git add (nama file) dan git add ./\* (untuk seluruh file)

- ![image info](./asset/git-add.png)

- (**_note_** add hanya dapat dilakukan setelah diinisiasi)

- cara melakukan commit adalah dengan mengetikan git commit -m "pesan atau catatan kita"

![image info](./asset/git-commit.png)

- (**_note_** commit hanya dapat dilakukan setelah file ditambahkan)
  <!-- Peserta mampu mempublish aplikasi ke Github -->
- #### **publish to Github**
- 1. untuk mempublish ke github kita perlu membuat sebuah repo
- 2. setelah itu kita inisiasi dan membuat remote baru dengan alamat yang sesuai dengan repo

  ```
  git remote add origin https://github.com/RioAldie/repo-saya.git

  ```

- 3. lalu kita buat branch baru, jika mengikuti default github nama branch kita akan menjadi main

  ```
  git branch -M main

  ```

- 4. setelah itu kita push semua file yang telah dicommit sebelumnya

  ```

  git push -u origin main

  ```

- contoh ![image info](./asset/git-publish.png)
- hasil ![image info](./asset/myrepo.png)
  <!-- Peserta mampu melakukan cloning Github ke local -->
- #### **Clone**
- untuk mengcloning sebuah repositori ke dalam local dapat menggunakan git clone
- 1. buat folder baru
- 2. masuk ke terminal sesuai dengan root folder
- 3. ketikan git clone (link dari repo yang akan diclone)
- 4. cloning berhasil
- contoh ![image info](./asset/git-clone.png)

## HTML

- **HTML(hyper text markup language)** adalah sebuah bahasa markup yang berfungsi sebagai kerangka dasar dalam pembuatan website.
- file html memiliki format namafile.html
- susunan html bisa dibuat dengan hanya element html,head,title,body tetapi setelah hadirnya html 5 susunannya berubah.
- contoh syntak html

```
  <html>
    <head>
      <title> website dengan HTML</title>
    </head>
    <body>
      Halaman Utama
    </body>
  </html>

```

- contoh syntax html5

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website dengan HTML 5</title>
</head>
<body>
    Halaman Utama
</body>
</html>

```

- jika kita menggunakan text editor vscode dan sublime terdapat snippet yang membantu kita menuliskan syntax awal html yaitu cukup ketikan **!** pada file html kita
- syntax didalam html terdiri dari susunan taq atau emement
- penulisan element atau tag umumnya adalah menggunakan <> sebagai pembuka dan </> sebagai penutup, walaupun juga terdapat beberapa element yang tidak memerlukan penutup element itu disebut void element.
- contoh tag HTML yang paling sering digunakan

  ##### Tag untuk memanipulasi Font/text

  - **h1,h2,h3,h4,h5,h6** adalah element yang digunakan untuk membuat judul didalam html, element ini dimulai dari h1 untuk ukuran terbesar dan diahiri h6 untuk ukuran judul terkecil

  ```
      <h1>Header 1</h1>
      <h2>Header 2</h2>
      <h3>Header 3</h3>
      <h4>Header 4</h4>
      <h5>Header 5</h5>
      <h6>Header 6</h6>

  ```

  - **p** adalah element tag yang digunakan untuk membuat sebuah paragraf dalam html

  ```
     <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta excepturi magni perferendis, totam neque corporis suscipit expedita. Libero, rerum? Ut cum officia architecto deserunt corporis amet mollitia fugit molestias exercitationem.</p>

  ```

  - **b,i,bold,strong,q** adalah tag untuk merubah styling font/text.

  ```
     <b>Untuk merubah text menjadi bold/bercetak tebal</b>
     <bold>Untuk merubah text menjadi bold/bercetak tebal</bold>
     <strong>Untuk merubah text menjadi bold/bercetak tebal</strong>
     <i>untuk merubah text menjadi italic/bercetak miring</i>
     <q>untuk menambahkan " " / tanda kutip atau merubah text menjadi quotes </q>

  ```

  ##### List dan Tabel

  - **ul,ol dan li** adalah taq untuk membuat list di html
  - li sebagai penampung data yang ada dilist atau sebagai item yang dilist
  - ul untuk membuat unordered list atau list yang tidak teratur
  - ol untuk membuat ordered list atau list yang teratur/berurutan

  ```
    <ul>
      <li> list item 1 </li>
      <li> list item 2 </li>
      <li> list item 3 </li>
    </ul>
    <ol>
      <li> list item 1 </li>
      <li> list item 2 </li>
      <li> list item 3 </li>
    </ol>

  ```

  - **table,th,tr,td** adalah element tag html untuk membuat sebuah tabel
  - table untuk membuat sebuah table itu sendiri
  - th untuk membuat tabel head
  - tr untuk membuat tabel row
  - td untuk membuat tabel cell

  ```
  <table border="solid">
      <tr>
          <th>name</th>
          <th>umur</th>
          <th>kota</th>
      </tr>

      <tr>
          <td>rio</td>
          <td>21</td>
          <td>nganjuk</td>
      </tr>
  </table>
  ```

  ##### Anchor

  - **a href** adalah tag element html yang berfungsi sebagai penampung link aktif dan sebagai navigasi

  ```
      <a href="#home"> tombol untuk pergi ke home </a> //contoh penggunaan a href untuk navigasi dihalaman dengan menggunakan id sebagai targetnya
      <a href="https://facebook.com"> tombol untuk pergi ke website lain </a> //contoh penggunaan a href untuk membuka website lain
  ```

  ##### Section,Div,Span

  - **Section** adalah tag html untuk mendefinisikan setiap sesi
  - **Div** adalah tag html untuk mendefinisikan divisi, element div sendiri sangat erat dengan konsep Box element
  - **Span** adalah tag yang sebenarnya tidak mempresentasikan apapun, span sering digunakan untuk memanipulasi text pada bagian tertentu span berkaitan erat dengan styling.

  ```
    <section>
      <div>
        ini adalah sebuah div didalam section <span> ini span </span>
      </div>
    </section>

  ```

  ##### Media atau Content

  - **img** adalah tag untuk menampilkan sebuah gambar
  - **audio** adalah tag untuk menampilkan suara
  - **video** adalah tag untuk menampilkan video

  ##### Semantic element

  - **semantic html** adalah tag html yang lebih mementingkan informasi yang ada, semantic html juga sangat berguna untuk menunjang peforma SEO.
  - **article** untuk membuat elemen artikel
  - **aside** untuk membuat elemen bagian samping
  - **details** untuk membuat elemen datail atau spoiler
  - **figcaption** untuk membuat teks caption pada figure
  - **figure** untuk membuat figur atau gambar pada artikel
  - **footer** untuk membuat footer
  - contoh implementasi semantic

```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic HTML</title>
</head>
<body>
    <header>
        <nav>
            navigasi
        </nav>
    </header>
    <article>Artikel 1
        <figure>gambar</figure>
    </article>
    <article>Artikel 2</article>
    <aside>Aside </aside>
    <footer>
        footer
    </footer>
</body>
</html>
```

## CSS

<!-- Peserta mampu memahami peran CSS pada web development  -->

- **CSS(Cascading Style Sheet)** adalah sebuah bahasa markup yang berfungsi untuk mempercantik sebuah halaman website
<!-- Peserta mampu memahami beberapa cara menyisipkan CSS ke dalam HTML  -->
- ##### **Cara penggunaan CSS**
- ada 3 cara penggunaan CSS
  **inline** > cara penggunaan CSS inline adalah menuliskan secara langsung sebuah code css kedalam sebuah tag element HTML
  - contoh kode css untuk merubah warna teks dengan inline css
  ```
    <p style="color: Blue;">Blue</p>
  ```
  **internal** > cara penggunaan CSS internal adalah dengan menuliskan kode css di satu file HTML.
- best practice dalam penggunaan internal CSS adalah dengan menuliskan kode css kita dibawah element head dan diatas body.

  - contoh kode css untuk merubah warna teks dengan internal css

  ```
  <style>
      p{
          color: blueviolet;
      }
  </style>

  ```

**external css**

- cara penggunaan CSS external adalah dengan menuliskan kode css kedalam file terpisah dengan format .css, lalu file tersebut akan dipanggil - - didalam html menggunakan element link - contoh pemanggilan css external

  ````
  <link rel="stylesheet" href="style.css">

      ```

  <!-- Peserta mampu memahami dan menggunakan sintaks dasar dari CSS  -->
  ````

##### **CSS Syntax**

- untuk menuliskan kode css yang benar kode css harus memiliki selector, property dan value property

```
  div{
    color: '#000000'
  }

```

- dari contoh diatas div merupakan selector, color merupakan property dan #00000 merupakan value dari properti
- selain itu css juga memiliki pseudo selector yang memiliki ciri khas : contoh div:hover{}
  <!-- Peserta mampu menerapkan styling CSS pada sebuah halaman HTML  -->
  <!-- Peserta mampu memahami dan menggunakan metode responsive web design menggunakan CSS  -->

##### **Responsive Design**

**Responsive website design** adalah website yang memiliki tampilan yang bagus saat website tersebut dibuka di berbagai device.

- untuk membuat responsive web design di css kita dapat menggunakan **Media Query**

  ```
  @media only screen and (max-width: 600px) {
    body {
      background-color: lightblue;
    }
  }

  ```

  <!-- Peserta mampu memahami dan menggunakan flexbox -->

##### **CSS Flexbox**

**Flexbox** merupakan konsep pengaturan layout yang mengatur ukuran elemen Child dari suatu Container untuk beradaptasi dengan Parent/Container-nya.

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

## Algoritma & Data Structures

#### Data Structures atau struktur data

- **Struktur Data** adalah cara penyimpanan , pengorganisasian , dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien.
- Manfaat Belajar Struktur data kita mampu menyusun data yang kita temui menjadi jauh lebih sistematis dan kita menjadi terbiasa berpikir by data dan berpikir secara kritis

#### Algoritma

- **Algoritma** adalah sederetan langkah-langkah logis yang disusun secara sistematis untuk memecahkan suatu masalah.
- Manfaat Belajar Algoritma adalah membantu kita mencari solusi dari masalah-masalah tertentu secara sistematis dan step by step.
- contoh algoritma sederhana menukar isi gelas A dan B
  - siapkan gelas C
  - masukan isi gelas A ke gelas C
  - masukan isi gelas B ke gelas A
  - masukan isi gelas C ke gelas B
  - isi gelas A dan B telah berhasi ditukar
- contoh penerapan algoritma menukar isi gelas A dan B kedalam sebuah bahasa pemrograman
  - start
  - buat variable gelasA = a, gelasB = b, gelasC
  - gelasC = gelasA
  - gelasA = gelasB
  - gelasB = gelasC
  - end
    **Big O Notation** adalah sebuah cara atau metode untuk melakukan analisa terhadap sebuah algoritma pemrograman terhadap waktu eksekusi.
- singkatnya big o notation ini sering digunakan untuk mendefinisikan kerumitas algortima oleh para programmer

###### penerapan algoritma dalam sebuah program Javascript

**contoh program mengetahui klasifikasi pengelompokan usia dengan diketaui umur**

```
<script>
        let umur = 40;
        if(umur <= 6){
            console.log('Balita')
        }else if(umur <= 11){
            console.log('Anak-anak')
        }else if(umur <= 16){
            console.log('remaja')
        }else if(umur <= 22){
            console.log('pemuda/pemudi')
        }else if(umur <= 40){
            console.log('dewasa')
        }else{
            console.log('tua')
        }
</script>
// output Dewasa

```

###### penerapan program struktur data dengan Javascript

**contoh program mengelompokan hewan reptil dengan array**

```
const reptil = ['ular','kadal','kura-kura','buaya']

```

## Javascript Dasar

- **javascript** adalah sebuah bahasa pemrongraman yang berfungsi untuk membuat halaman website menjadi lebih interaktif.
- javacript memiliki format file .js
<!-- Peserta mampu memahami dan menjalankan JavaScript -->
- javacript umumnya berjalan didalam web browser walaupun ada juga javascript yang berjalan didalam server yaitu NodeJs
- untuk menjalankan kode javascript kita bisa menuliskannya langsung didalam kode html didalam tag element script

```
  <script>
     console.log('Hello Skilvul')
  </script>

```

- sedangkan untuk best practice penggunaan javascript adalah dengan menulis kode js kita di file terpisah dengan format .js, lalu file tersebut akan kita panggil didalam file html

```
  <script src="script.js"></script>

```

- **variabel** adalah tempat untuk menyimpan suatu data
- didalam javacript ada 3 variabel yaitu
  - **var** (variabel pertama atau variabel bawaan dijavascript)
  - **let** (variabel yang ada dibuat di ES6, let sendiri ditujukan untuk menggantikan var)
  - **const** (variabel yang ada dibuat di ES6, const digunakan untuk menampung variabel konstanta/ bernilai tetap)

<!-- Peserta mampu memahami dan membedakan berbagai tipe data -->

#### Tipe Data

- **tipe data** didalam javascript ada tipe data primitif dan non-primitif

  - **primitif**
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

-**Non-Primitf** adalah tipe data yang didefinisikan sendiri oleh programer dan bisanya lebih dari satu nilai.

- contoh **Array** dan **Object**

  ```
    const hewanReptile = ['ular','buaya','kadal'];
    const mahasiswa = {
      nama: 'Rio Aldi E',
      umur: 21,
      Nim: '2013020017'
    }

  ```

#### Operator

- **Operator** adalah intruksi yang digunakan untuk melakukan suatu proses.
- operator didalam javascript

  - **operator Aritmatika** merupakan operator untuk melakukan operasi aritmatika.

    - penjumlahan ( + )
    - pengurangan ( - )
    - perkalian ( \* )
    - pangkat ( \*\* )
    - pembagian ( / )
    - modulus ( % )

  - **operator Penuagasan** merupakan operator yang digunakan untuk memberikan tugas kepada variabel
    - ( = ) memberikan sebuah nilai
    - ( += ) penambahan dan pengisian
    - ( -= ) pengurangan dan pengisian
    - ( \*= ) perkalian dan pengisian
    - ( \*\* ) pemangkatan dan pengisian
    - ( /= ) pembagian dan pengisian
    - ( %= ) modulus dan pengisian
  - **operator perbandingan** merupakan operator yang digunakan untuk membandingkan dua nilai, operator ini akan menghasilkan boolean.
    - ( > ) lebih besar
    - ( < ) lebih kecil
    - ( == ) sama dengan
    - ( != ) tidak sama dengan
    - ( >= ) lebih besar sama dengan
    - ( <= ) lebih kecil sama dengan
  - **operator logika** digunakan untuk melakukan operasi terhadap dua nilai boolean.
    - ( && ) dan atau AND
    - ( || ) OR
    - ( ! ) Negasi

<!-- Peserta mampu memahami dan membedakan control flow (conditional dan looping) -->

### Control FLow

- #### **Control flow** sebuah instruksi untuk mengatur alur dari algoritma dan program
- **If Else** adalah control flow percabangan yang digunakan untuk kondisi yang diinginkan dengan proses seleksi
- if else sering digunakan untuk control flow yang hanya memiliki sedikit kondisi

```
   let umur = 40;
        if(umur <= 6){
            console.log('Balita')
        }else if(umur <= 11){
            console.log('Anak-anak')
        }else if(umur <= 16){
            console.log('remaja')
        }else if(umur <= 22){
            console.log('pemuda/pemudi')
        }else if(umur <= 40){
            console.log('dewasa')
        }else{
            console.log('tua')
        }
    //output dewasa

```

- **Switch Case** adalah suatu bentuk kondisi percabangan bernilai true, maka blok kode akan dijalankan.
- switch case sering digunakan untuk percabangan yang memiliki banyak kondisi.

```
  let hari = 1;

switch (hari) {
    case 1 :
        console.log('Senin')
        break;
    case 2 :
        console.log('Selasa')
        break;
    case 3 :
        console.log('Rabu')
        break;
    case 4 :
        console.log('Kamis')
        break;

    default:
        console.log('libur')
        break;
}

```

### LOOPING

- #### **Looping** adalah sebuah pelurangan didalam bahasa pemrograman
- Loping di javascript dapat menggunakan for,while dan do while

- **while** adalah perulangan yang jumlah perulangannya belum diketahui

```
  while( angka < 10){
    console.log(angka)
    angka++;
  }

```

- **do while** mengulang statement sebanyak satu kali terlebih dahulu, kemudian akan mengecek statement didalam while apakah bernilai benar, jika bernilai benar maka akan diulang kembali.

```
  do{
    console.log(angka);
    angka++;
  }while(angka <10)

```

- **for** adalah perulangan yang sudah diketahui jumlahnya
- for harus memiliki
  -initial
  -condition
  -increment

```
  for(i=0; i<=10; i++){
    console.log(i)
  }

```
