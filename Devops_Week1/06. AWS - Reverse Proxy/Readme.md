# AWS - Reverse Proxy
## Requirements
* Update and upgrade the operating system.
* Install Webserver for reverse proxy.
* Create revere proxy from the application with port 3000 to port 80<br><br>

**1. Login ke server reverse proxy**<br>
**2. Update dan upgrade sistem**<br>
![Gambar 1 Reverse Proxy](screenshot/gambar1.png) <br><br>
**3. Install Nginx dengan perintah `sudo apt install nginx`**<br>
![Gambar 2 Reverse Proxy](screenshot/gambar2.png) <br><br>
**4. Masuk ke dalam folder nginx dengan perintah `sudo nano /etc/nginx`**<br>
![Gambar 3 Reverse Proxy](screenshot/gambar3.png) <br><br>
**5. Buat folder `dumbplay` untuk menyimpan file konfigurasi**<br>
![Gambar 4 Reverse Proxy](screenshot/gambar4.png) <br><br>
**6. Masuk ke dalam folder dumbplay**<br>
**7. Buat file konfigurasi dengan perintah `nano dumbplay-config` kemudian buat aplikasi mengarah ke port 80.**<br>
![Gambar 5 Reverse Proxy](screenshot/gambar5.png) <br><br>
**8. Kemudian include konfigurasi dumbplay tadi ke `nginx.conf`, save perubahan**<br>
![Gambar 6 Reverse Proxy](screenshot/gambar6.png) <br><br>
**9. Test konfigurasi file, dengan perintah `sudo nginx -t`, untuk mengecek syntas konfigurasi apakah berjalan dengan baik.**<br>
![Gambar 7 Reverse Proxy](screenshot/gambar7.png) <br><br>
**10. restart nginx dengan perintah `sudo systemctl resstart nginx`**<br>
**11. Selanjutnya arahkan domain name ke public ip reverse-proxy-server, untuk dapat berjalan di port 80, dan uncheck proxy status.**<br>
![Gambar 8 Reverse Proxy](screenshot/gambar7.png) <br><br>
**12. Buka browser kemudian arahkan url ke `rdwn.onlinecamp.id` untuk mengunjungi website.**<br>
![Gambar 9 Reverse Proxy](screenshot/gambar9.png) <br><br>