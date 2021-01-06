# [Seller] Negotations

Negotations digunakan untuk mengambil data negosiasi antara penjual dan pembeli, membalas negoisasi dari pembeli, menyetujui negoisasi dari pembli dan menolak negoisasi dari pembeli.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## Get Semua data Negoisasi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/negotiations"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
{
  "data": [
        {
            "id":23,
            "customer_id": null,
            "merchant_id": 92,
            "product_id": 25,
            "status_response": "waiting_seller",
            "status_nego": "active",
            "initial_price": 456465468,
            "nego_price": 20000,
            "nego_qty": 12,
            "school_id": "85491D19",
        }
    ],
}
```

endpoint ini digunakan untuk mendapatkan data negosiasi dari pembeli.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/negotiations`

## Post Membalas Negoisasi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/negotiations/reply"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "1",
        "nego_price" : "18000",
        "nego_qty" : "20",
        "message" : "Response Penjual"
      }'
```

> Contoh Json Response :

```json
{
  "message": "Negosiasi Berhasil direspon"
}
```

endpoint ini digunakan untuk membalas negosiasi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/negotiations/reply`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
negotiation_id |  | true | Id Negosiasi
nego_price |  | true | Harga Nego dari penjual
nego_qty |  | true | Banyak barang nego penjual
message | null | false | Pesan dari Penjual

## Post Menyetujui Negoisasi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/negotiations/accept"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "1",
      }'
```

> Contoh Json Response :

```json
{
  "message": "Negosiasi Berhasil diterima"
}
```
endpoint ini digunakan untuk menyetujui negosiasi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/negotiations/accept`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
negotiation_id |  | true | Id Negosiasi

## Post Menolak Negoisasi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/negotiations/reject"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "1",
      }'
```

> Contoh Json Response :

```json
{
  "message": "Negosiasi Berhasil ditolak"
}
```

endpoint ini digunakan untuk menolak negosiasi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/negotiations/reject`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
negotiation_id |  | true | Id Negosiasi

