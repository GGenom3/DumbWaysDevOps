1. Masuk ke aws ec2 lalu pilih instance dan launch instance <br>
![1.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/1.4.PNG)<br><br>
2. Pilih imagenya ubuntu server versi 18 lalu next pilih yang type instance t2 micro, untuk configure instance biarkan saja hanya auto assign public ip ganti jadi disable <br>
![2.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/2.4.PNG)<br>
![3.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/3.4.PNG)<br>
![4.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/4.4.PNG)<br><br>
3. Storage pakai 10gb lalu next ke security group, create new security group dan isi security group name. karna membuat bikin 2 server yaitu reverse proxy dan web app server maka
bikin 2x instance dan ketentuan kedua securitynya beda, untuk reverse proxy hanya open port ssh, http dan https saja sedangkan web app server open semua port. jika sudah bisa direview lalu finish <br>
![5.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/5.4.PNG)<br>
![6.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/6.4.PNG)<br><br>
4. karna rverse proxy butuh ip public maka setting di bagian elastic ip lalu pilih allocate ip, setingan lain biarkan saja jadi langsung klik allocate, karna untuk setting web app server butuh ip public untuk mendownload packagenya maka bikin satu lagi dan akan dihapus setelahnya, untuk menghubungkan elastic ip yang sudah dibuat klik action lalu associate elastic ip <br>
![7.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/7.4.PNG)<br>
![8.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/8.4.PNG)<br>
![9.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/9.4.PNG)<br><br>
5. Pilih instance yang dibuat tadi dan private ipnya <br>
![10.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/10.4.PNG)<br>
