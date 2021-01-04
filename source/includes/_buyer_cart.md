# [Buyer] Keranjang

<aside class="notice">
membutuhkan Autentikasi/Token <strong>buyer</strong>.
</aside>

## GET data keranjang

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/carts/"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
}'
```

endpoint ini digunakan untuk mendapatkan data keranjang.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts`

## Menambahkan barang ke keranjang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/add"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "product_id": 299,
    "quantity": 5
}'
```

> Example response:

```shell
{
    "id": 1,
    "merchant_id": 365,
    "school_id": "85491D19-0BA8-4946-90E6-2R0R8DFB985R",
    "selected": 1,
    "created_at": "2020-12-29T10:28:47.000000Z",
    "updated_at": "2020-12-29T10:28:47.000000Z",
    "cart_items": [
        {
            "id": 1,
            "cart_id": 1,
            "product_id": 299,
            "negotiation_id": null,
            "quantity": 5,
            "selected": 1,
            "created_at": "2020-12-29T10:28:47.000000Z",
            "updated_at": "2020-12-29T10:28:47.000000Z"
        }
    ]
}
```

endpoint ini digunakan untuk menambahkan barang ke keranjang.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/add`

### Query Body

| Parameter  | Default | required | Deskripsi     |
| ---------- | ------- | -------- | ------------- |
| product_id |         | true     | id Produk     |
| quantity   | null    | true     | Jumlah Barang |

## Menambahkan barang ke keranjang dari negosiasi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/add-nego"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "negotiation_id": 1
}'
```

> Example Response

```shell
{
    "id": 1,
    "merchant_id": 365,
    "school_id": "85491D19-0BA8-4946-90E6-2R0R8DFB985R",
    "selected": 1,
    "created_at": "2020-12-29T10:28:47.000000Z",
    "updated_at": "2020-12-29T10:28:47.000000Z",
    "cart_items": [
        {
            "id": 5,
            "cart_id": 1,
            "product_id": 299,
            "negotiation_id": null,
            "quantity": 5,
            "selected": 1,
            "created_at": "2020-12-29T11:15:31.000000Z",
            "updated_at": "2020-12-30T07:19:42.000000Z"
        }
    ]
}
```

endpoint ini digunakan untuk menambahkan barang ke keranjang dari negosiasi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/add-nego`

### Query Body

| Parameter      | Default | required | Deskripsi    |
| -------------- | ------- | -------- | ------------ |
| negotiation_id |         | true     | id Negosiasi |

## Memperbarui data barang di keranjang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/update"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "type": "selected",
    "cart_item_id": 5,
    "selected": 1
}'
```

> example response

```shell
{
    "id": 1,
    "merchant_id": 365,
    "school_id": "85491D19-0BA8-4946-90E6-2R0R8DFB985R",
    "selected": 1,
    "created_at": "2020-12-29T10:28:47.000000Z",
    "updated_at": "2020-12-29T10:28:47.000000Z",
    "cart_items": [
        {
            "id": 5,
            "cart_id": 1,
            "product_id": 299,
            "negotiation_id": null,
            "quantity": 5,
            "selected": 1,
            "created_at": "2020-12-29T11:15:31.000000Z",
            "updated_at": "2020-12-30T07:19:42.000000Z"
        }
    ]
}
```

endpoint ini digunakan untuk memperbarui data barang di keranjang.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/update`

### Query Body

| Parameter    | Default | required | Deskripsi                                           |
| ------------ | ------- | -------- | --------------------------------------------------- |
| type         |         | true     | tipe data yang di update `selected,quantity,remove` |
| cart_item_id |         | true     | id item keranjang                                   |
| quantity     |         | true     | jumlah barang                                       |
| selected     |         | true     | barang dipilih `0 atau 1`                           |
