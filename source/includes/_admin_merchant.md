# [Admin] Toko

## Get Semua Toko

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string",
    "email": "string",
    "address": "string",
    "rating": "integer",
    "verified_at": "datetime",
    "suspend": "boolean",
    "status": "unverified"
  }
]
```
endpoint ini digunakan untuk mendapatkan data Toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants?q=&status=&page=`


### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata Kunci Pencarian
status | string | false | Status
page | integer | false | Halaman

## Get Detail Toko

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "address": "string",
  "admin_note": "string",
  "bank_account": {"no": "string", "name": "string", "bank": "string", "branch": "string"},
  "banners": "string",
  "branch_id": "integer",
  "business_category": "string",
  "city": {"id": "integer", "name": "string"},
  "city_id": "integer",
  "couriers": "string",
  "created_at": "datetime",
  "created_by": "string",
  "deleted_at": "datetime",
  "district": {"id": "integer", "name": "string"},
  "district_id": "integer",
  "documents": {
    "npwp": {"no": "integer", "image": "string"}, 
    "siup": {"no": "integer", "image": "string"}, 
    "ktp": {"no": "integer", "image": "string"}, 
    "pkp": {"no": "integer", "image": "string"}
  },
  "email": "string",
  "email_verified_at": "datetime",
  "id": "integer",
  "image": "string",
  "is_umkm": "boolean",
  "latitude": "string",
  "longitude": "string",
  "main_category": "integer",
  "name": "string",
  "note": "string",
  "phone": "string",
  "postal_code": "integer",
  "power": "integer",
  "province": {"id": "integer", "name": "string"},
  "province_id": "integer",
  "qualified": "integer",
  "rating": "integer",
  "review_count": "integer",
  "review_total": "integer",
  "seller_type": "string",
  "signature": {"name": "string", "position": "string"},
  "slogan": "string",
  "slug": "string",
  "sosmed": {},
  "status": "string",
  "type": "string",
  "updated_at": "datetime",
  "updated_by": "string",
  "users": [{"id": "integer", "name": "string", "email": "string"}],
  "verified_at": "datetime",
  "verified_by": "integer",
  "village": {"id": "integer", "name": "string"},
  "village_id": "integer"
}
```

endpoint ini digunakan untuk mendapatkan detail Toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants/{id}`

## Get Detail Toko Simpel

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants/{id}/simple"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "id": "integer",
  "name": "string",
  "status": "string"
}
```

endpoint ini digunakan untuk mendapatkan detail Toko secara simpel.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants/{id}/simple`

## Get Data Produk By Toko

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants/{id}/products?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "admin_note": "string",
  "availability_status": "string",
  "brand": "string",
  "catalogue_id": "string",
  "categories": [{"id": "integer", "name": "string"}],
  "classification_catalogue": "string",
  "created_at": "datetime",
  "created_by": "string",
  "description": "string",
  "dimension": {"l": "integer", "w": "integer", "h": "integer"},
  "discount": "integer",
  "guaranty": "string",
  "id": "integer",
  "image": "string",
  "images": "array",
  "is_domestic": "boolean",
  "is_kemdikbud": "boolean",
  "is_secondhand": "boolean",
  "is_umkm": "boolean",
  "isbn": "string",
  "kind": "string",
  "merchant_id": "integer",
  "merchant_storage_id": "integer",
  "min_order": "integer",
  "name": "string",
  "power": "integer",
  "price": "integer",
  "price_zone_1": "integer",
  "price_zone_2": "integer",
  "price_zone_3": "integer",
  "price_zone_4": "integer",
  "price_zone_5": "integer",
  "product_category_id": "integer",
  "product_upload_id": "integer",
  "qty_available": "integer",
  "qty_sell": "integer",
  "qualified": "boolean",
  "rating": "string",
  "review_count": "integer",
  "review_total": "integer",
  "sku": "string",
  "slug": "string",
  "status": "string",
  "taxed": "boolean",
  "updated_at": "datetime",
  "updated_by": "string",
  "verified_at": "datetime",
  "verified_by": "string",
  "warranty": "string",
  "weight": "integer",
  "wholesales": [{"quantity": "integer", "price": "integer"}],
  "with_shipping_cost": "boolean" 
}
```

endpoint ini digunakan untuk mendapatkan data produk berdasarkan toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants/{id}/products?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci pencarian
status | string | false | Kata kunci status
page | string | false | Halaman

## Get Data Transaksi By Toko

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants/{id}/orders?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "bill": "integer",
  "bill_status": "string",
  "details": {},
  "id": "integer",
  "merchant": {
    "id": "integer", "name": "string", "email": "string", "phone": "string", "image": "string", "bank_account": "json"
  },
  "merchant_id": "integer",
  "order_date": "datetime",
  "order_no": "string",
  "purchase_status": "ready",
  "school": {"id": "string", "name": "string"},
  "school_id": "string",
  "shipping_cost": "integer",
  "status": "string",
  "status_updated_at": "datetime",
  "tax_price": "integer",
  "total_order": "integer",
  "total_price": "integer"
}
```

endpoint ini digunakan untuk mendapatkan data transaksi berdasarkan toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants/{id}/orders?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci pencarian
status | string | false | Kata kunci status
page | string | false | Halaman

## Post Verifikasi Toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/verify"
-H 'Content-Type: application/json'
-d '{
      "id": "integer",
      "verified" => "boolean",
      "note" => "string",
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk memverifikasi Toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/verify`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | integer | true | Id Toko
verified | boolean | true | Jika false toko dalam masalah
note | string | false | Catatan

## Post Blokir Toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/suspend"
-H 'Content-Type: application/json'
-d '{
      "id": "integer",
      "note": "string"  
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk memblokir Toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/suspend`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | integer | true | Id Toko
note | string | true | Catatan

## Post Aktifkan Toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/unsuspend"
-H 'Content-Type: application/json'
-d '{
      "id": "integer"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk mengaktifkan kembali Toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/unsuspend`


### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | integer | true | Id Toko
