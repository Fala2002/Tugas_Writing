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
  
