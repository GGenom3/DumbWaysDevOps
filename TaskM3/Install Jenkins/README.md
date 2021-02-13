1 Install java jdk agar dapat menjalankan jenkins, lalu install jenkins dengan perintah<br>
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add - <br>
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \<br>
    /etc/apt/sources.list.d/jenkins.list'<br>
sudo apt-get update<br>
sudo apt-get install jenkins<br><br>

2. Setting reverse proxy agar mengarahkan domain cicd ke ip local jenkins<br>
![1.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/1.4.PNG)<br>

3. Setelah setting reverse proxy, anjut login jenkins dengan domain yang sudah diset lalu ikuti step by step untuk instalasai plug in dan setting basic config jenkins<br>
