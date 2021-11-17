# [Admin] Pengguna


## Get Verifikasi Pengguna

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/admin-email/verify/{id}/{hash}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "id": "code",
  "message": "message"
}
```

endpoint ini digunakan untuk verifikasi pengguna.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/admin-email/verify/{id}/{hash}`

## Get Kirim Link Verifikasi Pengguna

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/admin-email/verification-notification"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "id": "code",
  "message": "message"
}
```

endpoint ini digunakan untuk mengirim link verifikasi pengguna.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/admin-email/verification-notification`

## Get Daftar Pengguna Admin

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/admins?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string",
    "email": "string",
    "email_verified_at": "dateime",
    "roles": [],
    "active": "boolean",
    "created_at": "dateime",
    "updated_at": "dateime"
  }
]
```

endpoint ini digunakan untuk mendapatkan data pengguna admin.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/admins?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Post Pengguna Admin Baru

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/admins"
-H 'Content-Type: application/json'
-d '{
      "name": "string",
      "email": "string",
      "roles": "array"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk menambah pengguna admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/admins`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | string | true | Email
name | string | true | Nama
roles | array | true | Rule

## Post Ubah Role Admin

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/admins/{id}/update-roles"
-H 'Content-Type: application/json'
-d '{
      "roles": "array"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk update role admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/admins/{id}/update-roles`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
roles | array | true | Rule

## Post Ubah Status Admin

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/admins/{id}/update-active"
-H 'Content-Type: application/json'
-d '{
      "active": "boolean"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk mengubah status admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/admins/{id}/update-active`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
active | boolean | true | Status
