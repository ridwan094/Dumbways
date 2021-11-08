# Buat docker images
## Membuat docker images untuk frontend
<br>

**1. Login ke server frontend.**<br>
**2. Download images node js, dengan menjalankan perintah `docker pull node:14.18.1-alpine`**<br>
![Gambar 1 create-docker](screenshot/gambar1.png) <br><br>
**3. Clone app frontend, `git clone https://github.com/sgnd/dumbplay-frontend.git`**<br>
**4. Masuk ke dalam folder dumbplay-frontend**<br>
**5. Buat docker file `sudo nano Dockerfile`**<br>
![Gambar 2 create-docker](screenshot/gambar2.png) <br><br>
**6. Simpan.**<br>
**7. Buat docker image frontend app, `docker build -t nama-file:tag`**
![Gambar 3 create-docker](screenshot/gambar3.png) <br><br>
**8. Buat container dari image frontend, `docker container create --name nama-container -p 3131:3000 nama-images:tag`**<br>
![Gambar 11 create-docker](screenshot/gambar11.png) <br><br>
**9. Jalankan container `docker run nama-container`**<br>
**10. Push image ke repository docker hub**<br>
![Gambar 4 create-docker](screenshot/gambar4.png) <br><br>
**11. Push repository di akun docker hub.**<br>
![Gambar 5 create-docker](screenshot/gambar5.png) <br>
![Gambar 12 create-docker](screenshot/gambar12.png) <br>
