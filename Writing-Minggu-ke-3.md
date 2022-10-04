# **Writing Minggu ke-3**

## **Javascript Intermediate**

### **Array dan Multidimensional Array**
- **Array** adalah sebuah tipe data non-primitif yang mampu menyimpan banyak data serta mampu menyimpan berbagai macam tipe data. Cara menggunakan array adalah dengan menggunakan kurung kotak, seperti let arr []. Contoh dari array sebagai berikut :
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
