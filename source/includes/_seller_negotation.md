# [Seller] Negotations

Negotations digunakan untuk mengambil data negosiasi antara penjual dan pembeli, membalas negoisasi dari pembeli, menyetujui negoisasi dari pembli dan menolak negoisasi dari pembeli.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## DATA Negotations

## Get Semua Data Negoisasi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/negotiations?q=&status=&page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```

> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "created_by": "string",
    "id": "integer",
    "initial_price": "integer",
    "merchant_id": "integer",
    "nego_price": "integer",
    "nego_qty": "integer",
    "product": {"id": "integer", "name": "string", "price": "integer", "image": "string"},
    "product_id": "integer",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "status_nego": "active",
    "status_response": "waiting_seller",
    "updated_at": "datetime",
    "updated_by": "string",
    "negotiation_history": [
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
  }
]
```

endpoint ini digunakan untuk mendapatkan data negosiasi dari pembeli.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/negotiations?q=&status=&page=`



## Get Data Detail Negoisasi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/negotiations/{id}"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```

> Contoh Json Response :

```json
  {
    "created_at": "datetime",
    "created_by": "string",
    "id": "integer",
    "initial_price": "integer",
    "merchant_id": "integer",
    "nego_price": "integer",
    "nego_qty": "integer",
    "product": {"id": "integer", "name": "string", "price": "integer", "image": "string"},
    "product_id": "integer",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "status_nego": "active",
    "status_response": "waiting_seller",
    "updated_at": "datetime",
    "updated_by": "string",
    "negotiation_history": [
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
  }
```

endpoint ini digunakan untuk mendapatkan data detail negosiasi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/negotiations/{id}`

## Post Membalas Negoisasi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/negotiations/reply"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "integer",
        "nego_price" : "integer",
        "message" : "string"
      }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk membalas negosiasi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/negotiations/reply`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
negotiation_id | integer | true | Id Negosiasi
nego_price | integer | true | Harga Nego dari penjual
message | string | false | Pesan dari Penjual

## Post Menyetujui Negoisasi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/negotiations/accept"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "integer",
      }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```
endpoint ini digunakan untuk menyetujui negosiasi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/negotiations/accept`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
negotiation_id | integer | true | Id Negosiasi

## Post Menolak Negoisasi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/negotiations/reject"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "integer",
      }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menolak negosiasi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/negotiations/reject`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
negotiation_id | integer | true | Id Negosiasi

