# [Buyer] Produk

<aside class="notice">
membutuhkan Autentikasi/Token <strong>buyer</strong>.
</aside>

## Get Data Diskusi Produk

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/products/{id}/discussion"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "created_by": "string",
    "customer_id": "integer",
    "id": "integer",
    "merchant_discuss_replies": [],
    "merchant_id": "integer",
    "message": "string",
    "product_id": "integer",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "updated_at": "datetime",
    "updated_by": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data diskusi produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/products/{id}/discussion`

## Post Buat Pesan Diskusi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/products/{id}/discussion-reply"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "message": "string"
      }'
```
> Contoh Json Response :

```json
{
  "created_at": "datetime",
  "id": "integer",
  "merchant_id": "integer",
  "message": "string",
  "product_id": "integer",
  "school_id": "string",
  "updated_at": "datetime"
}
```

endpoint ini digunakan untuk pengajuan negosiasi kepada penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/products/{id}/discussion-reply`

### Query Body

| Parameter  | Default | required | Deskripsi           |
| ---------- | ------- | -------- | ------------------- |
| message | string | false | Pesan
