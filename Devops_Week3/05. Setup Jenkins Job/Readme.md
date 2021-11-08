# Setup Jenkins Job
## Requirements <br>
* Install plugin Publish Over SSH
* Instance/Server app IP address
* aws-ssh-key
* System configuration
<br><br>

## Configure System in Jenkins
**1. Install plugin `publish Over SSH`**<br>
**2. Di halaman Dashboard masuk ke Manage Jenkins**<br>
**3. Pada System Configuration pilih Configure System**<br>
**4. Cari publish over ssh**<br>
![Gambar 1 create-jobs-jenkins](screenshot/gambar1.png) <br><br>
**5. Copy paste aws key yang digunakan server**<br>
**6. Beri nama server**<br>
**7. Masukkan hostname server**<br>
**8. Input username**<br>
**9. Beri nilai 0 pada `Timeout (ms)`**<br>
![Gambar 3 create-jobs-jenkins](screenshot/gambar3.png) <br><br>
**10. Test koneksi SSH ke server**<br><br>

## Create Job <br>
**1. Login ke server jenkins.**<br>
**2. klik create a job**<br>
**3. Masukkan nama project kemudian pilih freestyle project.**<br>
![Gambar 8 create-jobs-jenkins](screenshot/gambar8.png) <br><br>
**4. Pada bagian General input deskripsi project(opsional)**<br>
**5. Di bagian Source code management pilih `Git`**<br>
**6. Masukkan repository dan branch yang digunakan.**<br>
![Gambar 2 create-jobs-jenkins](screenshot/gambar2.png) <br><br>
**7. Untuk Build trigger pilih `Github hook trigger for GITScm polling`**<br>
![Gambar 9 create-jobs-jenkins](screenshot/gambar9.png) <br><br>
**8. Pada bagin Build pilih `Send files or execute commands over SSH`**<br>
**9. Kemudian `Verbose output in console` untuk bisa melihat log buildnya**<br>
![Gambar 10 create-jobs-jenkins](screenshot/gambar10.png) <br>
![Gambar 11 create-jobs-jenkins](screenshot/gambar11.png) <br><br>
**10. Di bagian transfer set isi source file, remote directory dan exec command**<br>
![Gambar 5 create-jobs-jenkins](screenshot/gambar5.png) <br><br>
**11. Set Execution time jadi 0**<br>
**12. Setelah itu Apply dan simpan.**<br>
**13. Build manual dengan klik Build Now.**<br>
![Gambar 6 create-jobs-jenkins](screenshot/gambar6.png) <br><br>

## Setup Webhook Github
**1. Login ke akun github**<br>
**2. Masuk ke halaman settings repository**<br>
**3. Pilih Webhook**<br>
**4. Add Webhook**<br>
**5. Masukkan hostname server jenkins payload URL `http://jenkins.joko.onlinecamp.id/github-webhook/`**<br>
**6. Kemudian pilih event `just the push event`**<br>
**7. Checklist Active**<br>
**8. Simpan Add Webhook.**<br>
![Gambar 12 create-jobs-jenkins](screenshot/gambar12.png) <br><br>

## Test Webhook <br>
**1. Lakukan perubahan pada repository**<br>
**2. Kemudian push**<br>
![Gambar 13 create-jobs-jenkins](screenshot/gambar13.png) <br><br>
**3. Tunggu beberapa saat hingga proses build jenkins selesai**<br>
**4. Masuk ke jenkins untuk melihat build run atau changes-nya**<br>
![Gambar 14 create-jobs-jenkins](screenshot/gambar14.png) <br><br>