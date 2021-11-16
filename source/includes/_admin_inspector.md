# [Admin] Pengawas

## Get Daftar Pengawas

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/inspectors?q=&status=&page="
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
    "updated_at": "dateime",
    "active": "boolean",
    "institution": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data pengawas.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/inspectors?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Post Pengawas Baru

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/inspectors"
-H 'Content-Type: application/json'
-d '{
      "name": "string",
      "email": "string",
      "roles": "array",
      "phone": "string",
      "institution": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk menambah data pengawas.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/inspectors`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | string | true | Email
name | string | true | Nama
roles | array | true | Rule
phone | string | false | Telepon
institution | array | true | Institusi

## Post Ubah Rule Pengawas

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/inspectors/{id}/update-roles"
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

endpoint ini digunakan untuk update role pengawas.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/inspectors/{id}/update-roles`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
roles | array | true | Rule

## Post Ubah Status Pengawas

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/inspectors/{id}/update-active"
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

endpoint ini digunakan untuk mengubah status pengawas.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/inspectors/{id}/update-active`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
active | boolean | true | Status
