1. Mengganti NAT menjadi bridge di vmware dengan cara klik setting pada virtual machine lalu network adapter diubah menjadi bridge dan apply <br>
![1.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/1.2.PNG) <br>
2. Set up ip address menggunakan text editor pada netmap di /etc/netmap/00-installer-config.yaml lalu isi sesuai ip static yang akan dibuat <br>
![2.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/2.2.PNG) <br>
3. Jika sudah ketikan sudo netmap apply lalu bisa dicek apakah ip sudah berubah static atau belum dan cek konektifitas lewat ping
![3.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM1/Image/3.2.PNG) <br>
