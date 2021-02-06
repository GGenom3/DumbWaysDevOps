1. Clone repository untuk backend dengan perintah <b> git clone https://github.com/sgnd/library-backend </b> github disini gunakan yang sudah difork tadi jadi github.com/user/library-backend dan sudah bisa langsung terhubung dengan ssh keygen tadi lalu masuk direktornya dengan perintah <b>cd</b><br>

2. Untuk berpindah ke branch deploy maka ketikan <b> git checkout 7.Deploy</b><br>

3. Edit config.json pada folder tadi lalu masukan username, password, nama database dan host ip dari masing masing databasenya lalu simpan<br>
![1.3.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM2/Images/1.3.PNG)<br><br>

4. Install package sequelize untuk memindahkan data yang ada di folder ke database mysql, ketikan <b>npm install sequelize-cli</b><br>

5. Ketikan <b>sequelize db:migrate</b> untuk memindahkan tablenya lalu sequelize <b>db:seed:all</b> untuk memindahakan isi dari table ke databasenya, jika tidak ada error maka backend sudah terhubung benar dengan database<br>
![2.3.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM2/Images/2.3.PNG)<br><br>

6. Jalankan dengan npm install dan akan berjalan pada port 5000
