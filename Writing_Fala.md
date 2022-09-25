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
  
- Penerapan algotitma luas segitiga menggunakan Javascript.
  ```
  let alas = 8;
  let tinggi = 10;
  let luas_segitiga = 0.5 * alas * tinggi;
  
  console.log(`luas segitiga dengan alas: ${alas} dan tinggi ${tinggi} adalah ${luas_segitiga}`);

## **HTML**
  
- HTML adalah singkatan dari <i>Hyper Text Markup Language</i>. HTML sendiri bisa diartikan sebagai bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet.
- Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML, yaitu Browser dan Code Editor.
- Visual Studio Code adalah code editor yang dikembangkan oleh tim engineer Microsoft.
- HTML Structure :
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

