1. - BASH merupakan default shell linux yang merupakan pengembangan dari bourne shell sehingga kompatibel di unix.
   - SH ialah shell standard unix yang terkenal sederhana, kompak dan cepat, shell sh dibuat pada tahun 1979 oleh stephen bourne dari at&t dengan memakai pemograman algol.
   
   
2. pertama aku masuk ke teks editor dengan perintah :
   
   ```
   sudo nano upd.ugd.sh
   ```
   
   ![Screenshot from 2022-11-22 17-10-39](https://user-images.githubusercontent.com/118157585/203288985-f047b09b-1a9e-4e60-b7e3-cc9b67ccc9c6.png)
   
   lalu kita ketikan perintah seperti di text editor tersebut
   
   ![Screenshot from 2022-11-22 17-14-11](https://user-images.githubusercontent.com/118157585/203288934-c7e8b11c-e1e0-45d5-a0bd-cc3f6f91dfbc.png)

    lalu kita beri permissionnya ke upd.upg.sh dengan mengetikan perintah:
    ```
    sudo chmod u+x upd.upg.sh
    ```
   ![Screenshot from 2022-11-22 17-11-14](https://user-images.githubusercontent.com/118157585/203288981-873e3c7d-feb5-4354-86ef-a87ab570002e.png)

    lalu kita eksekusi upd.upg.sh kita dengan menjalankan perintah berikut:
    ```
    sudo ./upd.upg.sh
    ```
    lalu muncul update nya

   ![Screenshot from 2022-11-22 17-13-44](https://user-images.githubusercontent.com/118157585/203288964-a1da79b0-d2d8-4b1d-86ca-c0d2507805b0.png)

    nah ini untuk tampilan saat upgrade nya.

   ![Screenshot from 2022-11-22 17-13-13](https://user-images.githubusercontent.com/118157585/203288969-c547446a-f64b-4072-9682-78c55d0dabdc.png)
   
3. first, nah disini kita edit akses port nya dengan perintah
   ```
   akses.port.sh
   ```
   ![Screenshot from 2022-11-22 23-10-00](https://user-images.githubusercontent.com/118157585/203364964-74b58748-fb07-49db-af0c-55eb2a700ef9.png)
   
   nah klo udh masuk ke editor, kita edit seperti yg diperintahkan yaitu buat akses ke port 22, 80, dan 443. bisa lihat gambar dibawah ini.
   
   ![Screenshot from 2022-11-22 23-08-49](https://user-images.githubusercontent.com/118157585/203364966-7c22f06f-51c6-4c8a-b05e-13613fbd13d5.png)
   
   nah disini file si akses.port.sh ini akan aku beri akses bisa di eksekusi dengan perintah:
   ```
   sudo chmod +x akses.port.sh
   ```
   
   ![Screenshot from 2022-11-22 23-10-33](https://user-images.githubusercontent.com/118157585/203364958-2de24038-cfc6-4ed2-acf3-9a26ea056bd5.png)
   
   lalu kita eksekusi dengan perintah.
   ```
   sudo ./akses.port.sh
   ```
   maka akan memberi akses kepada port port itu.
   
   ![Screenshot from 2022-11-22 23-10-55](https://user-images.githubusercontent.com/118157585/203364949-ecc03902-e607-4e0d-afc3-7a20ea0ca2f6.png)
4.
Pertama kita bikin file dulu yaitu dengan ketikkan perintah.
```
touch fikri.sh
```
![Screenshot from 2022-11-24 00-09-06](https://user-images.githubusercontent.com/118157585/203612872-a512219e-1b2c-4a28-aeb1-548ed9c4c604.png)

lalu kita bikin file lagi dengan ketikkan perintah.
```
touch maolana.sh
```
![Screenshot from 2022-11-24 00-08-55](https://user-images.githubusercontent.com/118157585/203612874-b627c02b-6256-4a42-96e5-7a943d33de7f.png)
lalu kita edit file maolana.sh dengan mengetikkan perintah :
```
nano maolana.sh
```
lalu save dan exit dari nano.

![Screenshot from 2022-11-24 00-06-39](https://user-images.githubusercontent.com/118157585/203612801-853ec770-efc5-407c-9e31-bed8b63037d3.png)

lalu kita edit file fikri.sh tadi dengan mengetikkan perintah.
```
nano fikri.sh
```
lalu ketik seperti gambar dibawah ini di nano untuk nanti kita tampilkan contoh cat.

![Screenshot from 2022-11-24 00-11-14](https://user-images.githubusercontent.com/118157585/203612821-f88a43f0-bf6f-4cce-a93e-4cf458c7f624.png)

kita ubah mode fikri.sh agar bisa eksekusi file nya dengan mengetikkan perintah :
```
sudo chmod +x fikri.sh
```
![Screenshot from 2022-11-24 00-10-29](https://user-images.githubusercontent.com/118157585/203612829-a7c95e0c-f07f-4e21-8e3d-b746d8be418a.png)

kita eksekusi file fikri.sh nya dengan mengetikkan perintah
```
sudo ./fikri.sh
```
lalu inilah untuk tampilan setelah di eksekusi, gambar dibawah ini adalah contoh untuk tugas yang cat

![Screenshot from 2022-11-24 00-11-42](https://user-images.githubusercontent.com/118157585/203612868-1ced7c3a-5cf6-4dd8-8e88-c15483a99ca2.png)
setelah contoh untuk cat selesai, sekarang kita masuk lagi ke 
```
nano fikri.sh
```
untuk tugas menampilkan contoh grep, disini kita akan mencari angka 1 di grep. kita ketikkan perintah dibawah ini untuk mencari angka "1" nantinya di grep

![Screenshot from 2022-11-24 00-18-29](https://user-images.githubusercontent.com/118157585/203612859-c95385cf-bd78-422a-a66a-94c9875a172d.png)

berhubung tadi kita sudah ganti mode si "fikri.sh" agar bisa di ekseskusi, maka langsung aja kita eksekusi dengan mengetikkan perintah 
```
sudo ./fikri.sh
```
nah inilah untuk tampilan mencari angka "1" dalam menggunakan grep.

![Screenshot from 2022-11-24 00-19-03](https://user-images.githubusercontent.com/118157585/203612865-8aabf2df-958d-40f7-9a68-055f704d6db7.png)

nah sekarang kita akan menampilkan untuk contoh "echo", kita masuk ke 
```
nano fikri.sh
```
lalu ketikkan perintah seperti gambar dibawah, ini adalah script untuk menampilkan "echo".

![Screenshot from 2022-11-24 00-20-35](https://user-images.githubusercontent.com/118157585/203612844-8e014eb7-3735-4bac-9a7b-3e34bb54c15e.png)
lalu kita eksekusi file "fikri.sh", dengan mengetikkan perintah
```
sudo ./fikri.sh
```
nah gambar dibawah ini tampilan untuk contoh echo yang kita edit di editor nano fikri.sh

![Screenshot from 2022-11-24 00-20-59](https://user-images.githubusercontent.com/118157585/203612848-2ee31046-b317-445a-a898-b5191a2e469f.png)
nah sekarang kita akan mencontohkan pemakaian sort, ini kita masuk ke editor lagi dengan mengetikkan perintah :
```
nano fikri.sh
```
lalu kita ketikkan perintah seperti gambar dibawah, ini fungsinya mengurutkan  data secara ascending.

![Screenshot from 2022-11-24 00-21-52](https://user-images.githubusercontent.com/118157585/203612851-94f6c1f3-8beb-4cb2-8739-f42769c60a7b.png)

nah lalu kita eksekusi untuk contoh sort nya dengan mengetikkan perintah
```
sudo ./fikri.sh
```
maka data akan berurut dari atas sampai bawah.

![Screenshot from 2022-11-24 00-22-23](https://user-images.githubusercontent.com/118157585/203612840-156cd23a-468a-4a6a-b099-3e427f570997.png)

nah sekarang kita masuk ke contoh mengganti teks menggunakan perintah sed, skrg kita masuk ke editor, lalu masukan perintah seperti dibawah.

![Screenshot from 2022-11-24 00-25-20](https://user-images.githubusercontent.com/118157585/203612834-da7fb7c1-37d6-483e-b3b0-d17a43b150a5.png)

nah setelah kita save, lalu kita eksekusi dengan mengetikkan perintah
```
sudo ./fikri.sh
```
taraaaaaaa, teks "Dumbways" udh berubah menjadi "Bootcamp"

![Screenshot from 2022-11-24 00-26-09](https://user-images.githubusercontent.com/118157585/203612831-e98dc0ee-db0e-4bb2-be82-c8bf1206fd82.png)


5.
ini salah satu contoh untuk penggunaan monitoring proses yang sedang berjalan scr lengkap
```
ps -aux
```
![Screenshot from 2022-11-24 00-41-15](https://user-images.githubusercontent.com/118157585/203613667-ad4c631b-9266-4b51-8706-b2808a04c192.png)




Challange :


untuk tantangan install NVM menggunakan bash saya masih berada di dalam direktori si manipulasi tadi dan file manipulasi yang tadi

pertama kita masuk ke 
```
nano fikri.sh
```
lalu edit seperti perintah gambar dibawah ini, setelah selesai lalu save

![Screenshot from 2022-11-24 00-33-09](https://user-images.githubusercontent.com/118157585/203612879-40941dfe-ea7a-407d-9713-1aa41f470fd4.png)
nah setelah kita udh selesai save, lalu kita eksekusi file 
```
fikri.sh
```

lalu akan muncul tampilan seperti dibawah, dan tunggu aja sampai proses instalasi selesai.
![Screenshot from 2022-11-24 00-33-34](https://user-images.githubusercontent.com/118157585/203614335-ee6eeb17-19db-4d80-85b3-f987d79ae318.png)
