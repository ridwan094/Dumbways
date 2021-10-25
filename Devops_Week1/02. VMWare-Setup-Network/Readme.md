# VMware-Setup-Network
## Change Network from NAT to Bridge
**1. Buat Virtual Machine atau jika sudah ada buka virtual machine**<br>
![Gambar 1 setup](screenshot/gambar1.png) <br><br>
**2. Masuk ke halaman Settings, Pilih Network, diberitahukan ada sebuah adapter yang terkoneksi ke jaringan NAT, pilih attached to dan ganti ke jaringan Bridge Adapter, selanjutnya pilih ok**<br>
![Gambar 2 vbox](screenshot/gambar2.png) <br><br>
**3. Masuk dan jalankan ubuntu server, tunggu hingga muncul halaman awal ubuntu server dan masukkan username dan juga password**
![Gambar 3 vbox](screenshot/gambar3.png) <br><br>
**4. jalankan perintah `sudo apt-get update && sudo apt-get upgrade` untuk mengecek update terbaru dan juga upgrade repositori terbaru agar aman digunakan**<br>
**5. disini saya membuat sebuah user baru dengan perintah `sudo adduser <username>` untuk membuat user baru dan menentukan password yang digunakan**<br>
![Gambar 4 vbox](screenshot/gambar4.png) <br><br>
**6. ketikan perintah `usermod -aG sudo <username>` untuk menambahkan user ke group sudo, atau dengan perintah `sudo nano /etc/sudoers` dan ketik `<username> ALL=(ALL:ALL) ALL` di dalam file, lalu tekan `CTRL+X` dan ketikkan y lalu ENTER, otomatis group sudo sudah ditambahkan ke dalam user baru**<br>
![Gambar 6 vbox](screenshot/gambar6.png) <br><br>
**7. Uji akses sudo dengan perintah `su - <username>`**<br>
**8. Masukkan user dan password baru yang telah sebelumnya dibuat**<br>
![Gambar 5 vbox](screenshot/gambar5.png) <br><br>
**9. ping ke alamat google dengan perintah `ping www.google.com`**<br>
![Gambar 13 vbox](screenshot/gambar13.png) <br><br>
**10. jalankan perintah `sudo apt-get install net-tools` dan ketikkan perintah `ifconfig` yang akan digunakan untuk melihat interface dan IP Address secara terperinci**<br>
**11. ketikkan perintah `sudo nano /etc/netplan/00-installer-config.yaml` untuk mengkonfigurasi alamat ip dan menentukkan IP Address yang ingin dirubah dan dijadikan static**<br>
![Gambar 7 vbox](screenshot/gambar7.png) <br><br>
**12. Masuk ke dalam file `/etc/netplan` dan ubah/setting alamat IP Address yang ingin digunakan, selanjutnya tekan `CTRL+X` dan ketik y, lalu tekan ENTER untuk menyimpan alamat IP yang sudah diubah**<br>
![Gambar 8 vbox](screenshot/gambar8.png) <br><br>
**13. ketikkan perintah `sudo netplan apply` untuk mengkonfigurasi alamat yang telah diubah sebelumnya dan ketikkan perintah `reboot` untuk merestart system**<br>
![Gambar 9 vbox](screenshot/gambar9.png) <br><br>
**14. login kembali dan ketikkan perintah `ifconfig` untuk melihat alamat IP Address yang telah diubah**<br>
![Gambar 10 vbox](screenshot/gambar10.png) <br><br>
**15. tes koneksi dengan perintah ping, untuk mengetahui apakah IP tidak bermasalah dan bisa digunakan**
![Gambar 11 vbox](screenshot/gambar11.png) <br>
![Gambar 12 vbox](screenshot/gambar12.png) <br><br>