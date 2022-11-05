# **Writing Minggu ke-2**

## **Back-End Developement**

### **My SOL Basic**
- **Database** tempat untuk menyimpan data agar suatu data dapat terstruktur dengan baik dan saling berrelasi. Informasi tersebut akan diolah, kemudian data yang dihasilkan dapat digunakan di dalam sebuah sistem. Contoh database SQL yaitu oracle, mariadb, posgresql, IBM DB2. 
- **My SQL Server** yaitu ketika membuat database terdapat server yang berjalan atau terdapat database yang berjalan atau beroperasi. 
- MySQL bersifat open source, comfortable untuk banyak platfom, serta multi user. 
- Untuk mengakses server dapat menggunakan workbench, dbeaver, tableplus, phpmy admin, datagrid, dan lain sebagainya. 
- Nomor port dari mysql sendiri yaitu 3306. Dalam database terdapat istilah field yang berarti kolom, record yang berarti baris serta ta
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
