# [Public] Toko

## Get Semua Toko

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/merchants?q=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "address": "string",
    "banners": [],
    "city": {"id": "integer", "name": "string"},
    "city_id": "integer",
    "district": {"id": "integer", "name": "string", "id_ongkir": "string"},
    "district_id": "integer",
    "id": "integer",
    "image": "string",
    "name": "string",
    "note": "string",
    "postal_code": "integer",
    "province": {"id": "integer", "name": "string"},
    "province_id": "integer",
    "rating": "string",
    "review_count": "integer",
    "review_total": "integer",
    "slogan": "string",
    "slug": "string",
    "type": "string",
    "verified_at": "datetime"
  }
]
```

endpoint ini digunakan untuk mendapatkan data toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/merchants?q=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
page | integer | false | Halaman

## Get Detail Toko

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/merchants/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "id": "integer",
  "name": "string",
  "address": "string",
  "branch": {"id": "integer", "code": "string", "name": "string"},
  "province": {},
  "province_id": "integer",
  "city": {},
  "city_id": "integer",
  "district": {},
  "district_id": "integer",
  "village": {},
  "village_id": "integer",
  "postal_code": "string",
  "longitude": "string",
  "latitude": "string",
  "slogan": "string",
  "note": "string",
  "type": "string",
  "slug": "string",
  "image": "string",
  "banners": "json",
  "deleted_at": "datetime",
  "verified_at": "datetime",
  "rating": "float",
  "review_total": "integer",
  "review_count": "integer",
  "couriers": "string",
  "is_umkm": "boolean",
  "qualified": "boolean",
  "business_category": "string",
  "email": "string",
  "phone": "string",
  "main_category": "integer",
  "seller_type": "string",
  "documents": "json",
  "bank_account": "json",
  "sosmed": "json",
  "signature": "json",
  "email_verified_at": "datetime",
  "created_by": "string",
  "updated_by": "string",
  "power": "integer",
  "admin_note": "string",
  "status": "string",
  "verified_by": "integer"
}
```

endpoint ini digunakan untuk mendapatkan data detail toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/merchants/{id}`

## Get Ulasan Toko

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/merchants/{id}/reviews"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "customer_order_item_id": "integer",
    "id": "integer",
    "message": "string",
    "product_id": "string",
    "rating": "integer",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "updated_at": "datetime"
  }
]
```

endpoint ini digunakan untuk mendapatkan ulasan toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/merchants/{id}/reviews`
