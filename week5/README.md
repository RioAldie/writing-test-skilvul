# Writing Week 5

## React Dasar

### React js

- Reactjs adalah sebuah Library javascript yang dapat digunakan untuk membantu pembuatan website disisi frontend, React Js dibuat dan dikembangkan oleh Facebook(sekarang menjadi META).
- React Berbasis Virtual DOM dan setiap element yang dibuat dengan react disebut React Component.
- React memiliki format '.jsx' untuk javascript dan '.tsx' untuk typescript.

### Instalisasi React

- ada berbagai cara untuk menggunakan React didalam project kita, dan yang paling mudah adalah dengan menggunakan template yang telah dicustom oleh react yaitu create-react-app atau CRA.
- berikut langkah menginstall react js dengan CRA - pastikan telah menginstall Nodejs - buka terminal dan pilih root folder - ketik npx create-react-app my-app (my-app sebagai nama folder) - tunggu sampai proses install selesai - setelah itu buka folder react di vscode dan kita bisa melihat susunan file react.

### React Component

- didalam sebuah react kita dapat membuat sebuah component seperti element html dengan menggunakan function
- react component memiliki beberapa kelebihan diantarnya - reusable / dapat digunakan berkali-kali - readable / lebih mudah dibaca - panjang kode menjadi lebih pendek dan rapih sehingga memudahkan proses debugging.
- contoh cara membuat react component

  ```
      export deafult const Card = () =>{
          return(
              <div>
                  <h1>Ini adalah sebuah card component</h1>
              </div>
          )
      }

  ```

  note: nama component harus diawali huruf kapital

- cara menggunakan react component hampir sama dengan cara menggunakan element html, hanya kita perlu melakukan import terlebih dahulu

  ```
      import Card from 'component/card';

      export default const Home = () =>{
          return(
              <>
                  <Card/>
              </>
          )
      }

  ```

### Class Component dan Functional Component

- React Component memiliki dua jenis yaitu class dan funtional
- **Class Component** adalah react component yang penulisannya menggunakan syntax ES6 class dan didalam class component kita dapat menggunakan state dan props, class component merupakan versi awal dari react component dan sekarang sudah jarang digunakan.
- **Function Component** adalah react component yang penulisannya menggunakan format function, pada awalnya kita hanya dapat menggunakan props didalam functional component akan tetapi setelah adanya hooks kita dapat menggunakan props dan state, functional component merupakan react component yang paling dianjurkan untuk digunakan sekarang ini.

### Props and State

- **Props** adalah Data yang dikirimkan oleh parent kedalam child.

  ```
      // home.js sebagai parent
      import Card from 'component/card';

      export default const Home = () =>{
          return(
              <>
                  <Card title="card HOME"/>
              </>
          )
      }
  ```

  pada kode diatas, saya mengirimkan props title kedalam Card

  ```
      // card.jsx
      export deafult const Card = ({title}) =>{
          return(
              <div>
                  <h1>Ini adalah sebuah {title}</h1>
              </div>
          )
      }


  ```

  pada code diatas card adalah sebuah child dan menerima sebuah props title.

- **State** adalah sebuah variabel/data yang dikelola dikomponen itu sendiri, pada versi awal react state harus merupakan sebuah object sedangkan setelah setelah adanya hooks kita dapat membuat state lebih mudah dengan useState.
- contoh state dengan hooks

  ```
      const [ nama, setNama ] = useState('');

  ```

### React Lifecycle

- Lifecycle didalam react memiliki tiga alur utama

- **Mounting** adalah sebuah siklus pertama ketika aplikasi dibuka.
- **Update** adalah sebuah siklus ketika terjadi perubahan data.
- **Unmount** adalah siklus setelah komponen dibuka.

- sebelum versi 16 atau adanya Hooks untuk memanipulasi Lifesycle didalam React harus menggunakan
  - componentDidMount();
  - componentWillUpdate();
  - componentWillUnMount();
- sedangkan untuk versi 16/ setelah Hooks sampai sekarang kita dapat menggunakan useEffect() untuk menghandle Lifecycle didalam React.

## React Lanjutan

### React Hooks

- **React Hooks** adalah Fitur yang memungkinkan untuk menggunakan state dan fitur React lainnya tanpa menuliskan sebuah kelas. Hooks menggunakan konsep Functional Component.

- untuk menggunakan Hooks harus menggunakan React versi 16.8 atau diatasnya

- ada beberapa Hooks yang disediakan oleh react, berikut hooks yang paling populer dan sering digunakan
  - **useState()** adalah hook yang digunakan untuk membuat dan memanipulasi sebuah state.
  - **useEffect()** adalah hook yang digunakan untuk menghandle lifecycle.
  - **useRef()** adalah hook untuk memanipulasi elemen DOM.
  - **useContext** adalah hook untuk memanipulasi sebuah Context API.
  - dll
- cara menggunakan hooks kita harus mengimport terlebih dahulu dari react

  ```
      import {useState} from 'react';

      export default const Home = () =>{
          const [name, setName] = useState('Rio')

        return(
            <>
                <p> nama saya  {}</p>
            </>
        )
    }

    //output: nama saya Rio

  ```
