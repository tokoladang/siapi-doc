# [Buyer] Complain

## Get Data Komplain

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/complains"
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
    "customer_order": {},
    "customer_order_id": "integer",
    "from": "string",
    "id": "integer",
    "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
    "merchant_id": "integer",
    "message": "string",
    "school": {"id": "string", "name": "string", "details": "json",…},
    "school_id": "string",
    "status": "string",
    "title": "string",
    "updated_at": "datetime",
    "updated_by": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/complains`

## Get Detail Komplain

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/complains/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{  
  "code": "string",
  "created_at": "datetime",
  "created_by": "string",
  "customer_order": {},
  "customer_order_id": "integer",
  "from": "string",
  "id": "integer",
  "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
  "merchant_complain_histories": [
    {
      "created_at": "datetime",
      "created_by": "string",
      "id": "integer",
      "merchant_complain_id": "integer",
      "message": "string",
      "role": "string",
      "sender": {},
      "updated_at": "datetime",
      "updated_by": "string"
    }
  ],
  "merchant_id": "integer",
  "message": "string",
  "school": {"id": "string", "name": "string", "details": "json",…},
  "school_id": "string",
  "status": "string",
  "title": "string",
  "updated_at": "datetime",
  "updated_by": "string"
}
```

endpoint ini digunakan untuk mendapatkan data detail Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/complains/{id}`

## Get Detail Komplain By Transaksi

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/complains/{orderId}/details"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{  
  "code": "string",
  "created_at": "datetime",
  "created_by": "string",
  "customer_order_id": "integer",
  "from": "string",
  "id": "integer",
  "merchant_complain_histories": [
    {
      "created_at": "datetime",
      "created_by": "string",
      "id": "integer",
      "merchant_complain_id": "integer",
      "message": "string",
      "role": "string",
      "sender": {},
      "updated_at": "datetime",
      "updated_by": "string"
    }
  ],
  "merchant_id": "integer",
  "message": "string",
  "school": {"id": "string", "name": "string", "details": "json",…},
  "school_id": "string",
  "status": "string",
  "title": "string",
  "updated_at": "datetime",
  "updated_by": "string"
}
```

endpoint ini digunakan untuk mendapatkan data detail Komplain berdasarkan transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/complains/{orderId}/details`

## Post Komplain Baru

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/complains/{orderId}"
-H 'Content-Type: application/json'
-d '{
      "title": "string",
      "message": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk membuat komplain baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/complains/{orderId}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
title | string | true | Judul
message | string | true | Pesan

## Post Tanggapi Komplain.

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/complains/{id}/reply"
-H 'Content-Type: application/json'
-d '{
      "message": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk menanggapi komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/complains/{id}/reply`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan

## Post Tutup Komplain

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/complains/{id}/close"
-H 'Content-Type: application/json'
-d '{
      "message": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk mengakhiri komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/complains/{id}/close`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan
