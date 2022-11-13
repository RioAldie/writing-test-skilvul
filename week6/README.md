# Writing Week 6

## React Lanjutan

### PropTypes

#### overview

- Proptypes merupakan library untuk menvalidasi props. Ini sangat membantu dalam meminimalkan bugs saat mengembangkan App besar. Jika props tidak benar type nya maka akan muncul warning.
- Pada versi terbaru React kita dapat langsung menggunakan proptypes tanpa menginstallnya terlebih dahulu, karena sudah include didalam react kita.

#### cara penggunaan

- cara penggunaan proptypes adalah
  - pertama kita import dulu PropTypes
  ```
      import PropTypes from 'prop-types'
  ```
  - setelah itu kita tulis syntax proptypes dibawah component kita,
  ```
  HelloWorldComponent.propTypes = {
      name: PropTypes.string
  }
  //HelloWorldComponent adalah nama component
  //name adalah props
  //string adalah tipe data
  ```

#### isRequired

- propsTypes dengan isRequired adalah props yang harus memiliki isi didalamnya
  - contoh
  ```
  HelloWorldComponent.propTypes = {
      name: PropTypes.string.isRequired
  }
  //kita tinggal menambahkan isRequired dibelakang tipe data
  ```

#### default props

- propstypes dengan default value adalah props yang jika dikirimkan kosong akan tetap berjalan karena memiliki nilai awal atau default
  - contoh
  ```
  HelloWorldComponent.defaultProps = {
      name: 'rio'
  };
  ```

## React Router

### react-router-dom

#### overview

- **react-router-dom** adalah sebuah third party library untuk melakukan routing didalam react.

#### cara menginstal

- untuk menggunakan react-router-dom kita perlu menginstalkan terlebih dulu didalam project react kita
  ```
      npm install react-router-dom
  ```

#### component penting react-router-dom

- berikut beberapa komponen react-router-dom v6 yang sering digunakan
  - BrowserRouter
  - Routes
  - Router
  - Link
  - Navigate

#### cara penggunaan

- cara menggunakan react-router-dom

  1. import semua component yang akan dibutuhkan dari react-router-dom, didalam root component kita(saya biasanya mengimport di dalam app.js)

  ```
  import {
      BrowserRouter,
      Routes,
      Route
       }
  from "react-router-dom";

  ```

  2. bungkus element children kita menggunakan BrowserRouter

  ```
  return(
      <BrowserRouter>
          ....
      </BrowserRouter>
  )

  ```

  3. bungkus semua element yang akan di route menggunakan Routes

  ```
  return(
      <BrowserRouter>
         <Routes>
          ...
         </Routes>
      </BrowserRouter>
  )

  ```

  4. menggunakan route untuk semua halaman dan masukan didalam Routes, path sebagai alamat atau path halaman dan element berisi component halaman tersebut.

  ```
  return(
      <BrowserRouter>
         <Routes>
           <Route path="/" element={<Home />}>
           <Route path="/dashboard" element={<Dasboard />}>
         </Routes>
      </BrowserRouter>
  )

  ```

5. sedangkan untuk berpindah halaman, didalam react-router-dom kita dapat menggunakan Link sebagai pengganti tag a html.

```
  import {Link} from 'react-router-dom';

  function Navbar(){
      return(
          <nav>
              <Link to="/">Home</Link>
              <Link to="/dasboard">Dashboard</Link>
          </nav>
      )
  }

```

#### Dynamic Route

- **Dynamic Route** adalah route yang bersifat flexsibel dimana nama pathnya bisa berubah, biasanya berupa id dan digunakan untuk menampilkan detail suatu item
- contoh dynamic route

  ```

  return(
    <BrowserRouter>
       <Routes>
         <Route path="/" element={<Home />}>
         <Route path="/dashboard" element={<Dasboard />}>
         <Route path="/item/:id" element={<Item />}>
       </Routes>
    </BrowserRouter>
  )

  ```

  ```
    import {Link} from 'react-router-dom';

    function ItemList(){
        return(
            <Link to="/item/7586kj2h21919">Detail</Link>
        )
    }

  ```

## State Management

- State management adalah sebuah cara untuk mengatur data / state kita bekerja, bisa juga untuk memisahkan antara logic dan view, dimana logic tersebut juga bisa reusable.

- beberapa state management yang sering digunakan di react
  - redux
  - context
  - zustand
  - recoil
  - react-query

## Redux

- **Redux** adalah sebuah library state management
  ```
      npm i redux
  ```

### React Redux

- **raect-redux** adalah sebuah third party yang digunakan untuk memanipulasi state didalam react.

- untuk menginstall react-redux kita dapat menggunakan command npm i react-redux, akan tetapi sebelum itu kita perlu menginstall redux terlebih dahulu
  ```
      npm i react-redux
  ```

#### store

- store menampung semua state dan action didalam aplikasi kita dimana biasanya state dan action tersebut disimpan dalam reducer, didalam redux sendiri kita hanya dapat menggunakan satu store.

  ```
  //membuat store
  const store = createStore(reducer);

  //memanggil / menggunakan store
  <Provider store={store}>
  </Provider>

  ```

#### provider

- provider adalah component tempat store dipanggi.

#### reducer

- reducer adalah bagian redux yang merubah state menjadi respon yang terjadi ketika Action di dispatch().

- untuk membuat reducer kita dapat menggunakan createReducer()

#### initial state

- initial state adalah value awal dari state kita, initial state biasanya berbentuk objek

#### dispacth

- dispatch adalah sebuah fungsi didalam redux
- untuk menggunakan dispatch kita dapat menggunakan useDispatch()

#### useSelector()

- useSelector berfungsi untuk memanggil state didalam redux dan menggunakannya di component kita.

### Redux-thunk

- Redux Thunk adalah middleware yang memungkinkan Anda memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi. Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.

- menginstall redux thunk
  ```
      npm i redux-thunk
  ```
- contoh async await didalam redux-thunk
  ```
  export const fetchTodoById = todoId => async dispatch => {
  const response = await client.get(`/fakeApi/todo/${todoId}`)
  dispatch(todosLoaded(response.todos))
  }

  ```
