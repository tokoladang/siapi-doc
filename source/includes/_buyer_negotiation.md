# [Buyer] Negosiasi

<aside class="notice">
membutuhkan Autentikasi/Token <strong>buyer</strong>.
</aside>

## Pengajuan Negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "product_id": "1",
    "nego_price": "200000",
    "nego_qty": "25",
    "message": "Saya Nego"
  }'
```

endpoint ini digunakan untuk pengajuan negosiasi kepada seller.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations`

### Query Body

| Parameter  | Default | required | Deskripsi           |
| ---------- | ------- | -------- | ------------------- |
| product_id |         | true     | id Produk           |
| nego_price | null    | true     | Harga Nego          |
| nego_qty   | null    | true     | Jumlah Nego         |
| message    | null    | false    | Pesan kepada Seller |

## Negosiasi Ulang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations/reply"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "product_id": "1",
    "nego_price": "200000",
    "nego_qty": "25",
    "message": "Saya Nego Lagi"
  }'
```

endpoint ini digunakan untuk pengajuan negosiasi ulang kepada seller.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations/reply`

### Query Body

| Parameter  | Default | required | Deskripsi           |
| ---------- | ------- | -------- | ------------------- |
| product_id |         | true     | id Produk           |
| nego_price | null    | true     | Harga Nego          |
| nego_qty   | null    | true     | Jumlah Nego         |
| message    | null    | false    | Pesan kepada Seller |

## Menerima Negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations/accept"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "negotiation_id": "1",
  }'
```

endpoint ini digunakan untuk menerima negosiasi yang diajukan kepada seller.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations/accept`

### Query Body

| Parameter      | Default | required | Deskripsi    |
| -------------- | ------- | -------- | ------------ |
| negotiation_id |         | true     | id Negosiasi |

## Membatalkan Negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/negotiations/cancel"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "negotiation_id": "777",
  }'
```

endpoint ini digunakan untuk membatalakan negosiasi yang diajukan kepada seller.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/negotiations/cancel`

### Query Body

| Parameter      | Default | required | Deskripsi    |
| -------------- | ------- | -------- | ------------ |
| negotiation_id |         | true     | id Negosiasi |
