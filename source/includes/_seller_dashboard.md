# [Seller] Global

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## Post Upload Gambar

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/upload"
-H 'Content-Type: application/json'
-d '{
      "file": "image",
      "type": "string"  
    }'
```
> Contoh Json Response :

```json
{
  "resource": "string"
}
```

endpoint ini digunakan untuk menambahkan gambar.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/upload`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
file | image | true | Gambar
type | string | true | Kategori Gambar

## Get Pengaturan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/settings"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
      "id": "integer",
      "name": "string",
      "type": "string",
      "content": "string",
      "scope": "integer",
      "enabled": "boolean",
      "created_at": "datetime",
      "updated_at": "datetime"
  }
]
```

endpoint ini digunakan untuk memperoleh pengaturan.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/settings`

## Post Cek Data Cabang

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/check-branch"
-H 'Content-Type: application/json'
-d '{
      "code": "string"
    }'
```
> Contoh Json Response :

```json
{
    "id": "integer",
    "name": "string",
    "code": "string",
    "note": "string",
    "active": "boolean",
    "created_at": "datetime",
    "updated_at": "datetime"
}
```

endpoint ini digunakan untuk cek data cabang.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/check-branch`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
code | string | true | Kode Cabang

## Get Dashboard

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/dashboard/index"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "transactions": "array",
    "merchants": "array",
    "products": "array"
}
```

endpoint ini digunakan untuk mendapatkan data dashboard.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/dashboard/index`
