# **Writing Minggu ke-1**

## **Unix Command Line**

### **CLI (Command Line Interface)**
- **Command Line Interface** adalah cara berinteraksi antara user dengan sistem operasi atau perangkat lunak komputer dengan memberikan atau menuliskan perintah untuk menjalankan suatu tugas tertentu. Contoh CLI antara lain sh, bash, zsh, cmd.exe.
- **Shell** adalah tampilan yang digunakan untuk memproses suatu perintah agar intruksi dapat berjalan sesuai dengan permintaan user. Selain itu, shell juga digunakan sebagai penerjemah user agar bisa terhubung dengan komputer.
- **Terminal** Terminal sendiri bisa disebut juga dengan shell. Terminal berarti tampilan atau tempat untuk mengetikkan baris perintah berbasis teks dalam suatu sistem operasi. Terminal berfungsi untuk memanajemen serta mencari berkas yang ada dalam komputer kemudian file tersebut diolah sesuai dengan keinginan.
- **File System Structure** adalah sebuah filesystem yang mengatur bagaimana data disimpan di dalam sebuah system. Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree atau pohon.
- **Command untuk Navigasi**
  - pwd (Print working directory), digunakan untuk melihat current working direktori.
  - ls (List), digunakan untuk melihat isi file yang ada di sebuah direktori.
  - cd <direktori> (Change directory), digunakan untuk untuk berpindah direktori.
- **Command untuk Manipulasi file dan direktori**
  - touch, digunakan untuk membuat sebuah file.
  - mkdir, digunakan untuk membuat sebuah direktori.
  - head, digunakan untuk melihat beberapa line awal dari sebuah file text.
  - tail, digunakan untuk melihat beberapa line awal dari sebuah file text.
  - cat, digunakan untuk melihat isi sebuah file.
  - cp, digunakan untuk mengcopy files atau directory.
  - mv (Move), digunakan untuk memindahkan files atau directory. Bisa juga digunakan untuk rename.
  - rm (Remove), digunakan untuk menghapus file atau directory.
  - cp-R, digunakan untuk menyalin directory.
  - mv-R, digunakan untuk memindahkan directory.
  - rm-R atau rm-d, digunakan untuk menghapus directory.

  
## **Git dan Github**
  
### **Pengertian**
- **Git** adalah tools atau software untuk programmer yang digunakan sebagai Version Control System. Version Control System maksudnya mencatat setiap perubahan pada file pada suatu proyek baik dikerjakan secara individu maupun tim.  Git biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
- **Github** adalah sebuah website dan layanan berbasis cloud bagi para developer untuk menyimpan dan mengelola kode, serta mendokumentasikan dan mengontrol perubahannya. Selain itu, kita juga dapat membuat atau mengupload kode yang sudah dibuat ke server GitHub dan kemudian melakukan coding secara online.

### **Pentingnya penggunaan git dan github**
Dengan menggunakan GIT dan Github, seorang programmer akan bisa bekerja dalam sebuat tim. Tujuan penggunaan git dan github yaitu mumudahkan programmer dalam berkolaborasi mengerjakan proyek yang sama tanpa harus susah copy paste folder aplikasi yang terupdate. Selain itu, kita juga tidak perlu menunggu rekan dalam satu tim menyelesaikan suatu program untuk berkolaborasi. Kita bisa membuat file didalam projek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.

### **Command pada git dan github**
  - Konfigurasi git. Dalam konfigurasi git terdapat 2 hal yang harus diperhatikan yaitu mengatur username, cara penulisannya git config --global user.name "Fala". Dan mengatur email, cara penulisannya git config --global user.email fala.alma@gmail.com
  - git init, digunakan untuk membuat repositori. Git init sendiri bisa diibaratkan seperti memasang memori card pada handphone dan hanya dijalankan satu kali saja.
  - git clone, digunakan untuk mengambil seluruh repositori dari lokasi yang dihosting melalui URL.
  - git status, digunakan untuk mengecek repository status, terjadi perubahan pada git atau tidak.
  - git add, digunakan untuk menambahkan file ke staging. Dalam penulisannya bisa seperti git add index.html atau bisa dengan git add .
  - git commit -m, digunakan untuk menyimpan files di staging sebagai commit. Git commit juga digunakan untuk menyimpan perubahan pada version control.
  - git log, digunakan untuk melihat histori perubahan atau riwayat commit yang sudah dijalankan.
  - git diff, digunakan untuk melihat detail perubahan.
  - git checkout, digunakan untuk kembali ke commit tertentu atau berpindah ke branch lain.
  - git reset, digunakan untuk reset files ke sebuah commit, perubahan di branch yang dihapus menjadi ‘untracked files’.
  - git revert, digunakan untuk undo commit, perubahan disimpan dalam commit. git revert akan membatalkan semua perubahan yang ada tanpa menghapus commit terakhir.
  - git branch, digunakan untuk melihat branch yang ada. Branch aktif ditandai dengan `*`.
  - git remote, digunakan untuk melihat daftar remote di repositori.
  - git push -u origin, digunakan untuk mengirim perubahan ke remote repositori.
  - git pull, digunakan untuk mengambil perubahan dari remote ke local.
  
  
## **Algoritma**
  
- Algoritma adalah sebuah langkah-langkah untuk menyelesaikan suatu permasalahan yang ada. 
- Contoh permasalahannya seperti apa yang harus kita lakukan ketika lapar? dari permasalahan tersebut pastinya terdapat beberapa solusi. Bisa saja seperti kita menuju ke dapur lalu memasak akhirnya kita bisa makan. Bisa saja kita pergi ke warung untuk membeli makanan tersebut lalu akhirnya kita bisa makan. Dan bisa saja terdapat solusi-solusi lain yang bisa kita lakukan ketika lapar. Setiap orang pasti berbeda-beda dalam menyelesaikan permasalahan tersebut.
- Ciri-ciri Algoritma antara lain :
  - Input, harus memiliki 0 atau lebih inputan. Contohnya Susu sachet.
  - Output, harus memiliki 1 inputan. Contohnya Segelas susu hangat.
  - Definiteness, memiliki instruksi jelas dan tidak ambigu. Contohnya mulai dari menyiapkan susu sampai dengan cara pembuatannya.
  - Finiteness, memiliki titik berhenti atau stop. Contohnya susu sudah selesai dibuat. 
  - Effectiveness, haruslah tepat sasaran dan efisien.
- Jenis proses algoritma antara lain :
  - Sequence, instruksi yang dijalankan secara berurutan. Misalnya gelas diisi dengan air, lalu air siap untuk diminum.'
  - Selection, instruksi yang dijalankan jika memenuhi suatu kondisi. Misalnya jika lampu merah, saya akan berhenti.
  - Iteration, instruksi yang berulang kali dijalankan selama memenuhi suatu kondisi. Misalnya selama belum sampai rumah, saya akan terus menyetir.
  - Concurrent, instruksi yang dijalankan secara bersamaan. Misalnya ibu mencuci baju sambil membersihkan rumah.
- Penyajian algoritma antara lain :
  - Deskriptif, penulisan algoritma dengan cara deskriptif seperti ketika kita menulis tutorial (tata cara) dengan bahasa sehari-hari.
  - Flowchart, penulisan algoritma flow chart atau diagram alir dengan menggunakan simbol bangun datar sebagai represenatsi dari proses yang dilakukan. Penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual.
  - Peseudo Code, penulisan algoritma peseudo code hampir menyerupai penulisan pada kode pemrograman. Pada umumnya pseudocode memiliki 3 bagian yaitu
  a. Judul, berisi tentang penjelasan dari algoritma yang dibuat.
  b. Deklarasi, mendefinisikan/menyiapkan semua nama (variabel) yang akan digunakan.
  c. Deskripsi, langkah-langkah penyelesaian masalah.
- Contoh Algortitma Sederhana : Perhitungan Luas Segitiga.
  - Masukkan alas.
  - Masukkan tinggi.
  - Luas segitiga adalah 1/2*a*t
  - Tampilkan luas segitiga.
- Penerapan algoritma luas segitiga menggunakan bahasa pemrograman C++.
  ```
  # include <iostream>
    using namespace std;
  
    int main (){
    int a, t;
    float luas;
    cout<<"Masukkan panjang alas = ";
    cin>>a;
    cout<<"Masukkan tinggi = ";
    cin>>t;
  
    luas = 0.5*a*t;
    cout<<"Luas Segitiga adalah "<<luas<<endl;
  
    return 0;
  }
  ```
- Penerapan algotitma luas segitiga menggunakan Javascript.
  ```
  let alas = 8;
  let tinggi = 10;
  let luas_segitiga = 0.5 * alas * tinggi;
  
  console.log(`luas segitiga dengan alas: ${alas} dan tinggi ${tinggi} adalah ${luas_segitiga}`);
  ```
## **HTML**
  
- HTML adalah singkatan dari <i>Hyper Text Markup Language</i>. HTML sendiri bisa diartikan sebagai bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet.
- Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML, yaitu Browser dan Code Editor. Visual Studio Code adalah code editor yang dikembangkan oleh tim engineer Microsoft.
- **HTML Structure** :
  ```
   <!DOCTYPE html>
    <html lang="en">
    <head>
         <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>My Personal Blog</title>
    </head>
    <body>
         <div>
            <p>Hallo nama saya Fala Alma'as Liyanti dari Universitas PGRI Madiun</p>
          </div>
    </body>
    </html>
  ```
- **HTML Tag** adalah sebuah penanda awalan dan akhiran dari sebuah elemen di HTML yang biasanya dibuat dengan kurung siku (<...>), lalu di dalamnya berisi nama tag dan kadang juga ditambahkan dengan atribut. Dokumen HTML memiliki 3 tag utama, yaitu ``<html>``, ``<head>``, dan ``<body>``. Contoh penulisannya :
  ```
    <!DOCTYPE html>
    <html lang="en">
      <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
         <title>Document</title>
      </head>
      <body>
       
      </body>
      </html>
   ```
  Source code diatas terdiri dari :
  - ``<!DOCTYPE>`` syntax mendefinisikan versi dari HTML yang digunakan dan harus dideklarasi sebelum tag <html>. <!DOCTYPE html>mendefinisikan bahwa dokumen ini adalah HTML5.
  - ``<html></html>`` adalah root element dari halaman HTML. Semua HTML tag lainnya harus dibungkus dengan tag ini.
  - ``<head>`` pada umumnya berisi ``<meta>``, ``<title>``, konten css/js internal maupun link ke file css/js eksternal.
  - ``<body>`` berisi konten website yang ingin ditampilkan pada browser.
- **HTML Element** merupakan sebuah komponen dalam halaman web, bisa berupa paragraf, judul, atau gambar.
  Struktur dari HTML Element bisa dituliskan seperti :
  ```
  <p style="color:red">This is a paragraph.</p>
  
  HTML element diatas terdiri dari 
  Opening Tag (tag pembuka) yaitu <p>.
  Closing Tag (tag penutup) yaitu </p>.
  Attribute yaitu style yang memiliki Value "color=red". 
  Content (konten) yaitu tampilan yang ingin ditampilkan di browser, This is a paragraph.

  ```
  Selain HTML Element, terdapat Empty HTML Element yaitu HTML yang memiliki Self-closing Tag, yang hanya memiliki Opening Tag (tag pembuka) dengan garis miring sebelum kurung tutup. Contohnya adalah ``<br />`` atau ``<img />``
  Contoh tag HTML :
  - Tag untuk membuat tulisan tebal
  ```
  <p>
  Nama saya <b>Fala</b>. Saya berumur <strong>20 tahun.</strong>
  </p>
  ```
  - Tag untuk membuat huruf miring
   ```
  <p>
    Nama saya <i>Fala Alma'as</i>
  </p>
  ```
  - Tag untuk menuliskan link yang memberikan informasi tambahan kepada sebuah element.
  ```
  <a href="https://www.dumetschool.com/blog/animasi-mobil-motor-berjalan-dengan-css">Ini Mobil</a> 
  ```
  - Tag untuk membuat list/daftar
  Ada dua tipe list di HTML, yaitu: Unordered list dengan menggunakan tag ``<ul>`` dan Ordered list dengan menggunakan tag ``<ol>``. Masing-masing list baik ``<ul>`` atau ``<ol>`` memiliki element ``<li>`` untuk mendefinisikan nilai-nilai dari list tersebut. Contoh penggunaannya :
  ```
  <!-- Unordered List -->
  <ul>
    <li>Mawar</li>
    <li>Melati/li>
    <li>Anggrek</li>
  </ul>

  <!-- Ordered List -->
  <ol>
    <li>Sapi</li>
    <li>Beruang</li>
    <li>Ikan</li>
  </ol>
  ```
  - Tag untuk menampilkan gambar
  ```
  <img src="https://bit.ly/3j6eb3B" alt="Cat" />
  ```
- **Semantic HTML** berarti menggunakan element html yang sesuai dengan kebutuhan konten. Element Semantic HTML juga bisa didefinisikan denganelemen-elemen yang menyatakan makna atau tujuan dari elemen itu sendiri. Element Semenatic HTML antara lain :
  - ``<header>`` digunakan untuk membuat kepala kop dari web. ``<header>`` berfungsi sebagai header bagi seluruh halaman HTML ataupun sebagai header bagi seksi-seksi tertentu seperti header bagi seksi elemen <article>. Elemen ``<header>`` pada halaman HTML diletakkan pada bagian paling atas dan bagian ini dapat berisi logo, nama website, dan menu navigasi yang terdiri atas deretan tautan atau link.
  - ``<footer>`` adalah elemen struktural yang digunakan untuk mengidentifikasi bagian catatan kaki sebuah halaman, dokumen, seksi, ataupun artikel. Elemen ``<footer>`` biasanya diletakkan pada posisi bagian paling bawah suatu halaman HTML. Tag elemen ``<footer>`` dapat berisi informasi tentang nama perusahaan, kontak, copyright dan nama pembuat web.
  - ``<nav>`` adalah element pada HTML yang dibuat untuk mempresentasikan link navigasi.
  - ``<article>`` adalah elemen yang digunakan pada membentuk konten yang berdiri sendiri (stand alone) yang tidak terkait dengan konten pada elemen lainnya di dalam halaman web. Misalnya seperti isi artikel, postingan forum, postingan blog, ataupun untuk komentar. Di dalam elemen ``<article>`` ini dapat berisikan berbagai kumpulan elemen lainnya seperti DIV (division), P (paragraf), IMG (image), dan lainnya.
  - ``<section>`` adalah bahasa yang bisa sebut bagian atau seksi. Section dapat diartikan sebagai cara code untuk mempresentasikan bagian-bagian dokumen atau aplikasi, seperti mengelompokan konten/dokumen menjadi beberapa bagian seksi, berdasarkan tema dan tata letak masing-masing.  
Contoh source code HTML Semantic :
  ```
  <body>

  <header>
    <h1>Belajar HTML</h1>
  </header>

  <nav>
    <a href="/home/">Home</a> |
    <a href="/about/">About</a> |
    <a href="/gallery/">Gallery</a> 
    <a href="/contact/">Contact</a> 
  </nav>

  <article>
    <h1>HTML adalah singkatan dari Hyper Text Markup Language.</h1>
    <p>HTML adalah bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet.</p>
  </article>

  <footer>
    Copyright &copy; 2022 by falaalma
  </footer>

</body>

- **Deploy** adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang. Untuk mendeploy,bisa menggunakan tools bernama Netlify. Cara menggunakannya yaitu masuk ke netlify.com lalu register seperti biasa menggunakan email atau github. Setelah itu masuk ke tab Sites lalu drag and drop seluruh folder html yang ingin dideploy. 

## **CSS**
  
- CSS adalah singkatan dari <i>Cascading Style Sheets</i>. CSS juga bisa diartikan sebagai bahasa komputer yang digunakan untuk menambahkan design ke suatu halaman website di internet. Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.
- **Menyisipkan CSS ke dalam file HTML**
  - **Inline CSS** yaitu menggunakan attribute style untuk menyisipkan kode CSS langsung di dalam HTML element. Contoh penulisannya :
    ```
      <!DOCTYPE html>
    <html>
      <head>
        <title>Inline CSS</title>
      </head>
      <body>

        <h1 style="color:pink;">Saya bahagia</h1>

      </body>
    </html>
    Pada script diatas, output yang dihasilkan adalah teks dengan tulisan Saya bahagia serta berwarna pink.
    ```
  
  - **Internal CSS** yaitu element ``<style>`` untuk menyisipkan kode CSS. Element ``<style>`` biasanya diletakkan di dalam element ``<head>``. Contoh penulisannya :
    ```
      <!DOCTYPE html>
    <html>
      <head>
        <title>Website Pertamaku</title>
        <style>
          body {
            background-color: yellow;
          }
          h1 {
            color: blue;
          }
          p {
            color: red;
          }
        </style>
      </head>
      <body>
        <h1>Website Pertamaku</h1>
        <p>Selamat Datang</p>
      </body>
    </html>
    Pada script diatas menghasilkan <body> dengan latar belakang berwarna kuning, tulisan di dalam <h1> berwarna biru, dan tulisan di dalam <p> berwarna merah.
    ```
  
