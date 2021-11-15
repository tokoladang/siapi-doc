# [Seller] Complain

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## Get Komplain Berdasarkan Pesanan

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/complains/{orderId}/details"
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
  "merchant_id": "integer",
  "message": "string",
  "school": {"id": "string", "name": "string", "details": "string", "funding_sources": "json",…},
  "school_id": "string",
  "status": "string",
  "title": "string",
  "updated_at": "datetime",
  "updated_by": "string",
  "merchant_complain_histories": [
    {
      "created_at": "datetime", "created_by": "string", "id": "integer", "merchant_complain_id": "integer", "message": "string", "role": "string",
      "sender": {"id": "integer", "merchant_id": "string"}, "updated_at": "datetime", "updated_by": "string"
    }
  ]
}
```

endpoint ini digunakan untuk mendapatkan data Komplain berdasarkan Pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/complains/{orderId}/details`

## Post Penjual Membuat Komplain Baru

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/complains/{orderId}"
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

endpoint ini digunakan untuk Membuat Komplain Baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/complains/{orderId}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
title | string | true | Judul
message | string | true | Pesan Komplain

## Post Penjual Menanggapi Komplain

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/complains/{id}/reply"
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

endpoint ini digunakan untuk menganggapi Komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/complains/{id}/reply`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan

## Post Penjual Menutup komplain

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/complains/{id}/close"
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

endpoint ini digunakan untuk menutup komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/complains/{id}/close`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan
