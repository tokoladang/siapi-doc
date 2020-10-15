# Autentikasi

Kami Menggunakan dua Jenis Autentikasi untuk dapat mengakses API. yang pertama menggunakan [Session API](/#session-api) yang hanya dipakai oleh Aplikasi Web Internal Kami. dan yang kedua menggunakan [API Token](/#api-token) yang dapat dipakai oleh Aplikasi Mobile atau aplikasi pihak ketiga.

ada 4 jenis endpoint dalam API:

1. `public` adalah endpoint untuk publik yang dapat diakses tanpa harus terautentikasi.
2. `buyer` adalah endpoint yang memerlukan login/token pembeli.
2. `seller` adalah endpoint yang memerlukan login/token penjual.
2. `admin` adalah endpoint yang memerlukan login/token admin.

<aside class="notice">
Setiap API endpoint selain jenis <strong>public</strong> membutuhkan Autentikasi.
</aside>

## Session API

> jenis: public

```shell
curl "https://siapi.siplah.tokoladang.co.id/public/csrf-cookie"
```

Autentikasi dengan Session API harus memanggil endpoint ini terlebih dahulu sebelum login. untuk mendaftarkan sesi ke server yang nantinya akan disimpan di cookies.

`GET https://siapi.siplah.tokoladang.co.id/public/csrf-cookie`

Setelah Itu Dapat melakukan Login Sesuai dengan jenis user.

### Login Pembeli

> jenis: public

```shell
curl -X POST "https://siapi.siplah.tokoladang.co.id/buyer/login"
  -H 'Content-Type: application/json'
  -d '{
    "email": "pembeli@mail.com"
    "password": "password_pembeli"
  }'
```

endpoint ini digunakan untuk login sebagai Pembeli.

### HTTP Request

`POST https://siapi.siplah.tokoladang.co.id/buyer/login`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Pembeli
password | null | true | Password Pembeli

### Login Penjual

> jenis: public

```shell
curl -X POST "https://siapi.siplah.tokoladang.co.id/seller/login"
  -H 'Content-Type: application/json'
  -d '{
    "email": "pembeli@mail.com"
    "password": "password_pembeli"
  }'
```

endpoint ini digunakan untuk login sebagai Penjual.

### HTTP Request

`POST https://siapi.siplah.tokoladang.co.id/admin/login`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Penjual
password | null | true | Password Penjual

### Login Admin

> jenis: public

```shell
curl -X POST "https://siapi.siplah.tokoladang.co.id/admin/login"
  -H 'Content-Type: application/json'
  -d '{
    "email": "admin@mail.com"
    "password": "password_admin"
  }'
```

endpoint ini digunakan untuk login sebagai Admin.

### HTTP Request

`POST https://siapi.siplah.tokoladang.co.id/admin/login`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Admin
password | null | true | Password Admin


## API Token

```shell
Authorization: Bearer {{TOKEN}}
```

Authentikasi jenis API Token digunakan untuk mendapatkan `token` yang digunakan sebagai `Authorization header`. Header harus disertakan setiap hit endpoint menggunakan API Token.

### Get Token Penjual

> jenis: public

```shell
curl -X POST "https://siapi.siplah.tokoladang.co.id/seller/token"
  -H 'Content-Type: application/json'
  -d '{
    "email": "pembeli@mail.com"
    "password": "password_pembeli"
    "device": "android"
  }'
```

> Contoh Json Response :

```json
{
  "token": "LKJlkj982rkoi"
  "user": {....}
}
```

endpoint ini digunakan untuk Mendapatkan Token Penjual.

### HTTP Request

`POST https://siapi.siplah.tokoladang.co.id/seller/token`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Penjual
password | null | true | Password Penjual
device | null | true | Jenis Perangkat `web, android, ios`

