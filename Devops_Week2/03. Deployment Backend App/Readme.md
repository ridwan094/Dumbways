# Deployment Backend App
**1. Masuk ke dalam server backend, lalu clone backend apps** [https://github.com/sgnd/dumbplay-backend](https://github.com/sgnd/dumbplay-backend).<br>
![Gambar 1 deploy-backend](screenshot/gambar1.png)<br><br>
**2. Buka Readme file di dalam folder backend.**<br>
![Gambar 2 deploy-backend](screenshot/gambar2.png)<br><br>
**3. Kemudian jalankan requirementnya.**<br>
* Install nodejs
* Copy .env-copy .env
* Import database dengan sequelize
<br>

![Gambar 3 deploy-backend](screenshot/gambar3.png)<br>
![Gambar 4 deploy-backend](screenshot/gambar4.png)<br>
**Edit Config.json file sesuaikan database username, password, nama database dan host addressnya.**<br>
![Gambar 5 deploy-backend](screenshot/gambar5.png)<br><br>

**4. lakukan secure copy untuk database dumbplay.sql dari server backend ke dalam server database. dengan perintah `scp -r dumbplay.sql host@ip:<tujuan>`**<br>
![Gambar 6 deploy-backend](screenshot/gambar6.png)<br>
![Gambar 7 deploy-backend](screenshot/gambar7.png)<br><br>

## Import Database dengan Sequelize
**1. Install sequelize-cli dnegan menjalankan perintah `npm install --save-dev sequelize-cli -g`**<br>
![Gambar 8 deploy-backend](screenshot/gambar8.png)<br><br>
**2. Kemudian install sequelize `npm install --save sequelize`**<br>
**3. Install mysql2 `npm install mysql2 -g`**<br>
**4. Migrate database, dengan menjalankan perintah `sequelize db:migrate` atau `node_modules/.bin/sequelize db:migrate`**<br>
![Gambar 9 deploy-backend](screenshot/gambar9.png)<br><br>
**5. Run backend apps dengan pm2 `pm2 start ecosystem.config.json`**<br>
![Gambar 10 deploy-backend](screenshot/gambar10.png)<br><br>
![Gambar 11 deploy-backend](screenshot/gambar11.png)<br><br>