Database yang digunakan disini mysql dengan galeria cluster sebagai load balancernya
<br>
1. Pertama tambahkan repository galeria key untuk verifikasi packagenya <br>
![1.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM2/Images/1.2.PNG)<br><br>

2. Masukan galeria pada repository apt pada <b>/etc/apt/sources.list.d/galera.list</b> <br>
![2.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM2/Images/2.2.PNG)<br><br>

3. Membuat file baru dengan <b>sudo nano /etc/apt/preferences.d/galera.pref</b> untuk memastikan software patched version yang dibutuhkan galera cluster, lalu <b>apt update</b> lalu install package <b>galera-3 mysql-wsrep-5.7</b><br>
![3.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM2/Images/3.2.PNG)<br><br>

4. Disable apparmor untuk memastikan galera dapat berjalan lancar dengan perintah <b>sudo ln -s /etc/apparmor.d/usr.sbin.mysqld /etc/apparmor.d/disable/
</b> <br>
5. Kemudian edit file berikut untuk menkonfigurasi galeria cluster dengan perintah <b>sudo nano /etc/mysql/conf.d/galera.cnf
</b> lalu edit pada bagian wsrep cluster address dengan kedua ip database yang akan diload balancing. Kemudian masukan wsrep node address sesuai ip address database yang sedang disetting dan isi namanya untuk mengenali ip berikut milik siapa<br>
![4.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM2/Images/4.2.PNG)<br><br>

6. Lakukan semua perintah sebelumnya pada database yang akan digunakan<br>
7. Ketikan perintah <b>sudo systemctl enable mysql</b> pada semua server database untuk meng enable mysql systemd service<br>
8. Ketikan perintah <b>sudo mysqld_bootstrap</b> pada node database yang digunakan sebagai database utama untuk mengaktifkan mysqlnya, jika tidak diketikan perintah tersebut maka untuk mengaktifkan dengan <b>sudo systemctl start mysql</b> tidak akan berjalan<br>
9. Jalankan node sisahnya dengan perintah <b>sudo systemctl start mysql</b>
10. Untuk mengecek apakah berjalan bisa diketikan perintah <b>mysql -u root -p -e "SHOW STATUS LIKE 'wsrep_cluster_size'"</b> dan jika valuenya bukan 0 maka berhasil
11. Terakhir bikin user untuk backend dapat terhubung dengan database dengan perintah <b>CREATE USER 'newuser'@'(ip backend)' IDENTIFIED BY 'password';</b> pada mysql kemudian grant access dengan perintah <b>GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'(ip backend)';</b>
