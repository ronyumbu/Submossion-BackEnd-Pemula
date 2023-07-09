---
# Submission Bookshelf API
- ### Kriteria 1 : Aplikasi menggunakan port 9000 ✅
- ### Kriteria 2 : Aplikasi dijalankan dengan perintah `npm run start` ✅
- ### Kriteria 3 : API dapat menyimpan buku ✅
- ### Kriteria 4 : API dapat menampilkan seluruh buku ✅
- ### Kriteria 5 : API dapat menampilkan detail buku ✅
- ### Kriteria 6 : API dapat mengubah data buku ✅
- ### Kriteria 7 : API dapat menghapus buku ✅

---
## Setup Node.js
- Klik *Terminal* -> *New Terminal*
- Ketik `npm init`
  * Setelah muncul **package name: (user)**, enter saja, jika sudah muncul pertanyaan **Is this OK? (yes)**, ketik `yes`
- Lalu ketik `npm install`, maka **package.json** dan **package-lock.json** akan muncul
- Pada **package.json**, ubah bagian script menjadi seperti ini:
  ```bash
  "scripts": {
    "start-prod": "NODE_ENV=production node ./src/server.js",
    "start-dev": "node ./src/server.js",
    "migrate": "node-pg-migrate",
    "lint": "eslint ./src"
  },
  ```
  
---
## Setup dependencies
- Klik *Terminal* -> *New Terminal*
- Hapi framework: ketik `npm install @hapi/hapi`
- Dotenv: ketik `npm install dotenv`
- Joi: ketik `npm install joi`
- Nanoid: ketik `npm install nanoid@3.x.x`
- Node pg migrate: ketik `npm install node-pg-migrate`
- Pg: ketik `npm install pg`
- Eslint: ketik `npm install eslint --save-dev`, lalu ikuti instruksi berikut:
    * Ketik `npx eslint --init`, kemudian akan diberikan pertanyaan, jawab dengan jawaban berikut:
        * How would you like to use ESLint? -> To check, find problems, and enforce code style.
        * What type of modules does your project use? -> CommonJS (require/exports).
        * Which framework did you use? -> None of these. 
        * Does your project use TypeScript? -> N.
        * Where does your code run? -> Node.
        * How would you like to define a style for your project? -> Use a popular style guide.
        * Which style guide do you want to follow? -> (Anda bebas memilih, sebagai contoh saya pilih AirBnB).
        * What format do you want your config file to be in? -> JSON.
        * Would you like to …… (seluruh pertanyaan selanjutnya) -> Y.
