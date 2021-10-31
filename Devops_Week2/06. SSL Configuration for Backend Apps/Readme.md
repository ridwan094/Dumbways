# SSL Configuration for Backend Apps
## Arahkan frontend api.js ke backend Apps
**1. Login ke server frontend**<br>
![Gambar 1 ssl](screenshot/gambar1.png) <br><br>
**2. Masuk ke folder `frontend/config`**<br>
![Gambar 2 ssl](screenshot/gambar2.png) <br><br>
**3. Edit file api.js arahkan `baseURL:` [https://api.joko.onlinecamp.id/api/v1](https://api.joko.onlinecamp.id/api/v1)**<br>
![Gambar 3 ssl](screenshot/gambar3.png) <br>
![Gambar 4 ssl](screenshot/gambar4.png) <br><br>
**4. Restart Apps,**<br>
![Gambar 5 ssl](screenshot/gambar5.png) <br><br>

## SSL Configuration
**1. Login ke instance/server gateway.**<br>
![Gambar 6 ssl](screenshot/gambar6.png) <br><br>
**2. Update dan Upgrade Sistem.**<br>
**3. Install Certbot untuk backend.**<br>
**4. Jalankan perintah `sudo certbot certonly -d api.joko.onlinecamp.id`**<br>
![Gambar 7 ssl](screenshot/gambar7.png) <br><br>
**5. Syntax penambahan SSL dari certbot.**<br>
![Gambar 8 ssl](screenshot/gambar8.png) <br><br>
**6. Test Konfigurasi `sudo nginx -t`**<br>
**7. Restart nginx `sudo service nginx restart`**<br>
![Gambar 9 ssl](screenshot/gambar9.png) <br><br>
**8. Buka website `joko.onlinecamp.id`**<br>
**9. Buat akun atau registrasi untuk testing koneksi ke backend.**<br>
![Gambar 10 ssl](screenshot/gambar10.png) <br><br>
![Gambar 11 ssl](screenshot/gambar11.png) <br><br>