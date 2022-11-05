# **Writing Minggu ke-2**

## **Back-End Developement**

### **My SOL Basic**
- **Database** tempat untuk menyimpan data agar suatu data dapat terstruktur dengan baik dan saling berrelasi. Informasi tersebut akan diolah, kemudian data yang dihasilkan dapat digunakan di dalam sebuah sistem. Contoh database SQL yaitu oracle, mariadb, posgresql, IBM DB2. 
- **My SQL Server** yaitu ketika membuat database terdapat server yang berjalan atau terdapat database yang berjalan atau beroperasi. 
- MySQL bersifat open source, comfortable untuk banyak platfom, serta multi user. 
- Untuk mengakses server dapat menggunakan workbench, dbeaver, tableplus, phpmy admin, datagrid, dan lain sebagainya. 
- Nomor port dari mysql sendiri yaitu 3306. Dalam database terdapat istilah field yang berarti kolom, record yang berarti baris serta tabel yang berarti kumpulan value yang dibangun oleh baris dan kolom, yang didalamnya berisikan atribut dari sebuah data.
- **Database NoSQL** adalah database yang tidak memiliki perintah SQL. Konsep penyimpanannya semi struktural atau tidak struktural, dan tidak harus memiliki relasi layaknya tabel-tabel MySQL.
- **DBMS** atau Database Management System adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada dalam media penyimpanan.
- **SQL** adalah bahasa yang digunakan untuk mengakses database. SQL juga dapat diartikan sebagai query yang digunakan untuk berinteraksi pada RDMS (Relational Database Management System). Contoh query SQL antara lain :
    - **DDL** atau Data Definition Language adalah kumpulan perintah SQL yang digunakan untuk membuat, mengubah dan menghapus struktur dan definisi metadata dari objek-objek Database. Contoh query DDL yaitu
        - **Create**, digunakan untuk membuat database atau tabel dari database. Penulisannya dapat seperti 
            ```
            create database favorite_movie; , atau
            create table student(
	            id int primary key not null auto_increment,
                name varchar(25),
                email varchar(25)
            );
            ```
        - **Alter**, digunakan untuk mengubah struktur dari tabel yang ada. Contohnya menambahkan kolom baru, mengubah tipe data, mengubah attribute, menghapus salah satu kolom, memodifikasi atau mengubah kolom, dan lain sebagainya. Penulisannya dapat seperti 
            ``` 
            alter table student add jurusan VARCHAR(25);


            //Maka tabel student akan mendapatkan tambahan jurusan varchar(25)
            ```
        - **Drop**, digunakan untuk menghapus Database, Table, dan lain sebagainya. Penulisannya yaitu
            ```
            drop table student;

            //Maka tabel student akan terhapus
            ```

    - **DML** atau Data Manipulation Language adalah kumpulan perintah SQL yang berfokus pada data. Contoh query DML yaitu
        - **Insert**, digunakan untuk menambahkan data pada tabel yang ada. Contoh penulisannya 
            ```
            insert into student values 
            (1, "Dea", "Dea@gmail.com", "Teknik Elektro"),
            (2, "Fala", "Fala@gmail.com", "Teknik Informatika"),
            (3, "Diana", "Diana@gmail.com", "Sastra Mesin");

            //Maka data tersebut akan tertulis di tabel student
            ```
        - **Update**, digunakan untuk mengedit isi pada data. Contoh penulisannya 
            ```
            update student set jurusan = "Sastra Informatika" where id = 1;

            //Maka data dengan id 1 pada kolom jurusan akan berubah yang sebelumnya Teknik Elektro menjadi Sastra Informatika.
            ```
        - **Select**, digunakan untuk menampilkan suatu data. Contoh penulisannya 
            ```
            select * from student;

            //Maka data pada tabel student akan tampil
            ```
        - **Select Alias (as)**, digunakan untuk menggunakan mengubah nama kolom agar output kolomnya sesuai dengan yang kita inginkan. Contoh penulisannya
            ```
            select * name as nama_mahasiswa from student; 

            //Maka nama kolom name akan berubah menjadi nama mahasiswa
            ```
        - **Select Where**, digunakan untuk mencari data dengan kondisi tertentu dengan command WHERE. Contoh penulisannya 
            ```
            select * from student where id = 3;

            //Maka akan tampil data student dengan id 3
            ```
            Selain itu terdapat **select where like** penulisannya
            ```
            select * from student where email like "%gmail.com"

            //Maka akan menampilkan data dengan bagian belakang atau pada email yang terdapat tulisan gmail.com

            select * from student where name like "Fa%"

            //Maka akan menampilkan data dengan bagian depan atau pada nama yang mempunyai awalan Fa
            ```
        - **Select Order By**, ORDER BY dengan menggunakan 2 kondisi yaitu ASC dan DESC. Ascending berarti menurutkan data dari yang terkecil ke terbesar. Sedangkan descending berarti mengurutkan data dari yang terbesar ke terkecil. Contoh penulisannya 
            ```
            select * from student order by id DESC;

            //Maka akan tampil data dengan urutan id terbesar ke terkecil.
            ```
        - **Select limit**, digunakan untuk membatasi berapa query yang akan dimunculkan dengan urutan dari atas. Contoh penulisannya
            ```
            select * from student limit 2;

            //Maka akan menampilkan 2 data student dari urutan atas yaitu data dea dan fala.
            ```
        - **Delete**, digunakan untuk menghapus data dalam tabel yang menjadi target. Contoh penulisannya 
            ```
            delete from student where id = 2;

            // Maka data di tabel student yang memiliki id 2 akan terhapus
            ```

- **Tipe Data** pada mysql antara lain 
    - **Number**, adalah tipe data yang berisi kumpulan karakter angka. Contoh tipe data number
        - **Int** yaitu tipe data untuk angka bulat contohnya : 1, 22, 99.
        - **float** yaitu tipe data untuk angka menggunakan koma.
        - **Decimal** yaitu tipe data angka pecahan (desimal), dimana jumlah angka pecahan (angka di belakang koma) sudah di tentukan dari awal.
    - **String** adalah tipe data berupa kumpulan karakter termasuk karakter simbol. Contoh tipe data string
        - **Char** yaitu tipe data string dengan fixed length dan memori sesuai panjang yang didefinisikan.
        - **Varchar** yaitu tipe data string dengan penyimpanan karakter yang fleksibel max 255.
        - **Text** yaitu tipe data string dengan penyimpanan yang lebih panjang dari varchar .
        - **Enum** yaitu tipe data yang khusus untuk kolom dimana nilai datanya sudah kita tentukan sebelumnya. 
    - **Boolean** adalah tipe data yang hanya menyimpan 2 tipe data yaitu TRUE dan FALSE, dan dapat di convert menjadi int dengan representasi TRUE = 1, dan FALSE = 0.
    - **Date time** adalah tipe data untuk menyimpan tanggal dan waktu. Contoh tipe data date time 
        - **Date** yaitu tipe data untuk menyimpan tanggal.
        - **Datetime** yaitu tipe data untuk menyimpan tanggal dan waktu.
        - **Time** yaitu tipe data untuk menyimpan waktu.
        - **Timestamp** yaitu tipe data untuk menyimpan tanggal dan waktu dan juga UTC nya atau timezone.
    - **Tipe Data Lain**
        - **Default** yaitu tipe data untuk set default value jika tidak di assign dengan value.
        - **Null** yaitu tipe data kosong atau tipe data yang belum di assign dengan value / data.

- **Tipe Database Relationships** 
    - **One to One** adalah relasi antara baris 1 dengan 1 baris lainnya atau setiap baris data pada tabel pertama dihubungkan hanya ke satu baris data pada tabel ke dua. 
    - **One to Many** adalah relasi antara baris 1 dengan baris lainnya lebih dari satu atau setiap baris data dari tabel pertama dapat dihubungkan ke satu baris atau lebih data pada tabel ke dua.
    - **Many to Many** adalah satu baris atau lebih data pada tabel pertama bisa dihubugkan ke satu atau lebih baris data pada tabel ke dua. Artinya ada banyak baris di tabel satu dan tabel dua yang saling berhubungan satu sama lain.


### **My SOL Lanjutan**
- **Key Pada SQL** 
    - **SuperKey** adalah kumpulan dari satu atau lebih dari satu key yang dapat digunakan untuk mengidentifikasi record secara unik dalam sebuah tabel.
    - **Candidate Key** adalah kumpulan satu atau lebih fields/columns yang dapat mengidentifikasi record secara unik dalam tabel.
    - **Primary Key** adalah kumpulan satu atau lebih fields/columns dari sebuah tabel yang secara unik mengidentifikasi sebuah record dalam tabel database. Valuenya tidak boleh berupa null ataupun duplicate value.
    - **Alternate Key** adalah key yang bisa digunakan menjadi primary key.
    - **Unique Key** adalah kumpulan dari satu atau lebih fields/columns di sebuah table database yang secara unik mengidentifikasi sebuah record dalam table database tersebut.
    - **Foreign Key** adalah field di sebuah table database yang menjadi Primary Key di table database lain.

- **Join Multiple Tables** yaitu mengambil records dari dua atau lebih table database yang memiliki relationship dan akan di sajikan dalam single result set. Join juga dapat diartikan sebagai penggabungan tabel yang dilakukan melalui kolom/key tertentu yang memiliki nilai terkait untuk mendapatkan satu set data dengan informasi lengkap. Pada join ini mirip seperti himpunan pada matematika. Contohnya 
    - **Inner Join** yaitu semua baris akan diambil dari kedua table yang akan di JOIN, selama columns cocok dengan kondisi yang sudah di tentukan. Selain itu dapat digunakan untuk menampilkan data hanya yang sesuai di kedua tabel. Contoh penulisannya 
    ```
    create database store;

    use store;

    create table category (
	    id int primary key not null auto_increment,
	    name VARCHAR(25)
    );

    create table product (
	    id int primary key not null auto_increment,
	    name VARCHAR(50),
	    price int,
	    category_id int,
	    FOREIGN KEY (category_id) REFERENCES category(id)
    );

    insert into category (name) VALUES
    ("food"), 
    ("baverage"), 
    ("ala carte"),
    ("dessert");

    select * from category;

    insert into product (name, price, category_id) VALUES
    ("nasi goreng", 20000, 1), 
    ("nasi gila", 25000, 1), 
    ("kwetiaw", 20000, 1),
    ("es teh", 5000, 2),
    ("air mineral", 0, 2),
    ("kerupuk", 5000, 3),
    ("gorengan", 10000, 3),
    ("sprit", 40000, 3),
    ("es doger", 20000, 3),
    ("es teh anget", 20000);

    select * from product;

    select product.id, product.name as product, product.price, category.name as category
    from product inner join category
    on product.category_id = category.id;

    //Maka akan tampil data id, name product, harga, serta name category.
    ```
    - **Left Join** yaitu menampilkan semua data sebelah kiri dari tabel yang di joinkan dan menampilkan data sebelah kanan yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis. Contoh penulisannya
    ```
    select product.id, product.name as product, product.price, category.name as category
    from product left join category
    on product.category_id = category.id;

    //Maka akan tampil data id, name product, harga, serta name category.
    ```
    - **Right Join** yaitu menampilkan semua data sebelah kanan dari tabel yang di joinkan dan menampilkan data sebelah kiri yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis. Contoh penulisannya
    ```
    select product.id, product.name, product.price, category.name 
    from product right join category
    on product.category_id = category.id;

    //Maka akan tampil data id, name product, harga, serta name category. Dan juga tampil category.name dessert dengan id name product serta harga nilai null.
    ```
- **Aggregate Functions** yaitu mengambil satu nilai setelah melakukan perhitungan pada sekumpulan nilai.
    - **MAX** yaitu fungsi mengembalikan nilai terbesar dari kolom yang dipilih. Contoh penulisannya ``select max(price) as max_price from product;``
    - **MIN** yaitu fungsi mengembalikan nilai terkecil dari kolom yang dipilih. Contoh penulisannya ``select min(price) as min_price from product;``
    - **SUM** yaitu fungsi mengembalikan jumlah total kolom numerik. Contoh penulisannya ``select sum(price) as total_price from product;``
    - **COUNT** yaitu fungsi mengembalikan jumlah baris yang cocok dengan kriteria yang ditentukan. Contoh penulisannya ``select count(category_id) from product group by category_id;``
    - **AVG** yaitu fungsi mengembalikan nilai rata-rata kolom numerik. Contoh penulisannya ``select avg(price) as rata_price from product;``
- **Group By** digunakan untuk mengelompokkan suatu data.
- **On** berarti dibagian mana data tersebut berada.
- **Where** untuk mengambil data dengan menuju ke kolomnya langsung, tidak dapat mengakses alias (as), serta tidak dapat mengakses aggregate.
- **Having** mirip seperti where tetapi bisa digunakan untuk mengakses alias(as), dapat digunakan pada aggregate, mengambil data dengan menuju ke kolom nama alias atau nama baru. 
