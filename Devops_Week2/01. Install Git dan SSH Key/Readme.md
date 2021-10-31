# Install Git dan SSH Key
## Fork repository backend apps
<br>

**1. Login ke akun Github.**<br>
**2. Buka repository backend apps yang akan di fork, `https://github.com/sgnd/dumbplay-backend`.**<br>
**3. Pada halaman repository backend apps,klik fork,maka akan otomatis akan masuk ke repository akun github kita.**<br>
![Gambar 1 git](screenshot/gambar1.png) <br><br>

## Buat SSH Key untuk Git
<br>

**1. Buat sebuah server/instance di AWS.**<br>
![Gambar 2 git](screenshot/gambar2.png) <br>
![Gambar 3 git](screenshot/gambar3.png) <br>
![Gambar 4 git](screenshot/gambar4.png) <br>
![Gambar 5 git](screenshot/gambar5.png) <br>
![Gambar 6 git](screenshot/gambar6.png) <br>
![Gambar 7 git](screenshot/gambar7.png) <br>
![Gambar 8 git](screenshot/gambar8.png) <br>
![Gambar 9 git](screenshot/gambar9.png) <br>
![Gambar 10 git](screenshot/gambar10.png) <br>
![Gambar 11 git](screenshot/gambar11.png) <br>
![Gambar 12 git](screenshot/gambar12.png) <br>
![Gambar 13 git](screenshot/gambar13.png) <br>
![Gambar 14 git](screenshot/gambar14.png) <br>
![Gambar 15 git](screenshot/gambar15.png) <br>
![Gambar 16 git](screenshot/gambar16.png) <br>
![Gambar 17 git](screenshot/gambar17.png) <br>
![Gambar 18 git](screenshot/gambar18.png) <br><br>

**2. Masuk kedalam server yang sudah dibuat sebelumnya, yaitu server backend dengan key**<br>
![Gambar 19 git](screenshot/gambar19.png) <br><br>
**3. melakukan update dan upgrade dengan perintah `sudo apt update & sudo apt upgrade`**<br>
![Gambar 20 git](screenshot/gambar20.png) <br>
![Gambar 21 git](screenshot/gambar21.png) <br><br>
**4. Install git dengan perintah `sudo apt install git`.**<br>
![Gambar 22 git](screenshot/gambar22.png) <br><br>
**5. Install SSH dengan perintah `sudo apt install openssh-server`**<br>
![Gambar 23 git](screenshot/gambar23.png) <br><br>
**6. Tambahkan user ke dalam config git.**<br>
**7. Jalankan perintah `git config --global user.name <username>`. kemudian jalankan perintah `git config --global user.email <email>`.**<br>
![Gambar 24 git](screenshot/gambar24.png) <br><br>
**8. Buat folder untuk menyimpan ssh key.**<br>
![Gambar 25 git](screenshot/gambar25.png) <br><br>
**9. Generate ssh key di dalam foder yang telah dibuat. lalu Jalankan perintah `ssh-keygen -t rsa -b 4096 -C "email"`.**<br>
**10. Masukkan nama file kemudian passphrase.**<br>
![Gambar 26 git](screenshot/gambar26.png) <br><br>
**11. Akan menghasilkan 2 key dan yang satunya berekstensi .pub (public).**<br>
![Gambar 27 git](screenshot/gambar27.png) <br><br>
**12. Tambahkan ssh key yang telah di generate tadi, dan ketikkan perintah `eval "$(ssh-agent -s)"` kemudian `ssh-add .git-ssh/git-ssh`.**<br>
![Gambar 28 git](screenshot/gambar28.png) <br><br>
**13. Selanjutnya masuk ke github account.**<br>
**14. Masuk ke settings, pada bagian Account settings buka SSH dan GPG Keys.**<br>
**15. Buat SSH Key, beri title kemudian copy-paste generated SSH key yang berekstensi `.pub` tadi. simpan kemudian masukkan password akun github.**<br>
![Gambar 29 git](screenshot/gambar29.png) <br><br>
**16. Kemudian test koneksi ke github, dengan perintah `ssh -T git@github.com`**<br>
![Gambar 30 git](screenshot/gambar30.png) <br><br>

## Git pull, push, dan merge pada server
**1. Git clone repository backend apps `git@github.com:ridwan094/git-dumbways.git`**<br>
**2. Buat sebuah branch `git branch development`**<br>
**3. Kemudian arahkan ke branch development `git checkout development`**<br>
![Gambar 31 git](screenshot/gambar31.png) <br><br>
**4. Ubah backend apps misal menambah atau menghapus file.**<br>
**5. Kemudian `git add .`**<br>
![Gambar 32 git](screenshot/gambar32.png) <br><br>
**6. Kemudian commit perubahan, jalankan perintah `git commit -m "perubahangit"`**<br>
**7. Kemudian push `git push origin development`**<br>
**8. Update branch dengan pull `git pull origin development`**<br>
**9. Merge branch git merge development production.**