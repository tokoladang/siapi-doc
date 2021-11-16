# [Admin] Promo

## Get Semua Promo

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/promos"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "code": "string",
    "created_at": "datetime",
    "created_by": "string",
    "description": "string",
    "enabled": "boolean",
    "id": "integer",
    "image": "string",
    "is_main": "boolean",
    "minimum_purchase": "integer",
    "name": "string",
    "product_category_id": "integer",
    "slug": "string",
    "type": "integer",
    "updated_at": "datetime",
    "updated_by": "string",
    "valid_from": "date",
    "valid_to": "date",
    "value": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data promo.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/promos`

## Post Promo Baru

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/promos"
-H 'Content-Type: application/json'
-d '{
      "name": "string",
      "image":  "file",
      "enabled": "boolean"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menambahkan data promo baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/promos`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Cabang
image | file | true | Gambar
enabled | boolean | true | Status

## Put Ubah Promo

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/promos/{id}"
-H 'Content-Type: application/json'
-d '{
      "name": "string",
      "image":  "file",
      "enabled": "boolean"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk merubah data promo.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/promos/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Cabang
image | file | true | Gambar
enabled | boolean | true | Status

## Delete Hapus Promo

> jenis: admin

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/admin/promos/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menghapus data promo.

### HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/admin/promos/{id}`
