# Install Jenkins
## Buat AWS Instance <br>
**1. Login ke akun AWS.**<br>
**2. Buat instance baru untuk jenkins.**<br>
**3. Login ke instance**<br>
**4. Update dan upgrade sistem**<br>
**5. Install Jenkins LTS.**<br><br>

## Install Jenkins versi Debian/Ubuntu <br>
**1. Install java `sudo apt install openjdk-8-jdk`**<br>
**2. Tambahkan apt repository jenkins `wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -`**<br>
**3. Eksekusi kode berikut `sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`**<br>
![Gambar 1 jenkins](screenshot/gambar1.png) <br><br>
**4. Update Sistem**<br>
**5. Install jenkins `sudo apt install jenkins`**<br>
![Gambar 2 jenkins](screenshot/gambar2.png) <br><br>
**6. Buka browser dan arahkan ke `ip-address-server:8080`**<br>
![Gambar 3 jenkins](screenshot/gambar3.png) <br><br>

## Setup Jenkins
**1. Akses halaman jenkins di port 8080**<br>
**2. Masukkan initial admin password, bisa dilihat di `sudo cat /var/lib/jenkins/secrets/initialAdminPassword`**<br>
![Gambar 4 jenkins](screenshot/gambar4.png) <br><br>
**3. Pilih jenis instalasi plugin jenkins(pilih yang suggested plugins) dan tunggu proses instalasi plugin selesai.**<br>
![Gambar 5 jenkins](screenshot/gambar5.png) <br>
![Gambar 6 jenkins](screenshot/gambar6.png) <br><br>
**4. Create admin jenkins. save and next**<br>
![Gambar 7 jenkins](screenshot/gambar7.png) <br><br>
**5. Konfigurasi jenkins URL. Start.**<br>
![Gambar 8 jenkins](screenshot/gambar8.png) <br><br>
**6. Halaman dashboard jenkins.**<br>
![Gambar 9 jenkins](screenshot/gambar9.png) <br><br>

## Reverse domain for jenkins <br>
**1. Login akun cloudflare.**<br>
**2. Pilih akun dan domain.**<br>
**3. Masuk ke menu DNS.**<br>
**4. Reverse subdomain untuk jenkins `jenkins.joko.onlinecamp.id`**<br>
**5. save.**<br>
![Gambar 10 jenkins](screenshot/gambar10.png) <br><br>

## Setup Reverse Proxy for Jenkins <br>
**1. Login ke server gateway.**<br>
**2. Masuk ke folder nginx `/etc/nginx/`**<br>
**3. Buat konfigurasi file `jenkins.joko.onlinecamp.id`**<br>
![Gambar 11 jenkins](screenshot/gambar11.png) <br>
![Gambar 12 jenkins](screenshot/gambar12.png) <br><br>
**4. Simpan, Test `sudo nginx -t`, restart nginx `sudo service nginx restart`**<br>
**5. Buka browser dan arahkan ke `jenkins.joko.onlinecamp.id`**<br>
![Gambar 13 jenkins](screenshot/gambar13.png) <br><br>
