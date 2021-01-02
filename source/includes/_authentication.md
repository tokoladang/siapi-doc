# Autentikasi

Kami Menggunakan dua Jenis Autentikasi untuk dapat mengakses API. yang pertama menggunakan [Session API](/#session-api) yang hanya dipakai oleh Aplikasi Web Internal Kami. dan yang kedua menggunakan [API Token](/#api-token) yang dapat dipakai oleh Aplikasi Mobile atau aplikasi pihak ketiga.

ada 4 jenis endpoint dalam API:

1. `public` adalah endpoint untuk publik yang dapat diakses tanpa harus terautentikasi.
2. `admin` adalah endpoint yang memerlukan login/token admin.
3. `seller` adalah endpoint yang memerlukan login/token penjual.
4. `buyer` adalah endpoint yang memerlukan login/token pembeli.

<aside class="notice">
Setiap API endpoint selain jenis <strong>public</strong> membutuhkan Autentikasi.
</aside>

## Session API

> jenis: public

```shell
curl "https://staging.siapi.tokoladang.co.id/public/csrf-cookie"
```

Autentikasi dengan Session API harus memanggil endpoint ini terlebih dahulu sebelum login. untuk mendaftarkan sesi ke server yang nantinya akan disimpan di cookies.

`GET https://staging.siapi.tokoladang.co.id/public/csrf-cookie`

Setelah Itu Dapat melakukan Login Sesuai dengan jenis user.

### Login Admin

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/login"
  -H 'Content-Type: application/json'
  -d '{
    "email": "admin@mail.com"
    "password": "password_admin"
  }'
```

endpoint ini digunakan untuk login sebagai Admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/login`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Admin
password | null | true | Password Admin

### Login Penjual

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/login"
  -H 'Content-Type: application/json'
  -d '{
    "email": "pembeli@mail.com"
    "password": "password_pembeli"
  }'
```

endpoint ini digunakan untuk login sebagai Penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/login`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Penjual
password | null | true | Password Penjual

### Login Pembeli

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/login"
  -H 'Content-Type: application/json'
  -d '{
    "code": "ouj78Kn...."
  }'
```

untuk login pembeli berbeda dengan login admin dan login penjual. pembeli harus login terlebih dahulu melalui website dapodik berikut: [staging](https://sso.datadik.kemdikbud.go.id/app/365F240F-FCD4-43B3-A871-088817A6EFBC) atau [produksi](https://sso.datadik.kemdikbud.go.id/app/84DC4A50-BF92-4D2B-9B62-1103329A3638), setelah sukses maka akan redirect ke server siplah dengan menyertakan query code yang nantinya digunakan untuk login ke aplikasi siplah.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/login`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
code | null | true | Code dari dapodik untuk login

## API Token

```shell
Authorization: Bearer {{TOKEN}}
```

Authentikasi jenis API Token digunakan untuk mendapatkan `token` yang digunakan sebagai `Authorization header`. Header harus disertakan setiap hit endpoint menggunakan API Token.

### Get Token Admin

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/token"
  -H 'Content-Type: application/json'
  -d '{
    "email": "admin@mail.com"
    "password": "password_admin"
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

`POST https://staging.siapi.tokoladang.co.id/admin/token`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Admin
password | null | true | Password Admin
device | null | true | Jenis Perangkat `web, android, ios`

### Get Token Penjual

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/token"
  -H 'Content-Type: application/json'
  -d '{
    "email": "penjual@mail.com"
    "password": "password_penjual"
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

`POST https://staging.siapi.tokoladang.co.id/seller/token`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Penjual
password | null | true | Password Penjual
device | null | true | Jenis Perangkat `web, android, ios`

### Get Token Pembeli

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/token"
  -H 'Content-Type: application/json'
  -d '{
    "code": "ouj78Kn...."
  }'
```

> Contoh Json Response :

```json
{
  "token": "LKJlkj982rkoi"
  "user": {....}
}
```

untuk get token pembeli berbeda dengan get token admin dan get token penjual. pembeli harus login terlebih dahulu melalui website dapodik berikut: [staging](https://sso.datadik.kemdikbud.go.id/app/365F240F-FCD4-43B3-A871-088817A6EFBC) atau [produksi](https://sso.datadik.kemdikbud.go.id/app/84DC4A50-BF92-4D2B-9B62-1103329A3638), setelah sukses maka akan redirect ke server siplah dengan menyertakan query code yang nantinya digunakan untuk get token ke aplikasi siplah.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/token`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
code | null | true | Code dari dapodik
