# AWS - SSL Configuration
### Generate API Key
**1. Login dan masuk ke dashboard cloudflare**<br>
**2. Pada bagian account klik my profile**<br>
**3. Masuk ke halaman API tokens.**<br>
![Gambar 1 SSL Config](screenshot/gambar1.png) <br><br>
**4. Pada bagian Global API Key, klik view, lalu akan muncul kotak dialog.**<br>
![Gambar 2 SSL Config](screenshot/gambar2.png) <br><br>
**5. Masukkan password untuk mendapatkan key.**<br>
**6. Copy dan simpan api key**<br>
![Gambar 3 SSL Config](screenshot/gambar3.png) <br><br>
**7. Login ke dalam server**<br>
**8. Buat folder kemudian di dalamnya buat file untuk menyimpan api key cloudflare.**<br>
![Gambar 4 SSL Config](screenshot/gambar4.png) <br><br>
**9. Di dalam file masukkan email dan juga api key, lalu simpan**<br>
![Gambar 5 SSL Config](screenshot/gambar5.png) <br><br>
**10. Setelah itu ubah hak akses folder ke 700 dan file 400.**<br>
![Gambar 4 SSL Config](screenshot/gambar4.png) <br><br>

## Install Certbot and the Cloudflare DNS authenticator plugin
**1. Update snapd `sudo snap install core; sudo refresh core`.**<br>
**2. Install certbot `sudo snap install --classic certbot`.**<br>
**3. Link certbot dari /snap/bin/certbot ke /usr/bin/certbot `sudo ln -s /snap/bin/certbot /usr/bin/certbot`**
**4. Generate SSL `sudo certbot`.**<br>
**5. masukkan email address**<br>
**6. kemudian Agree Terms of Service.**<br>
**7. pilih nama website yang akan dipakaikan HTTPS**<br>
**8. Tunggu request certificate untuk website berhasil generate.**
![Gambar 6 SSL Config](screenshot/gambar6.png) <br><br>
**9. Masuk ke folder config nginx untuk website `/etc/nginx/dumbplay`.**<br>
**10. Ketikkan perintah `cat dumbplay-config` untuk melihat perubahannya.**<br>
**11. kemudian test config `sudo nginx -t`**<br>
![Gambar 7 SSL Config](screenshot/gambar7.png) <br><br>
**12. Reload nginx `sudo systemctl reload nginx`**<br>
**13. Buka browser dan arahkan ke alamat url `rdwn.onlinecamp.id`**<br>
![Gambar 8 SSL Config](screenshot/gambar8.png) <br><br>