# **Writing Minggu ke-3**

## **Back-End Developement**

### **Sequelize**
- **Sequelize** adalah ORM Framework pada NodeJS. ORM sendiri berarti metode untuk membuat data, tabel, yang diconvert ke objek. ORM harus digunakan karena dapat memisahkan kode sql dari logic aplikasi, mempermudah maintance, serta menghindari ketergantungan aplikasi terhadap vendor database. Yang harus dilakukan saat membuat sequelize yaitu melakukan instalasi sequelize, melakukan define model atau membuat tabel, serta persist dan query atau memasukkan data dan mencari data. 
- Sequelize bisa digunakan dengan PostgreSQL, MySQL, MariaDB, SQLite, dan MSSQL.
- Langkah-langkah melakukan generated sequelize yaitu
    - Sequelize init
    - Melakukan setting database
    - Membuat table todo dengan ``npx sequelize-cli model:generate --name todo --attributes title:string,descroption:string,startTime:date,status:string``
    - ``npx sequelize-cli db:migrate``. Untuk melihat history atau perubahan pada table.
    - Jika ada yang salah, bisa mengembalikan (undo) ``npx sequelize-cli db:migrate:undo`` 
    - Ketika kita berhasil melakukan generate maka akan muncul 1 tabel baru yang bernama Tppdps dan SequelizeMete di database. 
- Saat melakukan sequelize init akan menghasilkan beberapa folder yaitu
    - config, untuk menyimpan file koneksi database.
    - model, untuk menyimpan semua model di projek.
    - migrations, untuk menyimpan semua file migrasi.
    - serta seeders, untuk menyimpan semua seed files.
- Seed adalah data awal yang digunakan untuk mengisi data di database untuk keperluan awal project menggunakan sequelize. 
- Ketika sudah berhasil melakukan generate maka kita dapat melakukan pengisian data seed didalam file seed generator. Terdapat 2 data yang diisi yaitu “up” untuk mengisi data di db, dan “down” untuk drop atau menghapus semua data seed di database.
- CRUD dengan express dan sequelize. Terdiri dari beberapa endpoint RESTful API yaitu 
    - Get All Todos. Menggunakan findAll() yang berfungsi untuk mencari banyak data dalam database, jika panggil tanpa parameter maka akan mengambil semua data.
    - Get Todo Detail By Id. Menggunakan findOne() yang berfungsi untuk mencari satu spesifik data dengan kriteria pada parameter.
    - Create New Todo. Menggunakan app.post yang berfungsi untuk menambahkan data ke dalam database. 
    - Update Todo By Id. Menggunakan app.patch yang berfungsi untuk mengupdata data berdasarkan id dalam database.
    - Delete Todo By Id. Menggunakan app.delete yang berfungsi untuk menghapus data berdasarkan id dalam database.
- Running migration menggunakan perintah ``npx sequelize-cli db:migrate``
- Jika mau undo migration, dapat menggunakan ``npx sequelize db:migrate:undo``

### **MongoDB dan Mongoose**
- MongoDB adalah database NoSQL yang menggunakan struktur data berbentuk Json untuk penyimpanan data. NoSQL berarti mengolah database dengan fleksibel dan tidak membutuhkan Query. MongoDB sering dipakai untuk aplikasi berbasis Cloud, Grid Computing, atau Big Data.
- Untuk proses run kita bisa menggunakan mongodb shell, tetapi untuk mempermudah pekerjaan, kita bisa menggunakan MongoDB GUI Tools yaitu mongodb compass. 
- MongoDB Atlas digunakan untuk mendeploy pekerjaan kita yang berkaitan dengan sistem database. Cara instalasi mongodb atlas yaitu pertama buka website mongodb atlas, pilih try free dan isi formulir pendaftaran yang telah disediakan, pilih Shared Cluster dengan starting free, lalu ikuti langkah langkah yang ada, setelah berhasil dibuat, sekarang kita bisa menghubungkan cluster kita menggunakan MongoDB Compass. 
- Saat membuat koneksi Setup IP dibuat 0 seemua dan buat MongoDB User, Copy connection string, untuk menghubungkan MongoDB Compass, lalu lembali ke MongoDB Compass dan Paste connection string yang kita punya. 
- Mongoose adalah library atau kata lain Object Modelling MongoDB untuk NodeJS. Mongoose merupakan ODM dari mongodb. Mongoose bisa digunakan untuk mengelola hubungan antara data, menyediakan validasi. Selain itu, juga digunakan untuk menerjemahkan antara objek dalam kode dan representasi Objek tersebut di MongoDB. 
- Dengan mongoose kita akan mendapatkan bermacam fitur yang dapat digunakan pada pengelolaan database.
- Hal hal yang harus diperhatikan saat menggunakan mongoose yaitu
    - npm install mongoose.
    - Membuat koneksi dengan menggunakan MongoDB database, yang diletakkan di .env. .env digunakan untuk menyimpan URL atau data rahasia yang tidak perlu dilihat di public.
    - Membuat schema dengan var userSchema = new Schema({}).
- const User = mongoose.model ('users', userSchema), model users dari schema yang telah kita dapat digunakancuntuk melakukan pengolahan data, atau operasi CRUD.
- CRUD pada mongodb antara lain
    - Menginstall express untuk routing dan body-parser, untuk menggunakan method Post dan testing API di postman.
    - Lalu untuk menampilkan keseluruhan data bisa menggunakan fungsi find().
    - Menggunakan method POST untuk mendaftarkan user, sebelum mendaftarkan kita mengecek dulu apakah user sudah ada atau belum dengan menggunakan findOne(), jika sudah ada akan muncul pesan error, jika belum terdaftar maka user akan didaftarkan menggunakan fungsi create().
    - Isi form raw dengan tipe JSON, atau bisa juga menggunakan form-data, untuk mendaftarkan user, setelah itu kita bisa menekan tombol send untuk mengirim request post.
    - Menggunakan fungsi findByID untuk mendapatkan data user berdasarkan id.
    - Menggunakan fungsi deleteOne() untuk menghapus satu data berdasarkan Id.
    - Menggunakan fungsi findByIdAndUpdate() untuk mengedit atau update satu data berdasarkan Id.
    - Populate ada kaitannya dengan relasi database. Populate adalah proses penggabungan 2 collection atau lebih menjadi satu objek JSON.
- start pada package json berisi start dan dev. Pada start menjalankan file utama node app.js, sedangkan dev digunakan untuk menjalankan file utama nodemon app.js

### **Docker**
- **Docker** adalah software yang menjalankan suatu aplikasi menggunakan container. Misalnya terdapat 2 komputer berbeda OS. Komputer B ingin menjalankan project A, tetapi terjadi issue (aplikasi tidak bisa dijalankan), maka agar tidak terjadi issue bisa menggunakan docker. Docker sendiri bisa dijalankan dengan 1 PORT saja.
- Docker men-sharing kernel dari host OS, serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja.
- Docker akan menyediakan hal-hal yang diperlukan untuk aplikasi mulai dari akses file, koneksi internet, hingga port agar aplikasi dapat berjalan dengan mulus.
- Permbedaan VM dan container yaitu VM memakan banyak resource dan waktu utk booting karena melakukan virtualisasi pada host hardware-nya. Sedangkan container kebalikannya dari vm, container melakukan virtualisasi pada host OS-nya.
- 3 hal yag harus diketahui pada docker.
    - Docker File (Blueprint) berisi state yang akan kita gunakan.
    - Docker Image berkaitan dengan project, dan ketika di run dia dibungkus oleh container.
    - Docker Container merupakan perwujudan dari image.
- Perintah-perintah dasar pada Docker yaitu 
    - docker pull, digunakan untuk mendownload image dari docker hub.
    - docker image, digunakan untuk melihat kumpulan images yang sudah terdownload.
    - docker run, digunakan untuk menjalankan container.
    - docker ps, digunakan untuk melihat container yang berjalan.
- Docker file adalah sebuah blueprint untuk  membuat image, dan bisa juga digunakan untuk membuat custom image menggunakan docker file.
- Docker Compose adalah cara untuk menjalankan lebih dari 1 container secara bersamaan dan saling terhubung.
