# Create and Setup Server
## Requirements:
* Create a server with ubuntu 20.x OS.
* Create two servers for reverse proxy and application with AWS.
* Server for revere proxy need a public IP Address.
* Server for the application only has a private IP Address.
* Setup security group and open ports 22,80,and 443 for reverse proxy.
* Setup security group and open all traffic for the application.

## Server Untuk Reverse Proxy
**1. Login ke dalam AWS Educate**<br>
![Gambar 1 AWS](screenshot/gambar1.png) <br><br>
**2. Pilih AWS Console, lalu pergi ke alamat link yang dituju**<br>
![Gambar 2 AWS](screenshot/gambar2.png) <br><br>
**3. Masuk ke halaman dashboard atau AWS Management console.**<br>
![Gambar 3 AWS](screenshot/gambar3.png) <br><br>
**4. Klik Launch a virtual machine**<br>
**5. Pada step 1 Choose an Amazon Machine Image(AMI), pilih Ubuntu Server 20.x**
![Gambar 4 AWS](screenshot/gambar4.png) <br><br>
**6. Step 2 pillih instance type sesuai kebutuhan, lalu klik next**<br>
![Gambar 5 AWS](screenshot/gambar5.png) <br><br>
**7. Step 3 Configure instance pilih Auto-assign public ip dan jadikan disable, lalu klik next**<br>
![Gambar 6 AWS](screenshot/gambar6.png) <br><br>
**8. Step 4 Add Storage, atur storage yang dibutuhkan, selanjutnya klik next**<br>
![Gambar 7 AWS](screenshot/gambar7.png) <br><br>
**9.Step 5 Tags biarkan saja default.**<br>
![Gambar 8 AWS](screenshot/gambar8.png) <br><br>
**10. Step 6 Setup Security Group. Create a new security group dan tentukan type yang diinginkan, disini setting untuk SSH, HTTP, dan HTTPS, selanjutnya klik reviee**<br>
![Gambar 9 AWS](screenshot/gambar9.png) <br><br>
**11. Step 7 Review Instance Lauch, biarkan saja, dan pilih Launch**
![Gambar 10 AWS](screenshot/gambar10.png) <br><br>
**11. Download key pair untuk digunakan login ke server nanti, lalu pilih Launch Instance.**<br>
![Gambar 11 AWS](screenshot/gambar11.png) <br><br>

### Allocate Elastic IP
**1. Masuk ke Elastic IPs yang terletak pada sidebar console bagian network & security.**<br>
![Gambar 12 AWS](screenshot/gambar12.png) <br><br>
**2. Kemudian Allocated Elastic IP address, AWS akan mengalokasikan sebuah IP yang dapat digunakan.**<br>
![Gambar 13 AWS](screenshot/gambar13.png) <br><br>
**3. Beri nama kemudian associate elastic ip address dengan server yang dituju**<br>
![Gambar 14 AWS](screenshot/gambar14.png) <br>
![Gambar 15 AWS](screenshot/gambar15.png) <br><br>
**4. Masuk ke instance kemudian refresh instances.**<br>
![Gambar 16 AWS](screenshot/gambar16.png) <br><br>
**5. Buka terminal, masuk ke direktori Documents dengan perintah `cd Documents`,  lalu buat directory baru dengan perintah `sudo mkdir /DumbWays/aws`**
![Gambar 17 AWS](screenshot/gambar17.png) <br><br>
**5. masuk ke dalam direktori aws dan lakukan perintah `chmod 400` untuk mengubah hak akses pada key pair `dumbways.pem`.**<br>
**6. Server bisa diakses melalui SSH menggunakan ip public.**<br>
![Gambar 18 AWS](screenshot/gambar18.png) <br>
![Gambar 19 AWS](screenshot/gambar19.png) <br><br>

## Server untuk Apps
**1. Login ke dalam AWS Console**<br>
**2. Masuk ke halaman dashboard atau AWS Management Console.**<br>
**3. Klik Launch a Virtual Machine**<br>
![Gambar 3 AWS](screenshot/gambar3.png) <br><br>
**4. Pada Step 1 Choose AMI cari ubuntu, kemudian pilih ubuntu server 20.**<br>
![Gambar 4 AWS](screenshot/gambar4.png) <br><br>
**5. Step 2 pilih instance type sesuai kebutuhan.**
![Gambar 5 AWS](screenshot/gambar5.png) <br><br>
**6. Step 3 Configure instance pilih auto-assign public ip menjadi disable.**<br>
![Gambar 6 AWS](screenshot/gambar6.png) <br><br>
**7. Step 4 Add Storage.**<br>
![Gambar 7 AWS](screenshot/gambar7.png) <br><br>
**8. Step 5 Tags biarkan default.**<br>
![Gambar 8 AWS](screenshot/gambar8.png) <br><br>
**9. Step 6 Setup security group, setting menjadi All trafic**<br>
![Gambar 20 AWS](screenshot/gambar20.png) <br>
![Gambar 21 AWS](screenshot/gambar21.png) <br><br>
**10. Gunakan key pair yang sama pada reverse proxy, lalu pilih launch instance**<br>
![Gambar 22 AWS](screenshot/gambar22.png) <br><br>
**11. Allocate Elastic IP untuk server apps.**<br>
![Gambar 23 AWS](screenshot/gambar23.png) <br>
![Gambar 24 AWS](screenshot/gambar24.png) <br><br>
**12. Akses Server**<br>
![Gambar 19 AWS](screenshot/gambar19.png) <br><br>