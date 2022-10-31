# **Writing Minggu ke-5**

## **Back-End Developement**

### **Web-Server dan RESTful API**
- **Web Server** adalah gabungan dari hardware dan software untuk tempat aplikasi berada nantinya, dimana aplikasi diakses menggunakan methods http. 
    - **Hardware** adalah komputer yang menyimpan perangkat lunak server web dan file komponen situs web. Server web terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web. 
    - **Software** adalah server web yang mencakup beberapa bagian dengan mengontrol bagaimana pengguna web mengakses file yang dihosting. Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP. Server HTTP dapat diakses melalui nama domain situs web yang disimpannya, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir. 
- **Static Web Server** terdiri dari komputer (perangkat keras) dengan server HTTP (perangkat lunak). Disebut "statis" karena server mengirimkan file yang dihosting apa adanya ke browser. 
- **Dynamic Web Server** terdiri dari server web statis ditambah perangkat lunak tambahan, paling sering server aplikasi dan database. Disebut "dinamis" karena server aplikasi memperbarui file yang dihosting sebelum mengirim konten ke browser melalui server HTTP.
- **Metode Request** terdiri dari 
    - **Tradisional** seperti ketika meminta halaman movies ke server netifly. Maka server mengambil halaman movies html lalu diberikan ke browser. Dalam metode tradisional ini perintah respon dan request berupa halaman html atau tampilan.
    - **Single Page Application/Client-Side-Render** yaitu ketika membuka aplikasi, lalu meminta ke server tetapi uniknya dia meminta dalam bentuk json saja bukan berupa halaman html. Json akan diberikan dari server ke browser. Lalu data akan ditanpilkan. Prosesnya dilakukan di web browsernya.
    - **Dynamic Site/Server-Side-Render** yaitu prosesnya dilakukan pada bagian server. Ketika meminta data maka dia akan menyiapkan halamannya. Lalu diberikan ke browser. Proses full dibagian server. Bisa juga memberikan dalam bentuk html atau json.
- **Database** adalah tempat untuk menyimpan datanya. 
- **Server** adalah bagian yang mengambil data. 
- **API Architectural Styles Comparison** antara lain :
    - CORBA, tahun 1991.
    - RDA, tahun 1993.
    - XML-RPC, tahun 1998.
    - SOAP, tahun 1999.
    - REST, tahun 2000.
    - JSON-RPC, tahun 2005.
    - ODATA, tahun 2007.
    - GRAPHQL, tahun 2015.
    -gRPC,tahun 2016.
- **REST** atau Representation State Transfer adalah salah satu arsitektur untuk membuat web service. Rules yang dimiliki oleh REST yaitu :
    - Uniform Interface.
    - Client Server.
    - Stateless.
    - Cacheable.
    - Layerd System.
    - Code on demand.
- API yang menerapkan rules dadi REST ini disebut dengen **Restful API**
- **HTTP Method** terdiri dari :
    - **GET** digunakan untuk mengambil suatu data.
    - **POST** digunakan untuk mengirim database ke server.
    - **DELETE** digunakan untuk menghapus suatu data.
    - **PUT/PATCH**, PUT digunakan untuk update data pada sebagian atau keseluruhan data. Sedangkan PATCH digunakan untuk update data pada sebagian saja. 
- **Status Code** 
    - 2xx berarti success.
    - 3xx berarti redirection.
    - 4xx berarti client eror (kesalahan pengguna).
    - 5xx berarti server eror (kesalahan server).
- **Rules Penulisan Endpoint API** 
    - Memakai huruf kecil.
    - Menggunakan dash (-) jika lebih dari satu kata.
    - Dibuat plural jika terdapat banyak data. 
    - Dibuat singular jika terdapat satu data.

### **Node JS**
- **Node JS** adalah javascript runtime yang dibangun oleh Chrome's V8 Javascript Engine. Runtime sendiri berarti tempat untuk menjalankan eksekusi. Node JS sendiri dibuat oleh Ryan Dahl pada tahub 2009. 
- Secara default, Node memiliki beberapa variabel global yang dapat diakses dan dimodifikasi, seperti global, process, dan lain sebagainya. Biasanya variabel process.env sering digunakan untuk menyimpan configuration ataupun credentials yang sifatnya rahasia, yang bisa digunakan di dalam aplikasi.  
- **Main Feature atau fitur utama** dari Node JS antara lain
    - File System.
    - Http dan Https.
    - REPL (Read, Eval, Print,Loop) merupakan terminal node.js.
    - Console.
- **Build In Module Node JS** yaitu :
    - **Console** adalah module bawaan dari javascript yang ada di node JS untuk digunakan sebagai debug atau menampilkan code secara interface.
    - **Process** adalah modules yang digunakan untuk menampilkan dan mengontrol prosess Node JS yang sedang dijalankan.
    - **OS module** adalah module yang digunakan untuk menyediakan informasi terkait sistem operasi komputer yang digunakan user.
    - **Module Util** adalah alat bantu / utilities untuk mendukung kebutuhan internal API di Node JS.
    - **Events** adalah kejadian yang terjadi di halaman web. Kejadian yang dimaksud di sini seperti aktivitas yang dikerjakan pada halaman web.
    - **Errors** merupakan modules yang dapat digunakan untuk mendefinisikan error di Node JS sehingga lebih informatif. 
    - **Buffer** merupakan modules yang digunakan untuk mengakses, mengelola dan mengubah tipe data raw atau tipe data bytes.
    - **Fs atau File System** merupakan module yang dapat membantu berinteraksi dengan file yang ada diluar code. FS paling sering digunakan untuk membaca file dengan ekstensi .txt, .csv, dan .json.
    - **Timers** merupakan modules yang digunakan untuk melakukan scheduling atau mengatur waktu pemanggilan fungsi yang dapat diatur di waktu tertentu.
- **NPM atau (Node Package Manager)** adalah package dan dependency manager utama pada NodeJS. Biasanya digunakan untuk mengelola library ketika akan digunakan. Dependency adalah suatu unsur metode untuk memisahkan dan mengintegrasikan berbagai program berbeda menjadi program yang utuh.
- **Node JS Web Server** Node.js memiliki built-in modul yang disebut HTTP, built-in modul ini memungkinkan Node JS mentransfer data melalui Hyper Text Transfer Protocol (HTTP). Modul HTTP dapat membuat server HTTP yang mendengarkan port server dan memberikan respons kembali ke klien.
- Untuk menggunakan modul HTTP, gunakan require().
- Gunakan method createServer() untuk membuat server HTTP.
- Callback function yang digunakan pada method http.createServer(), akan dijalankan ketika seseorang mencoba mengakses komputer pada port 8080.

### **Express Routing dan Middleware**

- **Express** adalah framework untuk membuat sebuah website aplikasi atau web server. 
- Didalam express terdapat istilah request yang berarti meminta data dari sisi client, dan response yang berarti merespon atau memberikan data atau apa yang client terima. 
- **Back end app** adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app. Umumnya server-side app membuat REST API
- **Parsing Request Body From HTTP**, Req.body berfungsi untuk menangkap nilai/data yang dikirimkan user dari interface / dari postman. 
- **Routes** adalah sebuah end point yang diapat kita akses menggunakan URL di website. Didalam routes, perlu menentukan method API, alamat dan response apa saja yang akan dikeluarkan. Aplikasi sederhana dapat berjalan dengan menggunakan node. Dan aplikasi tersebut akan berjalan di alamat ‘http://localhost:3000’. Kemudian kita dapat mengaksesnya di website dan menambah route yang akan kita akses yaitu “/”.
- **Method HTTP Request** antara lain :
    - Get dengan endpoint /items digunakan untuk mendapatkan semua data. 
    - Get dengan endpoint /items/:id digunakan untuk mendapatkan data berdasarkan identitas yang dipanggil.
    - Post dengan endpoint /items digunakan untuk menambahkan serta menyimpan item. 
    - Delete dengan endpoint /items digunakan untuk menghapus semua item yang ada. 
    - Delete dengan endpoint /items/:id digunakan untuk menghapus item tertentu.
    - Put dengan endpoint /items/:id digunakan untuk mengupdate suatu item. 
- **Response pada Node JS** antara lain :
    - res.download()
    - res.end()
    - res.json()
    - res.jsonp()
    - res.redirect()
    - res.render()
    - res.send()
    - res.sendFile()
    - res.sendStatus()
- Routing mengacu pada bagaimana endpoint sebuah website/aplikasi (URIs) merespons permintaan client. Menentukan rute  dapat menggunakan metode Express yang sesuai dengan metode HTTP. Misal app.get(), app.post(), app.all(), dan juga ap.use(). Terdapat juga app.listen() yang digunakan untuk memberitahu file yang berjalan.
- **Nodemon** adalah tools yang membantu developer,otomatis menjalankan aplikasi ketika di save dan ketika terdapat ubahan pada web server.
- **Middleware** adalah function yang mempunyai akses ke request dan respons dan next atau memfilter atau menyaring data sebelum ke database. Diibaratkan ketika kita memiliki stand minuman lemon,terdapat pembeli yang membawa buah lemon dari rumah untuk dibuat di stand kita. Nah kita pasti kesulitan untuk menentukan kesegaran buah tersebut serta membuang buah yang dikira busuk sehingga tidak dapat dibuat minuman. Dalam hal ini kita memiliki karyawan yang bertugas untuk mengecek kesegaran buah lemon tersebut, setelah itu karyawan yang mengecek tadi memberikan buah yang masih segar dan busuk ke dalam wadah terpisah lalu ke karyawan yang memiliki bagian menyetorkan serta membuang buah busuk tersebut memberikan buah segar ke kita dan membuang buah yang dikira tidak bisa digunakan. Akhirnya kita bisa membuat minuman dari buah yang dibawa pembeli menggunakan buah segar. Maka kita tidak perlu repot-repot untuk memlilih atau memfilter buah segar. Karyawan tersebutlah yang disebut dengan middleware. 
- **Tugas middleware** antara lain :
    - Menjalankan kode apapun.
    - Memodifikasi Object Request dan Object Response.
    - Menghentikan request-response cycle.
    - Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.
- **Jenis Middleware berdasarkan penggunaannya** yaitu
    - **Application Level Middleware**, adalah sebuh function middleware yang melekat ke instance object Application Express. Penggunaannya dengan cara memanggil method app.use().
    - **Router Level Middleware**, adalah sebuh function middleware yang cara kerjanya sama persis dengan application level middleware, yang menjadikan perbedaan adalah middleware function ini melekat ke instance object Router Express. Penggunaannya dengan cara memanggil method express.Router().
    - **Error Handling Middleware**, mengacu kepada bagaimana cara sebuah Express Application menangkap dan memproses error yang terjadi, baik itu berupa kesalahan yang synchronous maupun asynchronous.

### **Design Database With Mysql**   

- Dalam membuat design database pertama tama membuat requirement lalu mulai untuk mengidentifikasi entity dalam database. Entity Relation Model untuk mendesain database berdasarkan pelaku yang terlibat.
- Selanjutnya adalah menentukan attributes apa saja yang akan datanya akan dsimpan di dalam sebuah entity. Attributes yang di perlukan didalam entity kemungkinan sudah ada di dalam requirements document, atau mungkin juga diperlukan penafsiran diri sendiri sebagai database developer.
- Relasi dalam database terdiri dari one to one, one to many, many to one, many to many. 
- **One to one** adalah relasi yang terjadi antar field. 
- **One to many** adalah relasi antara satu field dengan beberapa field. 
- **Many to many** adalah relasi antara banyak field dengan banyak field. 
- Relasi antar tabel dihubungkan oleh Primary key dan foreign key.
- Selain itu, terdapat primary key serta foreign key dalam attribute database. Primary key adalah atribut yang tidak hanya mengidentifikasi secara unik suatu kejadian, tapi juga mewakili setiap kejadian suatu entitas.

### **Normalisasi Database** 

- **Normalisasi** adalah teknik untuk mengorganisir data ke dalam bentuk table, supaya data tidak redundant, mudah dicari, serta tidak terjadi anomali. 
- Normalisasi biasa digunakan untuk mendesign database yang dibentuk dari kumpulan data, design database yang kurang bagus (masih terjadi anomali). Anomali adalah ketika terdapat attribute bergantung dengan attribute lain yang bukan primary key. Normalisasi terdiri dari 3 jenis yaitu :
    - 1NF, tidak ada urutan dalam penyimpanan data, harus menggunakan tipe data yang sama pada satu kolom, harus ada primary key, tiap kolom harus berisi nilai tunggal.
    - 2NF, harus dalam bentuk 1NF, tidak ada partial depedency (attribute yang tidak ada hubungan dengan primary key akan dipisah).
    - 3NF, harus dalam bentuk 2NF, tidak ada transitif depedency (setiap attribute harus bergantung pada primary key supaya tidak terjadi transitif depedency).
