1. Membuat instance di aws dengan nama monitoring <br>
2. Setelah itu masuk ke instance monitoring kemudian install docker dan docker-compose<br>
3. Jika sudah terinstall docker compose maka selanjutnya membuat docker compose file dengan membuat 3 container dengan image dari luar, image yang dibutuhkan
adalah prometheus, node exporter dan grafana, untuk node exporter wajib diinstall/dockerize pada server yang ingin dimonitor<br>
![1.1.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/1.1.PNG)<br>
![2.1.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/2.1.PNG)<br><br>
4. Setelah berhasil membuat docker compose, pindah ke reverse proxy server untuk membuat link dari domain ke ip monitoring server lalu pada cloudflare masukan domain yang mengarah ke reverse proxy
![3.1.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/3.1.PNG)