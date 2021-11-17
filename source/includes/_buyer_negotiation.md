# [Buyer] Negosiasi

<aside class="notice">
membutuhkan Autentikasi/Token <strong>buyer</strong>.
</aside>

## Get Data Riwayat Negosiasi

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/negotiations/{id}/histories"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "customer_message": "string",
    "customer_price": "integer",
    "customer_qty": "integer",
    "id": "integer",
    "merchant_message": "string",
    "merchant_price": "integer",
    "merchant_qty": "integer",
    "negotiation_id": "integer",
    "payment_due": "integer",
    "status": "string",
    "updated_at": "datetime"
  }
]
```

endpoint ini digunakan untuk mendapatkan riwayat negosiasi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/negotiations/{id}/histories`

## Post Pengajuan Negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
      "customer_order_item_id": "integer",
      "nego_price": "integer",
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

endpoint ini digunakan untuk pengajuan negosiasi kepada penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations`

### Query Body

| Parameter  | Default | required | Deskripsi           |
| ---------- | ------- | -------- | ------------------- |
| customer_order_item_id | integer | true | Id item pesanan           |
| nego_price | integer | true | Harga nego          |
| message | string | false | Pesan

## Post Negosiasi Ulang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations/reply"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
      "negotiation_id": "1",
      "nego_price": "200000",
      "message": "Saya Nego Lagi"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk pengajuan negosiasi ulang kepada penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations/reply`

### Query Body

| Parameter  | Default | required | Deskripsi           |
| ---------- | ------- | -------- | ------------------- |
| negotiation_id | integer | true | Id Nego
| nego_price | integer | true | Harga
| message | string | false | Pesan 

## Post Menyetujui Negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations/accept"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "negotiation_id": "integer"
      }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk menyetujui harga yang diajukan kepada seller.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations/accept`

### Query Body

| Parameter      | Default | required | Deskripsi    |
| -------------- | ------- | -------- | ------------ |
| negotiation_id | integer | true | Id Negosiasi |

## Post Membatalkan Negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations/cancel"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "negotiation_id": "integer",
      }'
```

endpoint ini digunakan untuk membatalakan negosiasi yang diajukan kepada penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations/cancel`

### Query Body

| Parameter      | Default | required | Deskripsi    |
| -------------- | ------- | -------- | ------------ |
| negotiation_id | integer | true | id Negosiasi |
