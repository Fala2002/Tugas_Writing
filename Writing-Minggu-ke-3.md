# **Writing Minggu ke-3**

## **Javascript Intermediate**

### **Array dan Multidimensional Array**
- **Array** adalah sebuah tipe data non-primitif yang mampu menyimpan banyak data serta mampu menyimpan berbagai macam tipe data. Cara menggunakan array adalah dengan menggunakan kurung kotak, seperti let arr [ ]. Contoh dari array sebagai berikut :
```
let arr = ["Hallo", 1, true];
Atau bisa juga

let bunga = ['Melati',  'Tulip', 'Anggrek'];
console.log(bunga);
```
- Cara mengakses array, Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0. Contoh syntax :
```
let buku = ["Buku Cerita", "Buku Pelajaran", "Buku Dongeng"];
console.log(buku);

Output :
Array(3)
0 : "Buku Cerita"
1 : "Buku Pelajaran"
2 : "Buku Dongeng"

Array sepanjang 3 serta terdapat 2 index dalam array.
```
- **Update Array** , cara mengupdate array yaitu :
```
let buku = ["Buku Cerita", "Buku Pelajaran", "Buku Dongeng"];

buku[0] = "Buku Sejarah";
console.log(buku);

Output : ["Buku Sejarah", "Buku Pelajaran", "Buku Dongeng"]
```
- **Const in array**, Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain. tetapi const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable). Contoh syntax :
```
const warna = ['Merah', 'Putih', 'Biru'];
warna[1] = ['Kuning'];
 
console.log(warna);
Output : ['Merah', 'Kuning', 'Biru'];
```
- **Array Properti**, Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.Array properti terdiri dari :
  - **.length**, length akan mengembalikan nilai dari jumlah panjang data suatu array. Contoh syntax :
    ```
    let arr = ["Hallo", 1, true]
    console.log(arr.length);
    
    Output : 3
    ```
  - **.constructor**, constructor mengembalikan referensi ke fungsi array yang membuat objek.
  - **.prototype**, prototype mewarisi definisi array dengan menambah properti dan metode.
  - **.index**, mewakili indeks kecocokan berbasis nol dalam string.
  - **.input**, properti ini hanya ada dalam array yang dibuat oleh kecocokan ekspresi reguler.
- **Array Methods**, Array memiliki method atau biasa disebut built-in methods. Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
 - **.push()** adalah method yang digunakan untuk menambah data diakhir. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   console.log(arrBuah);
   
   arrBuah.push("Duku")
   console.log(arrBuah); //Output : "Jeruk", "Pepaya", "Rambutan", "Duku"
   ```
 - **.unshift()** adalah method yang digunakan untuk menambahkan data didepan. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.unshift("Mangga")
   console.log(arrBuah); //Output : "Mangga", "Jeruk", "Pepaya", "Rambutan"
   ```
 - **.pop()** adalah method yang digunakan untuk menghapus elemen terakhir. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.pop()
   console.log(arrBuah); //Output : "Jeruk", "Pepaya"
   ```
 - **.shift()** adalah method yang digunakan untuk menghapus elemen depan. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan"
   ];
   arrBuah.shift()
   console.log(arrBuah); //Output : "Pepaya", "Rambutan"
   ```
 - **.splice()** adalah method yang digunakan untuk menghapus ditengah. Dalam slice terdapat start atau awal/index, deletecount atau banyak data yang didelete, dan item atau data yang disisipkan. Contoh syntax :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan",
   "Anggur",
   "Semangka"
   ];
   arrBuah.splice(2) 
   console.log(arraBuah); //Output : "Jeruk", "Pepaya"
   
   arrBuah.splice(2, 1)
   console.log(arrBuah); //Output : "Jeruk", "Rambutan", "Anggur", "Semangka"
  
   arrBuah.splice(2, 1, "Buah Naga")
   console .log(arrBuah); //Output : "Jeruk", "Buah Naga", "Rambutan", "Anggur", "Semangka"
   ```
 - **.slice()** digunakan untuk mengembalikan shallow to copy (copy data) atau mengambil data dengan cara copy data. Contoh script :
   ```
   let arrBuah = [
   "Jeruk",
   "Pepaya",
   "Rambutan",
   "Anggur",
   "Semangka"
   ];
   let slice = arrBuah.slice(2, 4)
   console.log(slice); //Output: "Pepaya", "Anggur"
   
   let slice = arrBuah.slice(2)
   console.log(slice); //Output : "Rambutan", "Anggur", "Semangka"
   ```
- **Looping Array**, Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach(). Contoh script looping :
   ```
   let arrBuah = ["Anggur", "Jeruk", "Semangka", "Pepaya", "Rambutan", "Duku"];
   for(let i = 0; i<arrBuah.length; i++){
   console.log(arrBuah[i])
   };
   //Output : 
   Anggur
   Jeruk
   Semangka
   Pepaya
   Rambutan
   Duku
  
   Atau bisa juga
   for(let i = arrBuah.lengthh-1; i>0; i--){
   console.log(arrBuah[i])
   };
   //Output :
   Duku
   Rambutan
   Pepaya
   Semangka
   Jeruk
   Anggur
   ```
 - **.forEach()** adalah method untuk melakukan looping pada setiap elemen array. ForEach ini tanpa menggunakan return.Contoh script :
   ```
   arrBuah.forEach((item) => {
    console.log(item)
   });
   //Output :
   Anggur
   Jeruk
   Semangka
   Pepaya
   Rambutan
   Duku
  
   Contoh lain
   arrBuah.forEach((index,item) =>{
   if(index %2 == 1){
    console.log(index,item)
   }
   });
   //Output :
   1. Jeruk
   3. Pepaya
   5. Duku
   Script diatas digunakan untuk menampilkan index array ganjil.
   ```
 - **.map()** melakukan perulangan/looping dengan membuat array baru.Contoh script :
   ```
   let buah segar = arrBuah.map((item) =>{
   return item + " " + "segar"
   });
   //Output :
   0 : Anggur segar
   1 : Jeruk segar
   2 : Semangka
   3 : Pepaya
   4 : Rambutan
   5 : Duku
   ```
- **Array Multidimensional** Multidimensional Array bisa dianalogikan dengan array of array. Ada array didalam array. Contoh script :
   ```
   let arrMulti = [
   ["nama", "alpha"],
   ["umur", 17],
   ["kelas",  "JS"],
   ]
   console.log(arrMulti[0][1];
   //Output : "alpha"
   
   Atau bisa juga
   arrMulti[2][1] = "CSS"
   console.log(arrrMulti);
   Script diatas berarti teks JS dirubah menjadi CSS
   ```

### **Javascript Object**
- **Object** adalah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object.
- **Membuat sebuah object** Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel. Contoh script :
   ```
   let siswa = {
    nama : 'terra',
    umur : 17,
    hobi : 'memancing', 
    "nomor handphone" : 08256814086
    }
    console.log(siswa);
    ```
- **Cara akses object** Dalam mengakses object terdapat 2 cara yaitu menggunakan dot notation dan bracket. Selain itu, bisanya dalam mengakses object yaitu menggunakan console.log(object).
  - dot notation, misalnya ``console.log(siswa.nama);`` maka output yang dihasilkan yaitu terra
  - bracket, misalnya ``console.log(siswa['nama']);`` 
- **Memanggil nama object dengan variable** contohnya :
    ```
    let properti = "umur"
    console.log(siswa[properti]);
    ```
- **Menambahkan properti baru ke dalam object** Contoh script:
    ```
    Cara 1
    let buku = {
     Judul : "Mantan jadi manten",
     Penulis : "Hayati",
     "Jumlah halaman" : 250,
     };
     buku.tahun : 2022;
     buku.terjual : 3000;
     console.log(bukuu);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     
     Cara 2
     buku["penerbit"] : "gramedia";
     console.log(buku);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     penerbit : gramedia
     ```
- **Ganti properti lama** contoh script : 
     ```
     Cara 1
     let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     hewan.nama : 'kelinci',
     hewan.warna : 'hitam',
     console.log(hewan);
     //Output 
     nama : kelinci
     kaki : 4
     warna : hitam
     
     Cara 2
     hewan["kaki"]=2;
     console.log(hewan)
     nama : kelinci
     kaki : 2
     warna : hitam
     ```
- **Delete Properti** contoh script :
     ```
      let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     delete.hewan.warna;
     delete.hewan.kaki;
     console.log(hewan);
     //Output : nama : kucing
     ```
- **Method** adalah ketika ingin menambahkan sebuah function. Ada 2 method dalam object, yaitu :
  - **const greeting** contoh script :
    ```
    const greeting = {
     welcome : function(){
      return "halo selamat datang";
    };
     afterpay:function(){
     return "terimakasih sudah membeli produk kami";
     }
    };
    console.log(greeting.welcome()); //Output : halo selamat datang
    ```
  - **nested object** contoh script :
    ```
    let buku = {
     Judul : "Tips jago Javascript",
     Tahun : 2022;
     Penulis {
        Penulis1 : {
           Nama : "Reyhan",
           Umur : 28,
           Kota : "Jakarta"
           }
        Penulis2 : {
           Nama : "Fala",
           Umur : 25,
           Kota : "Madiun"
           }
        Penulis3 : {
           Nama : "Diana",
           Umur : 20,
           Kota : "Bandung"
           }
         }
    };
     console.log(buku.penulis.penulis1.nama);//Output : Reyhan
    ```
- **Built In Method (Object menjadi array** 
     ```
     let siswa = {
       nama : "Fala",
       umur : 20,
       hobi : "Berenang",
     };
     console.log(object.keys.(siswa)); //Output : 'nama', 'umur', 'hobi'
     console.log(object.values.(siswa)); //Output : 'Fala', '20', 'Berenang'
     ```
- **Looping Object** Looping sendiri berarti perulangan. Contoh scriptnya :
    ```
    let siswa = {
     nama : "Reyhan",
     umur : 22,
     kota : "Jakarta",
    };
    for(let key in siswa){
      console.log(siswa[key]); 
    //Output :
    Reyhan
    22
    Jakarta
    ```
- **Array of Object** adalah array yang menyimpan banyak object sebagai nilainya. Contoh script :
    ```
    let users = {
      {
       Nama : "Reyhan",
       Umur : 28,
       Kota : "Jakarta",
      },
      {
       Nama : "Fala",
       Umur : 20,
       Kota : "Bandung",
      },
      {
       Nama : "Diana",
       Umur : 24,
       Kota : "Madiun",
      },
    };
    console.log(user);
    
    Dengan menggunakan Map, maka
    let data = users.map((el) => {
     console.log(el.nama);
    });
    //Output :
    Reyhan
    Fala
    Diana
    ```
### **Rekrusif dan Modules**
- **Rekrusif** adalah function atau algoritma yang memanggil dirinya sendiri sampai kondisi tertentu. Rekrusif ini mirip seperti looping. Misalnya pada gambar ada gambar di dalam gambar. Terdapat 2 kunci pada rekrusif,yaitu base case atau titik berhenti dan recrusion case atau titik memanggil function. Contoh script :
  ```
  Menampilkan bilangan 1 2 3 4 5
  
  function deretAngka(n){
   if (n == 1) {
     console.log(n)
   } else {
     deretAngka(n-1)
     console.log(n);
    }
  }
  deretAngka(3)
  
  Atau contoh lain :
  Mencari angka faktorial
  Misalnya 5!
  Solusinya jika dijabarkan 5 x 4 x 3 x 2 x 1

  function faktorial(n) {
    if (n == 1) {
      return 1
    } else {
      return n * faktorial(n - 1)
    }
  }
  console.log(faktorial(3))
  //Output = 6
  ```
- **Modules** adalah cara untuk memisahkan kode ke file yang berbeda. Keuntungan dari modules yaitu mudah untuk mengelola kode serta kode tidak menumpuk di dalam satu file. Terdapat 2 kata kunci pada modules yaitu export dan import. Contoh script :
  ```
  // File Jepang.js
  export let motor = ["suzuki", "yamaha", "honda", "kawasaki"]
  
  let entertainment = ["anime", "manga", "wibu", "dorama"]
  export default entertainment
  
  export function sayHello() {
   console.log("hallooo")
  }
  
  import {apple} from './amerika.js';
   console.log(apple);
  
  // File Indonesia.js
  import {motor} from "./Jepang.js"
   console.log(motor);
   
  import Entertainment, { motor as motorJepang, sayHello  } from "./jepang.js"
  console.log(Entertainment);
  
  // File Amerika.js
  let apple = ["iphone", "macbook", "imac"]
    export {apple}
  
  Berdasarkan script diatas,
  - Indonesia hanya bisa import, karena dia file utama.
  - Jepang bisa melakukan import dan export.
  - Amerika hanya melakukan export.
  ```
- Hal hal yang harus dilakukan saat membuat modules adalah menambahkan type="module" pada script utama, lalu siapkan script ke-2 dan sebagainya untuk melakukan export, serta lakukan import pada file atau script utama.

### **Asynchronous**
