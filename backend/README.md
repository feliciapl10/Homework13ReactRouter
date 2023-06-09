- lakukan installasi dependencies
- pastikan memiliki docker
- pastikan memiliki docker-compose
- jalankan perintah `docker-compose up -d`
<!-- - install dependencies dengan perintah `yarn install`
- lakukan migrasi database dengan perintah `yarn migrate`
- jalankan perintah `yarn prisma generate`
- jalankan perintah `yarn start`
- untuk mengambil file dari upload, maka dapat diakses dengan `http://localhost:8000/uploads/{nama_file}` -->
- melakukan cd backend, melakukan npm install, dan npm run 
- buat terminal baru dan ketik psql postgres, membuat database dengan CREATE DATABASE react_router
- membuat file .env berisi database url
- buka terminal baru, lalu npm run migrate, menambahkan kode JWT_SECRET sesuai token di jwt.io pada halaman .env
- npm start untuk jalanin backendnya
- masuk ke folder frontend dan ketik cd frontend di terminal baru, lalu npm install dan npm run dev
- klik link local host yang muncul, lalu lakukan register untuk membuat akun, lakukan log in
- create buku, masukan data yang diperlukan (title, author, year, image) dan klik my website untuk melihat list buku yang sudah dibuat.
- untuk mengedit buku klik tombol edit, dan untuk menghapus klik delete
- untuk mengedit tampilan pada navbar websitenya, edit components bagian navbar.jsx
**Endpoint**


# POST /register


Endpoint untuk mendaftarkan pengguna baru.

## Request Body

name (string) : Nama lengkap pengguna.

email (string) : Alamat email pengguna.

password (string) : Password pengguna.

## Response

user (object) : Objek pengguna yang baru saja dibuat.


# POST /login
Endpoint untuk melakukan autentikasi pengguna

## Request Body

email (string) : Alamat email pengguna.

password (string) : Password pengguna.

## Response
token (string) : Token autentikasi yang dihasilkan.


# POST /books

Endpoint untuk membuat buku baru.

## Request Headers

 Authorization (string) : Token autentikasi.
## Request Body
 (Multi-part Form)
title (string) : Judul buku.

author (string) : Nama penulis buku.

publisher (string) : Nama penerbit buku.

year (string) : Tahun terbit buku.

pages (string) : Jumlah halaman buku.

image (file) : Gambar sampul buku.

### Response

book (object) : Objek buku yang baru saja dibuat.

# GET /books
Endpoint untuk mengambil semua buku yang tersedia.

### Response

books (array) : Kumpulan objek buku yang tersedia.

# PUT /books/:id
Endpoint untuk mengubah data buku.

## Request Headers

Authorization (string) : Token autentikasi.

## Request Parameters

id (number) : ID buku yang akan diubah.
Request Body

title (string) : Judul buku.

author (string) : Nama penulis buku.

publisher (string) : Nama penerbit buku.

year (string) : Tahun terbit buku.

pages (string) : Jumlah halaman buku.
## Response

book (object) : Objek buku yang telah diubah.

# DELETE /books/:id
Endpoint untuk menghapus buku.

## Request Headers

Authorization (string) : Token autentikasi.
## Request Parameters

id (number) : ID buku yang akan dihapus.

### Response

book (object) : Objek buku yang telah dihapus.


# GET /books/:id
Endpoint untuk mendapatkan detail buku berdasarkan ID.

## Request Headers

## Request Parameters

id (number) : ID buku .

### Response

book (object) : Objek buku yang .
