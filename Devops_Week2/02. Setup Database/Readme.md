# Setup Databases
## Buat instance baru untuk backend
**1. Login ke AWS Console, pilih EC2**<br>
**2. masuk ke instance, lalu Lauch new instance**<br>
**3. Buat instance baru untuk database**<br>
![Gambar 1 db](screenshot/gambar1.png) <br>
![Gambar 2 db](screenshot/gambar2.png) <br>
![Gambar 3 db](screenshot/gambar3.png) <br>
![Gambar 4 db](screenshot/gambar4.png) <br>
![Gambar 5 db](screenshot/gambar5.png) <br>
![Gambar 6 db](screenshot/gambar6.png) <br>
![Gambar 7 db](screenshot/gambar7.png) <br>
![Gambar 8 db](screenshot/gambar8.png) <br>
![Gambar 9 db](screenshot/gambar9.png) <br>
![Gambar 10 db](screenshot/gambar10.png) <br>
![Gambar 11 db](screenshot/gambar11.png) <br>
![Gambar 12 db](screenshot/gambar12.png) <br>
![Gambar 13 db](screenshot/gambar13.png) <br><br>

## Install database
**1. login ke dalam server database**<br>
**2. jalankan perintah `sudo apt update & sudo apt upgrade`.**<br>
![Gambar 14 db](screenshot/gambar14.png) <br>
![Gambar 15 db](screenshot/gambar15.png) <br><br>
**3. Install mysql dengan menjalankan perintah `sudo apt install mysql-server`.**<br>
![Gambar 16 db](screenshot/gambar16.png) <br><br>
**4. Jalankan perintah `sudo systemctl status mysql` apakah sudah running.**<br>
![Gambar 17 db](screenshot/gambar17.png) <br><br>
**4. Konfigurasi keamanan database dengan perintah `sudo mysql_secure_installation`**<br>
**5. Input password dan pertanyaan keamanan.**<br>
![Gambar 18 db](screenshot/gambar18.png) <br><br>

## Database dapat terkoneksi dengan klien
**1. Buka folder `/etc/mysql/mysql.conf.d`, lalu edit file `mysqld.cnf`**<br>
![Gambar 19 db](screenshot/gambar19.png) <br>
![Gambar 20 db](screenshot/gambar20.png) <br><br>
**2. Ubah ip address `bind address` ke ip address yang dituju/yang diboolehkan, disini saya mengubah bin-address ke `0.0.0.0` publik**<br>
![Gambar 21 db](screenshot/gambar21.png) <br>
*Note* **:** **mysqlx-bind-address tidak perlu ditambahkan jika memang tidak ada, jika ditambahkan manual akan menyebabkan crash pada mysql service**<br>

**3. save**<br>
**4. Restart mysql service dengan perintah `sudo service mysql restart`.**<br>
![Gambar 22 db](screenshot/gambar22.png) <br><br>
**5. Selanjutnya adalah grant akses host.**<br>
**6. Login ke mysql server `sudo mysql -u root -p`**<br>
![Gambar 23 db](screenshot/gambar23.png) <br><br>
**7. Ketikkan perintah/commend berikut `GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'password-user';`**<br>
![Gambar 24 db](screenshot/gambar24.png) <br>
![Gambar 25 db](screenshot/gambar25.png) <br><br>