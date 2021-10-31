# Reverse Proxy for Backend Apps
**1. Login ke server gateway.**<br>
![Gambar 1 reverse](screenshot/gambar1.png) <br><br>
**2. Update dan Upgrade System.**<br>
**3. Install Nginx.**<br>
**4. Masuk ke folder /etc/nginx/dumbplay**<br>
**5. Kemudian buat file config untuk backend apps `api.joko.onlinecamp.id`**<br>
![Gambar 2 reverse](screenshot/gambar2.png) <br><br>
**6. Edit arahkan proxy_pass ke ip private server backend.**<br>
![Gambar 3 reverse](screenshot/gambar3.png) <br><br>
**7. Save.**<br>
**8. Test config file `sudo nginx -t` untuk memastikan tidak adanya error.**<br>