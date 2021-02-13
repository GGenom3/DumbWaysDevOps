1 Mendownload docker image node versi 10.23.3-slim dari docker hub ke server dengan docker pull<br>
![1.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/1.2.PNG) <br><br>

2. Membuat dockerfile pada direktori tempat menyimpan file frontend/backend, dengan penjelasan:<br>
  FROM untuk images yang digunakan<br>
  WORKDIR untuk membuat direktori kerja apabali belum ada atau menggunakan suatu path direktori yang sudah ada<br>
  COPY untuk mencopy file dari satu direktori ke direktori lainnya atau direktori container<br>
  RUN untuk menjalankan perintah yang tersedia pada images yang disebutkan FROM<br>
  CMD untuk menjankan perintah pada shell<br>
![2.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/2.2.PNG)<br>

3. Untuk membuat image dari dockerfile menggunakan perintah docker build -t (nama images) . <br>
Jika terjadi error maka ada yang salah dengan konfigurasi dockerfilenya<br><br>

4. Push docker image yang sudah dibuat tadi ke docker hub kita<br>
![3.2.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM3/Images/3.2.PNG)<br>