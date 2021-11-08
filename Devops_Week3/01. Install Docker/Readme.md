# Install Docker

## Install docker di server frontend dan backend <br>
**1. Login ke server frontend dan backend.**<br>
**2. Update dan Upgrade sistem.**<br>
![Gambar 1 docker](screenshot/gambar1.png) <br><br>
**3. perbaharui apt untuk memungkinkan apt menggunakan repositori melalui Https**<br>
![Gambar 2 docker](screenshot/gambar2.png) <br><br>
**4. Tambahkan GPG key docker. `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`**<br>
![Gambar 3 docker](screenshot/gambar3.png) <br><br>
**5. Tambahkan repository docker, bisa menggunakan yang stable atau nightly channel.`echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`** <br>
![Gambar 4 docker](screenshot/gambar4.png) <br><br>
**6. jalankan update sistem `sudo apt update`**<br>
**7. Install docker.`sudo apt-get install docker-ce docker-ce-cli containerd.io`**
![Gambar 5 docker](screenshot/gambar5.png) <br><br>
**8. Cek versi dari docker, dan pastikan sudah berjalan.**<br>
![Gambar 6 docker](screenshot/gambar6.png) <br /><br />
**9. Untuk server backend, lakukan hal yang sama sesuai arahan dari step 1-7.**<br>
![Gambar 7 docker](screenshot/gambar7.png) <br /><br />

## Login ke docker hub
**1. masuk ke dalam website.** [hub docker](https://hub.docker.com/)<br>
**2. Buat akun docker di `hub.docker.com`**<br>
![Gambar 8 docker](screenshot/gambar8.png) <br /><br />
**3. Buka terminal atau masuk ke server, login docker menggunakan akun hub docker yang telah dibuat sebelumnya.**<br>
**4. jalankan perintah `docker login`**<br>
**5. Masukkan username dan password docker hub**
![Gambar 9 docker](screenshot/gambar9.png) <br /><br />