# Writing Week 7

## React Context

### Context

- **Context** berfungsi untuk mengirimkan data antar component, tanpa harus menggunakan Props secara manual.

- context merupakan fitur bawaan react di react v16 keatas, jadi kita tidak perlu melakukan penginstallan

### membuat context

- untuk membuat context kita dapat menggunakan createContext() dan kita harus menambahkan default value didalamnya.

  ```
        const initialState = {
            theme: 'dark
        }
      export const themeCtx = React.createContext(initialState);
        //initialState disini sebagai default value

  ```

### context provider

- Setiap objek Context dilengkapi dengan komponen Provider React yang memungkinkan komponen konsumsi untuk menerima perubahan context.

- Provider biasanya digunakan di root element atau parent component.

- Provider didalam context memiliki value yang dapat menampung state dan function, value inilah yang akan kita gunakan saat menggunakan content di component.

  ```
      const [theme, setTheme] = React.useState(initialState.theme);

      <themeCtx.Provider value={[theme, setTheme]}>
          {children}
      </themeCtx.Provider>

  ```

### menggunakan Context

- untuk menggunakan context ada dua cara yaitu
  - Context.Consumer
  - React.useContext()

#### Context.Consumer

- context consumer adalah cara lama kita dalam menggunakan react context sebelum adanya Hooks

  ```
  <MyContext.Consumer>
      {value}
  </MyContext.Consumer>

  ```

#### React.useContext()

- useContext() adalah cara menggunakan context yang paling direkomendasikan saat ini, useContext juga masih masuk kedalam react Hooks.

  ```
      const { theme, setTheme } = React.useContext(themeCtx);

  ```

## React Testing

### Unit Test

- Unit testing adalah sebuah pekerjaan dimana kita melakukan pengujian pada suatu bagian pada aplikasi yang kita buat.

- Tujuan dari unit testing sendiri yaitu untuk melakukan validasi setiap unit pada kode aplikasi agar berfungsi seperti yang diharapkan.

### Jest

- Jest adalah salah satu Library populer React yang digunakan untuk melakukan testing pada aplikasi react.

- untuk menginstall jest pada aplikasi react, kita dapat menggunakan
  `npm install --save-dev jest`
  command diatas akan menyimpan jest didalam developing saja.

#### test sederhana

- contoh test sederhana menggunakan Jest

  ```
      test('two plus two is four', () => {
      expect(2 + 2).toBe(4);
      });

  ```

  - expect berisi expetasi yang akan dilakukan
  - toBe berarti hasil yang diharapkan/dihasilkan

#### Truthiness

- truthtiness adalah method jest yang dapat kita gunakan untuk mengecek nilai value ataupun tipe data.

- contoh beberapa truthiness
  - toBeNull mengecek hasil harus null
  - toBeUndefined mengecek hasil harus undefined
  - toBeDefined lawan dari toBeUndefined
  - toBeTruthy mengecek if dimana apakah menhasilkan true
  - toBeFalsy mengecek if dimana apakah menhasilkan false

#### Asyn/Await

- didalam Jest kita dapat menggunakan Asyn/Await, biasanya Aysn/Await testing digunakan untuk mengetest fetching data dari API.
