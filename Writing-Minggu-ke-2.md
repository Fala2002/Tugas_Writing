# **Writing Minggu ke-2**

## **Javascript Scope dan Function**

### **Javascript Scope**
- **Scope** adalah Scope adalah konsep dalam flow data variabel. 
- **Blocks** adalah code yang berada didalam curly braces {}.
- **Global scope** adalah variabel yang dibuat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks. Contoh script :
  ```
  let myName = 'Fala';
  
  function greeting() {
    return myName;
  }
  console.log(myName);
  ```
- **Local scope** adalah mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. tidak bisa diakses diluar blocks. Contoh script :
  ```
  function greeting(){
      let MyName = 'Almaas'
      return myName
  }
  
  console.log(greeting())
  greeting(myName)
  ```
  
### **Javascript Function**
- **Function** adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Contoh script :
  ```
  function greeting() {
      return 'Hello world!';
  };
  
  Penjelasan script
  - function adalah function keyword.
  - greeting adalah identifier.
  - { return 'Hello World!' } adalah function body
  ```
- Perbedaan console.log() dan return adalah console.log() hanya menampilkan informasi ke dalam tab console JavaScript, sedangkan return akan mengembalikan sebuah nilai ke tempat di mana fungsi itu dipanggil.
- **Cara memanggil function**
  ```
  greeting()
  console.log(greeting());
  
  Dalam hal ini fungsi greeting() return valuenya adalah 'Hello world!'. Nilai dari return ini akan dikembalikan ke tempat pemanggilan fungsi tersebut, sehingga kode di atas saat dijalankan sebenarnya akan menjadi console.log('Hello world!)
  ```
- **Parameter Function** dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas. Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function pengurangan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.  Contoh script :
  ```
  function pengurangan(a, b) {
      return a - b;
  }
  ```
- **Argumen Function** adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya, jadi jika di function pengurangan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen. Contoh script :
  ```
  function pengurangan(a, b) {
      return a - b;
  }
  console.log(pengurangan(10, 5)) //output: 5
- **Default Parameter** digunakan untuk memberikan nilai awal atau default pada parameter function. Default parameters bisa digunakan jika ingin menjaga function agar tidak error saat dipanggil tanpa argumen. Contoh script :
  ```
  function salam(nama = 'orang'){
        return 'Haii' + nama
    }
    
    console.log(salam('Diana'))
    console.log(salam())
    ```
- **Function Helper** Kita bisa menggunakan function yang sudah dibuat pada function lain. Contoh script :
    ```
    function multiplyByNineFifths(number) {
      return number * (9/5);
    };
    function getFahrenheit(celcius) {
      return multiplyByNineFifths(celcius) + 32;
    };
    getFahrenheit(15); //returns 59
    ```
- **Arrow Function** adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version). Contoh script :
    ```
    const greeting = () => {
      return 'Hello wordl!';
    };
    
    const pengurangan = (a, b) => {
      return a - b;
    };
    ```
- **Short Syntax Function**
  - Zero Parameter
    ```
    const functionName = () => {};
    ```
  - One Parameter
    ```
    const functionName = paramOne => {};
    ```
  - Two or More Parameter 
    ```
    const functionName = (paramOne, paramTwo) => {};
    ```
  - Single-line block 
    ```
    const sumNumbers = number => number + number; 
    ```
  - Multi-line block 
    ```
    const sumNumbers = number => {
      const sum = number + number ;
      return sum;
    };
    ```
### **Eror dan Debbuging**
- Error objek dilempar ketika kesalahan runtime terjadi. Objek Errorjuga dapat digunakan sebagai objek dasar untuk pengecualian yang ditentukan pengguna. Kesalahan runtime menghasilkan Errorobjek baru yang dibuat dan dibuang.
- Tipe-tipe pada eror antara lain :
  - **EvalError**, yaitu membuat instance yang mewakili kesalahan yang terjadi terkait fungsi global eval().
  - **RangeError**,yaitu membuat instance yang mewakili kesalahan yang terjadi saat variabel numerik atau parameter berada di luar rentang validnya.
  - **ReferenceError**,yaitu membuat instance yang mewakili kesalahan yang terjadi saat mereferensikan referensi yang tidak valid.
  - **SyntaxError**, yaitu membuat instance yang mewakili kesalahan sintaks.
  - **TypeError**, membuat instance yang mewakili kesalahan yang terjadi saat variabel atau parameter bukan tipe yang valid.
  - **URIError**, membuat instance yang mewakili kesalahan yang terjadi saat encodeURI()atau decodeURI()melewati parameter yang tidak valid.
  - **AggregateError**, membuat instance yang mewakili beberapa kesalahan yang dibungkus dalam satu kesalahan ketika beberapa kesalahan perlu dilaporkan oleh suatu operasi, misalnya oleh Promise.any().
  - **InternalError**, membuat instance yang mewakili kesalahan yang terjadi saat kesalahan internal di mesin JavaScript dilemparkan. Misalnya "terlalu banyak rekursi".
  - **Constructor**, yaitu membuat error objek baru.
  - **Metode Statis** terdiri dari Error.captureStackTrace(), Error.stackTraceLimit, Error.prepareStackTrace()
  - **Instance Properties** terdiri dari Error.prototype.message, Error.prototype.name, Error.prototype.cause
- Debugging pada Javascript yang paling umum adalah dengan console.log() variabel yang ingin diperiksa. Terdapat 2 cara dalam debugging, yaitu :
  - Menggunakan alat pengembang chrome, buka halaman dengan kode JS (tekan cmd+o di macOS atau Ctrl+o di Windows) dan pilih file untuk di-debug, klik baris yang ingin didebug dan segarkan kembali halaman (F5).
  - Call Stack, jalur yang telah diambil program untuk mencapai titik saat menetapkan titik putus atau mengalami kesalahan. Contoh script :
    ```
    (function testing(){
        var obj = {
        add
    }
    function add(a, b) {
        var result = a + b
        return result.split('')
    }
    var stringResult = obj.add("1", "2") // stringResult becomes "12"
    var numberResult = obj.add(1, 2) // numberResult is never set, an error is thrown
    })()
    
    Penjelasan :
    - testing dipanggil secara otomatis karena ini adalah IIFE (immediately Invoked Function Expression);
    - variabel obj dideklarasikan dengan function add (menggunakan ES6 shorthand untuk fungsi dalam objek, itu akan sama dengan memiliki var obj = { add: add };
    - function add dipanggil dari variabel obj dengan dua string memiliki parameter, ada yang ditambahkan yang menjadikannya "12" dalam skenario ini dan kemudian split dipanggil sebelum mengembalikan ["1", "2"];
    - function add dipanggil lagi, kali ini dengan angka, nilai ditambahkan sehingga menjadi 3 tetapi kemudian, split (yang tidak tersedia untuk variabel tipe angka ) dipanggil yang membuat error dilemparkan;
    ```
- Alat untuk menghindari runtime errors antara lain :
  - Quokka untuk mengevaluasi kode pada saat mengetik.
  - Eslint untuk memastikan panduan gaya konsisten dan itu akan membawa satu atau dua kesalahan di sepanjang mengoding.
  - Untuk yang ingin menjadikan JS pengalaman mengetik yang lebih kuat, maka dapat melihat hal-hal seperti TypeScript.

## **Data Type Built in Prototype & Method**

### **Tipe Data** 
#### **Data Primitive**
- **string** adalah deretan karakter yang diapit oleh sepasang tanda kutip (" "). Selain itu, berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks.
- Properties, terdiri dari :
  - Constructor,untuk mengembalikan fungsi yang dibuat string prototipe objek.
  - Length,untuk mengembalikan panjang string pada javascript. Contoh script :
    ```
     const str = 'jerapah';
     console.log(str.length); // Output: 7
    ```
  - Prototype, untuk menambah metode dan properti ke dalam sebuah objek. Contoh script : Berawal dari kata hallo menjadi ollah
    ```
     String.prototype.reverse = function(){ 
       let s = " "    
       for (let i = String(this).length-1; i >= 0; i-- { 
         s = s + String(this)[i]
      } 
      return s 
      }
      console.log("hallo".reverse()) //Output: 'ollah'
    ```
- Method, terdiri dari :
  - charAt(), mengembalikan karakter pada index yang spesifik (posisi).
    ```
     let hewan = 'Dinosaurus';
      console.log(hewan.charAt(4)); //Output : s
     ```
  - indexOf(), membalikan posisi kemunculan pertama yang ditemukan dari teks yang ditentukan dalam sebuah string.
     ```
      const str = 'saya sedang belajar javascript';
      console.log(str.indexOf('a')); // 1 :: s(a)ya ... 
      console.log(str.indexOf('ja')); // 16 :: ... bela(ja)r javascript
     ```
  - lastIndexOf(), membalikan posisi kemunculan terakhir yang ditemukan dari teks yang ditentukan dalam sebuah string.
     ```
      const str = 'saya sedang belajar javascript';
      console.log(str.lastIndexOf('a')); // 23 :: ... belajar jav(a)script
      console.log(str.lastIndexOf('ja')); // 20 :: ... belajar (ja)vascript
      console.log(str.lastIndexOf('ja', 19)); // 16 :: ... bela(ja)r javascript
     ```
  - replace(), mencari string untuk nilai dan kembalikan string baru dengan nilai yang diganti.
     ```
      const str = 'aku sedang belajar javascript';
      console.log(str.replace('aku', 'saya')); // saya sedang belajar javascript
     ```
  - slice(), mengekstrak bagian dari string dan kembalikan string baru. Syntaxnya : slice(indeksAwal, indeksAkhir);
     ```
      const str = 'saya sedang belajar javascript';
      console.log(str.slice(5, 11)); // sedang
      console.log(str.slice(5)); // sedang belajar javascript
     ```
  - split(), memisahkan string ke dalam array substring. Syntaxnya : split(separator, limit);
     ```
      const str = 'saya sedang belajar javascript';
      console.log(str.split()); // ["saya sedang belajar javascript"]
      console.log(str.split(' ')); // ["saya", "sedang", "belajar", "javascript"]
      console.log(str.split(' ', 2)); //  ["saya", "sedang"]
     ```
  - substring(), mengekstrak bagian dari string antara dua posisi yang ditentukan.
     ```
      const str = 'saya sedang belajar javascript';
      console.log(str.substring(1, 3)); // ay
      console.log(str.substring(5)); // sedang belajar javascript
     ```
  - toLowerCase(), mengubah string menjadi huruf kecil.
     ```
      const str = 'Skilvul';
      console.log(str.toLowerCase()); //Output: skilvul
     ```
  - toUpperCase(), mengubah string menjadi huruf besar.
     ```
      const str = 'skilvul';
      console.log(str.toUpperCase()); //Output: SKILVUL
     ```
  - trim(), menghapus spasi dari kedua ujung string.
     ```
      const str = '     skilvul      ';
      console.log(str.trim()); // 'skilvul'
     ```
  - includes(), mengembalikan nilai true or false apalah dalam variabel ada string tersebut.
     ```
      let hewan = "Dinosaurus"
      console.log(hewan.includes("saur"); // Output : true
     ```
- **number** adalah bilangan bulat, pecahan, dan lain-lain yang berbentuk angka.
   ```
   const a = 19;
   console.log(a); // 19
   console.log(typeof a); // number
   console.log(a instanceof Number); // false    
   ```
- Properties (jarang digunakan, kebanyakan menggunakan methods number).
- Methods, terdiri dari :
  - isNan() --> NaN (Not a Number), untuk mengecek apakah ini bukan angka. Mengembalikan nilai Boolean, true jika nilai yang diuji NaN(bukan angka), false jika angka
     ```
      isNan("hallo") //true
      isNan(12345) //false, karena ini angka
      isNan(true) //false, karena boolean true dianggap sebagai 1, dan 1 itu termasuk angka
      isNan("12345") //false, karena ada angka didalam string
     ```
  - toString(), untuk mengubah angka menjadi string.
     ```
      let angka = 25
      angka.toString() //Output: '25'
     ```
  - toFixed(), menentukan jumlah angka dibelakang tanda koma. Return nilainya berupa string.
     ```
      let pi = 3.14159265
      pi.toFixed() //Output: '3'
      pi.toFixed(1) //Output: '3.1'
      pi.toFixed(4) //Output: '3.1415'
     ```
  - parseInt() dan Number(), mengubah string menjadi number.
     ```
      myString = "27";
      console.log(parseInt(myString)); // Output: 27
      console.log(Number(myString)); //Output: 27
     ```
#### **Data Non-Primitive**
- Object.
  Contoh:
   ```
    let a = [10]
    let b = a
    console.log(a === b) // true
    a.push(10)
    console.log(a) // [10, 10]
    console.log(a === b) // true
   ```
- Array
- Function
### **Math**
Contoh :
```
Math.pi //Output: 3.1415
Math.LOG2E //Output: 1.4426
Math.sqrt2 //Output: 1.4426 {menghitung akar dua}
```
- Methods Math
  - Math.abs(), mengembalikan nilai negatif menjadi nilai positif.
     ```
     Math.abs(-15) //Output: 15    
     ```
   - Math.pow(), menghitung pangkat.
     ```
     Math.pow(2, 2) //Output: 4
     ```
   - Math.sqrt(), menghitung akar.
     ```
     Math.sqrt(25) //Output: 5
     ```
   - Math.round(), membulatkan angka.
     ```
     Math.round(123.456) //Output: 123
     ```
   - Math.floor(), membulatkan angka kebawah.
     ```
     Math.floor(4.4) //Output: 4
     Math.floor(4.9) //Output: 4
     ```
   - Math.ceil(), membulatkan angka keatas.
     ```
     Math.ceil(5.6) //Output: 6
     Math.ceil(5.1) //Output: 6
     ```
   - Math.random(), menampilkan angka acak.
   
## **Javascript Introduction DOM dan Traversing**
- **Document Object Model** adalah jembatan supaya bahasa pemrograman dapat berinteraksi dengan dokumen HTML. Dengan DOM, JS dapat memanipulasi HTML. DOM sendiri berbentuk tree structure. 
-	**Element vs node** 
- Element :
  - Hanya terdapat Html element.
  - ``<span>, <div>``
  - ``<h1>Hello<h1>``
  - ```
      <ul>
        <li>Satu</li>
        <li>Dua</li>
        <li>Tiga</li
      </ul>
    ```
- **Node** adalah setiap bagian terkecil di html yaitu text, comment, span.

-	**Traversing Element** 
- Mengkases DOM :
- Akses ke bawah 
  - getElementbyId yaitu mengambil elemen html menggunakan id. 
  - getElementsbyClassName yaitu mengambil elemen html berdasarkan nama class. Output berupa html collection karena class name bisa berupa jamak dan dapat digunakan lebih dari satu class. Cara mengaksesnya sama dengan array berupa indeks. Perlu diingat bahwa HTML Collection bukanlah array. Dan modelist juga bukan array. 
  - geteElementsbyTagName, sama seperti getElementsbyClassName, tetapi mencari berdasarkan tag html yang digunakan. 
  - Children yaitu mendapatkan elemen children dari parents.
  - querySelector yaitu mengambil elemen html setiap elemen html dengan tag berkelas.
- Akses ke atas  
  - parentElement yaitu mengambil parent element berdasarkan childnya.
  - closest(), digunakan untuk mengakses parents.
- Akses ke samping 
  - previousElementSibling yaitu akses elemen yang sejajar sebelum element tersebut.
  - nextElementSibling yaitu sama dengan previousElementSibling setelah elemen tersebut.

## **Javascript DOM**

### **DOM Manipulation**
- Terdapat beberapa hal yang dapat kita lakukan untuk memanipulasi element HTML DOM dengan sintaks Javascript, antara lain :
- **Mencari Element HTML** , misalnya terdapat script seperti dibawah ini :
  ```
  <body>
    <div id="header"
      <p>
        <span>
      </p>
    </div>
    
    <div class="container"></div>
    <div class="container"></div>
  </body>
  ```
 
 - Dalam hal ini terdapat beberapa cara untuk mencari elemen html, yaitu 
   - Mencari 1 element dengan id tertentu. Dengan ``document.getElementById("header")``
   - Mencari beberapa element sekaligus dengan class tertentu. Dengan ``documents.getElementsByClassName("container")``
   - Mencari element menggunakan kombinasi selector seperti pada CSS ``document.querySelector("#header p span")``
 Selain itu juga terdapat beberapa cara untuk memanggil DOM Value, antara lain 
 - Memanggil tag HTML berdasarkan ID ``console.log(document.getElementByID("header))``
 - Memanggil tag HTML berdasarkan Class Name ``console.log(document.getElementByClassName("container"))``
 - Memanggil tag html berdasarkan query selector ``console.log(document.querySelector("#header "))``
 
 - **Mengubah Konten Element** 
  - **Dengan Element.textContent**. Element.textContent dapat digunakan untuk mengubah teks di dalam sebuah element. Contoh scriptnya :
    ```
    Kombinasi dari 
    <h1 id=website></h1>
    dan
    document.getElementById("website").textContent = "Ini Websiteku"
    
    Hasilnya seperti menulis
    <h1 id=website>IniWebsiteku</h1>
    ```
  - **Dengan Element.innerHTML**. Element.innerHTML dapat digunakan untuk mengubah konten HTML didalam sebuah element. Jika .textContent digunakan untuk menambahkan teks, maka .innerHTML dapat digunakan untuk menambahkan konten HTML. Selain menggunakan innerHTML, bisa juga menggunakan innertext untuk mengubah atau menambahkan konten HTML. Perbedaan innerHTML dan innertext yaitu innerHTML implementasi element html,lalu innertext menampilkan teks string. Contoh scriptnya :
    ```
    Misalnya ada tag list <ul id="list"></ul>
    Lalu bisa menambahkan item dengan 
    document.getElementById("list").innerHTML = "<li>Mawar</li> <li>Melati</li>"
    
    Maka hasilnya adalah
    <ul id="list">
      <li>Mawar</li>
      <li>Melati</li>
    </ul>
    ```
    Selain itu, misalnya ada script :
    ```
    Pada teks html
    <div id="app"></div 
    Lalu menambahkan item dengan
    
    pada teks javascript
    let app = document.getElementById("app")
    app.innerHTML = "Hallo"
    
    Maka hasilnya akan
    Hallo
    ```
 - **Membuat element HTML** . Dalam membuat element baru html kita bisa menggunakan method createElement(). Selain itu dalam createElement() ini kita juga bisa menyertakan nama tag spesifik yang dituju sebagai parameter. Setelah elemen baru terbuat, pastinya kita tidak ingin konten element tersebut kosong. Maka dari itu, bisa memanfaatkan append() dan appendChild(). Method append() yang menerima argument bertipe Node atau string, sedangkan jika ingin menyematkan elemen lain sebagai child dari elemen tersebut, gunakan appendChild(). appendChild() juga dapat digunakan untuk menambahkan ke DOM atau menyisipkan node saja. Contoh script :
    ```
    Jika terdapat element ini di HTML
    <div id="header"></div>
 
    Lalu setelah itu bisa menggunakan kode Javascript untuk membuat sebuah element heading
    const heading = document.createElement("h1")
    heading.textContent = "Ini heading"
    document.getElementById("header").appendChild(heading)
 
    Maka hasilnya
    <div id="header">
      <h1>Ini heading</h1>
    </div>
    ```
 - **Menghapus Element** , Untuk menghapus element kita bisa menggunakan ``remove()``. Contoh syntax :
    ```
    let end = document.getElementById("end")
    end.remove()
    ```
 -  **Mengecek dan melihat Attribute**. Kita bisa mengecek dan melihat attribute dalam HTML dengan :
    ```
    <a href= google.com" class="link">Google</a>
    
    //karena classname adalah html collection maka ditambahkan index array ke-0
    let link = document.getElementByClassName("link")[0]
    
    //untuk mengecek attribute 
    console.log(link.attributes)
    
    //untuk melihat punya attribute apa saja
    console.log(link.attributes("href"))
    ```
 -  **Menambahkan Attribute**
    ```
    link.setAttribute("Id", "google")
    ```
 - **Memberikan style** , kita bisa memberikan styling pada html dengan menggunakan javascript DOM, contoh syntaxnya :
    ```
    link.style.color = "black"
    link.style.border = "1px solid black"
    link.style.padding = "5px 20px"
    link.style.backgroundColor = "aqua"
    ```
 - **Menghapus style property**
    ```
    link.style.removeProperty("border") 
    ```
 - **Menambahkan style dari element**
    ```
    <style>
      #tess {
          width: 100px;
          height: 20px;
          background-color: brown:
      }
      
    let tess = document.getElementById("tess")
    let tessStyle = getComputedStyle(tess)
    console.log(tessStyle.height)
    ```
 - **List Class**
    ```
    <div class= "container">
    
    </div>
    
    let container = document.getElementsByClassName("container")[0]
    console.log(container.classList);
    ```
 - **Menambahkan Class**
    ```
    container.classList.add("home") 
    ```
 - **Menghapus Class**
    ```
    container.classList.remove("container") 
    ```

### **DOM Events dan DOM Form**
- Event berarti kejadian atau kegiatan atau interaksi yang terjadi pada website.
- Terdapat 3 cara dalam memberikan event, yaitu :
  - HTML Attribute.
    ```
    <h1 onclick="alert('selamat datang')">Hallo</h1>
    ```
  - Event propperty.
    ```
    <p id="paragraf">click me</p>
     
    paragraf.onclick = function () {
      alert("ini dari paragraf")
    }
    ```
    Atau bisa juga dengan tampilkan alert
    ```
    paragraf.onclick = tampilkanAlert

    function tampilkanAlert () {
      alert("ini alert")
    }
    ```
  - addEventListener()
    ```
    <button id="btn">klik saya</button>
    
    let button = document.getElementById("btn")
    button.addEventListener("click", function (event) {
      console.log(event.target)
      alert("ini dari button")
    })
    ```
- Event sendiri terdiri dari ;
  - click, adalah event yang terjadi ketika user melakukan klik atau tab. 
  - submit, adalah event yang biasanya terjadi pada form saat melakukan submision atau mengirim data pada form.
  - focus, akan diaktifkan ketika user melakukan klik atau tab.
  - blur, event terjadi karena element kehilangan fokus.
  - hover,event yang terjadi karena mouse, dimana saat pointer berada diatas element.
  - change, biasanya terjadi pada element input seperti input text, checkbox, radio, select-option, dan lain sebagainya. Event change terjadi saat nilai pada element tersebut berpindah.
  - scroll, event terjadi ketika user melakukan scroll.
