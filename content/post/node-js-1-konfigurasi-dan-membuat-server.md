---
title: "#1 Tutorial Node.JS - Konfigurasi & Membuat Web Server Dengan Express.JS"
date: 2023-02-24T10:10:09+07:00
draft: false
description: "Konfigurasi Dan Membuat Web Server Dengan Express.JS"
tags: ["nodejs", "javascript", "mern"]
image: "img/thumbnailnodejs-1.png"
---

<!--more-->

{{< img-nz-lazy "16x9" "Node.JS" "img/thumbnailnodejs-1.png" >}}


## Prerequisite

Dalam development Node.JS diperlukan beberapa hal yang harus terinstall atau tersedia, hal tersebut yaitu :
- [Node.JS](https://nodejs.org/en/)
- Code Editor Favoritmu (Contoh : [Visual Studio Code](https://code.visualstudio.com/))
- Niat *hehehehe :sweat_smile:

## Instalasi

Selanjutnya kamu perlu download [Node.JS](https://nodejs.org/en/) lalu menginstallnya. Setelah kamu berhasil install Node.JS kamu bisa test apakah instalasi-mu sudah betul atau belum menggunakan command ``node -v``di command prompt kamu, kalau berhasil maka akan muncul seperti :
```
> node -v
v16.17.0

```


Jika sudah seperti diatas, maka instalasi Node.JS sudah selesai dan berhasil.

## Buat Project Baru

Setelah kamu berhasil instalasi, maka untuk membuat project baru, kamu dapat melakukan hal ini :

1. Buat folder baru, misalnya terdapat di ```C:\Users\MYPC\Documents\Materi\belajarnodejs```
2. Buka command prompt dan masuk ke folder yang sudah kita buat tadi dengan perintah :
```
cd Documents\Materi\belajarnodejs
```
3. Setelah itu masukkan perintah :
```
npm init -y
```
Dengan perintah diatas, Kamu sudah berhasil membuat project baru.

4. Selanjutnya kita akan melakukan test dengan membuat file ```index.js```, lalu didalamnya kita tambahkan kode :
```
console.log("Hello World");
```

5. Setelah itu kita execute kode tersebut dengan mengetikkan perintah ``` node index.js ``` pada command prompt. Harusnya akan muncul :

```
Hello World
```

## Mengenal Nodemon

Ketika kita execute kode dengan menggunakan node, jika kita memiliki perubahan pada kode kita, secara default kita harus restart command node. Tentunya akan membuang waktu jika setiap perubahan harus kita restart secara manual. 

Oleh karena itu mari kenalan dengan package yang bernama *nodemon*. Dengan nodemon kita dapat melakukan perubahan tanpa repot restart command node. Cara instalasinya adalah :

- Di terminal ketikkan perintah
```
npm install nodemon
```
- Setelah itu kita ke file yang bernama ```package.json``` lalu kita mengetikkan perintah
```
"start": "nodemon index.js"
```

Perintah tersebut dimasukkan di dalam scripts, contoh jadinya kurang lebih seperti ini
```
{
  "name": "belajarnodejs",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon index.js"
  },
  "author": "Akbar Rahmat Mulyatama",
  "license": "ISC",
  "dependencies": {
    "nodemon": "^2.0.20"
  }
}

```
- Setelah itu di command prompt, kita hanya harus menuliskan 

```npm start``` 

## Membuat Web Server Dengan Express.JS

Untuk menggunakan Express.JS kita harus menginstallnya dengan cara  :
- Masukkan perintah ```npm install --save express``` pada command prompt
- Lalu di ```index.js``` masukan kode
```
const express = require('express')

const app = express()

app.use(() => {
    console.log("Hello web server")
})

app.listen(4000)
```
- Setelah itu kita jalankan lagi ```npm start``` dan buka browser dengan url ```http://localhost:4000```

Kita mungkin tidak dapat membuka website dengan url tersebut, namun jika dilihat di command prompt, maka akan muncul 

```Hello web server```

## Penutup
Selanjutnya kita akan membahas lebih detail lagi mengenai topik lain tentang Node.JS, stay tune :sparkles: