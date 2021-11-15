# Connect multiple server to prometheus
## Install Node Exporter pada server yang akan di monitoring <br>
**1. Login server app dan backend**<br>
**2. Install node exporter**<br>
![Gambar 1 multiple](screenshot/gambar1.png) <br>
![Gambar 2 multiple](screenshot/gambar2.png) <br>
![Gambar 3 multiple](screenshot/gambar3.png) <br>
![Gambar 4 multiple](screenshot/gambar4.png) <br>
![Gambar 5 multiple](screenshot/gambar5.png) <br><br>

**3. Login ke prometheus server yang telah dibuat**<br>
**4. Tambahkan ip address server yang akan di monitoring**<br>
**5. Edit file prometheus.yml `sudo nano /etc/prometheus/prometheus.yml` tambahkan ip address server di bagian target dengan port 9100**<br>
![Gambar 6 multiple](screenshot/gambar6.png) <br><br>

**6. Save**<br>
**7. Restart prometheus service `sudo systemctl restart prometheus.service`**<br>
**8. Masuk ke server prometheus di port 9090**<br>
**9. Pada bagian graph cari metric yang ingin ditampilkan**<br>
**10. Execute**<br>
![Gambar 7 multiple](screenshot/gambar7.png) <br><br>

## Menampilkan cpu dan memory process menggunakan grafana <br>
**1. Login ke server `monitoring.joko.onlinecamp.id` dan login ke grafana**<br>
**2. Pada bagian configuration tambahkan data sources dari prometheus**<br>
![Gambar 8 multiple](screenshot/gambar8.png) <br><br>

**3. Pada halaman setting grafana prometheus masukkan URL prometheus**<br>
![Gambar 9 multiple](screenshot/gambar9.png) <br><br>

**4. Save & test. pastikan datasource working**<br>
![Gambar 10 multiple](screenshot/gambar10.png) <br><br>

## Buat panel unruk networking <br>
**1. Add new panel kemudian edit**<br>
**2. Pada bagian Query, cari metric `node_network_receive_bytes_total` di kolom `Metrics Browser`**<br>
**3. Tambahkan function rate() `rate(node_network_receive_bytes_total[5m])`**<br>
**4. Add query baru, cari metric `node_network_transmit_bytes_total` di kolom `Metrics Browser`**<br>
**5. Tambahkan function rate() `rate(node_network_transmit_bytes_total[5m])`**<br>
**6. Kemudian pilih pada bagian panel option beri nama pada panel**<br>
**7. Klik Apply**<br>
![Gambar 11 multiple](screenshot/gambar11.png) <br>
![Gambar 12 multiple](screenshot/gambar12.png) <br><br>

## Buat panel untuk cpu usage <br>
**1. Add new panel**<br>
**2. Pada bagian Query, copy rumus berikut untuk menampilkan CPU usage**<br>
```
(1 - avg(irate(node_cpu_seconds_total{mode="idle"}[10m])) by (instance)) * 100
```
<br>

**3. Setelah itu graph akan terupdate jika berhasil**<br>
**4. Beri nama pada panel kemudian simpan.**<br>
![Gambar 13 multiple](screenshot/gambar13.png) <br><br>

## Buat panel untuk memory usage <br>
**1. Add new panel**<br>
**2. Pada bagian Query, cari dan set Metric Browser `node_memory_MemFree_bytes`**<br>
**3. Di bagian panel cari standard options. pilih unit `bytes(SI)`**<br>
**4. Pilih graph type `Gauge`**<br>
![Gambar 14 multiple](screenshot/gambar14.png) <br><br>

## Buat panel untuk storage <br>
**1. Add new panel**<br>
**2. Pada bagian Query, cari dan set Metric Browser untuk menampilkan available storage `node_filesystem_avail_bytes{mountpoint="/",fstype!="rootfs"}`**<br>
**3. Tambahkan query lagi untuk menampilkan size storage `node_filesystem_size_bytes{mountpoint="/",fstype!="rootfs"}`**<br>
**4. Di bagian panel cari standard options. pilih unit `bytes(SI)`**<br>
**5. Pilih graph type `Stat`**<br>
![Gambar 15 multiple](screenshot/gambar15.png) <br><br>