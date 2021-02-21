1. Membuat server untuk ansible atau bisa ditaruh disalah satu server seperti reverse proxy<br>
2. Install ansible seperti yang ada di documentation ansible dengan memasukan apt keynya, repositorynya dan install<br>
3. Jika sudah terinstall pertama membuat file inventory yang berisi alamat ip dari server yang akan dibuat/config dan user passnya, karna tidak menggunakan password tetapi sshkey maka tidak perlu diisi passwordnya<br>
![1.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/1.4.PNG)<br><br>
4. Setelah membuat inventory selanjutnya membuat file config ansible dengan isi link lokasi inventory dan lokasi sshkey<br>
![3.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/2.4.PNG)<br><br>
5. Setelah itu membuat file yml untuk menconfig beberapa server atau group server yang sudah disebutkan pada inventory, sebagai contoh disini yang
diconfig adalah frontend, jika config backend maka hosts diganti ke backend atau all jika config semua server, masukan apa saja yang ingin diconfig seperti
contoh disini menginstall docker pada server frontend<br>
![3.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/3.4.PNG)<br>
![4.4.png](https://github.com/GGenom3/DumbWaysDevOps/blob/main/TaskM4/Images/4.4.PNG)<br><br>