# [Admin] Cabang

## Get Semua Kode Cabang

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/branches?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "active": "boolean",
    "code": "string",
    "created_at": "datetime",
    "id": "integer",
    "name": "string",
    "note": "string",
    "updated_at": "datetime"
  }
]
```

endpoint ini digunakan untuk mendapatkan data Cabang.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/branches?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Post Cabang Baru

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/branches"
-H 'Content-Type: application/json'
-d '{
      "name": "string",
      "note":  "string",
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

endpoint ini digunakan untuk menambahkan data cabang baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/branches`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Cabang
note | string | true | Catatan
active | boolean | true | Status

## Put Ubah Cabang

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/branches/{id}"
-H 'Content-Type: application/json'
-d '{
      "name": "string",
      "note":  "string",
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

endpoint ini digunakan untuk merubah data cabang.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/branches/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Cabang
note | string | true | Catatan
active | boolean | true | Status
