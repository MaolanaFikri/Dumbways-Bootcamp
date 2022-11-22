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
   
   lalu kita eksekusi dengan perintah
   ```
   sudo ./akses.port.sh
   ```
   maka akan memberi akses kepada port port itu.
   
   ![Screenshot from 2022-11-22 23-10-55](https://user-images.githubusercontent.com/118157585/203364949-ecc03902-e607-4e0d-afc3-7a20ea0ca2f6.png)
