# **Writing Minggu ke-2**

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
