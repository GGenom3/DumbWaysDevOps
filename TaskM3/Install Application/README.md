1 Untuk membuat docker container, disini menggunakan docker compose yang dapat menjalankan beberapa container sekaligus, pertama install docker compose<br>
![1.3.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/1.3.PNG)<br><br>

2. Setelah menginstall, buat file yml dengan penjelasan:<br>
  version hanya bisa 2.2 keatas atau 3.3 keatas<br>
  nama service disini menggunakan frontend atau bisa diganti dengan nama lain<br>
  container_name untuk menamai contaier yang akan dibuat<br>
  image merupakan image yang akan dirun untuk containernya<br>
  stdin_open untuk koneksi tty<br>
  ports diisi ip dengan port yang digunakan dan convert port yang diinginkan, jika tidak diisi ip maka akan menjadi localhost/0.0.0.0<br>
![2.3.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/2.3.PNG)<br>

3. Jalankan docker compose untuk membuat container dan menjalankannya<br>
![3.3.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/3.3.PNG)<br>