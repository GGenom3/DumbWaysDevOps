1. Install plug in publish over ssh pada manage jenkins > plug in, setelah diinstall masuk ke configurasi dan scroll sampai publish over ssh
lalu isi frontend dan backend server dengan ip, username dan passwordnya untuk login dengan ssh dan bisa test dengan test configuration, 
jika berhasil maka akan tampil success<br>
![1.5.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/1.5.PNG)<br><br>

2. Setelah disimpan pilih new item dan masukan nama jobnya dan pilih freestyle job<br>
![2.5.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/2.5.PNG)<br><br>

3. Pada source code management masukan url git ssh dan credentials untuk mengakses gitnya dan pilih branch nya<br>
![3.5.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/3.5.PNG)<br><br>

4. Pada menu build pilih send files or execute over ssh, untuk ssh server > name pilih ssh server yang sudah dibuat tadi dan pada textbox exec masukan perintah
untuk pull git, membuat image dan deploy server dengan docker<br>
![4.5.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/4.5.PNG)<br><br>

5. Setelah selesai dapat mentestnya dengan build now, jika berhasil icon berwarna biru dan ada tulisan success, jika gagal bisa berwarna merah yang berarti error
atau kuning yang berarti unstable<br>
![5.5.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/5.5.PNG)<br><br

6. Untuk webhooknya pada repository github pilih setting > webhooks dan isi payload url dengan url jenkins ~/github-webhook/ dan content type bisa
application/json atau appliication/x-www-form-urlencoded, pilih just the push event untuk hooknya dan simpan