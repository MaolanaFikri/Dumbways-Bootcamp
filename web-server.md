1. Menurutku Server web atau yang dalam bahasa inggris disebut web server adalah perangkat lunak (software) dalam server yang berfungsi untuk menerima permintaan (request) berupa halaman web melalui protokol HTTP dan atau HTTPS dari klien yang lebih dikenal dengan nama browser, kemudian mengirimkan kembali (respon) hasil permintaan tersebut ke dalam bentuk halaman-halaman web yang pada umumnya berbentuk dokumen HTML.


2. Nah disini kita menjalankan 2 vm (multipass) yang kita beri nama "foi" "foi2" untuk penggunaan appserver dan nginx,bisa lihat gambar dibawah.
 
![Screenshot from 2022-11-25 01-36-10](https://user-images.githubusercontent.com/118157585/203851064-2a68afe6-93e2-43c1-9efb-0908b88c9a1d.png)

![Screenshot from 2022-11-25 01-35-59](https://user-images.githubusercontent.com/118157585/203851071-7523ae91-2f36-4dc6-b7f3-86ce3229639c.png)

3.

kita masuk ke teks editor dengan perintah

```
nano node.index.js
```

setelah masuk ke editor, lalu kita edit seperti gambar dibawah, dan langsung save.

![Screenshot from 2022-11-25 01-38-33](https://user-images.githubusercontent.com/118157585/203851480-4c81ca24-5d88-4063-a294-995841450b7f.png)

nah setelah itu kita ubah mode agar si node-index.sh bisa di eksekusi dengan perintah

```
sudo chmod +x node-index.js
```

![Screenshot from 2022-11-25 01-39-45](https://user-images.githubusercontent.com/118157585/203851478-0598f687-e638-44d5-add9-47fe9e13e258.png)

setelah sudah kita ubah modenya, lalu kita eksekusi dengan perintah

```
sudo ./node-index.js

```
![Screenshot from 2022-11-25 01-43-51](https://user-images.githubusercontent.com/118157585/203851473-45560358-9044-40e8-9ebb-bd1be545286b.png)

setelah itu kita lakukan clonning project dumbflix-frontend nya dengan perintah

```
git clone https://github.com/dumbwaysdev/dumbflix-frontend
```
![Screenshot from 2022-11-25 01-45-11](https://user-images.githubusercontent.com/118157585/203851443-c6cea867-91ef-4411-b827-3a1b7ebb7fc0.png)

sekarang kita masuk ke direktori dumbflix-frontend yang sudah kita download tadi dengan perintah
```
cd dumbflix-frontend
```

![Screenshot from 2022-11-25 01-46-00](https://user-images.githubusercontent.com/118157585/203851442-c4a8af60-a653-4784-bcef-c511f2c5b6a7.png)

setelah sudah masuk ke direktori dumbflix-frontend, lalu kita lakukan npm install untuk menginstall dependensi dengan perintah

```
npm install
```

![Screenshot from 2022-11-25 01-55-03](https://user-images.githubusercontent.com/118157585/203851447-fdd5652e-4398-409a-8cbc-5ec01276c4a8.png)

lalu jalankan pm2 dengan perintah
```
pm2 start npm --name "dumbflix_frontend" -- start
```
![Screenshot from 2022-11-25 01-55-49](https://user-images.githubusercontent.com/118157585/203851452-46d0af64-747c-4fec-96d8-f91235efa1cb.png)

pertama kita enablekan dulu firewall nya, dengan perintah
```
sudo ufw enable
```

nah disini kita akan setting firewall agar aplikasi pada server utama berada pada port 3000
```
sudo ufw allow 3000
```

![Screenshot from 2022-11-25 01-56-27](https://user-images.githubusercontent.com/118157585/203851454-ec61e390-2590-401b-bf67-26932a89c92a.png)

sekarang kita cek ip kita dengan perintah 
```
hostname -I
```
![Screenshot from 2022-11-25 01-56-55](https://user-images.githubusercontent.com/118157585/203851458-d7b3055d-b974-43a6-9eaa-4c4602f6acb9.png)

nah sekarang kita akses di browser dengan menggunakan ip server kita
```
10.43.191.119:3000
```


![Screenshot from 2022-11-25 01-57-44](https://user-images.githubusercontent.com/118157585/203851461-b28f49d5-8ce4-426d-bc94-2c942c26fff7.png)

4.
![Screenshot from 2022-11-25 01-53-45](https://user-images.githubusercontent.com/118157585/203855827-8c4f82e4-b442-4f82-878f-eb71d470715a.png)
![Screenshot from 2022-11-25 02-13-35](https://user-images.githubusercontent.com/118157585/203855853-82c325c1-ebc1-4993-b33b-74604f345d91.png)
![Screenshot from 2022-11-25 02-14-04](https://user-images.githubusercontent.com/118157585/203855869-2d097dd7-78fa-4043-8773-0bde41662ce2.png)
![Screenshot from 2022-11-25 02-14-34](https://user-images.githubusercontent.com/118157585/203855861-63f244b2-6783-418f-925b-44a658f62c7b.png)
![Screenshot from 2022-11-25 02-15-28](https://user-images.githubusercontent.com/118157585/203855862-c1fc0795-6f5b-4f2e-bbf9-3e4eef7574cf.png)

disini kita akan mengkonfirgurasi reverse proxy
masuk direktori konfigurasi nginx nya dengan
```
cd /etc/nginx
```
![Screenshot from 2022-11-25 02-29-50](https://user-images.githubusercontent.com/118157585/203855893-eb26773a-f63d-4164-b96c-1ff709c4ad99.png)

disini kita buat folder konfigurasi seperti gambar dibawah

![Screenshot from 2022-11-25 02-29-59](https://user-images.githubusercontent.com/118157585/203855895-b9b6ee2f-8d78-474d-9d3d-e18e211fd7f5.png)

masuk ke direktori nya dengan perintah seperti dibawah

![Screenshot from 2022-11-25 02-30-35](https://user-images.githubusercontent.com/118157585/203855896-1be411a1-cfd6-4cb0-aba3-2faa5bc88a3f.png)

setalah itu kita buat file konfigurasinya dengan mengetikkan perintah 
 ```
 sudo nano my.reverse-proxy.conf
 ```
 
![Screenshot from 2022-11-25 02-30-51](https://user-images.githubusercontent.com/118157585/203855897-a7a31f9a-66ea-4fcf-9d40-fd21798df6a0.png)

 setelah di text editor, masukkan perintah seperti
 ```
 server {
    server_name maolanafikri.xyz;

    location / {
             proxy_pass http://10.43.191.42:3000;
    }
}
```
![Screenshot from 2022-11-25 02-17-38](https://user-images.githubusercontent.com/118157585/203855859-2ed5c406-4433-42bb-a042-3a4c23cee652.png)

setalah save,skrg kita pergi ke direktori sebelumnya
```
cd ..
```

  ![Screenshot from 2022-11-25 02-30-59](https://user-images.githubusercontent.com/118157585/203855900-18cc335a-9883-488d-a8e5-f42a6b469b99.png)

lalu kita atur konfigurasi dari file nginx.conf
```
sudo nano nginx.conf
```

![Screenshot from 2022-11-25 02-31-23](https://user-images.githubusercontent.com/118157585/203855902-5fb9f0b5-1a49-43ff-8ebb-35b6de9c0929.png)

lalu cari bagian include, setlah itu tambahkan file konfigurasi kita
```
include /etc/nginx/fikri/*;
```

![Screenshot from 2022-11-25 02-19-03](https://user-images.githubusercontent.com/118157585/203855855-d2afb4fe-c5d1-4135-96cb-ee8b9ff265bd.png)

setelah di save, kita lakukan pengecekan syntax untuk memastikan apakah ada kesalahan dalam penulisan kode
```
sudo nginx -t
```


![Screenshot from 2022-11-25 02-41-53](https://user-images.githubusercontent.com/118157585/203855906-ea2e20ef-5b2d-4c3b-920a-e1c779907cfb.png)

lalu, kita perlu melakukan reload nginx kita agar nginx dapat mengenali perubahan file konfigurasi kita
```
sudo systemctl reload nginx
```

![Screenshot from 2022-11-25 02-42-09](https://user-images.githubusercontent.com/118157585/203855904-f7cbbb98-dca3-4d10-b9ed-3657a4c37fb7.png)

lalu kita cek ip kita dengan perintah 
```
hostname -I
```

![Screenshot from 2022-11-25 02-29-35](https://user-images.githubusercontent.com/118157585/203855891-12bc2ba6-f271-4c6d-aca1-e4d2e0f3bc7b.png)

setelah itu kita perlu setting host file yang ada di pc utama kita, host filenya berada di

```
cd /etc
nano host
```

dan masukan IP dari virtual machine nginx, serta nama domain yang akan kita gunakan

![Screenshot from 2022-11-25 02-25-19](https://user-images.githubusercontent.com/118157585/203855870-20dc2116-ccd0-47e3-b4e7-b0d23597841a.png)


5.
setelah itu kita akses domain kita dikomputer utama kita dengan mengetikkan perintah

```
fikri.xyz
```

![Screenshot from 2022-11-25 02-28-07](https://user-images.githubusercontent.com/118157585/203855877-8604ce50-ec1e-4b94-9a8a-24fc0e204584.png)

