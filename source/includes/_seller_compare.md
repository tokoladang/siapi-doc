# [Seller] Compare

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## Get Data Perbandingan

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/dashboard/compares?page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "compare": {
      "id": "integer", "school_id": "string", "code": "string", "is_used": "boolean", "created_by": "string"
      "school": "json", "funding_source": "json", "created_at": "datetime", "created_at": "updated_at", "updated_by": "string"
    },
    "compare_id": "integer",
    "compare_items": [
      {
        "compare_group_id": "integer",
        "id": "integer",
        "item_no": "integer",
        "negotiation_id": "integer",
        "price": "integer",
        "product_id": "integer",
        "product_image": "string",
        "product_name": "string",
        "quantity": "integer",
        "shipping": {},
        "tax_price": "integer",
        "total_price": "integer"
      }
    ],
    "courier": {"name": "string", "etd": "string", "cost": "integer", "address": "string"},
    "courier_name": "Kurir Toko",
    "id": "integer",
    "merchant_id": "integer",
    "shipping_cost": "integer",
    "status": "boolean",
    "tax_price": "integer",
    "time_limit": "integer",
    "total_price": "integer",
    "total_qty": "integer",
    "total_weight": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data perbandingan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/dashboard/compares?page=`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
page | integer | true | halaman

## Post Konfirmasi Perbandingan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/{groupId}/confirm"
-H 'Content-Type: application/json'
-d '{
      "time_limit": "integer",
      "shipping_cost": "integer",
      "shipping_etd": "integer"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk Konfirmasi Perbandingan.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/{groupId}/confirm`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
time_limit | integer | true | Waktu Pengerjaan
shipping_cost | integer | true | Ongkos Kirim
shipping_etd | integer | true | Lama Pengiriman
